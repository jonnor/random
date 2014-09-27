

Effectively free software
==========================

The case
---------

In a recent talk in Bergen, I said that while open source software is
massively successful, free software is not.
Now, I’m certain that we are much better off now compared to if there
had not been such a thing as “free software”.
But it is a fact that most users do not enjoy the 4 freedoms defined, many
because the software they use is not free. But others because the freedom
promised is not accessible to them. This then reduces the value of said freedom
significantly, leaving only the benefit that the software can be developed in
loose and synergetic collaboration - essentially the open source 

I will argue that free software, as [defined by the FSF](https://www.gnu.org/philosophy/free-sw.html),
is a prerequisite, but not enough to achieve software freedom for users.

Free software is a highly academic concept. Accessible only for a very
small percentage of software users out there.
Those who can, and have many hours of time to spend on learning how
to program, to setup toolchains, to build,
to learn project-specific communication channels, technical, and
social conventions and quirks.

I’d go as far as calling free software hypotethically free.
The definition requires the ‘freedom’ to run (for any purpose), study,
redistribute copies and modified versions - 
but has no requirements or even recommendations that this should be easy.

In practice, making use of these freedoms is very hard, as a user.

- Most applications are not shipped with source code by default (need to
fetch source control repo on the side)
- Most do not ship a build toolchain (need to set up your own, often from scratch)
- Even then, you only have a toolchain to build for your own platform
(not those of your friends and other users)
- Not easy to host derivative builds of applications
- Most applications can only be installed once on a system (not easy to
move between different versions)

Yes, solving these in a better way could lead to many more forks.
“branching was always easy, merging is the hard part”


Even among established contributors to FOSS, very few contribute
outside a small number of project.
Even if we do use many other applications,
and are definitely annoyed or missing some functionality at times,
the barrier to making use of the freedom is so high that even
we who have done the same thing before shy away from the task.

I propose that to effectively achieve software freedom, we must move away from
treating lowering of barriers to hacking and contributing as a means
to produce free software - but instead see it as a goal in itself.
Free software should be measured on how well it provides users with software freedom.

Software freedom is not a meaningful concept for a
person if it is not within their reach.


Seen from the user perspective
--------------------
Trying to define the steps user needs to go through, from being exposed
to the software to making use of their freedom.
Goal is that this can be used to evaluate how well current softwares do and
detect both small pain-points and make amendments in current workflows,
as well as propose entirely new engagement models and workflows.

To be able to make use of the freedoms promised by free software, the user must:
* Use free software
* Be aware that the freedoms are available to them
* Understand the implications: that if they want to change or fix something, they can

When wanting to excersize the freedom
* Determine which functional area must be changed to achieve the goal
* Find the code that corresponds to the relevant functional area
* Make a (valid) change to the code, "build it", and see the result
* Continue changing the code until the results are as desired
* Save the changes for later use
* Re-use their customizations with new versions of the software
* Publish their customized version, ready for others to run

TODO: split up into each of the 4 freedoms?

Analytics
-----------
While user stories can shed some light on how good the process is, we ideally also have
robust analytics to evaluate it in a quantitative way.

Conversion rate:

* Out of the number of users exposed to the software, how many make a change to its 'code'


What can we do?
------------------

Short-term:

* Good documentation
* Well-defined extension points
* Stable APIs
* Plugin architecture
* Continuous integration
* SDK shipped with application
* High-level automated tests (BDD)

Longer-term:

* Establishing connections between functionality (what exist,how is it
supposed to work) and the ‘code’  (how it is made)
* Different programming models. More introspectable, more interactive,
more visual, more exploratory
* Moving away from “application” as an artifact of “source code” going
though a “build”, to having app and IDE be two faces of the same thing
* Using optimization techniques from the commercial world and apply it to usage of freedom.
A-B testing, goal tracking, funnels. Gamification?




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

