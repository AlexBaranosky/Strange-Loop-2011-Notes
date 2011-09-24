
Tools I can use to conduct a similar discussion/talk to convince others of the value of these things!

"Simplicity is a Prerequisuite for Reliability"

Word origins
============

could we go back to what these words REALLY mean?

Simple: sim-plex - one fold

Complex

Easy: ... lie near

vs hard

Simple
======

One/fold braind
One role
One task!
One concept
One dimension

But not
    one instance
    one operation
    about lack of interleaving, not cardinality

Interleavage is an Objective notion

Easy
====

Near, physically
    on our own hard drive, in our toolset, IDEA apt get gem install

Near, to our current understand/skill set
    familiar - mentally near

Overly fixated on these two meanings of easy.

If y9ou want everything to be familiar, you learn NOTHING

Third meaning of easy:

Near, to our capabilities.

Easy is RELATIVE - unlike simple.

Construct vs Artifact
=====================

over time we glom stuff onto the artifact, not the original construct

programmer convenience
programmer replaceability

Limits
======

We can only hope to make reliable those things we understand

We can only consider a few things at a time

Interwined things must be considered together (burden!  and combinatorial)

Complexity undermines understanding

Change
======

refactoring and tests allow us to make change with ZERO impact....   just kidding ... sarcasm

If you change sofware you need to analyse and figure what needs to change.

Ability to reason about your application is critical to changing it with out fear

NOT talking about formal proofs!

Debugging
=========

What's true of every bug in the field

passed the test, and the type checker.

Now what the heck do we do?

"Guard rail" driven development?  Do the guard rails guide you places?

You need to be able to reason about a program to find the BUGS!

We can solve the sprint problem: we just fire the starting pistol every hundred yards.

If you ignore complexity - you will invariably sloooowwww down over time.

Ease focus, fast at start, slow down every sprint to redo everything

Siplicity focus, a bit slower at the start, but then ramp up toa higher steady state of productivity

Easy Yet Complex?
=================

Many compicating constructs are
    succintly descirbe
    familiar
    available
    easy to use

What matters is what the program yields!

When there is complexity there (insidental complexity, because has nothign to do with the artifact you created)

Benefits of Simplicity
======================

Ease of understanding
Ease of change
easier debugging
Flexibility

Making things Easy
==================
bring to hand byinstalling

getting approved for use
become familiar by learning, trying
but mental capability?
   not goign to move very far
   make things near by simplifying them

Juggling - how many balls you want in the air?  How many of those you want to be application complxity, and how many incidental complexity?

Parens
======

Not at hand for most
nor familiar
but are they REALLY simple?

Not in CL/Scheme
    overloaded for calls and grouping

this is a valid complaint

Adding a data structure for grouping, e.g. vectors, makes each simpler

now they are easy to you!

What is In Your Toolkit?
========================

COmplex           Simple

state, objects    Values

methods           functions, namespaces

vars              managed refs

inheritence, switch, matching   polyumorphism

syntax              data

imperative loops, fold                  set functions

actors                 queues

ORM                      declarative data manipulation

conditionals              rules

inconsistency             consistent


Complect
========

archaic - braid together

don;t do it

complecting thigns is a source complexity

best to avoid in the first place

Compose
=======

to place together

composing simple copmpnents is the way we write robust software!

can make simple systems byu making them modular!

What do we want to make these two things allowed to think about??

AKA, program towards abstractions! BBO

Don't be fooled by code organization

State is Never Simple
=====================

Complects value and time
it is so EASY!

interleaves everything that touches it, directly or indirectly

Not all refs/vars Equal
=======================

but they're not the same

All warn of state, help reduce it

Clojure and Haskell refs compose value and time
   alow you to extract a simple value

   provide abstractions of time

Does your var do that?

State c-> Everthinyg they touch

Objects c-> State, identity, value

MEthods c-> function and state, namspaces

Syntax c-> meaning, order

Inheritance c-> types

swithicng/matching     multiple who what pairs

variables                value, time

loop, fold             what/how

actors                 what to do, who does it

ORM                    OMG

Simplicity != Easy

The Simplicity toolkit
======================

You do not need C#/JAva/C++.  you can make big systems with dramatically simpler tools.

We make hundreds of variations tha tmake it tough to manipuolate thhe seence of this stuff (data).  We should use simple data so we can write code to work on the essence of this stuff.

Datalog?
rules - libraries, prolog

(didn't typ ethis list of places to get the simple versions, review the video for that)
Environmental complexity
========================

Resourrce, eg memory, CPU
inherent complexity in impl space
   all components fight for these

   Segmentation
         waste

Individual policies don't compose
    makes things more complex

Absstraction for Simplicity
===========================

not HIDING

Who, What, When, Where, Why and How
I don't know; I doon't want to know

*What*
operations
form abstractions from related sets of functions
   small sets

Represent them with ploymorphism constructs
   speicify inputs outputs semantics
   use only values, and other abstractiosn

Don';t Complect with HOW

How, is somebody else's problem.

Data engine or logi engine, you can do that stuff!!

Who
===
Entities impl abstractions
Build from, subcomponents direct-injection style
    pursue many subcomponents
    eg, policy

Dont complect with
   component details

*How*
Impl logic
Connect to abstractions and entities via polymorphism constructs
Prefer abstractions that don't dictate how
   declarative tools

Dont compect with
    anything :_)

*When, Where*
Strenouously avoid complecting thiese with the design
can seep in via diretly connected objects

Use queues

If you're not using quques extensive you should start right away, like right after this talk

*Why*
The policy and rules of the application
Often strewn everywhere
     losts thefdfadsdff

Information is Simple

you ruin it, byhiding it behind a micro language, wrong because it is complex.

thwarts generic data composition
ties logic to representation du jour

Represent data as data


Bottom line is that simplicity is a chocie.

We have culture of complexity.  We're in a self-reinforcing rut.

REquires constant vigilance.

Requires sensibilities and care, easy != simple

Develop sensibilities around entanglement

     Seeeeeing the complecting.

Reliability tools (testing, refactoring, etc)  all safety nets that don't touch this problem.

Choose simple constructs over complecitygenerating constructs

ints the artifacts, not the authoring

create abstractions that have simplicity as the basis
simplify the problem space before you start

simpicity often mean you have more things... not about counting

Reap the benefits!

Parting joke
============

Tell them this when they try to seel you a soffisticated type system :P ;)
