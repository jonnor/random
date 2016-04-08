
Currently machines for independent digital fabrication are stand-alone things,
commonly a box you put on your desktop. This form-factor is convenient in
in that it can be placed anywhere there is a moderate amount of horizontal space.
However, it takes up precious work-surface.
Stowing and taking forward requires physically moving machine, often also fiddling with cables.
The machine is usually not very well noise-insulated either, making it
unappropriate for continious use in a personal environment.
The form-factor is also very tailored for a sit-down-in-front

These issues could perhaps be alleviated by thinking of digital fabrication as an
integrated part of structural elements and furniture of a home, workplace or lab.

Guiding principles/requirements

* Machines can reproduce a large part of themselves
* Material stock and custom parts must be readily available
* Takes up minimal space when idle
* Machine is always ready to run. Connect, chose design -> go
* Internet-enabled, can monitor&control machine
* Targetted for unsupervised use, and not disturbing other work
* Self-contained, only requires power. Tools included
* Series of complementary machines
* Cheap unit, scaling by adding more units "horizontally"


Wall-mounted 3d-printer
------------------------

When idle, Z-bed is at top. As the machine progresses, the bed comes down.
Depending on exact design, could be possible to make it as little as 10-15 cm tall when not in use.
A tricky part space for the Bowden tube and filament spool.
[Pellets extrusion](http://richrap.blogspot.no/2014/12/no-more-filament-quest-for-universal.html)
is an interesting alternative.

Could be constructed using a CoreXY top section, with an Ultimaker-like Z-platform.

The top part could be open or enclosed in a cabinet.
If Z axis is fastened to build platform (instead of to XY section),
the underside of the machine when idle will just be bottom of build plate.
This could give a very Star Trek Replicator like asthestics, with objects
being constructed by a "hidden" machine.

Standard cabinet sizes are around ~60 cm wide, 75 cm tall and ~35 cm deep.
Could fit two medium sized printers side-by-side.


CNC-router+laser-engraver table
------------------

Standard desk sizes are around 120 cm wide, 60-80 cm deep.
For a sitting-desk, the available height of the plate is 10-15 cm.
Dictated by bottom being above your legs, work surface height being ergonomic.
Using motorized legs (sit/stand like Ikea Bekant) could provide flexibility in work position.

This probably limits the material thickness to ~5 cm.
More than plenty for typical router work: 2D/2.5D operations on sheets.
3d-milling tall vax models etc. would require a different tool (preferably 4-5d).
More suited for the cabinet-style of a 3d-printer.

Material should be feed in from front/back of machine.
Table should include compartments with the required tools.
The top-plate should be transparent (polycarbonate/acrylic/glass).

Lock/clamps coming in from side would secure material, at least for standard right-angled sheets.
Microswitch on the Z-axis for knowing material thickness. Could also verify plane-ness.

A cyclonic dust separator could allow to keep vacuum noise/particle-emission down?
Alternative would be to let the entire chamber have suction, pulling particles to the back and out.

Laser would be a diode type, mounted directly on the head, next to spindle.

An X-Carve/Shapeoko could behaps be used as a starting point for constructing.
Challenge is the very limited Z-height.

In an industrial setting, N (1-10) of these could be positioned on top of eachother in a "rack".
The material could be input from the back, possibly automatically fed appropriate material from store.
The machined sheet exits on the front. A packaging machine can put into boxes and label.
For decentralized manufacturing, should be placed at place which regularly get goods and people stop by,
like a grocery store or coffee-shop.
