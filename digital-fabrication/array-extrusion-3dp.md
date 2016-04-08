
# Array Extrusion for FFF/FDM 3d-printing

## Motivation

Current FDM 3d-printers are relatively slow.
Given a typical nozzle size of 0.4 mm and a solid object the printer needs to visit every millimeter.
For a large model this is a very long distance.

The nozzle size gives the lower limit on acheivable resolution,
so if increasing the size the resolution goes down.
On most printers, changing the nozzle requires manual re-tooling and is not done during normal operation.

## Concept

Extruder head with multiple nozzles, with individually controllable height and Y offset.

A side-effect of this design is that also can supports multiple materials.
It can use hardware and material from standard desktop 3d-printers.

## Operating modes

This enables two additional operating modes, in addition to standard single-nozzle extusion:

* Parallel infill.
All nozzles set at same height, next to eachother.
Infill density can be controlled by adapting the angle of the head with respect to the.
* Serial wallbuilding.
Each nozzle height is set one layer higher than the next.
All nozzles are dynamically aligned to follow path of objects wall.
Builds N layers of wall in one pass.

If one were to drop the serial wallbuilding feature,
then individual nozzle positioning is not needed.

## Implementation notes

### Rotating head

Requirements

* 180 degrees+ rotation
* Fits 3-5 hotends

### Nozzle Z and Y movement

Requirements

* Compact, especially in X-head axis, to fit several next to eachother in array
* Stable against vibrations/momentum of head
* Largely producable using 3d-printer (reprappable)
* Y range: maybe 50 mm
* Z range: maybe 5 mm

Possible mechanisms

* Stacked cartesian, Z on moving Y.
* Double SCARA / five-bar linkage.
* Pantograph / four-bar linkage.
* Linear parallel manipulator

References

* [Northwestern uni: Pantograph design](http://hades.mech.northwestern.edu/index.php/Design_and_Control_of_a_Pantograph_Robot),
including forward and inverse kinematics
* [DexTAR: double SCARA educational robot](http://www.mecademic.com/DexTAR.html),
includes browser simulation of kinematics, with singularity simulations.
* [Reprap SCARyllA: Dual (parallel) arm SCARA laser engrave](http://forums.reprap.org/read.php?185,490216).
Lots of links to exisiting designs and software.
* [Plotclock, home-made parallel robot](https://www.youtube.com/watch?v=EAsmDU7EGsc)
* [Reprap Wally, dual-SCARA 3d-printer](https://www.youtube.com/watch?v=iVg7WrgHJik&ebc=ANyPxKpRKsjBh649X_R8OOi9qAqbzFH_-N0OcMRwg5ypfubvSu2X-JdP-ekmXUzED4lHHqUzn1eX8XBe0UJi4rcY27xdv6QpjQ&nohtml5=False)
* [Linear parallel manipulator kinematics](http://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=6076213)

## Development

* Build a head with 3+ static nozzles
* Add controlled rotation of head
* Mount to a large CNC machine (ex Shopbot)
* Run tests of parallell infill feature
