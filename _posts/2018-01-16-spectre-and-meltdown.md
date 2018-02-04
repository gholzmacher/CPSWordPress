---
ID: 738
post_title: Spectre and Meltdown
author: pkelley
post_excerpt: ""
layout: post
permalink: >
  https://www.criticalpathsecurity.com/spectre-and-meltdown/
published: true
post_date: 2018-01-16 00:12:29
---

	<p><img src="https://www.criticalpathsecurity.com/wp-content/uploads/2018/01/dumpsterfire-1024x576.jpg" alt="" width="695" height="391" /></p>
<p>Spectre and Meltdown are the names given to variations on a vulnerability that affects nearly every computer chip manufactured in the last 20 or so years. Unfortunately, the flaws can only be described as catastrophic in nature.</p>
<p>In the first days of 2018, published research revealed that flaws arise from features built into chips that help them run faster, and while software patches are available, they have had impacts on system performance. In fact, it seems that the cure has been far more devastating than the actual vulnerability.</p>
<p>Supporting this argument, SolarWinds has created other visualizations of its cloud post Meltdown/Spectre and most of the results are ugly. Throughput was down as much as 40 per cent on its Kafka rig, while CPUs spiked by around 25 per cent on Cassandra. In large environments, such as AWS, this is significant. </p>
<p>Spectre and Meltdown are the names given to different variants of the underlying vulnerability that affects nearly every computer chip manufactured in the last 20 years and could allow attackers to get access to data previously considered completely protected. </p>
<p>All of the variants of this vulnerability involve a malicious program gaining access to data that it shouldn't have the right to see, and do so by exploiting two important techniques used to speed up the chips, called speculative execution and caching.</p>
<p> </p>
<p>The problem arises when caching and speculative execution start grappling with protected memory.</p>
<p>While the CPU is waiting to find out if the process is allowed to access that data, thanks to speculative execution, it starts working with that data even before it receives permission to do so. In theory this is still secure, because the results of that speculative execution are also protected at the hardware level. The process isn't allowed to see them until it passes the privilege check, and if it doesn't pass the check, the data is discarded.</p>
<p>The problem arises because the protected data is stored in CPU cache even if the process never receives permission to access it. And because CPU cache memory can be accessed more quickly than regular memory, the process can attempt to access certain memory locations to find out if the data there has been cached — it still won't be able to access the data, but if the data has been cached, its attempt to read it will be rejected much more quickly than it otherwise would. </p>
<p> </p>
<p>Spectre and Meltdown both open up possibilities for dangerous attacks. For instance, JavaScript code on a website could use Spectre to trick a web browser into revealing user and password information. Attackers could exploit Meltdown to view data owned by other users and even other virtual servers hosted on the same hardware.</p>
<p>Patches have already been rolled out by Intel, Microsoft, Apple, and Google. Unfortunately, serious performance hits are currently being seen with the new patches.  This makes some environments, notable AWS, to become to slow to be viable for current production needs.</p>
<p> </p>
<p>So what now?<br />In short, we wait for newer patches which don't impact performance to such a degree. This is more of a "bandaid" than a fix.  I expect future processors to have a better grasp on how to handle this issue. </p>