---
ID: 991
post_title: 'The Basics:  The Drone Chronicles'
author: pkelley
post_excerpt: ""
layout: post
permalink: >
  https://www.criticalpathsecurity.com/the-basics-the-drone-chronicles/
published: true
post_date: 2018-07-11 16:51:05
---
<img title="Wikipedia" src="https://www.criticalpathsecurity.com/wp-content/uploads/2018/07/First_MQ-9_Reaper_taxies_at_Creech_AFB_2007-1024x680.jpg" alt="Wikipedia" width="1024" height="680" />

At Critical Path Security, we spend quite a bit of time performing research on threats against the public and government sectors.  Much of that research leads us to discover that missing patches and default credentials far surpass any other mechanism used to breach an environment.

In a typical Penetration Testing engagement, we will compromise several assets on the network using default credentials in well under 2 minutes.  Often, this leads to a total breach of the environment. Malware can spread much faster.

The attack on the Creech Air Force Base in Clark County, Nevada was another example of those attacks.  This time, the default credentials for a Netgear router (admin/password) granted access to a military network with classified information. To be more specific, the manuals and information about the airman assigned to the base’s Reaper maintenance unit were siphoned and placed on the dark web for sale. The gravity of the breach is yet to be determined.
<blockquote>The military has yet to determine the extent of the breaches but will be investigating the attack. “[This is a] disturbing preview of what a more determined and organized group with superior technical and financial resources could achieve,” the group stated.</blockquote>
Unfortunately, this is an extraordinarily common event and it is happening all across the globe.  These tactics are used against small businesses to distribute ransomware, as well as against aging power grid components to cause disruptions and damage.

In fact, a simple search on Shodan.io will render the results of thousands of devices which are easily accessible with little more than a web browser and "admin/admin". These devices range from simple routers, as used against Creech, to satellites, trains, web cameras, and more.

The device at Creech was a router, which provides extensive paths of communication to several, if not all, assets on the internal network. The hacker told Recorded Future that he frequently “entertains” himself by watching live streams of sensitive footage from airplanes and border surveillance cameras. Using the router as a pivot point, these tactics and techniques can be easily applied in nearly all networks.

[caption id="attachment_993" align="aligncenter" width="920"]<img src="wp-content/uploads/2018/07/drone.png" alt="" width="920" height="613" /> Recorded Future[/caption]

Fortunately, it's an easy thing to solve and generally costs nothing to the owner.  When devices are purchased and introduced to the home or business networks, changing the credentials should be the very first step, to be followed quickly by software updates from the manufacturer. You can often find step-by-step instructions on how to properly change the credentials and remove unnecessary services.

At Critical Path Security, we always strive to offer additional free solutions to solve these sorts of problems. A free script to use in the BRO-IDS platform is available <a href="https://github.com/CriticalPathSecurity/bro-scripts/blob/master/mass_default.bro" target="_blank" rel="noopener">here</a>. Follow the normal steps of loading the script into local.bro and perform a broctl deploy to restart. If BRO-IDS observes a connection to a device utilizing a set of commonly known credentials, a notice will be delivered to the logs. If you are already a client of Critical Path Security and use our Managed SOC service, this behavior is already being monitored.
<blockquote>"192.168.1.182 is engaging ftp sessions with a network device (192.168.1.231) using default credentials - ftp / ftp."</blockquote>
As always, should you bump into hurdles along the way, feel free to reach out to the Critical Path Security team.  We're here to help.

-Patrick