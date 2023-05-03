# HAIMqttOmniBridge

This is a way of getting HAI Omnipro information into Hubitat.   Could not find anything so I put this together to make it work and hopefully this will help someone else.

First you need to setup a great piece of code https://github.com/excaliburpartners/OmniLinkBridge  which gets the information into mqtt.

Then import these sets of code into your hubitat drivers code section.  By default the code is setup to look in the mqtt folder of omnilink.

Then add a device and use the associated driver.  In the preferences enter your mqtt ip address.


Area Driver:

For this driver it is setup to monitor one area for Alarm status.   Night, Away, Home etc...

In preferences you enter a string of the area you want to track for instance "area1"

Zone Driver:

For this driver it is setup to monitor a zone in your HAI system.   Secure, Not_ready.   

I have converted those to hubitat contact sensor of open, closed.

In preferences you enter a string of the zone you want to track for example "zone22"

Unit Driver:

For this driver it is setup to operate HAI controled switches. 

In preferences you enter a string of the unit you want to operate for example "unit20"


