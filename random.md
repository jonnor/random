

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
Those who can , and have many hours of time to spend on learning how
to program, to setup toolchains, to build,
to learn project-specific communication channels, technical, and
social conventions and quirks

I’d go as far as calling free software hypotethically free
The definition requires the ‘freedom’ to run (for any purpose), study,
redistribute copies and modified versions
but has no requirements or even recommendations that this should be easy

In practice, making use of these freedoms is very hard, as a user.

Most applications are not shipped with source code by default (need to
fetch source control repo on the side)
Most do not ship a build toolchain (need to set up your own, often from scratch)
Even then, you only have a toolchain to build for your own platform
(not those of your friends and other users)
Not easy to host derivative builds of applications
Most applications can only be installed once on a system, not easy to
move between different versions
Connections between 

Yes, solving these in a better way could lead to many more forks
“branching was always easy, merging is the hard part”


Even among established contributors to FOSS, very few contribute
outside a small number of project. Even if we do use many other
applications, and
are definitely annoyed or missing some functionality at times, the
barrier to making
use of the freedom is so high that even we who have done the same
thing before shy away from the task

I propose that to effectively achieve software freedom, we must move away from
treating lowering of barriers to hacking and contributing as a means
to produce free software -
but instead - software freedom is not a meaningful concept for a
person if it is not within reach


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

TODO: split up into each of the 4 freedoms?
When wanting to excersize the freedom
* Determine which functional area must be changed to achieve the goal
* Find the code that corresponds to the relevant functional area
* Make a (valid) change to the code, "build it", and see the result
* Continue changing the code until the results are as desired
* Save the changes for later use
* Re-use their customizations with new versions of the software
* Publish their customized version, ready for others to run

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
A-B testing, goal tracking, funnels. Gamification

