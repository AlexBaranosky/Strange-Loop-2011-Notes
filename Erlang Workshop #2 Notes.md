OTP and Erlang are really one and the same.  OTP's name means little, but was an internal marketing push within Ericson so they could use Erlang for another project.  Open Telecom Platform = 3 buzz words. :)

Behaviours like interfaces.

Use Behavior to pull out boilerplate from basic server implementations:
init, send, loop,

asynchronous init in OTP needed so we can guarantee ability to start up say 10 processes in a *specified* order

Building TCP/IP Server -

Erlang myth debunked: no one really uses hot code swapping in production

Supervisors
===========

supervisors watch other processes and do stuff based on what they see.

They watch things that die.

Hieracrchy of sueprvisors, who monitor childnodes, who could be workers, or could be other supervisors. Usually not very deep hierarchy... deep hierarchy is a code smell essentially.  All rooted through a single root supervisor.

When they see a dead process, they startup another using a known good state.

Hotswapping can be *really* nice for development to reload the code.

Applications
============

How to know how to structure the applications? Each application = pieces that  provide *singular* services. Number of applications equal to number of services you need to provide.

Closing
=======

Every large program in Erlang that does not use OTP

History
=======

Designed for telecom, all other languages sucked for their requirements after 2 years of search.

Soooo let's build a language, with that set of requirements. This is why Erlang is so suitable.  Also, this approach to language design is unique.

Originally implemented in Prolog, no longer.
