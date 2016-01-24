# Code as communication
A perspective on code aestetics and how to evaluate

'code' is a key mechanism, inherent to the process of software development
today, this is mostly textual, imperative.
Though sometimes it is more functional, or declarative

what is good code?
hard question. Possibly highly context dependent, and subject to many subjective evaluations.
Many times, a particular view on the topic, seemingly boils down to tradition or fashion
Conclusions are made, but rarely is the method of evaluating code aestetics stated or discussed.

This is important, for without this, how can we reason about what makes a
good code/programming style, or a good programming language?

## Concept

I'd like to argue that one useful way of seeing code is as
'a body of communication'. (needs rephrasing, sounds very wishywashy)
in two ways:
1) communication from programmer, to the computer
Specifying how
2) communication from original programmer, to other programmers (and oneself, days/months/years later)
Reading the code, possibly

communication models
lossy communication channels
*difference between what was intended [to be communicated] and what recepient think [was communicated]*
ambiguity

in natural language between good communicators, what happens?
in case of ambiguity or underspecified communication, receipient:
. makes it clear that they are not certain having received what was attempted sent
. informs about what they received, asks about the missing/conflicting parts
so that sender can alter or augment their communication
-> a compiler should work in the same way
a current failing is that we assume (but don't verify) communication from programmer -> computer,
which is not a good model of how human communications work

## System-first understanding

the low-level code, statements/expressions/blocks/functions/classes is not the most important
Rather, the bigger picture, the system/architecture is key
(of course, since code is needed for the realization, it remains important)
Both because it is the function of the entire system that is of importance for users of the system,
and code must be subordinate, and serve this purpose
But also because an understanding of the individual pieces is informed by the
general concepts, approaches and styles of the system it is a part of

arguably a failing of the current programming languages,
the architecture of a system is not well communicated through its code

there are many ways of modelling systems and architecture, but most of these are not executable (as code)
when described on a whiteboard, between stakeholders, other communication mechanisms are used
flowcharts, dataflow diagrams, class diagrams, state-machine diagrams, entity relation diagrams

Often these important pieces of communication are ephemeral, never stored anywhere.
Or maybe they are preserved as pictures, static, unsearchable and disconnected from what executes
Over time they typically cease to reflect reality more and more

UML and similar tools were a dead-end, cause it is disconnected in same way.
Need single-source information
Approaches built on top of existing programming language may help.
For instance NoFlo/Flowhub/MicroFlo-style FBP, where the dataflow networks
*are* the executable thing (communication to machine)
*and* the visual entity seen/discussed (communication between stakeholders).

## Communicating changes
Most software is continiously changing
Software engineering is arguably more about managing the process of changing the code,
from what we have now, to what we need and want to have (as soon as possible).
The act of writing (new) code in isolation, is secondary

to manage, we currently use 
(textual) version control systems, expressing changes as textual diffs. Example: git
text and line-oriented, no knowledge about programming language constructs blocks (if,else) and functions
it has minimal understanding of files being moved, or parts renamed, or what the roles of code in different files have

Will be case until new approaches emerges and becomes established,
like semantics diffs for imperative code (TODO: link example used in Linux kernel),
or manipulating code not as text but through their ASTs and changes through diffs or rewrite rules on these,
or more model-based approaches with built-in change management tools

consequences of textual change management, with code-as-communication
want changes to be clear, easy to understand for other developers
for review during inclusion,

preferred:
changes to public interfaces are made clear
syntaxtical changes separate from semantical. Whitespace changes, codestyle, symbol renaming (only in private code!)


Examples

delimiters of lists, and other multi-line statements
bad: languages where statement delimeter (,) cannot be present at end of list (JSON, C++, Python)
reason: causes two-line change instead of one.
Increases likelyhood of having to manually resolve git merge conflicts for simple changes/additions
workaround example: in C++ initializers, use : for first line then prefix ,
better: language allows , on all lines () or does not require explicit , at all (YAML, CoffeeScript)
The start (\[) and end-terms (\]) should also be on separate lines, for same reasons


