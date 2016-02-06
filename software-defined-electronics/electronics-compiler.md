
How to make hardware as easy as software?
It is all done with EDA tools (which are software),
digital-fabrication machines can do large amounts of manufacturing (which are software controlled).

In software world, one can create usecase-specific programs
by including a set of libraries, and then only having to
add the glue that goes between them.
Electronics one mostly has to research, schemaify and lay out every
single part - even when trying to reuse existing circuits, modules.
Comes from app note PDFs, reference circuits in datasheets.
'dead tree' representations

```
Module system
    Libraries
    Open source
    Searchable
    Installable with 1 click
    Standarized formats
    Defined interfaces
    Pluggable
Compiler
    Different targets
    Modules which plug together
    Fully custom/monolithic board
    Board with modules represented, w/possibility of breaking them apart
Optimizations
    'inlining'
    size, costs, performance
Automated testing
    Simulated
    Hardware
```

## Notes from OSHW 2014

From [Open Hardware Summit 2014, Rome](http://2014.oshwa.org/) unconference on *Making Open Hardware Scale*.

[Google doc](https://docs.google.com/document/d/17laLM8CJIrpnUkXHXsCj8pGjNrwcg1uGi6cjrWV8Ps8/edit?usp=sharing)

Improve the process in going from a prototype created from stock breakouts/shields,
to custom board(s) more suitable for low to medium scale manufacturing.

Current workflow
* Take OSHW breakout boards , build prototype (great)
When integrating into custom board:
* Copy in the schematics of breakouts, wire together manually (problem1)
* Redo the layout from scratch (problem2)

Idea: allow to define reusable functional blocks (components) and systems composed of such components.

Components include everything needed to use realize the system, on at least two levels:
1) Prototype: as breakout board and their connectors
2) Custom board: schematics+layout snippets

Next steps:
* Prototype software solution that allows defining components,
and plugging them together into a bigger design and get a PCB out
Possibly based on Fritizing or Upverter
* Interact with OSHW distributors who sell breakouts/baseboards etc,
SparkFun/Adafruit/Arduino
– find out if they would help in contributing to component library


## References

Projects I'd like to use this

* [brushless](https://github.com/jonnor/projects/tree/master/brushless)
* [currentsource](https://github.com/jonnor/projects/tree/master/currentsource)
* [sensorblock](https://github.com/jonnor/sensorblock)

Related notes

* [sensorblock braindump](https://github.com/jonnor/sensorblock/blob/master/doc/braindump.md)
* [noflo-eda braindump](https://bitbucket.org/jonnor/noflo-eda/src/master/doc/braindump.md?at=master)

Out there on the Internet

* some Hackernews thread on 'why electronics is so hard/slow'
* [PCBMODe](https://github.com/boldport/pcbmode).
Python-based SVG scripting tools for laying out PCBs, with JSON input and CSS-like 'stylesheets'.
