---
ID: 757
post_title: AutoSploit and Collateral Damage
author: pkelley
post_excerpt: ""
layout: post
permalink: >
  https://www.criticalpathsecurity.com/autosploit-and-collateral-damage/
published: true
post_date: 2018-02-04 11:03:23
---
&nbsp;
<p style="text-align: center;"><img src="https://www.criticalpathsecurity.com/wp-content/uploads/2018/02/Screen-Shot-2018-02-04-at-9.46.04-AM.png" alt="" width="509" height="401" /></p>
Last week, a toolkit was released, that based solely on results from Shodan, would automatically engage vulnerable devices around the world with exploit code.  A short time ago, right after the release of MIRAI, a fellow team member had developed some code that would scour the Internet, find devices using default credentials and automatically reset them.  We had a long discussion about the legality of using such code.

His modification of the MIRAI botnet would scan the Internet for devices using default credentials and reset those credentials or shut down the device, all together.

Essentially, it's the loose interpretation of walking around a neighborhood, breaking into homes, for the sole purpose of locking the windows. In that context, it's absolutely illegal. In theory, the intentions were in the right place.

So, should a tool like AutoSploit be illegal?  I'm not entirely certain.  What I am certain of, is this tool, along with a Shodan.io API key, permits "Script Kiddies" and criminals to very effectively break into networks and cause tangible harm. The tool doesn't discriminate about what networks and devices that it breaches.  That's the reality.

Accepting that AutoSploit is more about collecting access to many networks, instead of targeted environments, would gear this activity towards the accelerated buildup of botnets for C&amp;C and ransomware.

That being said, is this really the fault of the device owner?  Are the vendors in the wrong for providing and applying patches quick enough? Is it the person crawling in through digital "open windows" at fault?

Tough questions.

When I look at this new generation of tools, there are several significant issues that AutoSploit brings to the table:

AutoSploit is just the beginning of a new reality around cybersecurity, in regards to attacks and incident response.  Where we once had a few moments to get devices online and time to test patches before deployment, we will now need to aggressively adjust those timetables. Based solely on previous experience, this is a very dangerous practice. Making rapid code and environment changes to critical infrastructure can literally cost lives.

Accepting that AutoSploit is part of a new generation of weaponry,  we can apply this same logic to environments where automatic exploitation and rapid delivery of patching is life-threatening. When these toolkits are able to automatically pivot into internal networks, move linearly, and land on sensitive equipment (such as medical devices), we will witness the loss of life due to vulnerable software code.  Unfortunately, most of those devices weren't developed with security in mind, nor with a "drop dead date".  They are able to live for decades in vulnerable states with relatively non-existent paths for updates and upgrades.

Additionally, manufacturers and vendors rarely inform a customer of precisely what level of risk they are being asked to accept when deploying the vendor's solution. Therefore, they may have no idea what the proper channels and approaches are for the remediation of currently unknown vulnerabilities. To that measure, they might not know that they even "own" that responsibility.

Lastly, most of us should probably be concerned with the collateral damage of tools like AutoSploit.  Even if we patch everything we have, either in or on our networks, will that be enough?  If we employ a vendor that BYODs (Bring your own device) which are vulnerable, can it take down portions of our network due to saturation and exhaustion of associated resources?  This is the very situation that I witnessed at a "Big Box" retail company a few years ago. Solar panels were incorporated to save money, but the panel's digital controllers were running vulnerable versions of NTP and operating systems.

Unfortunately, they didn't get to choose when the vendors patched their systems. Nor could they contractually perform the patching, themselves.
Autosploit-style tools are inevitable and the associated threats will evolve.  In the long run, AutoSploit, MIRAI, and similar tools will bring with them a more focused approach to the topic of information security.  It will spark some innovation in alerting, compensating controls and rapid remediation cycles.  My hope is that the associated collateral damage will not be substantial.