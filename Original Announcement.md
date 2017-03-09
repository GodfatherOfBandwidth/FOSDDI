# FOSDDI
Free Open Source DHCP DNS IPAM Project

==========================================================
Project Proposal and Call for Feedback: FOSDDI

==Abstract==

There is a need for a FOS DDI solution, commercial solutions do exist but they are cost prohibitive and not attainable for many institutions.  All of the components necessary for a FOS DDI solution are now available, all that remains is to create the ability for these tools to communicate programmatically.

This paper proposes using ISC Bind, ISC Kea, and PHPIPAM as the basic building blocks of a DDI solution and extending their functionality where/if necessary.  Feedback and volunteers are welcome.

==Detail==

Like many system and network admins I find myself in need of the ability to keep track of many IP addresses.  Traditionally this has been the purview of the mighty and humble spreadsheet.  However; once an organization reaches a certain size, or your patience finally runs out, the task of tracking IPs manually becomes burdensome and, many times, error prone.  

As most people can tell you documentation is the most boring part of almost any job, but it is also one of the most important parts. As our day-to-day responsibilities are carried out the task of updating that IP change or removing that old reservation becomes less important than the manager worried about project X.  After a time everyone forgets about the IP list maintenance and now you are left with incomplete and incorrect documentation.

This project's goal is to provide a simple yet powerful tool that allows an administrator to quickly and simultaneously configure, provision, and document their DHCP and DNS infrastructure using a graphical user interface.


=Tackling DNS=

ISC BIND is an excellent DNS server, it is the gold standard of DNS servers.  Its scalability and performance are excellent.  BIND also allows for dynamic updating of records which is important for maintaining uptime of critical services.

For integration into a DDI solution little to no changes should need to be made to BIND.  The goal is to interact with the DNS service using established methods.

=Onward to DHCP=

ISC Kea is a new DHCP server that is showing immense promise, with the advent of using a database and having an API to work with DHCP can now be configured and tweaked programmatically in a much more efficient way.  

Integrating Kea into a DDI platform should be rather straightforward if the necessary API calls are available.  At the time of this writing I do not know enough about the APIs to say much about them.  

=True IPAM at last=

PHPIPAM is a web based GUI for tracking IP address usage and static assignments, this is the tool that your spreadsheet wishes it could be.  But it lacks a crucial feature to make it an excellent tool.  It cannot interface with your DHCP server or your DNS server.  Changes made in the IPAM interface exist only as documentation with a pretty face.

This is where I foresee the bulk of the modification necessary to produce a working DDI solution will take place.  Hooks will need to be added in the correct locations that trigger API calls to Kea and also updates to BIND when necessary. 

==The Plan==

My idea is to use IPAM as a sort of pseudo front-end for BIND and Kea.  I have chosen the project PHPIPAM (but that decision is up for debate).  I would like to extend PHPIPAM in such a way that one need only ever make changes in the web interface and all necessary configuration directives are then given to the proper server.

This plan results in a few things:

A single point of management, no longer will it be necessary to configure 3 separate text files on 3 individual servers.  

Create a new subnet in the web GUI, the changes are applied in real time to your DHCP and DNS servers.

Did you make an error in that last config file?  Must have, DHCP wont start … Changes made programmatically are done by proven calls / procedures and cannot muck up your configs.  

Changes are also tracked and logged.

Lots of other things I can’t think of right now because I’m tired.

==The Call==

This project is in its infancy.  I am putting this information in the public domain so early for a few reasons.  

First, there is the chance that I have completely missed something and I am attempting to re-invent the wheel with this project.  In this case I welcome anyone to send me the info on the project that has the same or similar functionality … I would REALLY like to know about it.

Second, I am attempting to gauge public interest in a FOS DDI solution.  I can personally see many, many possible deployment scenarios, but others may not and I welcome any constructive criticism others may have.

Thirdly, I am looking for feedback regarding my chosen group of tools.  I know there are other IPAM tools available.  I have looked into many of them and felt PHPIPAM was the best and is still actively being developed.  But I am not omniscient and there may be a better solution available that I am unaware of.  I do feel the the choices of BIND and Kea are rather solid, but I am willing to entertain anything at this point.

Fourth and finally, I am looking for volunteers.  People who might be interested in assisting in developing and/or testing this project are welcome to contact me.  I am very serious about developing this project into a fully fledged, production ready, enterprise grade, etc. solution.

==Comments and Contact information==

I welcome any feedback, comments, or questions, please post them to GitHub.  I will do my best to respond to questions in a timely manner. 
