# Reading list
Misc. things I've read, and bothered to make notes about.

Most recent entries on top.

## Kipple Field Notes
by Hillary Predko

[Kipple Field Notes](http://www.hillarypredko.com/kipple/1-the-things-we-carry/)

Making is shaping the world around us
"over 90% of the resources taken out of the ground become waste within 3 months"
"consumer products contains on average only 5% of the raw materials involved in the process of making and delivering it"

"Innovation favours disruption, a romantic idea,
but disruption in the lives of vulnerable people can be violence." 
 
"Maker culture does not provide a critique of industrial production that holds up when examined against the reality of full scale industrial production, and the complexity of emerging manufacturing-based markets like China."

"Maybe escaping the city as it is is the first step to building something new. Hundred of builders in concert, labouring out of sight, waiting to unveil a vision of a more livable city."

How to compete with industrial-scale consumerism?
How much of the benefits are fundamental?
How much due to the scale, being the standard way.
How much due to actively hiding negatives as externalities,
be it on resources, people or culture?

## Out of the tar pit
By Mosely & Marks

[PDF](http://ben.moseley.name/frp/paper-v1_01.pdf)

Read October 24, 2017

Argues that state & control is cause of much accidental complexity (ref Brooks) in programs.
Evaluates object-oriented, functional programming and logic programming against this.

In 7.2.2 it argues for one case where accidental state may be preferable to deriving from inputs.
When it depends on the whole history of inputs, and its own previous values. Like in an interactive game.
Their rationale is that keeping current state is the more natural way to express the system. 

I do agree, but would like to add that this formulation is also *less stateful*,
in the sense that it does not have to store inputs back since the beginning of time.
One can then know that new state must depend only on current state and inputs,
the prior 'history' of inputs as well as initial state, is irrelevant.

7.3.2 argues for separating pure logic, state and control (how execution of logic is performed).
This is very much what I've been doing in dlock13, Rebirth, dhang, toollock, firmware.
Maybe even as far as using a different language:
"there is no sense in having control specification primitives in a language for state"

A dedicated language for state could be a kind of schema with constraints/properties,
allowing to *declare* what is considered a 'valid' state. And similarly for input/output data.
It could have facilities/tools, for instance generation of data exemplars within what is valid.
For low-level implementation languages (like C++), it may also generate validator code,
as well as de/serialization code. It may be possible to use knowledge of valid/invalid to
perform static checking, for instance for integer overflows.
Such ideas came up when working on Agree.js

Section 8 introduces the relational data model as a proposed solution.
To use this as a fundamental data representation reminds a bit of of Eve.
Section 9 introduces the concept of 'Functional Relational Programming'

## Seeing Whole Systems
By Nicky Case

Seen: August 26, 2017

[The Now Long Now Foundtion - Nicky Case - Seeing Whole Systems](http://longnow.org/seminars/02017/aug/07/seeing-whole-systems)

> Maps are not useful *despite* being simplified, but *because *

> Cause and effect are *not linear*:
> A effect can be its *own cause* future in time, they have loops.

*Reinforcing* loop. Positive feedback. Creates exponential growth or dramatic decay.
*Balancing* loop. Negative feedback. Stabilizes. Creates  periodic patterns, dampened sines

Systems are chaos. Example: dual-pendulum. Impossible to accurately predict. 
> Prediction is for chumps

> Are we bound to be like Sisiphous?
> Always pushing the ball up the hill, only to have it roll down again.
> Don't move the ball, move the hills!

Done by reinforcing or strengthen loops (reinforcing or balancing).

Very similar to ideas I had in Berlin/Helsinki.
"gravity" and the environment being a/the major influencer of decisions/outcome.
 Do I have any notes from it? What spawned me thinking about it?

## The Future of Software Engineering
Seen: November 4, 2016

[YOW! 2015 - Glenn Vanderburg - The Future of Software Engineering](https://www.youtube.com/watch?v=Tg9D7UE4TyI)

Premise: The act of creating software today has little to do with engineering.
And it is not because it should not, but because software engineering so far has
failed to be a useful/productive model/disipline.


> The Engineering Method is the use of heuristics to cause the best change
> in a poorly understood or uncertain situation within the available resources
Billy Vaughn Koen, Discussion of The Method. (context: mechanical engineering)

> the emperical process control model provides and excersises control 
> through frequent inspection and adaptation for processes that are
> imperfectly defined and generate unpredictable and unrepeatable outputs

> the picture of the software designer deriving his design in a rational way
> from a statement of requirements is quite unrealistic
> No system has ever been developed that way, and probably none ever will
David Parnas


> There is no essential difference between design and production,
> since even the production will include decisions which influence the performance
> of the software system, and thus properly belong in the design phase
Peter Naur, 1968

"The source code is the design document". The "built product" (following civil engineering model),
is the deployed/running thing on servers.
Given the design, we can "build" the product effectively instantatiouly and for no money,
exactly and deterministically, each time.

> Embrace the code as design documents, formal specification, and modelling tool.



## Hard work is not enough
Seen: September 22, 2016.

[Hard work is not enough](https://medium.com/practicing-developer/hard-work-is-not-enough-406856133a35#.97eqdrroo)

> Instead, pay attention to two things:
> 1. The things that you are drawn to which allow you to use your skills and life experiences in the most effective possible way.
> 2. The things that you know will have a *clear and positive impact* on *real people* *who you care about*.


## Inventing on Principle
Seen: February 21, 2016 (possibly once before too?)

[Bret Victor - Inventing on principle](https://www.youtube.com/watch?v=PUv66718DII)

Bretts working on ideas and getting them out into the world.
Principle: Creators needs *immediate* connection with what they create.

> So much of creation is discovery

Need to explore a lot in order to discover.

Example: Mario-like platformer.

* Time control/travel.
* Both back-forward manually,
* but also ability to seeing whole 'alternate universe' timelines from changing the code.

> People who are software engineers are just people very good at 'playing computer',
> envisioning what the computer will do with a given piece of code.

Example: Binary search

* Show actual values, including that of loops

Example: Analog electronics design

* Scrubbing through data inspectors to see matching/corresponding data in others
* Comparing two edges by clicking on one inspector. Shadow shown all other inspectors.

> Why do we have these squiggly symbols (electronics notation).
> Because they are easy to write on paper.
> But a computer is not paper.
> It is new medium, and we need to revisit these ideas.

> REPL are considered interactive programming - because its the best thing we can do on a teletype...

> I think about the millions of pieces [ideas] that are locked in peoples heads.
> [because the tools need to express them are not available]
> ...
> When I see a violation of [my principle]... [it hurts].. [a tragedy]
> I feel it my *responsibility* to do something about it
> .. Activist lifestyle, dedicate yourself to fighting for a cause
> Not just for social activist. They typically fight by organising.
> You can *fight by inventing*.

Did not just solve a problem, but also discovered/created the problem - that noone else saw.
Recognised a wrong which had been unacknowledges in society before.

Path of the craftsman: perfecting a skill.
Path of the problemsolver: go into a field, find a problem, solve it.
Path of the activist: find a principle and make it your cause.

How to find your principle?
Do many things. Use the experiences to find out what I care about.

Principles are diffent from ideas/thoughs because they are actionable.
Applied as a question, easily divides scenarios into a yes or no.


## We're doing everything wrong
Seen: February 21, 2016

[We're Doing It All Wrong](https://www.youtube.com/watch?v=TS1lpKBMkgg)
Paul Phillips, Pacific Northwest Scala 2013.

Key ideas

* Retricting expressiveness in language can make it more powerful,
in that tools/compilers can optimize for that usecase/task.
* Maybe a family of tools/languages instead of a "general purpose" one
* AST as canonical representation, not text.
* Changes (to code) as the primary input. Incremental build/verifiation

Some work on code-as-AST

* http://lambdu.org | [HN thread](https://news.ycombinator.com/item?id=11142911)
* http://sediment.io
* (maybe) [Jetbrains MPS](https://www.jetbrains.com/mps/)


## Improvind Our Ability to Improve
Read: January 24, 2016

[Improving Our Ability to Improve: A Call for Investment in a New Future](http://www.almaden.ibm.com/coevolution/pdf/engelbart_paper.pdf).
Dr. Douglas Engelbart, IBM Co-Evolution Symposium, September 24 2003

> ...we are not yet really making good progress 
> toward realizing the really substantial payoff that is possible.  That payoff will come 
> when we make better use of computers to bring *communities of people together* and to 
> *augment the very human skills* that people bring to bear on *difficult problems*.


> We need to move beyond understanding the computer as some 
> kind of fancy printing machine and begin to
> use it to analyze and manipulate the 
> symbolic content of our work, extending our
> own capabilities.

> The feature of humans that makes us most human – that most clearly 
> differentiates us from every ot
> her life form on Earth – is not our opposable thumb, and 
> not even our use of tools. It is our ability to
> create and use symbols.


