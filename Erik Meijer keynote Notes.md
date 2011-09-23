
NoSql => unfortunate, negative name.

Big Data All about Variety
==========================

Like Extreme programming, good idea, but name can put some folks off.

Big data, same thing.  Not just size byt also bout the multilicity of data models and about interaction patterns between producers and consumers.

volume, variety, velocity in a 3d space.


noSQL is the dual of SQL
========================

COSql, more user friendly name :)

Objects vs Tables
=================

if you're using an oo language you are using a key value store.

    NoSql               => think objects
    Relational database => think tables

hence devs tend to like NoSql!

Objects
=======

"I do consider assignments statements and pointer variables to be among computer science's most valuable treasures."

-- Donal Knuth

Cannot hide the pointers and imperative code, it is very improtant to computing.

Amazon SimpleDB Sample Query Dataset
====================================

new Product(), data class object

pointer in memeory, then values assigned to key-value combos.

Then in C# you can make LINQ queries against that Product

Once again, dude, objects ARE key-value datastores!

Tables
======

Normalizing data is a strange thing => I think it de-normalizes it! ;)

Took that one Product, and had to split it into 3 classes.

Keywords needs to have ProductId that points to a legit Product, and maitain referential integrity.

Now my lookup got crazy, cus I need to do a join.

"Now, my brain is the size of a peanut: I cannot understand this anymore." - Erik Meijer

Frege 1848-1925
===============

One problem of relational model, is that it is not compositional.

Objects
Fully compositional

vaalue := scalar
          new { ..., name = value}

Tables
Non compositional

value := {..., name = scalar }

But there are advantages to forcing data to be non-composed.  I can make more assumptions about the data, because I know the shape of the data.

NULL semantics are a mess.

Impedance Mismatch
==================

Problem with having two languages.

Hence ORMs!  - you want to deal with your relational data as if they were objects.

ORMs get quite complicated ya see.  gn6m22

If you're in the relational worlds and you use joins, you have to be careful.  Indexes are there to speed up joins.  A simple index is basically a precomputed join.

Mathematicians are way smarter than us, and have figured everything out already.

Category Theory
===============

Category theorists are relally the first oo programmers on the planet.

CT => programming agaisnt an itnerface of a function.

Duality. (that's a math thing)

We sa computer scientists need to work more as scientists, not driven by emotion but by objective stuff.

SQL is the Duality of noSQL. !!

stop this noSQL talk; let's start calling it coSQL!  Because they are not in conflict.

They are in harmony... yin-yang.

Yin mean "open" - coSQL is open!

SQL is a closed world where everything fits, so you can take advantage of that structure.

The fact that the two can transmute into each other.'

Consequences of Duality
=======================

Relational row, knows its identity
coSQL cannot be sure of equality without having the pointer to the objects as well.

Transactions are sweet for SQL (clsoed system)

Cannot stop the world on the web... you have to eventual consistency slash syncinfg up (open world)

Summary
=======

Shouldn't pick one based on fashion. But look at your requirements to decide which model fits best!
