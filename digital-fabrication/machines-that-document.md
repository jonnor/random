Machines that document
======================

Workshop proposal made for [MakerCon Nordic 2014](https://gist.github.com/jonnor/33f5bf53646fab84bb2d)

Case study: 3d-printing

What should be documented:

* Purpose of object/project
* Meta| Author(s), license, timedate, geotag
* CAD| project files (.scad, .fscad)
* CAD| output files (.stl)
* CAD| Render/preview of 3d-model
* CAM| Slicer settings (cura.ini)
* CAM/MC| Time to print, material use, cost
* Machining instructions
* Material(s) used, filament
* MC| Machine info, printer used
* MC| Timelapse/video of production
* MC| Pictures of machined result
* Assembly instructions
* Pictures of assembled/in-use result


Key architecture questions

* How to make sure users still have freedom in which SW they use,
especially for CAD/machine-independent parts
* How to track artifact/file relationships and versioning
* How to engage user in inputting 

Software pieces

* CAD: FreeCAD??
* CAM (slicing): Cura/CuraServer
* Machine control: Octoprint
* Content/assets: Github repo (git)
* Video content: Youtube, Vimeo
* Website: Github pages (Markdown+Jekyll)
* Thingiverse: http://www.thingiverse.com/developers/rest-api-reference
* Social media: Twitter, Instagram, Facebook

Other crazy ideas

* Use a robot, either multicopter or humanoid,
to go around and ask hackerspace members what they are creating + take pictures
* Use Google Glass or similar + voice to record non-automatable input

