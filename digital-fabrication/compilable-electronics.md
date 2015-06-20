# HackerNews Discussion, Jun 2015
[Link](https://news.ycombinator.com/item?id=9723899)

tlrobinson 4 days ago

    Discrete electronic components (resistors, capacitors, transistors, simple ICs and sensors, etc)
    are sort of the "assembly language" of electronics, but the vast majority of programmers never touch assembly.

    There have been attempts to create higher level abstractions (like Arduino "shields", etc)
    but the cost (time and money) to produce reusable modules is huge relative to the cost of the components,
    whereas CPUs are so fast the overhead of higher level languages and function calls is usually insignificant.

    I'm not sure what the solution is. Maybe better software, and methods of manufacturing small runs of boards? 

jononor 0 minutes

    We need compilers, high-level languages and 'linkers'.
    A way to represent module interfaces, allowing multiple module implementations:
    from a ready-made board (like an Arduino shield), to an 'optimized' piece of an integrated board for whole system.
    A package manager to easily download and integrate such modules into ones project... 


# Open Hardware Summit 2014 - Unconference - Making Open Hardware Scale

Session Proposer/Coordinator: Jon Nordby <jononor@gmail.com>

Participants

* Jason Kridner <jkridner@beagleboard.org>
* Pierros Pappadeos <ppapadeas@gmail.com>
* John Jiannelos
* Zachary Menegakis


## Session Name/Topic
Modular Hardware Design Tools/Workflow


## Insights and key ideas
Improve the process in going from a prototype created from stock breakouts/shields,
to custom board(s) more suitable for low to medium scale manufacturing.

Current workflow
* Take OSHW breakout boards , build prototype (great)
When integrating into custom board:
* Copy in the schematics of breakouts, wire together manually (problem1)
* Redo the layout from scratch (problem2)

Idea: allow to define reusable functional blocks (components) and systems composed of such components. Components include everything needed to use realize the system, on at least two levels:
1) Prototype: as breakout board and their connectors
2) Custom board: schematics+layout snippets

Next steps:
* Prototype software solution that allows defining components,
and plugging them together into a bigger design and get a PCB out
Possibly based on Fritizing or Upverter
* Interact with OSHW distributors who sell breakouts/baseboards etc,
SparkFun/Adafruit/Arduino
– find out if they would help in contributing to component library



## Key resources (Link to relevant documents and resources)

https://upverter.com/


## Extended Notes

Motivations /personas

* Hacker, prototype quickly using what is lying around, then make a custom board
* Businesses, integrate known-working reference designs quickly
* Newbies, don't know how to solve a problem, want to specify what then get proposed solution, or at least warning about known problems

Existing modular systems

* Breakout boards (SparkFun, Adafruit etc)
* Littlebits
* Tegel Mikroelektronika
* GVS
* Grove
* Tinkerkit (Arduino)
* Relayr.io / Wunderbar
* Olimex UEXT

Daugherboards extensions

* Arduino Shields
* Beagleboard Caps
* Raspberry Pi hats

Different definitions of “modularity”

* Interoperable interconnectivity, on same level
* The different architectural levels in one system

Typical types of components

* Embedded Linux computer
* Microcontroller
* Signal conditioning (filters, amplifiers etc)
* Motor drivers

Constraints and parameters

Examples: CPU power, RAM, I/O pins, I/O current drain/sink, signal bandwidth

Constraints can also be software-driven, by API abstractions in software
Know you can reuse software code depending on hardware choice
Arduino APIs components becoming uC "standard", implemented by ChipKit/Energia/..
On Linux, std OS interfaces: GPIO, SPI, I2C

* Specify parameters/constraints, get a suggestion for starting point

* Need to allow customizations/manual tweaks after starting point
* Ideally customizations would not break the mapping between functional components ↔ schematics/layout (allowing two-way transformation)



# Prototyping ideas, February 2014

* Create a couple of circuits to be used as "components" on Upverter
* Tag/declare the input and output "ports", either in
* Read in JSON format exports from Upverter components
* Create a new JSON file with all component instances included, and nets between components connected
* Re-upload to Upverter?
* Do auto-layout of components, auto-tracing for component connections
* Get Gerber files out for PCB production

[Upverter electronics File format conversion tool](https://github.com/upverter/schematic-file-converter)

## Electronics system architecture

When designing complex electronics systems, one spends a fair bit of time
on the overall architecture. As all decisions flow from this, it is important
to get concensus and nail down this design before continuing with others.

At this level one is mostly interested in the large functional components,
how they are connected (power and control-signals), and to get a feel for
it will work overall.

If one could draw this as a graph of components in Flowhub, it would provide
for a top-level view that one can collaborate on and drill down to details on,
and that one can visualize and play with interactively. It should be possible
to simulate a whole system!

Components should include:

* Power supplies / media converters
* Embedded Linux devices (running NoFlo Node.js)
* Desktop/mobile clients (running NoFlo browser)
* Microcontrollers/boards (running MicroFlo)
* Perphiperhals like LEDs
