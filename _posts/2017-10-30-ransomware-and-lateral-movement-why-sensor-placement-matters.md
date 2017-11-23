---
ID: 462
post_title: 'Ransomware and Lateral Movement: Why sensor placement matters!'
author: pkelley
post_excerpt: ""
layout: post
permalink: >
  https://www.criticalpathsecurity.com/ransomware-and-lateral-movement-why-sensor-placement-matters/
published: true
post_date: 2017-10-30 01:27:59
---
When I work with enterprise organizations in regards to their security posture, I usually run into the same scenario. The Information Security has a reduced budget and a more traditional approach to security.  Unfortunately, as the global landscape of enterprise networks continues to evolve, it's clear this approach won't be applicable.

In a new generation of adversarial attacks, inside-out attacks are becoming more common and lateral movement through leaked exploits is the new game. As we've seen in the past with XP exploits - MS08-067, unpatched workstations and servers are the new "norm".

With the new ransomware, "BadRabbit", the attackers used EternalRomance, an exploit that bypasses security over Server Message Block (SMB) file-sharing connections, enabling remote execution of instructions on Windows clients and servers. This attack leverages the same methods revealed in the Shadowbrokers code release. NotPetya also leveraged this exploit.

<!--more-->

Bad Rabbit initially landed on affected networks through a "driveby download" attack via compromised Russian websites, but also leveraged TOR addresses. Arriving as an Adobe Flash update, Bad Rabbit has multiple ways of spreading itself across networks, but largely by exploiting open SMB connections on an infected Windows system.  This is commonly seen as an "IPC$" or "C$" mapping.

&nbsp;

<img class="aligncenter size-large wp-image-464" src="http://www.criticalpathsecurity.com/wp-content/uploads/2017/10/Screen-Shot-2017-10-29-at-5.58.55-PM-1024x657.png" alt="" width="1024" height="657" />

It's important to notice that it can also exploit the Windows Management Instrumentation Command-line (WMIC) scripting interface to execute code remotely on other Windows systems on the network. This leaves artifacts at both a network (RPC) and process (command line) level. When wmic.exe (or the schtasks API) is used to remotely create processes, Windows uses RPC (135/tcp) to communicate with the the remote machine.

When reviewing the leaked information about the ransomware, I was immediately reminded of previous research around EternalRomance and EternalFlame. So, when I noticed this exploit uses an "empty" SMB transaction packet to attempt to push instructions into the memory of another Windows computer, I knew I was likely looking at the reuse of leaked NSA exploit code. When leveraged in previous engagements, either with the Python variant or Metasploit, I could expect the exploit to immediately be successful or cause a crash. In most situations, it was a success.

Taking the attack a step further, it leverages the use of the commercial DiskCryptor code to encrypt the victim's hard drive and the presence of "wiper" code that could erase drives attached to the targeted system.

DiskCryptor describes their software as an open encryption solution that offers encryption of all disk partitions, including the system partition.

<img class="aligncenter size-full wp-image-465" src="http://www.criticalpathsecurity.com/wp-content/uploads/2017/10/Screen-Shot-2017-10-29-at-6.13.21-PM.png" alt="" width="954" height="468" />

As shown above, proper placement of Suricata and Bro can provide the visibility teams need to quickly isolate infected hosts and protect the surrounding assets.

This leads to a very important conclusion. We know that assets will be deployed to the enterprise network without all of the possible patches applied. We know that new variants of malware and ransomware have the ability to spread quickly across the network. We now know that placing IDS solutions and sensors exclusively at ingress/egress points simply won't provide sufficient visibility into these new attacks.

It's time to have some serious discussions about what your organization needs to protect itself. It's not about getting more tools, but properly leveraging what you already have.

Are you ready to take a new look at defense? Give us a call.