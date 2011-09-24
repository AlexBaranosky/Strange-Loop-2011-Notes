
Art of MetaObject Protocol - most important book on OO programming in a decade
==============================================================================

Best books of how does one develop an API properly?  What are the critical decisions you need to make abou your API so your users can swap in different decisiosn on how things should work.

How are black boxes so hard to reuse!!??

You want to create a spreadhsead program for the billionth time.

You cant make grid soquares with windows... instead you reduplicate all of Windows, because you can't repurpose windows !!!

So you got these hemotomas of duplication.  Fuck me.  Now you need to reduplicate the whoel thing with one minor change.

His arguments is there's no such thing as hiding details, because every dedcsion you make WILL show through.

Let's take a different route?  What if instead of hiding we divide it up, give hooks for people to change particular impls.

CLOS solves this with reflection... a meta-interface to control the base class.

Ideally program optimistically... like actually useOS windows for our spreadsheet windows.  Swap pout the stuff so we havwe lightweight hooks instead of the heavy weight default hooks Windows uses.

neither OOP nor Fucntional will solve this problem.

We end up with a case where worse is better.  We choose the 70-80% solution. Fuck us.  We end up maintaining things forever.

JQuery is totaly undscalable useful.

UIKit is monstrous.  no continuoum between the two choices.

Is there a wprld where worse is not bertter?
============================================

Predicate dispatch - idea is to subsume pattern matching fromm fucntional with generic methods from CLOS.

Best literature is OCAML, ML, Haskel papers.

Lazy Haskell pattern matching.

Luc Marangot -  awesome paper.

No lexer

No Parser

Radical Simpplicity

* seq patterns
* seq IPersistent
* or patterns
* guards
* local binding with 'as'
* local matching

* fully extensible
* pattern match on Java objects

* vector patterns - bit mapped vector trie
* wait, what about primitive arrays, bytes? etc?

impossible to guess whats desired

not smart enough compiler

Runtime abstractions over byts === too costly

Instead, Nolen gvies hooks into the compiler for extension on types like bytes or arrays

Zero Overhead, Jvm does crazy inlining and awesomeness.

Faster than scala for primitive array pattern matchign.

Thankfully, Clojure 1.3 made low level operations efficient.

ClojureScript
=============

Will it help us avoid some of the problems inherent in writing code in the browser?

MApping Dilemma
===============

how well do our languages allow us to delay making decisiosn about concreitions?

how well do our languages let us pick strategies - including


Alan Kay, Peter norvig, Dan Ffriedman


Trsadioinal OO needs to go otu the door
=======================================

Good parts will rise though.

Colelctively learn how to extend languages.

BOOK: The Reasoned Schemer

More:
=====

Api should present the simplest interface possible... aka provide default behaviour.  But when they need to tweak the system, it'll be much better if that hook is there for them.

Q: should everything be public??
================================

no, I don't think no private... but we should seriously consider the options and think about the repercussions, how doe siti effect the solution to the problem.

Q: programs to be tasks... then programs that are written to be a tool to implement a class of problems.
========================
good stuff

Q: Is the pattern matching lazy or eager?
=========================================

Not lazy, but will behave the same way it will in Haskell

Q: Generic programming. How's it relate to the mapping dilemma?
===============================================================

Yes. we'd like to be able to program more generically.

PREDICATE DISPATCH
==================

Need to make it performant.

How can we make pattern matching more extensible.  Add new pattern cases at any point in the match???







