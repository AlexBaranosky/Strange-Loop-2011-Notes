Importance of being concurrent
=============================

spend more time waiting on data than we do computing our response

let's wait for as many things as we can at once

fork - task - join
     - task -

but thread don't grow on trees

so we use a thread pool

What about nested concurrency?
==============================

When you have data dependencies between synchronous tasks, then sometimes you can be waiting for threads to comlete that will never get to start, because there aren't any threads left in the thread pool

These are not mutually exclusive solutions

fork join vs asynchronous callbacks

Publsiher/Subscriber
====================

textbook pattern


