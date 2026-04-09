# Marvell PCIe 7 Switch: Existential Threat to Astera Labs

## DesignCon demos have given away what is coming!

**Feb 02, 2025**

**Likes:** 0

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Please check the [‘about’ page](https://irrationalanalysis.substack.com/about) for a list of active positions.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice, and readers should **always do their own research before investing in any security.**

  * Feel free to contact me via email at: _irrational_analysis@proton.me_




* * *

Marvell is working on a PCIe switch. They are very far along in the development. I am 99% confident on this after seeing several incredible demos ad DesignCon.

Before getting started, my biases.

I have lost a lot of money trying to short [ALAB 0.00%↑](https://substack.com/discover/stocks/ALAB).

[![](https://substackcdn.com/image/fetch/$s_!_y7y!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1fdad737-841f-47e8-894a-e3db32f10088_1438x2664.jpeg)](https://substackcdn.com/image/fetch/$s_!_y7y!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1fdad737-841f-47e8-894a-e3db32f10088_1438x2664.jpeg)

I have made a lot of money trading [MRVL 0.00%↑](https://substack.com/discover/stocks/MRVL) options.

[![](https://substackcdn.com/image/fetch/$s_!rzr4!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F01bf99c0-7df2-4080-bdb4-eda588a0666a_1439x2710.jpeg)](https://substackcdn.com/image/fetch/$s_!rzr4!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F01bf99c0-7df2-4080-bdb4-eda588a0666a_1439x2710.jpeg)

I currently have a small covered call (buy-write) position in Astera Labs.

[![](https://substackcdn.com/image/fetch/$s_!G_mG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3627ae82-aefe-4365-ada1-025a645e08f4_1439x747.jpeg)](https://substackcdn.com/image/fetch/$s_!G_mG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3627ae82-aefe-4365-ada1-025a645e08f4_1439x747.jpeg)

At the time of writing have hold no position in Marvell stock or options but reserve the right to trade both [ALAB 0.00%↑](https://substack.com/discover/stocks/ALAB) and [MRVL 0.00%↑](https://substack.com/discover/stocks/MRVL) at any time without warning. 

# Contents:

  1. Analysis of DesignCon Demos

  2. PCIe Switch Market Overview

  3. Someone warn Gavin Baker lmao!




* * *

## [1] Analysis of DesignCon Demos

There were two Marvell TSMC N3 PCIe 7 demos at that stood out to me…

  1. 43 dB insertion loss

    1. 1.6e-10 pre-FEC bit-error rate.

    2. No active cooling.

  2. 45 dB insertion loss

    1. 1.7e-8 pre-FEC bit-error rate.

    2. No active cooling.

    3.  **No Tx FIR! Extreme strain on receiver!**




Remember that official PCIe 7 spec is 1e-6 pre-FEC BER at a 36 dB bump-bump insertion loss.

I have a detailed post on communication systems.

Please read it if you are interested in the technical/engineering background.

The conclusion is simple…

 **Marvell PCIe 7 SerDes is KICKASS.** This is incredible. I cannot express how impressive this is. 

It’s so amazing, I spent most of the conference trying to figure out as much as possible. Thankfully, one of the booths gave me permission to take a picture.

[![](https://substackcdn.com/image/fetch/$s_!1ZS9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7a083902-eccf-43cd-a8c1-3cb887992ef6_1251x1024.png)](https://substackcdn.com/image/fetch/$s_!1ZS9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7a083902-eccf-43cd-a8c1-3cb887992ef6_1251x1024.png)

This PCB is extremely suspicious. **It is highly unusual to have connectors where the Rx (receiver) traces are removed.**

The only logical justification I can think of is that Marvell wants to stress test Tx crosstalk… which is a problem in switches.

Furthermore, the demo GUI clearly displayed **“FPGA version”.** There are no FPGAs on the board so there must be an integrated FPGA on die. This too is highly unusual for a SerDes test chip. **I think they are using FPGA logic to try out simple (reduced scale) switching digital logic.**

This test chip is an old trial run of a PCIe switch product. **Marvell probably already has a full PCIe 7 switch sampling to customers privately.**

## [2] PCIe Switch Market Overview

For a long time, PCIe switches were effectively an [AVGO 0.00%↑](https://substack.com/discover/stocks/AVGO) monopoly. Astera Labs saw an opportunity with Amazon (largest customer) and Nvidia AI server head nodes. They made a niche PCIe switch (Scorpio-P) that has the perfect product market fit.

  * Half the price of competing Broadcom PCIe switch.

  * Has exactly the number of lanes needed for AI head nodes.

  * Amazon has a ton of warrants (call options) that exercise if they buy a lot of chips from Astera Labs and **Amazon hates Broadcom.**




[![](https://substackcdn.com/image/fetch/$s_!Th-P!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcab0237d-8887-4d1d-b34a-60cf99555b4e_1204x415.png)](https://substackcdn.com/image/fetch/$s_!Th-P!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcab0237d-8887-4d1d-b34a-60cf99555b4e_1204x415.png)

[![](https://substackcdn.com/image/fetch/$s_!AoFJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff724e48e-0401-4372-8fa2-8c29c3e66aad_1215x1348.png)](https://substackcdn.com/image/fetch/$s_!AoFJ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff724e48e-0401-4372-8fa2-8c29c3e66aad_1215x1348.png)

[![](https://substackcdn.com/image/fetch/$s_!5VRp!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4cd65ac8-da66-419d-aa02-493b7ce20dc0_1288x1252.png)](https://substackcdn.com/image/fetch/$s_!5VRp!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4cd65ac8-da66-419d-aa02-493b7ce20dc0_1288x1252.png)

The funny thing is, nothing prevents Broadcom or Marvell from being a fast-follower and making the same niche product.

Broadcom is busy with semi-custom silicon from their innovative [3.5D platform](https://www.broadcom.com/info/ai/3point5d) and seems to be ignoring PCIe switches.

Marvell is not. They are coming for Astera Labs lunch!

 **Importantly, Broadcom and Marvell both make their own excellent in-house SerDes while Astera Labs licenses lower-quality SerDes from a supplier.**

[![](https://substackcdn.com/image/fetch/$s_!sOmk!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff21553a6-2e5a-4c94-aea3-f793ad9d3b73_1228x1191.png)](https://substackcdn.com/image/fetch/$s_!sOmk!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff21553a6-2e5a-4c94-aea3-f793ad9d3b73_1228x1191.png)

 **The SerDes they use is so weak, every connection needs a retimer chip, increasing BOM cost and reducing power efficiency.**

Amazon has likely already purchased enough chips to meet their warrent conditions. This would explain why Amazon has abandoned Astera Labs PCIe retimers in favor of Marvell re-timers. (Amazon has a similar warrent agreement with Marvell)

[![](https://substackcdn.com/image/fetch/$s_!MCry!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F342c284b-9f98-4f7a-aa81-fa77938bf968_1531x1111.png)](https://substackcdn.com/image/fetch/$s_!MCry!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F342c284b-9f98-4f7a-aa81-fa77938bf968_1531x1111.png)[Marvell Expands Strategic Collaboration with AWS to Enable Accelerated Infrastructure for AI in the Cloud](https://www.marvell.com/company/newsroom/marvell-expands-strategic-collaboration-aws-enable-accelerated-infrastructure-ai-cloud.html)

Amazon has a habit of propping up companies they are invested in with purchase-volume based warrents. Look at Rivian stock. Great example of the Amazon warrent cycle. **Astera Labs has already lost the Amazon re-timer socket to Marvell. PCIe switch is very likely to be next!**

Sell-side is modeling PCIe switches as a majority-Astera market. This is incredibly wrong.

  * Marvell makes their own SerDes and thus has higher gross margins.

  * Marvell’s performance is much better, eliminating the need for re-timed connections on every PCIe switch port.

  * Amazon has new Marvell warrents and no longer has an incentive to purchase inferior chips from Astera Labs.




[![](https://substackcdn.com/image/fetch/$s_!wCxJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd39e5718-9bd5-460e-ace5-037e0166c9f4_1546x1021.png)](https://substackcdn.com/image/fetch/$s_!wCxJ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd39e5718-9bd5-460e-ace5-037e0166c9f4_1546x1021.png)

## [3] Someone warn Gavin Baker lmao!

One of the nice things about running this newsletter is the opportunity to meet people I never would have met through my normal engineering dayjob.

Finance people like drama. So lets talk drama!

[![](https://substackcdn.com/image/fetch/$s_!7iNA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F77e4bfd9-9faf-4279-b0a3-b7387dc354cf_1020x748.png)](https://substackcdn.com/image/fetch/$s_!7iNA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F77e4bfd9-9faf-4279-b0a3-b7387dc354cf_1020x748.png)

Gavin baker is one of my favorite people to follow on X/Twitter. He is simultaneously a genius and a moron. It’s remarkable. His intelligence is bimodal. Very rare.

He invested in [ALAB 0.00%↑](https://substack.com/discover/stocks/ALAB) back when they were private and has since double downed. 

[![](https://substackcdn.com/image/fetch/$s_!6bbC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Feda1861d-ee51-42d8-af3e-f93a8538291d_874x987.png)](https://substackcdn.com/image/fetch/$s_!6bbC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Feda1861d-ee51-42d8-af3e-f93a8538291d_874x987.png)[Linik](https://x.com/GavinSBaker/status/1813592308773945387)

[![](https://substackcdn.com/image/fetch/$s_!uwG4!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa2e7d161-e605-460e-9b7a-43db182a9d9e_885x567.png)](https://substackcdn.com/image/fetch/$s_!uwG4!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa2e7d161-e605-460e-9b7a-43db182a9d9e_885x567.png)[Link](https://x.com/GavinSBaker/status/1863609675519770749)

One of the reasons I like Gavin Baker so much is his 13F history is unhinged. This dude trades like a degenerate retail trader. Seriously, go check out his 13F history. He opens and liquidates positions in multiple dangerous/toxic stocks each quarter. He must have some kind of setup that exempts him from capital gains taxes

[![](https://substackcdn.com/image/fetch/$s_!xcIh!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F26024660-e8e8-4436-9333-f54cd6843a84_1439x2822.jpeg)](https://substackcdn.com/image/fetch/$s_!xcIh!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F26024660-e8e8-4436-9333-f54cd6843a84_1439x2822.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!oc63!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcf0592d3-ecd5-422f-9493-c8fba38d31c7_1439x2822.jpeg)](https://substackcdn.com/image/fetch/$s_!oc63!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcf0592d3-ecd5-422f-9493-c8fba38d31c7_1439x2822.jpeg)

Even last week as the DeepSeek chaos was killing every AI-related stock, Gavin Baker was defending [ALAB 0.00%↑](https://substack.com/discover/stocks/ALAB) implicitly. 

[![](https://substackcdn.com/image/fetch/$s_!MKWv!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff3abc2b1-4f90-495b-bcec-d0310efe3648_590x1049.png)](https://substackcdn.com/image/fetch/$s_!MKWv!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff3abc2b1-4f90-495b-bcec-d0310efe3648_590x1049.png)

I am going to tag him on X/Twitter but he might not read tagged tweets from a nobody like me.

Financial professionals who are subscribed… please send this to Gavin lol. Someone needs to warn him. I seem to be the only person who noticed what Marvell was actually demoing at DesignCon. **The on-die FPGA logic and unusual Tx-only ports on the PCB scream “PCIe switch”.**

Marvell is going to eat Astera Labs lunch. Consensus is extremely wrong.

Subscribe for engineering-driven investment analysis.

Subscribe

Someone needs to warn Gavin Baker lol.

[Share](https://irrationalanalysis.substack.com/p/marvell-pcie-7-switch-existential?utm_source=substack&utm_medium=email&utm_content=share&action=share)
