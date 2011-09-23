
Email organization application
==============================

Desktop component in C#

The cloud component in Haskell.

Why Haskell?
============

Do I know the language? Can I be productive in it?

cAn I hired good people?

Do I know the terrain well enough t

Language knowledge
==================

Haskell expert

But had never written any C# or used a modern IDE at all

Both seemed to work out fine

Hiring: signal
==============

HAskell experts hard to find

Coding chops of Haskell experts are great devs generally in ANy language

Mere interest in Haskell (or Clojure or Scala) are indicators you'd be a good hire

Python used to be a good "knows language X" filtering method, but not any longer

Yet, the precence of C# on a resume is completely useless to a hiring manager.

Hiring: noise
=============

What does working with HAskell involve?

Write a few lines of code

Load it into the interactive interpreter (ghci)

Did the interpreter give a type error? (fix it)

Did the code load?  Try it out by hand.

Did it work? Build the native-code app and try thatone recall that?.

Difference from other Environments
==================================

The "edit then dump into interpreter" feels like lisp

- With the exception of the typechecker telling you how loopy your reasoning is

The "compile a native app" part feels a lot like C++.

The "lack of IDE support" bit feels a bit like 1994.

And For an Aside...
===================

1994 -


Cloud Bit
=========

Haskell in the cloud

Haskell code does machine learning


github.com/mailrank




QuickCheck
==========

Cannot say enough good things about QuickCheck - seek it out, and figure out how to use it - or write your own.

QuickCheck is shockingly more effective than traditional unit tests.

If there is only one thing you take out of this talk, it is "I must use property based testing"

How has it worked out?
======================

Close to beta

written http load tester to beat it up

(Think AppacheBench of httperf, only better)

Haskell vs C#
=============

It's a decent language

LINQ is pretty nice

even for vi/emacs veteran, IDEs are pretty nice

Resharper is pretty sweet

Types
=====

C# has very limited local type inference

Some language features (properties) encourage really shitty APIs, and MS goes to town with them in theiir APIs

Concurrency
===========

after using STM, then C#'s old school concurency stuff seems like going back to the dark ages

* by far the single biggest bug was a concurrency related bug from a related piece of 3rd party code!

Should you be using Haskell?
============================

There are enoguh libraries these days, teaching materials decent, and community will help you out when needed



