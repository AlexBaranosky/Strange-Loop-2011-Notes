
how to think about Map/Reduce if you are coming from the relaitonal database world.

He's from Basho Technologies!

Riak scalable
highly available (lose a node, still good to go)
networked
key value store.

Everythign you write and read is replicated 3 times: spread around the cluster ofmachines.  Thus it is highly availabel.

Riak Data Model: keys and values!

unlike some kv stores, you can store your data however you want: xml, json, images

Keys get grouped in buckets which are categories.

GET    riak/bucket/key
PUT    riak/bucket/keyx
DELETE riak/bucket/keyxlso can use protocal bufers

Riak store metadata with keys.

Cotnent-type
last-modifeied
link
x-riak-meta-*

were two ways to query, now 4 ways!
===================================

* Link traversal ("walkoing"
* full text search
* secondary indexes
* map/reduce : NOT a query language, NOT a framework, Na database, not just hadoop

Why MapREduce
=============

easy distribution, cus just concerned with inputs and outputs of computations

Data Locality.

Scales up and down: one machine or one hundred machines!

"It's just code" (simple, unlike relationsal ideas)

Understanding Map
=================

1 datum -> 11 call

Extract

Transform

Filter

Understanding Reduce
====================

List of N data -> M calls

Sum, Count, Group

Sort, Limit

Max, Min

NOT for batch processing.

NOT for views and indexes.

NOT for crunching your entire sdataset

NOT limited to one of each function

IS for low latency jobs/queries (fdits into one web request)

IS for limited, known inputs (you know the keys)

IS any sequence of MAP and Reduce functions can be composed

Features
========

Can use JS or Erland to write teh queries, Erlang slightly more performant

Can search 2I inputs

Link phases

Key-Filters (keys containing data about that object)

Key-specific data

Phase-specific data

Riak MapReduce Quirk
====================

Values are opque
Map phases take input lists
Erlang > JavaScript
Built-ins > Source
Reduce funs generally applied more than once.  No gurantee that it will get your whole dataset, or that it will run only once.

Simpel Query
============

POST /mapred
Content-type: apllicatioon/json

{
    :inputs:[["people", "seancribbs"],
             ["people", "pharkmillusp"]o

SQL Translated to MapReduce
===========================

Duplication of data is ok, with denormalization.  If it makes queries easier, than do it!

SELECT <fields>
===============

WHERE <conditions>
==================


