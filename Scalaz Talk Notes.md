Capital IQ, Boston, Scalaz contributor since 2008

Functional Programmign in Scala - Book coming out next Spring.... (always dubious)

Library for purely functional programming Scala.

Type which add composability and modularity.

Function?
=========

A => B

and for any value of A always gives you the same result of B

Side-Effect?
============

reading/writing
re-assigning variables
setting fields
mutating data structures
throwing exceptions


Referential; Transparency
=========================

enables the sumbstituion model of computation

compute subexpressions, sort of likea tree, then compose them into the result of the program

Side-Effects = Lie
===================

Int => Int , but launches missle!

Why?
====

Modularity, and ability to repurpose the elements of your program.

Compositionality, the property that you can undersand a program when you understand the subexpressions, and also the rules by which they are combined.

FP is a Discipline in Scala@@@  You can F it up
===============================================

Scalaz is here to help you not fall wagon. :)

import scalaz._
import Scalaz._

Getting Started
===============

A => Identiry[A]
M[A] => MA[M[_], A]
etc...

Type-Safe Equality
==================

===

map.get(x) == y

ifI have an equal for A, I automatically have an equality for Option[A]

Monoid Typeclass
================

Semigroup, is something with an append function(M, M) => M

Monoid is a Semigroup with a 'unit' called zero  ... |+|

Examples:
=========

Int+ 0
Int * 1
|| false
A => A compose and identity
List[A] => ++ and Nil
+ ""

Monoids Compose
===============

(1, "foo") |+| (3, "bar") => (4, "foobar")

Monoids Add modularity
======================

def sum(A:Monoid].........

Then you can call sum on any monoid implementation

Foldable
========

foldMap ???? // google that ish

Validation
==========

Purely functional error handling

Validation only logs the FIRST error, after you fix the first, then you will see the second error, because of the semantics of flatMap

If failure type is a semigroup then you can accumulate validationf ailures!!! SWEET.

how? -> using |@|

ValdationNEL = Validation[NonEmptyList[E], A]

// see the slides from the talk to see sample code of different ways to validate.

- can conert a list of validations, into a validation containing a list -- just use sequence method

Applicative Functors
====================

any M[A] can be composed with |@| if there's an Applicative for it

TODO
====

review the slides for learning material

State
=====

state monad

Generic
=======

Can write a zipwithIndex that only depends on Traverse, and then voila.

#scalaz on Freenode

use State for IO in Scalaz
