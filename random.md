
Effectively free software
==========================

Moved to [./effectively-free-software]


The case for open source in disruptive startups
===================================
disruptive = new technology, new markets, new ideas
startup = risky, uncertainty

Background
* Talking with companies in early phases, “want” to be open. Fairness, ability to to talk about their work
* Unsure how to do openness without risking business, what to open, what to not
* Unsure how to argue for openess with respect to investors, lawyers and other non-technical stakeholders

Need to understand how openness relates to business strategy
Exact balance will be particular to company

Robustness

* Significant parts of the IP available to employees (and anyone else!) in case company goes bust
* Can reuse this in new efforts, learn from failure without having to start from scratch

Demonstrating ethos

* Technical know-how
* Ability to ship working software
* Becoming a thought leader

Letting others help build and realize the vision

* Including your customers
* Building mindshare for the new ideas, technology, Legitimizing/validating the concept
* Targetting different usecases, regional areas. Integrating with different other ecosystems
* Ecosystem of companies pushing in the same general direction

Recruiting

* Self-motivated, -driven people
* Ability to assess exactly what they can do and the way they work
* Motivation key for productivity, especially in mind and social work
* Need to consider non-monetary aspects of motivation

Free access to excellent development tools/services

* Source repositories: Github, Bitbucket
* Continious integration: Travis CI
* QA: Saucelabs
* Hosting: Heroku, OpenShift, Github pages

Policy

* Benefit: clear guidelines for making day-to-day decisions
* Components, libraries - open by default
* Solution, services - closed by default

Moving away from thinking

* diametrically opposed openness != business
* that free and open source software cannot be a sustainable economical models 
* employees trading their (mind) labor (benefiting the company) for a paycheck (for food on table)

Move towards a model

* Where people work for themselves, driven by own learning and personal goals 
AND for the benefit of the company
AND for people outside the company (through creation of open technologies)
* of trust, that with a strong vision, clear goals one can better reach these by trusting others whos interests are aligned to work towards the same goal
* seeking synergy between people, companies, goals - instead of 
* People-first instead of company-first


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


## Apps

Most apps are shit, but they do have the potential to solve actual problems. Random ideas:

### Resistor finder

You prototype electronics and have a bunch of resistors (and other components) lying around in
a pile/box/whatever so you can reuse them instead of just taking new ones and always making this pile grow.
But it is quite tedious to find the riought value from such a pile.
Worst is when you spend a lot of time, and then realize what you need is not there.

Point smartphone camera to the pile. The app would scan the video contiously to find resistors based on their color coding.
For a sparse pile it could overlay the info onto image. Or build up a list of available values.
Could allow user to indicate desired resitor value, and then show just the location of that in the image.

