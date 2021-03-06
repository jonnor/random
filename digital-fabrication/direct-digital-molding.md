
# Background

When making complex, 3D shapes using CNC milling it can be
highly beneficial to start from a rough shape, made additivly.
This reduces the materials having to be machined,
making more efficient use of material stock and potentially saving time.

But additive manufacturing methods, like FDM 3d-printing is quite slow.
Mold-making for casting the part has substantial setup time.
This can make the potential time saving of having a rough shape unavailable
for large parts, or small batches.

What if we had a digital fabrication device tailored explicitly
for making such rough shapes, which would shape the material directly into a slightly oversided 3d-object.

# Concept

An array of pins, with individual height control over the pins.
Similar to what is called 'bed of nails' in automated electronics testing,
and to the popular [pinart toy](https://en.wikipedia.org/wiki/Pin_Art).

Simplest version would have pins on just the bottom, and ability to wall of the other 5 sides.
Would allow to create solid 3d-shapes with a regular shaped base (flat or some simple geometry).

If there would be pins on bottom and top, could also create shells with varying thickness.

Depending on the resolution of the pins, one could have a high-strength cloth between the pins,
basically 'interpolating' between the points of the pins.

Could cast rough shapes out of resin. Either foam or hardplastic. Polyurethane/Silicone.
Could use a filler+binder. Wood/paper, with glue/epoxy.
Or could heat sheet material and thermoform similar to vacumforming. HIPS/acrylic.
Instead of vacum, could use pressurized air inside a bag. Should allow to create shells of relatively uniform thickness.
With advanced enough materials, maybe one could even find a way to support pouring of molten metals?

Some processes, like thermoforming may allow more complex shapes if the pins can move while
the forming takes place.

# Actuation

## Considerations

An initial target could have maybe 10 mm between pins.
100 x 100mm would then be 10x10 pins, or 100 in total.
The device is naturally very sensitive to the costs per-pin,
limiting both resolution and size. So reducing this is perhaps the key consideration.

Should be able to resist quite a lot of backpressure, at least after having.
Some gearing for mechanical leverage would make sense. It also increases Z-precision.
Maybe a locking system?

Can one reduce costs not having one drive/motors on each pin?
For instance using timing belts which can be coupled in and out?

* Rotary servos with linkage
* Linear actuators. 
* Linear electromotors

Hydraulic or Pneumatic may also be an option, especially if it can be digitally fabricated.

See [electromotor project](http://github.com/jonnor/projects/tree/master/brushless)

## Row-based actuation

Problem with one-actuator per pixel display is that number of actuators grows with N*M, or if N=M then N^2.
If we instead update row-wise, one row at a time, and then lock a set row in place, we can use only N actuators.
This is essentially a tradeoff between maximum update rate (one actuator per) and lowest costs (only 1 actuator).

Each pin could be evenly spaced with holes along the vertical axis.
The actuator pushes one row of pins to the correct height.
Then a set of metalrods is pushed the row of pins, locking each pin in the row at the right height.
This process continues for each row. At the end the locking rods go through all the pins.

Potentially one could to similar with hydraulic pistons, assuming one could get reliable cheap valves for each piston.
This could increase Z-resolution a lot, though maybe harder to miniturize in X/Y and more complex/costly to make.

If one can get setting of one row to take less than 3 seconds, then one set M=20 rows within 1 minute.
Betwen 5mm and 3 mm Z resolution seems realistic with lasercut parts. And similarly down to 3 mm X/Y resolution.
These numbers make it feasible to use for casting rough metal shapes (by pressing the pins into sand)
- and only have to mill relatively little, regardless of the shape of desired form.
For hard materials like metal this may save significant amount of time.
For softer ones, milling directly may be just as fast, or that the extra tool does not justify the savings.

The unit could be such that the pins/rack is interchangable. This way one can have multiple shapes, with a single machine.
For instance two racks put towards eachother could make an enclosed volume.
One could also use multiple machines together, and in this way build up bigger surfaces quicker.

# Interface integration

One could also envision interface device working along same principle, sensing
the shape. This could be seen as a low-resolution 3d-scanner and/or a tactile
3d-input device.

This concept has ben dubbed as "Digital Clay",
[1](http://www.cc.gatech.edu/~jarek/images/DigitalClay.pdf),
[2](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.473.1582&rep=rep1&type=pdf).

If used in combination with such fabrication device,
may potentially allow user to manipulate the object being formed in real-time.

# Related prior art

## Shape displays

Canonical example is probably [inFORM](http://tangible.media.mit.edu/project/inform/) by [Tangible Media Group](http://tangible.media.mit.edu/vision/) at MIT.
The [original paper](http://tmg-trackr.media.mit.edu/publishedmedia/Papers/527-inFORM%20Dynamic%20Physical%20Affordances/Published/PDF), describes implementation.

30x30 pins, 3.175 mm apart.
Uses motorized slide-pots, ALPS RSA0N11M9A07. Seem to be around 20 USB/piece.
Similar device from [Sparkfun](https://www.sparkfun.com/products/10976).
6 pins on each custom PCB, for total of 150 boards(!).

Lumen, using a shape-memory-alloy
http://makezine.com/2009/12/16/the-lumen-a-physical-3d-display/

Snoil, based on ferrofluids
https://vimeo.com/6680282

## Jacquard looms

Controls many many relatively small heddles.
Though typically only has a couple of height-positions for them.

TODO: research what systems exists

## Misc

Selective sheet thermoforming using pressurized air,
in [Design at Large presentation](https://www.youtube.com/watch?feature=player_detailpage&v=cLUyTK72xXU#t=1646) by Stefanie Mueller.
Presentation has good information on 'adaptive' or 'low fidelity' digital manufacting techniques.

