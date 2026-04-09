# Tower Semi, Fabrinet, and the Incredible Nvidia 1.6T Transceiver Ramp

## Excessive extrapolation of two earnings call transcripts.

**Aug 22, 2025**

**Likes:** 0

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Please check the [‘about’ page](https://irrationalanalysis.substack.com/about) for a list of active positions.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice and readers should **always do their own research before investing in any security.**

  * Feel free to contact me via email at: _irrational_analysis@proton.me_




* * *

Ok this is sloppy work. I am very tired and going to handwave a lot of things. Proper SiPho deep-dive in a few months probably.

TLDR;

[FN 0.00%↑](https://substack.com/discover/stocks/FN) and [TSEM 0.00%↑](https://substack.com/discover/stocks/TSEM) going to the moon.

[LITE 0.00%↑](https://substack.com/discover/stocks/LITE) neutral or modest positive. 

[MRVL 0.00%↑](https://substack.com/discover/stocks/MRVL) negative.

[COHR 0.00%↑](https://substack.com/discover/stocks/COHR) might be completely fucked. 

Irrelevant to [AAOI 0.00%↑](https://substack.com/discover/stocks/AAOI). (they are in their own chaos land)

Mild positive to [SITM 0.00%↑](https://substack.com/discover/stocks/SITM)

# Contents:

  1. Oversimplified Basic Terminology and Background

  2. Tower Earnings Call

  3. Fabrinet Earnings Call

  4. Nvidia Transceiver Architecture Guesses

  5. Who wins, who loses.




## [1] Oversimplified Basic Terminology and Background

Lasers are made on III-V material. The most common of which is Indium Phosphide (InP).

InP wafers are typically 2/3/4 inch in size. Defects are also way higher. In simple terms, yield is shit and cost is high.

There are two popular types of lasers, VCSEL and DFB.

DFB stands for distributed feedback.

[![](https://substackcdn.com/image/fetch/$s_!r8s9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F406ee75a-1e2a-4ac7-9dc9-4d73194463c6_600x178.jpeg)](https://substackcdn.com/image/fetch/$s_!r8s9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F406ee75a-1e2a-4ac7-9dc9-4d73194463c6_600x178.jpeg)

Intuitively, this light that bounces between two mirrors, gaining energy each bounce, then ejecting itself at high power through one of the mirrors.

VCSEL stands for vertical-cavity surface-emitting.

[![](https://substackcdn.com/image/fetch/$s_!086l!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F76c6ad1f-cb2b-4a27-86e9-9f8ff908c9c7_396x346.png)](https://substackcdn.com/image/fetch/$s_!086l!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F76c6ad1f-cb2b-4a27-86e9-9f8ff908c9c7_396x346.png)

It sends light vertically from the chip.

How the physics of these things work is irrelevant for todays discussion. I suck at physics and wont bother.

All you need to know is these are the two popular flavors of laser and they have different use cases and attributes. 

* * *

Transceivers that use VCSEL lasers are typically in this configuration.

[![](https://substackcdn.com/image/fetch/$s_!u0rV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd1cbf307-b853-426e-af3e-1d1b405015fc_852x359.png)](https://substackcdn.com/image/fetch/$s_!u0rV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd1cbf307-b853-426e-af3e-1d1b405015fc_852x359.png)

This setup is nice because it reduces complexity and cost. It has been dominant for transceivers up to 100G per lane (800Gbps per module).

With the transition to 1.6T transceivers (200G per lane, 8 lanes), VCSEL has a big problem.

Reliability. 

[![](https://substackcdn.com/image/fetch/$s_!lkQj!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F40595b2e-b326-4820-962c-b81463176e01_761x564.png)](https://substackcdn.com/image/fetch/$s_!lkQj!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F40595b2e-b326-4820-962c-b81463176e01_761x564.png)

There are at least 10 companies trying to make 200G VCSEL work. Most of them are going to fail.

So there is a reason why VCSEL architecture is getting replaced with Externally Modulated Laser (EML) AKA “Continuous Wave” (CW) laser systems.

There are two types of EML. Very important you understand this as it matters a lot to the investment thesis.

[![](https://substackcdn.com/image/fetch/$s_!WW5o!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F94e15b19-f2e1-494c-9862-45d6e0930f54_848x528.png)](https://substackcdn.com/image/fetch/$s_!WW5o!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F94e15b19-f2e1-494c-9862-45d6e0930f54_848x528.png)

The first EML architecture has a sperate SiPho chip. This is typically made by Tower Semi. Glofo has competing SiPho nodes and investors should go ask them why they are not getting meaningful orders. 🤡

The benefit of this EML architecture is it avoids reliability issues as a function of bandwidth.

Drawback is power and cost.

When any of you hear “alignment” in the context of optics I want you to think “pain and suffering”.

In a SiPho EML architecture, you need to align the DFB with the SiPho chip, then the SiPho chip with the fiber. There are also various lenses and isolators (reflection blockers) that need VERY PRECISE alignment. 

So SiPho EML has serious cost and yield issues (at module assembly level) compared to VCSEL.

The other issue is power requirement of the laser. Every time you try to couple light (shine it from one thing into another), you lose a non-trivial amount of power.

Thus, DFBs need to run much higher power than VCSEL to achieve the same reach.

(as an aside VCSEL cannot hit high power)

Now let’s look at the final architecture, monolithic InP EML.

[![](https://substackcdn.com/image/fetch/$s_!y63O!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7b1c487d-4d04-4ac8-8104-c7c13a7ac6da_840x486.png)](https://substackcdn.com/image/fetch/$s_!y63O!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7b1c487d-4d04-4ac8-8104-c7c13a7ac6da_840x486.png)

Now, there is no SiPho PIC. Just one big InP chip that has the laser and modulator (thing that wiggles light) on the same monolithic device.

The benefit of this scheme the DFB/laser can be much lower power and you have far less alignment hell to deal with.

The drawback is now a VERY LARGE CHIP is on tiny specialty wavers with trash yield relative to silicon.

* * *

So quick re-iteration.

VCSEL is great but has serious reliability issues at 200G per lane. Many are trying to deal with this problem, most will fail. The smart players are moving to SiPho EML.

SiPho EML has satanic suffering related to alignment and needs high-power DFB lasers. 

Monolithic InP EML looks like a great middle ground until you realize tiny InP wafer yield is shit.

* * *

Finally, there are three primary types of modulators in a EML system.

  1. MZI (Mach Zhender Inferometer)

  2. Ring

  3. Electoabsorbtion




Electroabsorbtion is shit. 

**Only Nvidia can make rings work in production volume at the time of writing.** (Ayar Labs has a demo platform. Lightmatter claims to have something that exists but there is no evidence thing has ever turned on and worked… looking forward to Hot Chips 2025)

Everyone else uses MZI.

 **Rings way better than MZI if you can get them to work (big if)**

## [2] Tower Earnings Call

I read the transcript twice. Second reading was after Fabrinet reported. Missed the critical info on first reading.

[![](https://substackcdn.com/image/fetch/$s_!UddT!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd55064cd-9b43-4ad0-8484-d9f256bd2e28_888x755.png)](https://substackcdn.com/image/fetch/$s_!UddT!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd55064cd-9b43-4ad0-8484-d9f256bd2e28_888x755.png)

Typically, receive side of a normal (non-ring) transceiver uses discrete photodiodes.

You know the light emitting diodes (LEDs) shining into your eyeballs right now?

There are LEDs that do the opposite too. Convert light into electricity.

Take a look at this VCSEL style 400G transceiver.

[![](https://substackcdn.com/image/fetch/$s_!JA29!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6616feac-d6f1-4ed7-9682-c2843d1f58bf_746x436.png)](https://substackcdn.com/image/fetch/$s_!JA29!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6616feac-d6f1-4ed7-9682-c2843d1f58bf_746x436.png)

Blue crayon circle is the receiver stuff, including discrete (or loosely integrated) photodiodes.

In a SiPho EML DFB Tx, the stuff above blue crayon circle would be replaced with four InP DFB (not VCSEL) lasers, one SiPho chip from tower, and a shit ton of lenses.

[![](https://substackcdn.com/image/fetch/$s_!TEHs!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcc86f1ea-4076-430a-bd18-01a209bfb00c_485x267.png)](https://substackcdn.com/image/fetch/$s_!TEHs!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcc86f1ea-4076-430a-bd18-01a209bfb00c_485x267.png)

* * *

I am 99.999% confident Tower CEO is talking about ring add/drop filters on Rx. This makes total sense. There is no other possible thing he can be talking about. Its fucking rings. Its Nvidia. They ported their ring design from TSMC SiPho to Tower SiPho.

More on this in section [4].

## [3] Fabrinet Earnings Call

Stock tanked because numbers bad.

Numbers bad because there is a component shortage for Fabrinet’s “largest customer”.

COUGH COUGH NVIDA

COUGH COUGH TOWER SEMI SIPHO PIC

[![](https://substackcdn.com/image/fetch/$s_!9Xj-!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fca82fce4-3f51-441e-a720-21772892cdc9_1314x446.png)](https://substackcdn.com/image/fetch/$s_!9Xj-!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fca82fce4-3f51-441e-a720-21772892cdc9_1314x446.png)

[![](https://substackcdn.com/image/fetch/$s_!q2HL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0acb8c21-5d83-494d-8b26-ba075a30c84e_1345x665.png)](https://substackcdn.com/image/fetch/$s_!q2HL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0acb8c21-5d83-494d-8b26-ba075a30c84e_1345x665.png)

## [4] Nvidia Transceiver Architecture Guesses

First lets start with a baseline SIPho EML using MZI.

[![](https://substackcdn.com/image/fetch/$s_!D7Bv!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdda65098-8271-4dcb-a6c8-ad36fea37273_869x778.png)](https://substackcdn.com/image/fetch/$s_!D7Bv!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdda65098-8271-4dcb-a6c8-ad36fea37273_869x778.png)

Now let’s look at my various guesses for Nvidia’s ring architecture.

[![](https://substackcdn.com/image/fetch/$s_!7l9B!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb40af190-cca4-4351-850c-8796dd0a63fb_850x1146.png)](https://substackcdn.com/image/fetch/$s_!7l9B!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb40af190-cca4-4351-850c-8796dd0a63fb_850x1146.png)

[![](https://substackcdn.com/image/fetch/$s_!IRzl!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1e38e372-fe19-4b03-a584-a432751c465b_832x1133.png)](https://substackcdn.com/image/fetch/$s_!IRzl!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1e38e372-fe19-4b03-a584-a432751c465b_832x1133.png)

InP/DFB/laser content is bad. Expensive.

Nvidia ring architecture is prob 1/2 the InP content of competing MZI EML solutions. Maybe even 1/4.

MZI modulators need a lot of input light because they have high insertion loss.

Rings have tiny insertion loss.

There are a few people who have been arguing with me on Twitter about how the shortage is InP, not Tower SiPho.

This is a reasonable thesis. There is an InP shortage.

 **What if I told you a ring architecture from Nvidia requires a fraction of the InP content and each DFB laser can be at much lower power?**

## [5] Who wins, who loses.

Semianalysis had a core research note on Tower recently. It is very well done. Part of it talks about SiPho (what I care about) but there is a lot more useful information about non-SiPho and high quality math/modeling.

And yet… Tower stock has barely moved. Im not sure why SA core research moved Astera Labs stock 20% in one day and this note on Tower Semi had no effect.

SA Core Research subscribers… did you forget to read the Tower note…?

 **My take is there might be even more upside just from SiPho.**

Let’s talk about Coherent.

[![](https://substackcdn.com/image/fetch/$s_!0T52!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbd42b292-a5fc-4722-b117-cd4919313e38_604x1295.webp)](https://substackcdn.com/image/fetch/$s_!0T52!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbd42b292-a5fc-4722-b117-cd4919313e38_604x1295.webp)One of my life goals is to get audited by the IRS and/or SEC. Explain my insane trading style to federal agents.

As you can see, I have engaged in particularly degenerate behavior for this one.

It was working until it didn’t. 

[![](https://substackcdn.com/image/fetch/$s_!kUgK!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4335b864-76f3-4e1f-808b-0988e88e44d7_661x1296.webp)](https://substackcdn.com/image/fetch/$s_!kUgK!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4335b864-76f3-4e1f-808b-0988e88e44d7_661x1296.webp)

My entire thesis revolved around Coherent’s unique 6-inch InP process technology.

<https://www.coherent.com/news/blog/indium-phosphide-wafer-fab>

[![](https://substackcdn.com/image/fetch/$s_!GBS8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcf138c24-b152-4345-b5fd-946d305386a9_1410x460.png)](https://substackcdn.com/image/fetch/$s_!GBS8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcf138c24-b152-4345-b5fd-946d305386a9_1410x460.png)

There are two ways of looking at this.

  1. Incredible advantage to Coherent.

  2. They NEED this, it probably has bad yield, and they are getting crushed by the Chinese on cost.




Earnings call transcript implies they are getting annihilated by the Chinese.

[![](https://substackcdn.com/image/fetch/$s_!yNhq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9e9968a4-b59c-4807-bdc3-68b3019c3a98_997x722.png)](https://substackcdn.com/image/fetch/$s_!yNhq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9e9968a4-b59c-4807-bdc3-68b3019c3a98_997x722.png)

What’s worse is, Nvidia is now coming for Coherent’s margins too.

Let’s take a look at a Coherent InP monolithic EML. They so helpfully put a nice picture in their investor day slide deck.

[![](https://substackcdn.com/image/fetch/$s_!OQaf!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe2ca8592-1300-4d6c-bbb3-1e8724190c1d_741x287.png)](https://substackcdn.com/image/fetch/$s_!OQaf!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe2ca8592-1300-4d6c-bbb3-1e8724190c1d_741x287.png)Shoutout to COHR investor relations team. Thanks for putting together nice slides so I can easily explain why you are possibly doomed.

See the long structure I highlighted with a blue crayon bracket?

That is a MZI modulator.

Given everything you have read in this post, do you think this InP wafer space should be used to print many tiny lasers, or a handful of these “gumstick” like structures.

You think the yield of _“Complex InP PIC”_ is good?

You think those 6-inch InP wafers have good yield? Maybe there is a reason everyone else is on 2/3/4 inch.

* * *

Innolight, Accelink, Eoptolink, TFC, and many other Chinese transceiver companies are very likely using the standard (baseline) 8 DFB, 2 SiPho PIC configuration for 1.6T transceivers.

Coherent already is at a cost disadvantage to these guys.

I spent around half an hour using the semianalysis yield calc tool to guess how large various PIC architectures would be. (Nvidia ring vs standard MZI EML)

<https://semianalysis.com/die-yield-calculator/>

 **The cost of the PIC from Tower is trivial compared to other costs in a transceiver.**

  1. DSP logic chip

  2. InP/DFB/Laser content

  3. # of alignments




It insane how cheap the Nvidia’s ring architecture can be. 

Transceiver margins usually suck. Like 20%.

Nvidia can charge like 50-70% gross margins on these ring based (and internal DSP) 1.6T transceivers and still undercut Coherent and others on pricing.

[![](https://substackcdn.com/image/fetch/$s_!_9Hc!,w_1456,c_limit,f_auto,q_auto:good,fl_lossy/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7b29e343-c9fb-4857-ad6a-535286fb3e07_498x326.gif)](https://substackcdn.com/image/fetch/$s_!_9Hc!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7b29e343-c9fb-4857-ad6a-535286fb3e07_498x326.gif)

Its crazy. I am making really pessimistic assumptions here.

* * *

So to summarize.

Coherent might be doomed. 

Marvell is probably not going to have a good time. I forgot to mention but ring modulators have very different voltage swing requirements compared to MZI or VCSEL. Much higher voltage swing needed. 

Also, rings have nonlinear responses so PAM4 is EXTREAMLY painful. Gearboxing from 8x 200G PAM4 to 16x 100G NRZ has huge benefits. 

[![](https://substackcdn.com/image/fetch/$s_!wyXp!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcd2ec2ef-665b-4ede-b8e5-a5e0bedad26b_762x592.png)](https://substackcdn.com/image/fetch/$s_!wyXp!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcd2ec2ef-665b-4ede-b8e5-a5e0bedad26b_762x592.png)Look at the x axis units. Look at how crazy narrow the frequency response is.

<https://people.engr.tamu.edu/spalermo/ecen689_oi/lecture11_ee689_rrm_tx.pdf>

 **In other words, if Nvidia is really using rings (which I am very confident in), then they must also use their own custom DSP logic chip to properly drive the Tx rings.**

Sitime helps with PPM sync and this is a perfect application. Mild positive to them. Not sure how much of this is incremental. 

Lumentum is neutral to mild positive. They have very good DFB lasers. Nvidia might take a fairly large chunk of Lumentum module business (~20%? GM) but instead Lumentum will sell a shit ton of DFB lasers at very high gross margin.

Tower and Fabrinet are going to the moon. This is incredible opportunity for both. Market for some reason has not figured this out.

* * *

 **Nvidia can charge very aggressive gross margins AND STILL undercut Coherent and potentially several others on pricing.**

 **The ring modulator architecture and internal DSP is a massive structural advantage.**

 **Nvidia is not limited by InP/EML shortage. Thier architecture needs SIGNIFICANTLY less InP content and might even work with lower quality (lower power) InP DFB lasers.**

Disclosures of all positions in trading account. I have large long positions in Tower and Fabrinet. Large Marvell short. Small short for Coherent. Too afraid to size up.

[![](https://substackcdn.com/image/fetch/$s_!TXfT!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4561e298-d42d-4b24-b262-02beca1aabaf_777x1192.webp)](https://substackcdn.com/image/fetch/$s_!TXfT!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4561e298-d42d-4b24-b262-02beca1aabaf_777x1192.webp)

[![](https://substackcdn.com/image/fetch/$s_!iag_!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6c2c8cb8-2f7c-4f02-864e-b020a27b35a0_1373x1127.webp)](https://substackcdn.com/image/fetch/$s_!iag_!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6c2c8cb8-2f7c-4f02-864e-b020a27b35a0_1373x1127.webp)

Subscribe for engineering-driven investment analysis.

Subscribe

Share with Coherent IR

[Share](https://irrationalanalysis.substack.com/p/tower-semi-fabrinet-and-the-incredible?utm_source=substack&utm_medium=email&utm_content=share&action=share)
