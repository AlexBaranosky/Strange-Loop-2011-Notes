
Functional Datastructures in Scala
==================================

Sequential ones, and Associative ones

Modern Computer architecture and how that efects how we design dsata structures

Immutable immutable immutable

But..... copy on write is extremely slow.

What we want
=======usii=====

Comparable aymptotic performance

Non-degraded versions (full persistence)

-> structural sharing, most cleverness in functional datastructures is in this idea of structural sharing

Singly-Linked List
==================

Not impressive in regards to complexity.  most everything is O(n)

A list is either... a cons cell with a value anda  tail,.... and empty list, called nil

These are the only cases.

Banker's Queue
=============

linked list is ineficient as a queue.

Naive persisted queue

Two lazy singly linked lists, front list for dequeue, rear list for enqueue

PEridically reverse rear into the front

Lazy amortization.


(dude in crowd: scheduler makes bankers queue more efficient)

2-3 finger Tree
===============

Ideal persistence dequeff  Lovely, but actually incrdibly slow...

Red black Tree
==============

balanced binary search tree

To prevent imbalanced trees --> color every single node in thertree either red or black.  Every path we follow will pass through the same number of reds as blacks

no red node can have a red parent.

IF you get these two properties you end up with a generally well balanced tree,.

four cases we consider for rebalancing.

PAtricia Trie - Fast MErgable Integer trie
==========================================

similar complexity to red black tree, but has logn union!

Trie" short for "data in the leaves"

branches are empty (contain a part of the key)

Bitmapped Vector Trie
=====================

comes from Clojure

functional analog to java arraylist

O(1) for madddddddd operations.  Only concat insert and prepend are O(n)

ALMOST!

Actually its not O(n), but O(log32n)  ...

n is the index into the vector.  On jvm indexes are limited to 2.5 billion.  Log32 of 2.5 billioon is a little less than 7.

This means that for any rational size dataset (aka it fits in memory), thus for all practical purposes they are actually O(n)

max seven depth of arrays of arrays (each array with lenght 32) --> max depth we will ever need is 7 deep, and thus at most any dereference will only need a max of 7 array dereferences, which is friggin fast on any machine. (and 14 bit operations! also really fast)  on really alrge datasets, this datastructure BEATS java.util.ArrayList (2 billion range)

How the heck do we beat a simple array?

-> locality of reference!

aka it uses arrays that pack nicely into memeory.


caching, bitesize data chunks

JVM considerations, heap locality

-> blows up the 2-3 finger tree, spreading the objects all over the heap.  Almost everything you do is going to be a cache miss!  Whcih takes a zillion years in cpu terms.  Totally unusable. (most use banker's queue instead... runtimes understand it better)

...

All data in the leafs, hence it is a trie.

Bibiliography
=============-

Okasaki, Purely Functional Data Structures

Okasaki, Red-Black Trees in a Functional Setting

Fast Mergeable Integer Maps

Hinz & Patterson - Finger trees a simple general purpose data structure
