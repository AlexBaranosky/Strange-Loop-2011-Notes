
Founder of the Multiverse STM impl for Java, used in Akka.

Also commiter on Akka.

newIntRef()

AtomicInt
synchronized
volatile

atomic {a.get()}

if a exception inside atomic block, then the write will be rolled back

ReliabilityProperties
=====================

Atomicity
Consistency

=====================

can add consistency checking in your Java code with if(xyz) throw new Exception();

Isolation
=========

again, atomic { ... } saves the day

Deadlock
========

Conclusion
==========

great technology in isolation: Multiverse

breaks down as soon as you are going to combine it with different solutions that are not optimized for use with STM.

Way to get around it is to use STM more as a database.

