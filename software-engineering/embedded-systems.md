
# Embedded software development

Some brainstorming around best-practices.
Mostly in context of microcontroller/bare-metal programming.
Some taking inspiration from the Rust programming language.

## Separate application logic from I/O code

I/O code and platform-specific code should be separated from the application logic.
This allows to verify large parts of the application more easily.

## Only allow unsafe for I/O

https://doc.rust-lang.org/book/unsafe.html

`static mut` should not be allowed.
Raw pointer manipulation shold not be allowed.

Application code should be written without any `unsafe`.
Only platform and I/O abstractions may use it.

The compiler options can enforce this, by using `#![deny(unsafe_code)]` or `#![allow(unsafe_code)]` in the code.
These inline options follow the module hierachy. So one can set the default at the crate level.
This means that there is no need to configure it in Cargo. 

All compiler lint options can be listed using `rustc -W help`

## Dynamic allocation

Should not be used in general.
It be comes hard to ensure that enough memory will always be available.
Problem is extra hard if different, causing memory fragmentation.

For narrow usecases, dynamic allocation may be allowable.
Should then only be done for types of one particular size.
The memory area which is used for dynamic allocation should be static, with a fixed up-front size.
Ideally the memory area is put on the stack, which should automatically check that it fits on device.
If heap is disabled, stack-overflows can also be ruled out.
Allocation/deallocation should happen explicitly, and visible in the high-level code.
Failure to allocate must have a well defined error handling.
Tests must exercise allocation failures, by invoking the external conditions that may cause them.

Is it possible implement this restricted "dynamic" allocation without `unsafe` code?
We want to use the borrow checker / lifetime, to eliminate possibility of as many issues as possible.

Some discussions on [stack overflow protection in Rust](https://github.com/rust-lang/rust/issues/16012)

## Test application logic extensively

Functional testing of the application as a whole.
Unit-tests for important functions.
Tests should be able to run both on host and on device.

## Additional lints

Any particularly relevant Rust lints?

https://github.com/Manishearth/rust-clippy

## Simulating external environment

The platform and I/O abstraction should allow for external devices to be simulated,
using the same language as the embedded software itself. Test suites should be able to

In simulation code it can be useful to use general-purpose (not embedded-specfic) 
For instance statistical functions. 

## Interactive UI simulation

Have the application run inside a UI can run on the host,
emulating the inputs and outputs of the system.
Lets one test/validate user interaction without having the final hardware.
A simulation which can execute by just opening a web-browser is the easiest to use.

A standard touch-screen device like a phone or tablet running the UI
can be a standing for physical buttons in a full-system interaction demo/test. 

Rust will be compilable to JS/WASM, and can then be executed in browser.
Alternative is to establish a protocol between the device code, and the simulator/UI.
Both should fit within the Platform/IO abstraction.

Recommended to use a standard file-format as the basis, so it can be edited easily.
For instance SVG as a simple 2d UI model, make interactive by attaching JavaScript.
Or one can go full 3d, possibly using (exports of) the CAD models for manufacturing.

## Used for integration-testing

If other software has a dependency on our embedded device,
it should be possible to use the code as part of an integration test suite.
Most likely the code will run on host.

## System test

A software-controllable test rig should cause inputs, and observe outputs of device.
From perspective of a user, or.
Rig may also be able to cause certain environmental conditions, ie temperature changes or EMC.

## New state as a function of current state and inputs

Lifts all dependencies out, making them explicit and testable.

Finite state machine
Pure functional. Monads
Functional-reactive-programming
Syncronous languages

## Separate state specification from application

Idea: Let the code calculate a new state, as a declarative data-structure.
Then have a separate function for realizing this state.

Challenge, transitions between states.
For instance a sinewave generator with a given frequency.
Upon a change in frequency, how should it switch over from one frequency to another?
Abruptly? At the next zero crossing? Gradually shifting frequency? Cross-fade new with current sine?
Some of these methods may have parameters.
And if the values is not change, its not a transition.
What to do if changing the value again while an existing transition is still ongoing?

Problem exists in general for pheripherals which have "hidden" state (like actions over time).
