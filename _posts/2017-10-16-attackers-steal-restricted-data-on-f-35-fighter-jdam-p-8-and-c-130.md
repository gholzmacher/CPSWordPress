---
ID: 444
post_title: >
  Attackers steal restricted data on F-35
  fighter, JDAM, P-8 and C-130
author: pkelley
post_excerpt: ""
layout: post
permalink: >
  https://www.criticalpathsecurity.com/attackers-steal-restricted-data-on-f-35-fighter-jdam-p-8-and-c-130/
published: true
post_date: 2017-10-16 17:10:27
---
In a scenario that's become all too common these days, it seems that a subcontractor responsible for the development of F-35, JDAM, P-8, and C-130 parts and assemblies has been hacked.

Unfortunately, it wasn't just credit card and other consumer data compromised. It was detailed information on some of the world’s major shared military defense systems – aircraft, bombs and naval vessels. Additionally, it seems that this breach has been active for a bit of time.

In fact, it was said that almost a year ago, in November 2016, by the Australian Cyber Security Centre (ACSC):
<blockquote>…became aware that a malicious cyber adversary had successfully compromised the network of a small Australian company with contracting links to national security projects. ACSC analysis confirmed that the adversary had sustained access to the network for an extended period of time and had stolen a significant amount of data.</blockquote>
The attackers had been inside the company’s network at least since the previous July, had “full and unfettered access” for several months, and exfiltrated about 30GB of data including, “restricted technical information on the F-35 Joint Strike Fighter, the P-8 Poseidon maritime patrol aircraft, the C-130 transport aircraft, the Joint Direct Attack Munition (JDAM) smart bomb kit, and a few Australian naval vessels.”

Though the company was not named, it has been described as a 50-person company with a single IT person handling all aspects of Information Technology and Security. It's also apparent that the company was not compliant with CSC or similar regulatory frameworks, as...

<!--more-->
<blockquote>There was no protective DMZ network, no regular patching regime, and a common Local Administrator account password on all servers. Hosts had many internet-facing services.

Access was initially gained by exploiting a 12-month-old vulnerability in the company’s IT Helpdesk Portal, which was mounting the company’s file server using the Domain Administrator account. Lateral movement using those same credentials eventually gave the attacker access to the domain controller and the remote desktop server, and to email and other sensitive information.</blockquote>
<em><strong>Critical Path Security recommends the following, at the very least:</strong></em>
<ul>
 	<li>Use application allow lists so only run approved programs</li>
 	<li>Patch applications like Flash, web browsers, Microsoft Office, Java and PDF viewers</li>
 	<li>Patch operating systems</li>
 	<li>Restrict admin privileges based on user duties</li>
 	<li>Perform network and system log data</li>
 	<li>Utilize a full-featured IDS or IPS solution</li>
</ul>
Read the <a href="https://www.acsc.gov.au/publications/ACSC_Threat_Report_2017.pdf" target="_blank" rel="noopener">ACSC report</a> for more information.