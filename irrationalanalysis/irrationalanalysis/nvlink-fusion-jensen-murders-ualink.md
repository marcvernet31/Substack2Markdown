# NVLink Fusion: Jensen Murders UALink with Galaxy-Brain Strategy

## Custom AI silicon landscape re-shaped. Massive winners and losers.

**May 22, 2025**

**Likes:** 0

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Please check the [‘about’ page](https://irrationalanalysis.substack.com/about) for a list of active positions.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice, and readers should **always do their own research before investing in any security.**

  * Feel free to contact me via email at: _irrational_analysis@proton.me_




* * *

Mr. Leather Jacket has once again outsmarted his ennemies.

The recent announcment of “NVLink Fusion” is an incredible strategic move that has re-shaped the entire AI ASIC market.

To understand why, we need to go into technical details.

[![](https://substackcdn.com/image/fetch/$s_!lsTG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F63c532e8-a87d-443e-bd83-10510a13165d_841x594.png)](https://substackcdn.com/image/fetch/$s_!lsTG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F63c532e8-a87d-443e-bd83-10510a13165d_841x594.png)

# Contents:

  1. PHY vs Protocol

  2. Explanation of the Announcement

  3. IEEE 802.3ck/dj KR vs VSR vs Nvlink C2C vs NVLink5

    1. Reach and Tradeoffs

    2. Why “Open” is not Necessarily Better

    3. Practical (Visual) Overview

  4. Strategic Impact

    1. Nvidia

    2. Synopsys, Cadence, and Alphawave

    3. Broadcom

    4. Alchip, Marvell, and Amazon

    5. Astera Labs

    6. MediaTek and Google

    7. Fujitsu and Qualcomm

    8. AMD and Other UALink **LOSERS**




* * *

## [1] SerDes vs Protocol

Communication links are divided into layers. There exists a standard model called OSI.

[![](https://substackcdn.com/image/fetch/$s_!GQ9K!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa011351a-70cb-4487-984d-84a2e4925915_971x455.png)](https://substackcdn.com/image/fetch/$s_!GQ9K!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa011351a-70cb-4487-984d-84a2e4925915_971x455.png)<https://en.wikipedia.org/wiki/OSI_model>

You don’t need to understand this entire mess. PHY means “physical layer”, which is often referred to as SerDes. This is the analog hardware that moves raw bits from point A to point B. Everything above the PHY is digital logic or software for managing higher level functions.

Every interface you are familiar with (Ethernet, PCIe, HDMI, USB, HBM, DDR) has a PHY and “the other stuff”.

 **The PHY is the differentiator.**

 **Only two companies have high-quality 200Gbps SerDes PHYs.**

 **Nvidia and Broadcom.**

NVLink5, NVLink C2C, AMD Infinity Fabric, Ethernet, InfiniBand, UALink, Broadcom Scale-Up Ethernet, PCIe, and so on are terms that refer to the PHY, upper layer, and entire stack… interchangeably. This leads to unfortunate confusion.

For example, NVlink5, Ethernet and InfiniBand are structurally very similar at a PHY level.

AMD Infinity Fabric is structurally similar to PCIe.

 **UALinik and Broadcom Scale-Up Ethernet official specs literally say the PHY shall be IEEE 802.3dj Ethernet.**

[![](https://substackcdn.com/image/fetch/$s_!VHIg!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F69e99f52-037f-4b70-93e8-7083bcaab163_850x403.png)](https://substackcdn.com/image/fetch/$s_!VHIg!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F69e99f52-037f-4b70-93e8-7083bcaab163_850x403.png)[UALink draft 1.0 spec. ](https://t.co/TJGzUuSfnf)

[![](https://substackcdn.com/image/fetch/$s_!mmXm!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F670c4206-f49d-4642-b9d1-6098f72129ea_986x798.png)](https://substackcdn.com/image/fetch/$s_!mmXm!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F670c4206-f49d-4642-b9d1-6098f72129ea_986x798.png)<https://docs.broadcom.com/doc/scale-up-ethernet-framework>

Remember that PHY quality is the real differentiator. All the other stuff is low-value digital and software plumbing that any semi-competent team can implement.

 **In other words, UALink can only be as good as the Ethernet PHY implemented by the customer.**

Given that neither Nvidia or Broadcom are actively participating in UALink, there exists no high-quality option on the market.

* * *

## [2] Explination of the Announcment

Ryan Smith (on behalf of ServeTheHome) made an excellent diagram explaining what is actually happening.

[![](https://substackcdn.com/image/fetch/$s_!vBdl!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9caf1f3b-50a2-432b-beda-23d8194c0155_636x805.png)](https://substackcdn.com/image/fetch/$s_!vBdl!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9caf1f3b-50a2-432b-beda-23d8194c0155_636x805.png)[NVIDIA Announces NVLink Fusion: Bringing NVLink to Third-Party CPUs and Accelerators - ServeTheHome](https://www.servethehome.com/nvidia-announces-nvlink-fusion-bringing-nvlink-to-third-party-cpus-and-accelerators/)

NVLink C2C (short range 200G SerDes) is now open to license as an IP block to third parties. This means partner companies can add this hardware directly to their chip design.

NVLink5 (long range 200G SerDes) **IS NOT LISCENSED.** Nvidia will be selling a “fusion chiplet” that has NVLInk C2C on one end and NVLink 5 on the other. Intuitively this is an asymmetric re-timer. One SerDes go in, other SerDes go out.

Long-reach SerDes IP critical to Nvidia’s moat **IS NOT LISCENSED.** This block is only available on the fusion chiplet made by (and fully controlled by) Nvidia.

This allows Nvidia to dictat3e configurations. As Ryan Smith said, only two scenarios are allowed:

1\. Third party ARM CPU (Fujitsu, Qualcomm) + Nvidia GPU

2\. Nvidia Grace ARM CPU + third party ASIC + Nvidia NVLink Fusion chiplet

 **[NOT SUPPORTED]** Third party ARM CPU (Fujitsu, Qualcomm) + third party ASIC + Nvidia NVLink Fusion chiplet

Nvidia will simply refuse to sell the fusion chiplet, kneecapping the **UNSUPPORTED** config to single-node operation as NVLink C2C does not have enough reach to exit the PCB of a single node.

[![](https://substackcdn.com/image/fetch/$s_!PeRL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4114405f-9086-4656-985b-da50d1edd258_220x220.gif)](https://substackcdn.com/image/fetch/$s_!PeRL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4114405f-9086-4656-985b-da50d1edd258_220x220.gif)

* * *

## [3] IEEE 802.3ck/dj KR vs VSR vs Nvlink C2C vs NVLink5

Official Ethernet spec is called IEEE 802.3 and these standards are locked behind a paywall.

“ck” is for 106.5Gbps while “dj” is for 212.5Gbps speed per lane.

I only have a PDF for 802.3ck on my personal laptop but trust me that dj (212.5Gbps) spec is very similar to an outsider. There are major differences but those go beyond the scope of this post.

Out of spite towards a standards body that shills “open-ness” while locking critical documentation behind very expensive paywalls, I will be re-publishing some snippets directly from the (several hundred page) spec.

[![](https://substackcdn.com/image/fetch/$s_!YSNQ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffedd8908-3765-45f0-ba99-64ead9037afc_487x610.png)](https://substackcdn.com/image/fetch/$s_!YSNQ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffedd8908-3765-45f0-ba99-64ead9037afc_487x610.png)Sue me, assholes.

### [3.a] Reach and Tradeoffs

As you can see in the spec, there are additional members of the alphabet soup such as “KR”, “LR”, “C2M”, and “VSR”. This is because Ethernet is divided up into sub-standards based on reach.

[![](https://substackcdn.com/image/fetch/$s_!kAVx!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F42d883d0-cae5-445c-9526-55dee3344272_769x77.png)](https://substackcdn.com/image/fetch/$s_!kAVx!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F42d883d0-cae5-445c-9526-55dee3344272_769x77.png)

[![](https://substackcdn.com/image/fetch/$s_!B4PC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F16feeec9-c2fd-4a58-ac7c-020aeb53c118_766x67.png)](https://substackcdn.com/image/fetch/$s_!B4PC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F16feeec9-c2fd-4a58-ac7c-020aeb53c118_766x67.png)

[![](https://substackcdn.com/image/fetch/$s_!POfg!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fecffa258-60c1-45a4-b6a7-6f8e29ed69dc_787x163.png)](https://substackcdn.com/image/fetch/$s_!POfg!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fecffa258-60c1-45a4-b6a7-6f8e29ed69dc_787x163.png)

[![](https://substackcdn.com/image/fetch/$s_!_zWy!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F21a89270-c2c6-4992-aa3a-ca704ac86a4e_1383x806.png)](https://substackcdn.com/image/fetch/$s_!_zWy!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F21a89270-c2c6-4992-aa3a-ca704ac86a4e_1383x806.png)OIF piggy-backs off of IEEE.

Analog (PHY/SerDes) designers can target one or more of these reach specs. For example, one PHY IP might support KR, LR, and C2M but cannot handle VSR. Another PHY (from the same company) can be designed to support C2M and VSR only.

There are power, area, and performance tradeoffs. PHYs designed for long reach will have larg DSP (digital signal processing) chains. Say around 40-80 FFE taps. Meanwhile, a short-reach Ethernet PHY may only have 15-30 FFE taps.

Many more changes can be made. I am giving you one vague (intentionally obfuscated) example.

NVLink C2C is analogous to a C2M or VSR style Ethernet SerDes. Short reach, lower power and small die area.

NVLink5 is analogous to a super KR style Ethernet SerDes. Ultra-long reach, large die area, guzzles power.

Let’s look at some snippets from official spec so you can get an intuitive understanding.

 **Note:** _IEEE 802.3 defines a standard package model of 4 dB insertion loss for both Tx and Rx. The bump to bump (realistic) loss is whatever the table says + 8 dB. Most people calibrate out the package via de-embedding. IEEE provides a “informative and unofficial” MATLAB script called the “COM” (channel operating margin) script that does this de-embedding. Everyone uses it._

KR (backplane) spec.

[![](https://substackcdn.com/image/fetch/$s_!-y5g!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F11eaa07a-77e9-40ba-92b0-da58f680f1b4_801x543.png)](https://substackcdn.com/image/fetch/$s_!-y5g!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F11eaa07a-77e9-40ba-92b0-da58f680f1b4_801x543.png)

CRC (chip to chip) spec requires testing at different (lower) insertion loss.

[![](https://substackcdn.com/image/fetch/$s_!INxO!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc2845b9a-532e-4a2a-b538-0f63f0aa5376_816x409.png)](https://substackcdn.com/image/fetch/$s_!INxO!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc2845b9a-532e-4a2a-b538-0f63f0aa5376_816x409.png)

There are 5-8 of these, depending on how you count.

Can one SerDes drive all of these channels in a power efficient, high-performance manner? **No.**

It is standard to make (at least) two SerDes. One for super long reach and lots of nasty reflections. Another for short reach for power sensitive applications.

[![](https://substackcdn.com/image/fetch/$s_!HcEp!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F795844a5-d678-4419-a1ef-1dd490b7b62b_617x97.png)](https://substackcdn.com/image/fetch/$s_!HcEp!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F795844a5-d678-4419-a1ef-1dd490b7b62b_617x97.png)

* * *

### [3.b] Why “Open” is not Neccisarily Better

The best way to explain this stance is with some examples.

[![](https://substackcdn.com/image/fetch/$s_!aD2y!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa458d03b-caf9-474b-b505-f67b58b39a11_771x318.png)](https://substackcdn.com/image/fetch/$s_!aD2y!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa458d03b-caf9-474b-b505-f67b58b39a11_771x318.png)

Ethernet transmitters have a 5-tap digital FIR filter. This digital pre-distortion filter allows for correcting of reflections and channel conditions, improving performance. When you plug in an Ethernet device (really any modern SerDes), the remote receiver requests different Tx FIR settings in a process called link training.

Because both sides need to agree on the possible configuration space ahead of time, rules must be set in place within the standard.

Maybe 7-tap FIR filter would help. You have to use 5 if you ar3e building for Ethernet. Maybe NVLink5 has more FIR taps to accommodate stronger reflections from the backplane. No idea.

Some rules make sense. For example, the absolute value of all the taps summed must be less than or equal to one. This makes sense as you don’t want to scale the signal at this stage as that would mess with analog transmitter specs.

What does not make sense as the artificial limits of each taps sign and strength. Why must C(1) and C(-1) be negative? Why limit the strength of the taps?

From digital filter theory, these limits seem pointless. Ask a group of SerDes engineers why these limits to Tx FIR exist and 95% of them won’t be able to give you an answer.

* * *

Every engineering standard has some dumb shit jammed into it. For Ethernet, look no further than “differential effective return loss”, dERL.

“Return loss” is a measure of how “reflective” a circuit is. Reflections are bad so you want this number to be low.

Traditionally, you measure ERL on a machine called a VNA and plot the s-parameters. There is some mask where you line has to stay under. Thats it. Easy.

[![](https://substackcdn.com/image/fetch/$s_!KlJd!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7af8e2f8-96b9-4a5d-887f-393ff0e60a74_1353x779.png)](https://substackcdn.com/image/fetch/$s_!KlJd!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7af8e2f8-96b9-4a5d-887f-393ff0e60a74_1353x779.png)It’s simple. Plug thing into box. Measure squiggle. If squiggles bellow linear mask, then pass.

Modern Ethernet requires dERL, a retarded, overcomplicated, nonsensical measurement where you have to feed s-parameters into a five-thousand line MATLAB script from hell such that it spits out a number nobody actually understands. Some dumbass at Intel came up with this joke of a measurement and shoved it into spec. 

I hope Lip-Bu Tan fires him.

[![](https://substackcdn.com/image/fetch/$s_!FIaP!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F206ba5c3-8efe-4304-a41c-6802f33f1575_614x456.png)](https://substackcdn.com/image/fetch/$s_!FIaP!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F206ba5c3-8efe-4304-a41c-6802f33f1575_614x456.png)

[![](https://substackcdn.com/image/fetch/$s_!hsv7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F93a34097-915c-47c9-a0ea-5f01c5f07a6d_498x498.gif)](https://substackcdn.com/image/fetch/$s_!hsv7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F93a34097-915c-47c9-a0ea-5f01c5f07a6d_498x498.gif)

* * *

Finally, we have temperature ranges

Ethernet requires the PHY to operate anywhere from -40C to +125C die temp.

Yes, those numbers are really what is required.

The reason for such extreme temperature requirements is the Ethernet PHY might be in an industrial/automotive scenario. Say a hot factory with poor cooling or a cell tower in a snowy environment. Designing the PHY to perform well across this wide temperature range is not only difficult, **it forces performance sacrifices.**

Do you think Nvidia gives a shit if NVLink works at -40C? **NO!**

They designed the SerDes to work really well at 20-90C die temp probably as that is what can happen in a liquid cooled datacenter.

* * *

### [3.c] Practical (Visual) Overview

Let’s look at the GB200 board and rack-scale NVL72 system to understand why NVLink5 and NVLink C2C are materially different even though both are 200Gbps SerDes.

[![](https://substackcdn.com/image/fetch/$s_!cJsT!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd655fe12-40e3-4442-8890-4252a97039c8_710x963.png)](https://substackcdn.com/image/fetch/$s_!cJsT!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd655fe12-40e3-4442-8890-4252a97039c8_710x963.png)

As you can see, the distance between the CPU and GPU (covered by NVLink C2C) is rather short. **More importantly, its just a PCB which means there are not many strong reflections.**

Reflections require heavy DSP to correct. NVLink C2C (just like a VSR or C2M Ethernet PHY) can cut a lot of stuff to save power and die area.

NVLink5 has to deal with the now legendary Amphenol overpass cables and backplane. All you investors wondered why that shit has caused so many problems… hopefully now you understand.

REFLECTIONS! REFLECTIONS! REFLECTIONS!

[![](https://substackcdn.com/image/fetch/$s_!sObp!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcdeb7851-a968-4930-b5bc-896a9a94a108_220x165.gif)](https://substackcdn.com/image/fetch/$s_!sObp!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcdeb7851-a968-4930-b5bc-896a9a94a108_220x165.gif)

REFLECTIONS! REFLECTIONS! REFLECTIONS!

 **Every connector adds a possibility for impedance mismatch and reflections.** Fucks up the signal real quick. Testing so many connections at once has been a nightmare but innovative companies such as **Multilane** have developed a unique solution that is rapidly improving the manufacturing landscape.

<https://www.multilaneinc.com/>

## [4] Strategic Impact

This move by Mr. Leather Jacket is truly galaxy-brain. It fucks over so many competitors. Truely glorious. Jensen is playing 420-dimentional chess as the Hypersaclers munch on checkers pieces and crayons.

[![](https://substackcdn.com/image/fetch/$s_!KDG_!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc9849963-0ccc-4dff-b1ee-e2822d056029_480x270.gif)](https://substackcdn.com/image/fetch/$s_!KDG_!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc9849963-0ccc-4dff-b1ee-e2822d056029_480x270.gif)Visual approximation of Amazon Trainium 3 program management.

 **NVLink Fusion re-shapes the entire AI ASIC landscape.**

### [4.a] Nvidia

This is a massive strategic win for Nvidia. Jensen has murdered UALink before it could be born. The lock-in from this NVLink Fusion program is incredible. Nvidia forces NVLink C2C PHY and MAC upon 3rd party chips, locking those designs into the Nvidia ecosystem. Important, differentiating IP (long-reach NVLink5) is protected by keeping it in a Nvidia-only Fusion chiplet they design, supply (via TSMC) and track.

 **Money is not the objective here.** Even if Nvidia charges $100M in NRE for the NVLink C2C IP to 10 customers, that is only $1B in one-time revenue. Actually nothing in the grand scheme of things. $100M of NRE for a single IP block is a ridiculous number BTW. The actual prices are almost certainly much lower.

But then what of the Fusion chiplets? It’s a small die with high yield. Even if Nvidia charges 90% gross margins, the revenue will be small relative to Blackwell GPUs at 70-75% gross margins at **MUCH HIGHER ASP.**

Make no mistake, this is Nvidia trying to murder all competition except Broadcom. Brilliant long-term strategic move.

[![](https://substackcdn.com/image/fetch/$s_!DDK5!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2e595bc1-8eff-498a-b16d-7d92936acbbf_400x600.png)](https://substackcdn.com/image/fetch/$s_!DDK5!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2e595bc1-8eff-498a-b16d-7d92936acbbf_400x600.png)

### [4.b] Synopsys, Cadence, and Alphawave

All three of these companies lose in various severity. The IP departments of Synopsys and Cadence just got their TAM slashed as Nvidia is now directly competing with them using a completely superior 200G PHY.

Both Synopsys and Cadence will be fine as investments. The core EDA business is unaffected. The IP departments are kinda toasted. Some people are prob going to be fired.

[![](https://substackcdn.com/image/fetch/$s_!Xj3K!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F74140d4d-3c39-41e4-ab93-0725abaf6416_320x240.gif)](https://substackcdn.com/image/fetch/$s_!Xj3K!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F74140d4d-3c39-41e4-ab93-0725abaf6416_320x240.gif)

Alphawave is in deep shit.

That Qualcomm acquisition offer is probably gona go BYE BYE. LOOOL.

[![](https://substackcdn.com/image/fetch/$s_!5NXs!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8ad3ebf3-1cc7-434f-9fa4-a5f1ba04b00e_186x162.gif)](https://substackcdn.com/image/fetch/$s_!5NXs!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8ad3ebf3-1cc7-434f-9fa4-a5f1ba04b00e_186x162.gif)I need to break out advanced Risitas.

### [4.c] Broadcom

You may think this hurts Broadcom but I think NVLink Fusion is neutral at worst, probably a net benefit to Broadcom.

Nvidia is murdering several competitors who also compete with Broadcom. Thus, the market becomes a brutal duopoly/oligopoly where both sides print money and the customers have no choice but to pay.

### [4.d] Alchip, Marvell, and Amazon

The Trainium 3 dumpster fire has been glorious entertainment.

First, Amazon pays NRE to both Alchip and Marvell for Trainum 3 under the same codename. Supply-chain degens go nuts arguing who got awarded this shit project before it becomes clear Taiwan buy-side is right and Alchip got it.

Then, Alchip fucks up integrating the Synopsys 200G SerDes and has to re-spin. Now rumor is Marvell got the Trn3 IO die even though their 200G SerDes is crap too.

Amazon is trying to figure out how to salvage this shitshow as both Alchip and Marvell join the NVLink Fusion program. 

**Marvell is now openly admitting their 200G SerDes is shit.**

[![Image](https://substackcdn.com/image/fetch/$s_!lEwK!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F20fd2634-c71d-4255-8109-f68b4162f493_1717x1222.jpeg)](https://substackcdn.com/image/fetch/$s_!lEwK!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F20fd2634-c71d-4255-8109-f68b4162f493_1717x1222.jpeg) Put that extra Ace of Clubs down Matt Murphy!

### [4.e] Astera Labs

Asteral Labs is working on their own 200G SerDes because the Synopsys/Cadence/Alphawave 200G is not good enough. Currently, Astera Labs re-packages Synopsys SerDes. They know they need to make something better. **Every port on their stuipd PCIe switch needs a fucking re-timer.**

Now that you know why Astera Labs OpEx is blowing up, what happens to that R&D now that they have joined NVLink fusion? PCIe switch market just got a lot smaller.

### [4.f] MediaTek and Google

If corporations are people, then Hock Tan has Google by the balls. It is well known within industry that Google has been **DESPERATLY** trying to find **ANYONE** with a **viable** 200G SerDes so they can design-out Broadcom. Google has pinged every single vendor multiple times over the past two years and nobody can meet their ridiculous post-FEC requirements. MediaTek has already failed once on N4P and is rumored to have failed again on N3P. According to a trusted contact in Taiwan, half the MediaTek SerDes team has left to join Nvidia recently.

 **Maybe they know they are doomed now that MediaTek has joined the NVLink Fusion program.**

[![](https://substackcdn.com/image/fetch/$s_!0JPb!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F924e1698-6e7c-4abb-b669-a2c510bb5774_1170x1149.jpeg)](https://substackcdn.com/image/fetch/$s_!0JPb!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F924e1698-6e7c-4abb-b669-a2c510bb5774_1170x1149.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!qE5h!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F89a3f21f-c506-4df8-a458-1e8fb6c78586_1200x600.avif)](https://substackcdn.com/image/fetch/$s_!qE5h!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F89a3f21f-c506-4df8-a458-1e8fb6c78586_1200x600.avif)

Mr. Leather Jacket seems to have killed MediaTek’s 200G SerDes team and forced Google back to Broadcom or into NVLink Fusion.

[![](https://substackcdn.com/image/fetch/$s_!5kog!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F151065a0-e522-4cd4-8108-f25c48e141b9_292x354.png)](https://substackcdn.com/image/fetch/$s_!5kog!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F151065a0-e522-4cd4-8108-f25c48e141b9_292x354.png)

### [4.g] Fujitsu and Qualcomm

The vanilla V2 ARM IP CPU cores in Nvidia Grace are crap. Fujitsu and Qualcomm are making custom ARM-compliant CPU cores that will go into a server product. NVLink Fusion is a great win for both. Instant access to a very large market that commands higher margins than the cloud-native cheapo CSS chiplets ARM makes for the Hyperscaler internal CPU workloads.

I hate to say it but this is… good… for Qualcomm. 

(very funny though… Qualcomm execs hate Nvidia)

### [4.h] AMD and Other UALink **LOSERS**

UALink is an AMD specification that they donated to the consortium. Early UALink draft specs said **“AMD CONFIDENTIAL UNDER NDA”** in big bold letters and the top of each page alongside the AMD logo. Subtle.

Jensen has brutally murdered UALink like that one scene from “Game of Thrones”.

You remember... the red wedding.”

AMD was already in deep shit because UALink switches were super far out. Most likely 2027 volume ramp. Semianalysis has highlighted this problem several times.

<https://semianalysis.com/2025/04/23/amd-2-0-new-sense-of-urgency-mi450x-chance-to-beat-nvidia-nvidias-new-moat/>

Who is going to want to develop UALink switches now? Astera Labs has already defected to NVLink fusion. Are the random crypto miner losers turned AI switch vendors gona help AMD defeat Nvidia Vera-Rubin? **LOOOOOL**

Everyone associated with UALink is a NVLink fusion loser.

[![](https://substackcdn.com/image/fetch/$s_!2-Px!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8d5ece65-7bfd-48eb-b05a-fbf77840bb08_220x189.gif)](https://substackcdn.com/image/fetch/$s_!2-Px!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8d5ece65-7bfd-48eb-b05a-fbf77840bb08_220x189.gif)

The “L” in “UALink” stands for “LOSER”.

L

O

S

E

R

Subscribe for engineering-driven investment analysis.

Subscribe

Share?

[Share](https://irrationalanalysis.substack.com/p/nvlink-fusion-jensen-murders-ualink?utm_source=substack&utm_medium=email&utm_content=share&action=share)
