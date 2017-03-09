==FOSDDI==

@@@@@@@@@@@@@@@@@@@

FOSDDI IS RECRUITING!!!!!
Drop me a line if you are interested in 
participating in the project!

We need people in all positions:

Web developer? … come on down!
DB/SQL Experience? … We need you.
Social Media / Public Relations … Yip, you too.
…
If you have a skill you think would benefit the project I would love to talk to you.
Drop me a line here on github!

@@@@@@@@@@@@@@@@@@@

Free Open Source DDI (DHCP - DNS - IPAM)

FOSDDI is now under active development.  After a year of waiting, it is time ... time to arise from my slumber ... *****cough***** ... *****ahem***** ... Where was I? Oh yes! FOSDDI, it is COMING!!!

This space will evolve as the project matures so expect changes!

FOSDDI has three main parts:

1) DHCP

2) DNS

3) IPAM

DHCP:

FOSDDI uses the Kea DHCP server from ISC.  Kea has a number of compelling features that make it ideal for this project.  Importantly are the abilities to store leases and configuration parameters in a database and interaction with the running DHCP instance via a RESTful API.

DNS:

FOSDDI uses the venerable DNS server BIND from ISC.  As a rule, FOSDDI uses the latest stable version for stability and security rationale.  Although you  will most likely get any recent version to work, FOSDDI will only be tested against the current stable release.

IPAM:

IPAM (IP Address Management) is handled by a custom built web based GUI.  The guiding principal behind this GUI is function over form.  Not to say the GUI won’t look good, but rather that it is designed to facilitate the most efficient way possible to work with the DHCP and DNS services.

IPAM functions were originally planned to be done via a separate project called PHPIPAM.  However; several attempts to contact the maintainers proved fruitless and after a code review it was determined the amount of work necessary to retrofit an existing project and continually backport changes would be far greater than developing our own GUI  … so … here we are!

==Usage/Deployment==

FOSDDI is meant to be deployed on a dedicated server in a single host or high availability cluster  configuration.

To achieve HA FOSDDI makes use of a few FOSS projects; HAProxy, Apache, MariaDB.

The bright side is that when you use multiple servers you spread the load over them and do not necessarily need very powerful gear.  Also, FOSDDI loves to be virtualized and can be deployed in any virtualization flavour you like.

An HA deployment should contain at least 3 servers but may contain many more.

