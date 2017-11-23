---
ID: 440
post_title: >
  Protecting Against Key Reinstallation
  Attacks in WPA2 (KRACK)
author: R. Brice
post_excerpt: ""
layout: post
permalink: >
  https://www.criticalpathsecurity.com/protecting-against-key-reinstallation-attacks-in-wpa2-krack/
published: true
post_date: 2017-10-16 16:24:57
---
Just recently, a paper was leaked in regards to a vulnerability in WPA2 that affects just about everyone who uses a wireless connection. More specifically, the vulnerability lies at the 3rd stage of the 4-way handshake used by WPA2 to provide authentication and session key agreement. The attack also requires an evil twin access point since the session key is derived from the MAC address.

The paper, written by Belgian researchers, Mathy Vanhoef and Frank Piessens, is 16 pages long and goes into detail on the various exploitations possible. We don’t want to rehash everything here when you can go straight to the source, so for those who want to know the technical ins and outs of this vulnerability, we recommend reading about it from the horse’s mouth: <a href="https://papers.mathyvanhoef.com/ccs2017.pdf" target="_blank" rel="noopener">https://papers.mathyvanhoef.com/ccs2017.pdf</a>

What most people probably want to know, though, is “how do I avoid getting hacked?” The safest and most immediate solution is switch to wired for the time being. Although the chances of a hack are low, if you live in an area with a high population density that has more technically inclined people, and if you’re responsible for protecting significant assets, your chances of experiencing a hack go up. So for now, and until patches are released by various vendors, we recommend moving to wired networking. For those of you on laptops without an Ethernet port, you can purchase USB to Ethernet dongles online or at your local tech store. Yes, this is inconvenient for many people, so each person will have to weigh that inconvenience vs. the sensitivity of the data they work with and make the best decision for them.

<!--more-->

The paper does state that on WPA2-CCMP, an attacker can replay and decrypt packets, but not forge them, whereas on WPA2-TKIP (or WPA2-GCMP) forging packets is possible. Thus if you’re going to continue using wifi before patches are released, at least make sure you’re using WPA2-CCMP. The paper also says (in section 3.2) that Windows operating systems and iOS are more resilient to the attack because they don’t exactly follow the 802.11 standard. However, just because you’re on a Windows computer or using an iPhone doesn’t mean you’re completely secure from exploitation. Certain aspects of the attack will still work on those platforms.

The most important point we can drive across is this vulnerability is one of the most broad and significant we’ve seen in a long while. On one hand, that’s a good thing because it will get more attention and hopefully faster patches. On the other hand, chances are no matter who you are, you’re vulnerable.