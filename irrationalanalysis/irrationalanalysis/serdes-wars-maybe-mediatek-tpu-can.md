# SerDes Wars: Maybe MediaTek TPU Can Be Salvaged by... Semtech

## CTLE is Key

**Dec 15, 2025**

**Likes:** 0

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice, and readers should **always do their own research before investing in any security.**

  * Feel free to contact me via email at: _irrational_analysis@proton.me_




* * *

Edit: Dan from Semianalysis made a glorious thumbnail.

[![](https://substackcdn.com/image/fetch/$s_!UYiD!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7bbdfe81-6e60-4ea4-9773-238f1b7f04ec_896x1200.png)](https://substackcdn.com/image/fetch/$s_!UYiD!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7bbdfe81-6e60-4ea4-9773-238f1b7f04ec_896x1200.png)

This is a very quick note based on the Taiwan rumor mill pissing me off and subsequently making me realize I might be super wrong.

[![](https://substackcdn.com/image/fetch/$s_!VHB-!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F259a615a-fec5-4b39-b037-25f44f63a6ad_589x984.png)](https://substackcdn.com/image/fetch/$s_!VHB-!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F259a615a-fec5-4b39-b037-25f44f63a6ad_589x984.png)<https://x.com/dnystedt/status/2000358972071747917>

My immediate reaction was this is bullshit and Google is playing games, trying to negotiate with Broadcom.

But… I have been hearing a lot of chatter about Google using Semtech ACC for 200G per lane in 2027. Which does not mean much on its own.

However, recently a trusted contact told me Semtech CEO is hyping up using the ACC chip (linear equalizer) **on PCBs too.**

 **That means something.**

CTLE = continuous-time linear equalizer

CTLE = linear equalizer

Multiple phrases, same underlying meaning.

Here is what the Synopsys SerDes CTLE looks like:

[![](https://substackcdn.com/image/fetch/$s_!6xTR!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa9f8bdb1-d115-4a01-8329-34bdcdfeb9d1_1252x706.png)](https://substackcdn.com/image/fetch/$s_!6xTR!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa9f8bdb1-d115-4a01-8329-34bdcdfeb9d1_1252x706.png)

All you need to know is CTLE is a type of amplifier.

All amplifiers add noise to your system.

All (active) amplifiers burn extra power.

So there is a limit to how much amplification you can get away with.

Adding an extra CTLE in a cable or on a PCB in addition to the SerDes Rx CTLE(s) will eventually hit diminishing returns.

To understand the design tradeoffs, let’s look at this excellent Maxim/Analog datasheet.

<https://www.analog.com/media/en/technical-documentation/data-sheets/MAX24104.pdf>

[![](https://substackcdn.com/image/fetch/$s_!FaDs!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2128d438-a8a5-4a45-ba9b-76cfcb4df039_908x427.png)](https://substackcdn.com/image/fetch/$s_!FaDs!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2128d438-a8a5-4a45-ba9b-76cfcb4df039_908x427.png)

[![](https://substackcdn.com/image/fetch/$s_!WZLs!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe7dcaaf7-65e9-49fb-bb38-94f98cc2ce73_1381x793.png)](https://substackcdn.com/image/fetch/$s_!WZLs!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe7dcaaf7-65e9-49fb-bb38-94f98cc2ce73_1381x793.png)

First, notice that the noise induced by the linear equalizer depends on:

  * Data Rate

  * Equalization (gain) Setting

  * Channel Loss




[![](https://substackcdn.com/image/fetch/$s_!ZpQw!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F11d22472-f3bd-4160-be77-324ffcb537a1_1375x979.png)](https://substackcdn.com/image/fetch/$s_!ZpQw!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F11d22472-f3bd-4160-be77-324ffcb537a1_1375x979.png)

Here is how to read above plots.

Plot 3 is the baseline.

Plot 1 is after the linear equalizer with system running at 10.3 Gbps.

Plot 2 is after the linear equalizer with system running at 13.5 Gbps.

Both plot 1 and plot 2 show significant extra noise compared to the baseline in plot 3.

Plot 2 is worse than plot 1 because the linear equalizer performance degrades as data rate increases. 

**Key Points (sorry being repetitive but need to hammer these in):**

  * ALL AMPLIFIERS ADD NOISE

  * What matters is if the amplifier is placed in the appropriate location to provide more benefit (gain at Nyquist) relative to the intrinsic noise it adds to the system.




[![](https://substackcdn.com/image/fetch/$s_!fjPU!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F90557f36-2d09-41e0-a003-4c8ad129a0be_1398x1214.png)](https://substackcdn.com/image/fetch/$s_!fjPU!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F90557f36-2d09-41e0-a003-4c8ad129a0be_1398x1214.png)

There exists a sweet spot (range) where placing the linear equalizer makes sense.

Too close to the SerDes Tx and you hit saturation.

Too far away and the amplifier noise overpowers benefits. 

[![](https://substackcdn.com/image/fetch/$s_!BlhI!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1e1c0362-fa51-465a-a123-24f9a42f9ec1_1042x1191.png)](https://substackcdn.com/image/fetch/$s_!BlhI!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1e1c0362-fa51-465a-a123-24f9a42f9ec1_1042x1191.png)

With a proper datasheet, some sample parts, and basic test equipment, it is relatively straightforward to calculate what the placement range is and how much benefit there will be to system performance.

Unfortunately, Semtech are assholes and it is borderline impossible to get the damn datasheet.

First, the 224G part is not even listed on their website.

Second, the datasheet for the 112G part (GN8112) is impossible to get.

<https://www.semtech.com/products/signal-integrity/signal-conditioners/gn8112#resources>

[![](https://substackcdn.com/image/fetch/$s_!VFP4!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1c7adabc-c1b8-4b27-b8b8-d1799caeed11_1116x976.png)](https://substackcdn.com/image/fetch/$s_!VFP4!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1c7adabc-c1b8-4b27-b8b8-d1799caeed11_1116x976.png)

I made a stupid “MySemtech” account with my work email. But the private portal is missing this datasheet. I have asked multiple times for this datasheet and they ghosted me each time.

I write stuff here for free as a hobby and almost never ask for anything in return.

This is a rare instance of me asking for something.

 **Someone get me the damn datasheet for this GN8112 part.**

 **Bonus points if you can get me the datasheet for the 224G part.**

email to: _irrational_analysis@proton.me_

* * *

“Up to 15dB equalization” means nothing without understanding the noise floor and tuning/shaping options of the CTLE.

Also, the “transparent link-training” claims are technically true but practically bullshit.

Here is a summary of how linear equalizers effect a system design:

#  **Pros:**

Peaking at Nyquist, adding gain min-channel.

 **Can make a sub-standard SerDes from MediaTek viable against Broadcom SerDes.**

#  **Cons:**

Adds noise to the system.

1.5-2.5 pj/bit energy impairment. (away from the ASIC so not too bad… does not make thermal density worse)

A hellish nightmare to tune. (channel specific, high PVT variation)

Makes link-training much more painful.

Single-source supplier (Semtech) because Macon sucks.

* * *

I have previously covered MediaTek SerDes here:

[![ISSCC 2025: Ultra High-Speed SerDes](https://substackcdn.com/image/fetch/$s_!RoY0!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F978c4585-e143-4b20-82a9-44f1dbcca208_619x410.png)

#### ISSCC 2025: Ultra High-Speed SerDes

[Irrational Analysis](https://substack.com/profile/135313705-irrational-analysis)·February 20, 2025[Read full story](https://irrationalanalysis.substack.com/p/isscc-2025-ultra-high-speed-serdes)](https://irrationalanalysis.substack.com/p/isscc-2025-ultra-high-speed-serdes)

They showed their N4 design back in February (ISSCC) and it had some… very bad choices.

[![](https://substackcdn.com/image/fetch/$s_!LtgT!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F50466cf2-c904-4e61-972a-63992d0468eb_780x458.png)](https://substackcdn.com/image/fetch/$s_!LtgT!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F50466cf2-c904-4e61-972a-63992d0468eb_780x458.png)

Modern high-speed SerDes only has one DFE tap.

They have two which makes DFE-propagation burst errors SO MUCH WORSE.

The reason for this crazy DFE design is because of a different crazy.

[![](https://substackcdn.com/image/fetch/$s_!ykRN!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8c13ea08-fa56-4030-9e6a-6b40405d20b6_726x777.png)](https://substackcdn.com/image/fetch/$s_!ykRN!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8c13ea08-fa56-4030-9e6a-6b40405d20b6_726x777.png)

They added gain to their ADC interleaves which is crazy. 99% confident the 32-tap floating DFE coefficient is to cancel out the massive sampling error.

As you can see, the gain in the ADC interleaves is approximately 8 dB at most.

What if…

  * They removed this gain.

  * Removed the extra DFE tap.

  *  **Convinced Google to add a shit ton of Semtech linear equalizers all over the PCB and make all cables ACC instead of DAC.**




I CANNOT CONFIRM THIS THEORY WITHOUT THE SEMTECH DATASHEETS.

PLEASE EMAIL ME DATASHEETS OR CONVINCE SEMTECH TO TALK TO ME.

Subscribe for engineering-driven investment analysis.

Subscribe

Share?

[Share](https://irrationalanalysis.substack.com/p/serdes-wars-maybe-mediatek-tpu-can?utm_source=substack&utm_medium=email&utm_content=share&action=share)
