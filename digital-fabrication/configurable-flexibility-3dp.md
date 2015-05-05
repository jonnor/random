
When 3d-printing parts in flexible materials (like NinjaFlex),
one has large variations of material properties depending on
the thickness and patterns used when depositing material.

Because of the additive in for instance FFF/FDM,
it is possible for these properties to vary *within* the same
object produced without additional complications
(like using multiple materials or processes).

Usecases for flexible or semi-flexible objects includes comfortable
wearables/textiles, as well as mechanical applications such as
tires, belts, gasket/seals, shock absorbers, vibration & noise dampeners.

Several aspects of current (December 2014) 3d printing software
however make it hard to actually make use of these properties in design.


Current state
---------------

* Very few applications support selective infill (exclusion/inclusion regions)
* Vast majority of patterns are uniform and non-directional
* Infill patterns typically only on XY plane
* Only one infill pattern for XY plane
* Only one infill pattern throughout all layers (along Z axis)

Slic3r has many non-standard [infill patterns](http://manual.slic3r.org/expert-mode/infill)
(including some directional like Archimedean Chords, Octagram Spiral),
and the ability to change [fill angle](http://manual.slic3r.org/expert-mode/infill-optimization)

Simplify3d has ability to set up multiple "processes" with
[different infill for parts of object](http://www.simplify3d.com/support/tutorials/different-settings-for-different-regions-of-a-model)


Hacks, development
---------------------

* In Cura etc, specify very high wall thickness to keep small features at 100% fill.
* Design in hollow-ness of object, use high infill for rest
* [Swap-gcode-at-Z](http://umforum.ultimaker.com/index.php?/topic/8736-different-infill-settings-per-layer/)
* [Prusa: Using unprintable holes to force shells](http://josefprusa.cz/selectively-making-parts-of-object-stronger-o/)
* [ http://forums.reprap.org/read.php?1,192641 ]
* [Special infill using OpenSCAD, include spherical fill](https://github.com/rptynan/Topper)
* [Infill calculation using model intersection and OpenSCAD](http://garyhodgson.com/reprap/2012/01/thoughts-on-fill-algorithms)
* [How infill is implemented in Cura](http://umforum.ultimaker.com/index.php?/topic/5937-ability-to-shift-infill-pattern-in-cura/?p=54789)
* [Adaptive infill](http://axuv.blogspot.no/2012/01/adaptive-infill.html)
* [Interactive simulation on 3d-print strength](http://www.autodeskresearch.com/publications/3dprintoptimization)
* [Dynamic infill using tesselation](http://www.plunk.org/~hatch/HyperbolicTesselations/)

Existing knowledge
-------------------

Existing industries using similar/related techniques to infill.

* Textiles: weaving and rope-making
* Use of composites materials
* Structural mechanics like bridge making (trusses, space frame, arch)

[Types of Weaves - Fundamentals of composite manufacturing](https://books.google.no/books?id=aCm9yvodiJcC&lpg=PA250&ots=qp6qBa3Z6n&pg=PA249#v=onepage&q&f=false)
twill, basket, satin, leno


Interaction ideas
-------------------

Specifying infill patterns as a mix of primitive patterns

    - - - horizontal
    | | | vertical
    / / / 45* forward
    \ \ \ -45* backward
    o o o circular
    () () elliptical (w/ different angles)

Each of the patterns would have an infill percentage,
and could have a

    | | | | | |   50 % 1-0
    ||  ||  ||  50 % 2-0
    |  |||  |   50 % 1-0-3


While this possibly gives the neccesary flexibility, it still
leaves the burden of determining appropriate patterns to the user,
with no feedback apart from printing and running real-life test.

Instead one could allow the user to *declare desired strength/flexibility constraints*
and use Finite Element Method or similar to determine what infill material would
be suitable.

A less formal/rigorous way would be to allow *weightpainting* to modify relative strength/flexibility,
similar to use in 3d inverse-kinematics/animation.

Small test/simulation scenarios could be used to visualize flex behavior.


Desired workflow
------------------

1) In CAD software, specify desired properties of regions (3d polygons).

2) Allow to import these property regions also into the slicer.

Implementation ideas
-------------------

Implement in Cura, in src/infill.cpp

Maybe implement in FreeCAD 3d-print workbench instead of directly in Cura GUI, to avoid problems
with how to communicate the infill properties/constraints from CAD to slicer.

Possible testcases
------------------

* Electronic drum pad
* NinjaFlex wristband


