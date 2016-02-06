
Objects we have around us today are dumb.
They don't know what they are, how they work, how they were made or how they can be maintained or fixed.

On every object, have a RFID/NFC tag(s) + printed URL (maybe QR code).
Printed part also acts as geometric marker(s) at known location on object.
Contain a unique id, per instance produced. Example:
https://obj.jonnor.com/de305d54-75b4-431b-adb2-eb6b9e546013

References repository of information about object

* 3d-models, code, schematics
* relationships, versions
* design, history, license
* usage, assembly, repair instructions
* lifecycle, origin, recycling instructions
* cost/availability of replacement

Structured information primary, but also any type of free-form,
to accomodate things not fitting in ontology.


Example workflow
-------------

* Detect faulty object
* Tap its NFC tag with phone/tablet
* See 3d-model superimposed on camera image
* Explore the object to understand how it works
* Possibly use interactive guided debugging
* Identify what is broken, pieces needed to fix
* Chose how to produce pieces
* Pieces will have RFID tag information

Implementation ideas
---------------------

Needs software integration when producing/creating, ideally into CAD/CAM step. Use as revision-control?
Publishing the information should be default, not require extra steps.

When producing, have tooling that help with creating,
and attaching the tags at correct positions.
Dedicated area in CNC/laser with sheet of tags, create as part of normal job?
Alternatively a dedicated printer as the "label-maker".
Automatically give the parts not big enough to warrant tag just URL, or alphanumeric identifers.
3d-print: embossed, laser/mill: engraved.

Graph database. REST API.
Hosted service. Open source. Pay for non-open source objects?
Web-based app access, optional native integration
Federation, allow use custom domain, custom instance
Default to replicate to hosted service (master). Allow config, opt-out.
App to try URL as-is, then fall over to central version, then archive.
Allow creating objects, relationship also before publishing.
Store in artifacts/blobs. Back/forward refs.
Maybe also do partial graph-db sync for offline-cache in clients.

Allow referencing/linking sub-parts by their generated ID and/or given shortid in
prose for instructions etc. "Attach #foo to #bar"

Importing/sync from existing repositories. Thingiverse, Umagine, GrabCAD
Allow automated syncing also *to* these?

Possibly related
----------------

* WikiData?
* [Smarter CAD](https://github.com/jonnor/projects/tree/master/smart-cad)
* [QR description tags](https://github.com/jonnor/projects/tree/master/displaycase#qr-description-tags)
* [Reality Editor by MIT](http://www.realityeditor.org/).
Introspectable objects + linking web-enabled IDE like [Flowhub](http://flowhub.io) integration could enable similar
* FabMicroHouse...

Crazy:

* Bitcoin blockchain? Producing a physical item as proof-of-work??


