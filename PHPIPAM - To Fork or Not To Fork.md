PHPIPAM has been dropped from this project.

After several attempts to contact the project maintainers were un seccessfull and after a code review it was determined that the difficulties arising from using a separatly maintained project would not be the best course of action.

So ... that answers the fork or no fork question ... There is no fork.

===============================

******This section is outdated and will probably be deleted soon******

As I get further into this project it seems that the changes necessary to PHPIPAM will
render it essentially unusable as only a documentation tool (which has been its primary
purpose).  It may be possible to make it so FOSDDI integration is enabled by a 
configuration directive, or a checkbox in the GUI ... but this seems like it would be
a LOT of work and could add a lot of confusion.

The development cycle of PHPIPAM seems much more concerned with stability so forking the 
project doesn't actually sound all that bad.  We could gain all the benefits of the excellent
GUI PHPIPAM has to offer while coding in the necessary bits to make the integration with 
Kea and BIND work out-of-the-box.  At the same time, we can remove the bits that are 
not necessary for FOSDDI functions (IE: removing storing subnet info in its onw DB, since
all the info should reside in the Kea DB, which by definition should be up to date).

Any changes that may be beneficial to the PHPIPAM project would (of course) be submitted for
upstream adoption. Should the PHPIPAM team decide they want to integrate anything we produce
they are welcome to it.

When PHPIPAM does release a new build care should be taken to integrate such changes into
the fork ASAP, doubly so for any security updates.  With this in mind care should be taken
that all the modifications in the forked PHPIPAM be well documented so that when rebasing
is necessary it can be done as painlessly as possible.

I will contact the PHPIPAM dev team and ask thier opinion on forking PHPIPAM.  There
is the possibility that they have better ideas and can point me down a better path.

===============================
