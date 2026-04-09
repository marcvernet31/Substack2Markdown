# OFC 2026 Irrational Recap

## Glorious conference.

**Mar 27, 2026**

**Likes:** 0

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice and readers should **always do their own research before investing in any security.**

  * Feel free to contact me via email at: _irrational_analysis@proton.me_




* * *

So much amazing stuff. Honestly barely covering half of what I want to cover.

I realize the audience here is rather varied. There are engineers and students who care about technical stuff. Then a wide variety of sophisticated investors. Then the retail and pod-monkey idiots who want to ape into shit.

Hopefully the material is organized such that every group gets something useful out of this.

[![](https://substackcdn.com/image/fetch/$s_!746Z!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd110f0ec-080c-40c2-9e0c-039747b8584c_668x358.png)](https://substackcdn.com/image/fetch/$s_!746Z!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd110f0ec-080c-40c2-9e0c-039747b8584c_668x358.png)

MESSA SO EXCITED!

LETS GO!

* * *

# Contents:

  1. Key Useful/Investable Topics (randomized order)

    1. VCSEL CPO: Cope and Nuance

    2. Semtech CTLE (Mediatek TPU Probably Doomed)

    3. Lumentum To The Moon

    4. Huber Schuner OCS

    5. Nvidia Super Overkill Transceiver

    6. Broadcom/Meta CPO Reliability Update

    7. I DESPISE MICRO-LED IN ALL FORMS

    8. Optics Reach and Credo Dilemma

    9. Marvell Seems Panicked: Anti-DSP Jihad Response?

    10. Tower vs GloFo Sipho: NOT EVEN CLOSE 

    11. Apology to Zephyr on Furukawa Laser

    12. AAOI Booth

    13. 400G EML vs SiPho

    14. Impressive Ciena Presentation

    15. Incredible Santec Tunable Laser

    16. Arista Super LPO (XPO)

  2. Cool Shit 

  3. Public Markets: Re[tail]-Tard and Pod Monkey Summary

  4. Trading Account 3/27/2026 Snapshot




* * *

## [1] Key Useful/Investable Topics (randomized order)

There is no meaning behind the ordering. I made this up stream of consciousness and was too lazy to re-order. 

Skip to whatever you find interesting. Read it all. IDK.

### [1.a] VCSEL CPO: Cope and Nuance

I don’t like VCSEL CPO/NPO, but willing to admit it could be viable if done right. The details matter.

In a way, only one attribute matters, data rate of the VCSELs.

VCSEL cannot go above 112G per lane. There are major reliability issues. 

[![](https://substackcdn.com/image/fetch/$s_!uXTi!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Face920e5-a906-4834-8ba2-9da62380ed0f_1650x1259.png)](https://substackcdn.com/image/fetch/$s_!uXTi!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Face920e5-a906-4834-8ba2-9da62380ed0f_1650x1259.png)

While there were several presentations on 200G/lane VCSEL (can it perform, bandwidth limits), NOBODY address reliability concerns. I find it amusing people give shade to sipho-based CPO reliability but ignore the massive problems 200G VCSELs face.

[![](https://substackcdn.com/image/fetch/$s_!Qn0U!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe5021ed2-cf94-44a8-a766-f0161c34c600_1706x910.png)](https://substackcdn.com/image/fetch/$s_!Qn0U!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe5021ed2-cf94-44a8-a766-f0161c34c600_1706x910.png)

You can see Coherent presenter have a brief moment of self-awareness before reverting to the (wrong) stance that 200G VCSEL can work. 

* * *

Next, we have Furukawa.

[![](https://substackcdn.com/image/fetch/$s_!FyBi!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcefebf57-18d6-4d7c-8fad-80895c7245ff_1625x936.png)](https://substackcdn.com/image/fetch/$s_!FyBi!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcefebf57-18d6-4d7c-8fad-80895c7245ff_1625x936.png)

Thats an… ok eye you have there. Show me what it looks like with all lanes active, dumping crosstalk/noise into each other.

[![](https://substackcdn.com/image/fetch/$s_!_5Hu!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff99643ea-a452-4535-8b96-d291d9ecb530_1659x914.png)](https://substackcdn.com/image/fetch/$s_!_5Hu!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff99643ea-a452-4535-8b96-d291d9ecb530_1659x914.png)

[![I Am Disgusted GIFs | Tenor](https://substackcdn.com/image/fetch/$s_!50nA!,w_1456,c_limit,f_auto,q_auto:good,fl_lossy/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F674dac30-5f32-4c56-8b15-6f01aa0cb078_220x251.gif)](https://substackcdn.com/image/fetch/$s_!50nA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F674dac30-5f32-4c56-8b15-6f01aa0cb078_220x251.gif)

 **ENCHANCE**

[![](https://substackcdn.com/image/fetch/$s_!v3_h!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffde9374b-ce23-48fe-9cf9-48565c652977_1241x1131.png)](https://substackcdn.com/image/fetch/$s_!v3_h!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffde9374b-ce23-48fe-9cf9-48565c652977_1241x1131.png)

A TDECQ at 3 dB or higher is an outright failure. Real commercial products have TDECQ of ~1.7 dB or lower in datacom, 2.5 dB or lower in telco/longhaul.

So Furukawa is displaying a 41/48 = 85% failure rate lol.

Credit to them for actually showing this data. 

**ENCHANCE MOAR**

Here is a random eye I picked.

[![](https://substackcdn.com/image/fetch/$s_!a7Jx!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F22013249-78af-43a6-aa6f-ffe13b8aab0e_537x394.png)](https://substackcdn.com/image/fetch/$s_!a7Jx!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F22013249-78af-43a6-aa6f-ffe13b8aab0e_537x394.png)

It’s quite bad. This is what the eye of a SerDes that has suffered catastrophic ESD damage (fried transistors) looks like. Terrible RLM. To my eye (pun intended) seems to be < 0.75 RLM. 

[![](https://substackcdn.com/image/fetch/$s_!_a8b!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9dce4feb-5f72-4d84-aa84-599b8d8ca60a_864x441.png)](https://substackcdn.com/image/fetch/$s_!_a8b!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9dce4feb-5f72-4d84-aa84-599b8d8ca60a_864x441.png)

* * *

Now that we have established 200G VCSEL is a bad idea, let’s focus on how “slow” the VCSELs should go.

Here is Lumentum’s 32G NRZ per lane demo.

[![](https://substackcdn.com/image/fetch/$s_!sARD!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6e083f50-d318-4a9b-8387-508bd4bed6ef_1170x662.png)](https://substackcdn.com/image/fetch/$s_!sARD!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6e083f50-d318-4a9b-8387-508bd4bed6ef_1170x662.png)

[![](https://substackcdn.com/image/fetch/$s_!CqDl!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F906d409c-060a-4728-a305-445982e70b60_948x530.png)](https://substackcdn.com/image/fetch/$s_!CqDl!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F906d409c-060a-4728-a305-445982e70b60_948x530.png)

These results are frankly mediocre. Only four channels are active and channels 1+4 are aggressively over-peaked.

Because the rate per lane is so slow, they were forced to have very high density and thus the system is much more susceptible to electrical crosstalk. 

* * *

Coherent also had a VCSEL NPO/CPO demo but theirs ran at 100G per lane.

[![](https://substackcdn.com/image/fetch/$s_!crUz!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4cf9cdda-3bf3-4c4c-a6c2-a95ba5aba611_1209x765.png)](https://substackcdn.com/image/fetch/$s_!crUz!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4cf9cdda-3bf3-4c4c-a6c2-a95ba5aba611_1209x765.png)

[![](https://substackcdn.com/image/fetch/$s_!yf5i!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc217c3b7-71b7-4785-9cd7-656d3f00f9bb_1698x1026.png)](https://substackcdn.com/image/fetch/$s_!yf5i!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc217c3b7-71b7-4785-9cd7-656d3f00f9bb_1698x1026.png)

I am annoyed they are hiding the math function(s). Would have been nice to see the TDECQ instead of BER.

But overall, this approach is better than Lumentum’s 32G/lane VCSEL NPO/CPO.

In my opinion, the “correct/optimal” rate for VCSEL NPO/CPO is either 64G NRZ or 112G PAM4. 

Still don’t like this category of solution but willing to tolerate it’s existence. Engineering is about choosing the right tradeoffs and problems to tackle. SiPho better but wish VCSEL friends luck. You guys gona need it.

### [1.b] Semtech CTLE (Mediatek TPU Probably Doomed)

Previously, I had a tinfoil hat theory that Mediatek TPU could only work if they used a huge amount of Semtech CTLE (linear equalizer // “the ACC chip”) across both cables and PCBs.

For months I have been trying to get the damn datasheet for this part. Legit impossible.

But… finally got the curves I was looking for at the Semtech LPO presentation.

For context, basically the same Semtech chip goes into LPO, ACC, and potentially on-board. It’s just an analog amplifier. A damn good one.

[![](https://substackcdn.com/image/fetch/$s_!65uA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4ad9a629-f15a-4fe9-9d8d-15e610fcf6df_1672x1022.png)](https://substackcdn.com/image/fetch/$s_!65uA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4ad9a629-f15a-4fe9-9d8d-15e610fcf6df_1672x1022.png)

These analog amplifiers (CTLE) are very sensitive to input power. 

Too little input power and they just add noise.

Too much input power and they get saturated and kill linearity.

It is absolutely critical that the link-training algorithm adjusts the Tx FFE to optimize the Semtech CTLE independently of the receiver EQ (CTLE + FFE + DFE).

In other words, this shit is difficult. Painful.

But.. the results are incredible.

[![](https://substackcdn.com/image/fetch/$s_!r6VE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F40673927-b908-4fd2-b56f-38abc047a77f_1555x932.png)](https://substackcdn.com/image/fetch/$s_!r6VE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F40673927-b908-4fd2-b56f-38abc047a77f_1555x932.png)

[![](https://substackcdn.com/image/fetch/$s_!abO1!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F672eab53-deb2-4f6d-bf33-c09946c14246_1555x962.png)](https://substackcdn.com/image/fetch/$s_!abO1!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F672eab53-deb2-4f6d-bf33-c09946c14246_1555x962.png)

Now here is where the complexity comes in. Look at this example.

[![](https://substackcdn.com/image/fetch/$s_!maRk!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F50a16afc-0f68-46c2-82bc-358d69d22bd0_1540x900.png)](https://substackcdn.com/image/fetch/$s_!maRk!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F50a16afc-0f68-46c2-82bc-358d69d22bd0_1540x900.png)

[![](https://substackcdn.com/image/fetch/$s_!B1GW!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff113da7f-0113-4e30-80bc-ca05863696e0_1482x459.png)](https://substackcdn.com/image/fetch/$s_!B1GW!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff113da7f-0113-4e30-80bc-ca05863696e0_1482x459.png)

In this example, the Tx FFE is 9-taps which is frankly unrealistic. Real modern systems have 5 taps. 

As you can see, there is only one programmable parameter for the CTLE.

[![](https://substackcdn.com/image/fetch/$s_!O4ff!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F18008a54-84c2-485e-8bd7-227da397fc99_667x527.png)](https://substackcdn.com/image/fetch/$s_!O4ff!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F18008a54-84c2-485e-8bd7-227da397fc99_667x527.png)

Every modern SerDes also has a CTLE. Often multiple stages of CTLE. The reason is that tuning the shape of this response is critical to optimizing performance, especially across a wide variety of channels.

Here is what the Synopsys CTLE(s) look like.

[![](https://substackcdn.com/image/fetch/$s_!S73Z!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fefcb64e1-218f-4390-88fe-b050d1189c4c_1257x714.png)](https://substackcdn.com/image/fetch/$s_!S73Z!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fefcb64e1-218f-4390-88fe-b050d1189c4c_1257x714.png)

[![](https://substackcdn.com/image/fetch/$s_!dQhr!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff9d1a6db-cae4-45fc-ad18-89767af6bf0d_1226x681.png)](https://substackcdn.com/image/fetch/$s_!dQhr!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff9d1a6db-cae4-45fc-ad18-89767af6bf0d_1226x681.png)

Semtech’s chip does not have these fancy adjustment knobs. Only peaking/gain. This is fine for their target market and honestly somewhat expected. The reason I have been trying to get the datasheet is to confirm my suspicion.

 **In light of this new information, I am convinced Mediatek TPU is absolutely cooked.** There is no way this Semtech chip can save them. Not enough tuning options, particularly at low frequency. That is the real killer and what I was looking for.

To be clear, this is not bad for Semtech stock. It went from a possible ~5X to “only at 2-3x. I own a shit ton of Semtech stock and have high conviction. The nice thing is these chips are useful in copper (ACC), LPO/XPO, NPO, and traditional re-timed transceivers!

All of you debating copper vs optics… there is a name that wins in everything lol.

Also the Semtech chip is way better than equivalent Macom part. If I hear one more finance person tell me people are multi-sourcing Semtech/Macom analog amps and they similar performance I shall scream.

### [1.c] Lumentum To The Moon

Lumentum is the only high-power (350+ mW class) laser vendor who publicly declares their linewidth spec.

[![](https://substackcdn.com/image/fetch/$s_!xcyI!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff7eb23f3-2b61-45aa-9304-ac78b5911265_1248x628.png)](https://substackcdn.com/image/fetch/$s_!xcyI!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff7eb23f3-2b61-45aa-9304-ac78b5911265_1248x628.png)

[![](https://substackcdn.com/image/fetch/$s_!B_lx!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa92e51c9-2fe2-4ba6-ba52-7e00773b3362_775x592.png)](https://substackcdn.com/image/fetch/$s_!B_lx!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa92e51c9-2fe2-4ba6-ba52-7e00773b3362_775x592.png)

[![](https://substackcdn.com/image/fetch/$s_!TjsK!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F11177a61-5aa0-42f9-aac4-4915807a5a93_1262x621.png)](https://substackcdn.com/image/fetch/$s_!TjsK!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F11177a61-5aa0-42f9-aac4-4915807a5a93_1262x621.png)

Wall-plug efficiency of ~13% at 30C. Very good. Should still be well above 10% industry target at 50C.

* * *

As a bonus, they even have a 800 mW DFB (at 50C!!!!) with 0.1 MHz linewidth.

[![](https://substackcdn.com/image/fetch/$s_!CP-r!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe5b0baa2-cb31-4964-96fd-5a7b589ce655_1145x725.png)](https://substackcdn.com/image/fetch/$s_!CP-r!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe5b0baa2-cb31-4964-96fd-5a7b589ce655_1145x725.png)

SMSR is excellent indicating good quality of the grating and reduced mode-hop risk.

[![](https://substackcdn.com/image/fetch/$s_!fgSC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1c31df48-834c-4e7c-9804-5bfd29e98e4d_744x455.png)](https://substackcdn.com/image/fetch/$s_!fgSC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1c31df48-834c-4e7c-9804-5bfd29e98e4d_744x455.png)

Asymmetry of the sidemodes is interesting.

* * *

Many keep asking me about what I think about various Lumentum competitors who also claim to have high-power laser solutions for CPO.

Coherent is the most popular, but AAOI and Furukawa also getting more interest. 

My answer is simple. **Show me the linewidth.**

 **LUMENTUM IS THE ONLY COMPANY WHO PUBLICLY DISCLOSES THEIR LINEWIDTH. GO ASK THEIR COMPETITORS WHAT THEIR LINEWIDTH IS. NONE WILL ANSWER YOU. THERE IS A REASON FOR THIS.**

[![](https://substackcdn.com/image/fetch/$s_!02Jb!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa6d20b9f-453a-4a67-9418-5135b4b4f6be_864x982.png)](https://substackcdn.com/image/fetch/$s_!02Jb!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa6d20b9f-453a-4a67-9418-5135b4b4f6be_864x982.png)

[![](https://substackcdn.com/image/fetch/$s_!-Yb6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1ff9d109-4ba6-4584-b1c3-1f82a29fffa4_1440x1058.jpeg)](https://substackcdn.com/image/fetch/$s_!-Yb6!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1ff9d109-4ba6-4584-b1c3-1f82a29fffa4_1440x1058.jpeg)

I’m not fucking selling. Lumentum is comically cheap if you understand the deep engineering moat they have and insane capacity plans for these ultra-high power lasers.

[![](https://substackcdn.com/image/fetch/$s_!TMJi!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F45cea9c9-337b-4ba4-8f9f-22de092b0b26_800x909.png)](https://substackcdn.com/image/fetch/$s_!TMJi!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F45cea9c9-337b-4ba4-8f9f-22de092b0b26_800x909.png)

Lumentum and Coherent both got $2B investments each from Nvidia on March 2nd, 2026.

In under 3 weeks, Lumentum bought a huge fab to ramp production. 

**What has** **Coherent done with their Jensen bux?**

Could it be that linewidth is a critical performance specification that only Lumentum discloses because everyone else linewidth is bad?

* * *

I want to really hammer this point home for all the spreadsheet enthusiasts out there who don’t understand shit about communications systems engineering. 

Here is a public research paper you can find in < 10 minutes of searching on Google Scholar. Pay attention. Eat your fucking broccoli, pod monkeys.

[![](https://substackcdn.com/image/fetch/$s_!Bbf6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc72ebb97-98fa-4a7e-bfe2-8835a7d1d4fd_818x819.png)](https://substackcdn.com/image/fetch/$s_!Bbf6!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc72ebb97-98fa-4a7e-bfe2-8835a7d1d4fd_818x819.png)

[![](https://substackcdn.com/image/fetch/$s_!m0px!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8e6b9e4a-1856-4853-99f1-68e0bd95905c_1015x657.png)](https://substackcdn.com/image/fetch/$s_!m0px!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8e6b9e4a-1856-4853-99f1-68e0bd95905c_1015x657.png)

Ring modulators are much more sensitive to linewidth than MZI modulators.

[![](https://substackcdn.com/image/fetch/$s_!lRxy!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7568be85-f043-4d3c-bf22-7a9099d2802c_1033x1070.png)](https://substackcdn.com/image/fetch/$s_!lRxy!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7568be85-f043-4d3c-bf22-7a9099d2802c_1033x1070.png)

And by sensitive, I mean the extinction ratio is murdered by higher linewidth.

There is a massive structural shift where ring modulators are being mass adopted by everyone (except Celestial/Marvell) involved in CPO.

 **Historically, narrow laser linewidth was needed for coherent (16QAM, 64QAM) modulation of long-distance links such as ZR, not datacom.**

 **With the mass adoption of ring modulators, led by Nvidia, linewidth has suddenly become much more important for a MUCH LARGER MARKET (DATACOM) THAT IS RAPIDLY EXPANDING (CPO).**

* * *

 **There is no viable pure-play competitor to Lumentum.** Broadcom has an excellent internal laser department but the stock is obviously not a pure-play to narrow-linewidth ultra-high-power CPO lasers.

[![](https://substackcdn.com/image/fetch/$s_!atf_!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F78ebc238-d820-48c0-a4ac-92df80d6b482_1696x928.png)](https://substackcdn.com/image/fetch/$s_!atf_!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F78ebc238-d820-48c0-a4ac-92df80d6b482_1696x928.png)

[![](https://substackcdn.com/image/fetch/$s_!mygM!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0d6e95f3-db14-49a9-9a31-9d4e14d3ec15_602x1195.png)](https://substackcdn.com/image/fetch/$s_!mygM!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0d6e95f3-db14-49a9-9a31-9d4e14d3ec15_602x1195.png)

### [1.d] Huber Schuner OCS

Over the past few months, several people have pinged me about the Huber Schuner OCS and I sort of gave a lazy response because was busy with other things.

Ran into this at their booth and… there might be something here.

[![](https://substackcdn.com/image/fetch/$s_!UteW!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd7742302-bd27-4c85-9776-d0596a68d080_1449x778.png)](https://substackcdn.com/image/fetch/$s_!UteW!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd7742302-bd27-4c85-9776-d0596a68d080_1449x778.png)

[![](https://substackcdn.com/image/fetch/$s_!QufA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F441a863f-8c62-4d01-ac2a-cab6e90fb895_833x943.png)](https://substackcdn.com/image/fetch/$s_!QufA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F441a863f-8c62-4d01-ac2a-cab6e90fb895_833x943.png)

[![](https://substackcdn.com/image/fetch/$s_!ATxq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1927d561-b4b7-45d9-a520-a874d65689b0_627x1299.png)](https://substackcdn.com/image/fetch/$s_!ATxq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1927d561-b4b7-45d9-a520-a874d65689b0_627x1299.png)

There are three broad categories of OCS.

  1. MEMS (Lumentum)

  2. Piezoelectric (Huber Schuner)

  3. Liquid Crystal (Coherent)




MEMS/Lumentum is winning by a wide margin because it is overall the best, particularly in terms of insertion loss.

(how much light you lose going through the switch)

Coherent loves to say how their OCS is differentiated from MEMS. No moving parts! More reliable! More scalable!

[![](https://substackcdn.com/image/fetch/$s_!XnYt!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F000d72d7-a60b-4cbf-9240-ce97b4c91dae_1375x935.png)](https://substackcdn.com/image/fetch/$s_!XnYt!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F000d72d7-a60b-4cbf-9240-ce97b4c91dae_1375x935.png)

[![](https://substackcdn.com/image/fetch/$s_!F2w4!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc32a6d71-8f33-4c3b-80fb-3035145cffbc_1479x821.png)](https://substackcdn.com/image/fetch/$s_!F2w4!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc32a6d71-8f33-4c3b-80fb-3035145cffbc_1479x821.png)

It’s differentiated by being bad. Very high insertion loss between ports that are right next to each other. Surprising lack of uniformity as well.

Spoke with a Huber Schuner employee and allegedly their OCS insertion loss is 1.5-2 dB depending on the size of the switch. 

For comparison, here is Lumentum’s public claims on their MEMS OCS insertion loss.

<https://www.lumentum.com/en/blog/optical-circuit-switches-in-ai-hyperscale-data-centers>

[![](https://substackcdn.com/image/fetch/$s_!O0lb!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffe4e91aa-ff06-4534-aa7b-c470aaebd0e6_1254x395.png)](https://substackcdn.com/image/fetch/$s_!O0lb!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffe4e91aa-ff06-4534-aa7b-c470aaebd0e6_1254x395.png)

Lots of people asking me about Lumentum vs Coherent OCS.

Maybe stop thinking about Coherent and give Huber Schuner a look. 

### [1.e] Nvidia Super Overkill Transceiver

At the TFC booth (everyone laugh at the Himax bulls), Nvidia showed three versions of their 1.6T transceiver platform. All of them use the internal Nvidia DSP. Another L for Marvell lmao.

First we have the regular (fully re-timed) version.

[![](https://substackcdn.com/image/fetch/$s_!zWQl!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd1a73c49-70a8-4028-9b1c-0291e3d126d0_1421x790.png)](https://substackcdn.com/image/fetch/$s_!zWQl!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd1a73c49-70a8-4028-9b1c-0291e3d126d0_1421x790.png)

[![](https://substackcdn.com/image/fetch/$s_!mmxQ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcfdee54b-34b1-41f5-ba4d-1cea2da4b6a3_1559x928.png)](https://substackcdn.com/image/fetch/$s_!mmxQ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcfdee54b-34b1-41f5-ba4d-1cea2da4b6a3_1559x928.png)

~15 pj/bit, excellent loopback BER.

* * *

Then the LRO/TRO (half DSP) version.

[![](https://substackcdn.com/image/fetch/$s_!Qe77!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb934ee1b-7302-4dd6-949b-89b78338d1c4_1290x1097.png)](https://substackcdn.com/image/fetch/$s_!Qe77!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb934ee1b-7302-4dd6-949b-89b78338d1c4_1290x1097.png)

[![](https://substackcdn.com/image/fetch/$s_!qWm7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe5da583b-c9fa-4005-ad06-34f58ed4bd99_1414x962.png)](https://substackcdn.com/image/fetch/$s_!qWm7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe5da583b-c9fa-4005-ad06-34f58ed4bd99_1414x962.png)

~10 pj/bit, good loopback BER.

* * *

And now for the shocking sipho/COUPE version using ring modulators.

[![](https://substackcdn.com/image/fetch/$s_!0JD2!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F050e61e9-f009-4bfe-819d-946dba097999_968x1052.png)](https://substackcdn.com/image/fetch/$s_!0JD2!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F050e61e9-f009-4bfe-819d-946dba097999_968x1052.png)

[![](https://substackcdn.com/image/fetch/$s_!0861!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd2b69ca2-3f26-4f5d-aae5-8c52576dfe6d_1586x1001.png)](https://substackcdn.com/image/fetch/$s_!0861!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd2b69ca2-3f26-4f5d-aae5-8c52576dfe6d_1586x1001.png)

~14.5 pj/bit, incredible unheard-of performance.

Those of you who have not worked on this stuff cannot understand how insane these pre-FEC BER numbers are.

Getting 7/8 lanes to e-14 BER is insane. Even with extreme levels of cheating (cherry picking parts, slam die temp to 25C with large chiller) it is borderline impossible to hit this performance level.

Nvidia accomplished this using the power of hybrid bonding, TSMC COUPE, and ring modulators. Extreme co-design.

[![](https://substackcdn.com/image/fetch/$s_!G9RH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd82de655-99e9-48e2-91fc-3f87443c8314_590x524.png)](https://substackcdn.com/image/fetch/$s_!G9RH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd82de655-99e9-48e2-91fc-3f87443c8314_590x524.png)

Obviously, these transceiver with COUPE inside is massive overkill and economically unviable. Way too expensive.

But still… extraordinarily impressive marketing demo. Taking shots at Broadcom lol.

### [1.f] Broadcom/Meta CPO Reliability Update

[![](https://substackcdn.com/image/fetch/$s_!hBXk!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F71965115-fa76-4936-b7cf-0375bd343097_1628x961.png)](https://substackcdn.com/image/fetch/$s_!hBXk!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F71965115-fa76-4936-b7cf-0375bd343097_1628x961.png)

This is the old data they already showed. 

[![](https://substackcdn.com/image/fetch/$s_!baP0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F134b461f-903d-49f4-ae49-4bd8504b248e_1642x971.png)](https://substackcdn.com/image/fetch/$s_!baP0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F134b461f-903d-49f4-ae49-4bd8504b248e_1642x971.png)

And here is the new data. They found some interesting hardware bugs. Will get to that shortly.

[![](https://substackcdn.com/image/fetch/$s_!aLnO!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc426776c-6cf4-4f27-b96f-4193045020c4_1506x882.png)](https://substackcdn.com/image/fetch/$s_!aLnO!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc426776c-6cf4-4f27-b96f-4193045020c4_1506x882.png)

My blood pressure goes up every time some dumbass says CPO is less reliable than transceivers.

Motherfucker do you even know what FEC symbols are?

[![](https://substackcdn.com/image/fetch/$s_!uDav!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F322ecb7d-9030-4d5b-b48e-0bb276a9d6ad_1640x958.png)](https://substackcdn.com/image/fetch/$s_!uDav!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F322ecb7d-9030-4d5b-b48e-0bb276a9d6ad_1640x958.png)

Amusingly, they had a minor problem with the ELSFP laser driver. Refused to comment on what “SMT component” had degradation issues but my guess is a capacitor. Probably switched some particular decap from tantalum to MLCC or vice-versa. Capacitors do not like heat.

This is why phase 2 CPO testing has “updated build standards”.

[![](https://substackcdn.com/image/fetch/$s_!dkEK!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F07c0162c-eb9c-4d41-847c-6c7ba65341e2_1531x841.png)](https://substackcdn.com/image/fetch/$s_!dkEK!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F07c0162c-eb9c-4d41-847c-6c7ba65341e2_1531x841.png)

Finding these kinds of annoying problems well before mass-deployment in a production environment is exactly why Meta has gone to all this trouble.

Great stuff. Incredibly bullish SiPho CPO.

### [1.g] I DESPISE MICRO-LED IN ALL FORMS

I am getting annoyed at the number of people pinging me on Micro-LED.

 **I HATE THEM ALL.**

 **I HATE THE STUPID MICROSOFT PAPER.**

 **I HATE EVERY SIGNEL MICRO-LED EFFORT EQUALLY WITH THE FIRE OF A THOUSAND SUNS.**

Previously have covered the bullshit Microsoft paper here.

Going to snip the micro-LED section.

[![](https://substackcdn.com/image/fetch/$s_!ueog!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbc125a1c-05c4-4e7d-9175-ec6cf15b45b4_788x991.png)](https://substackcdn.com/image/fetch/$s_!ueog!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbc125a1c-05c4-4e7d-9175-ec6cf15b45b4_788x991.png)

[![](https://substackcdn.com/image/fetch/$s_!vQCE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0d479827-2f0c-4811-b357-db480093d003_576x465.png)](https://substackcdn.com/image/fetch/$s_!vQCE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0d479827-2f0c-4811-b357-db480093d003_576x465.png)

[![](https://substackcdn.com/image/fetch/$s_!NkIZ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe1fb589f-b0d8-4500-a623-f64309b66ffe_770x984.png)](https://substackcdn.com/image/fetch/$s_!NkIZ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe1fb589f-b0d8-4500-a623-f64309b66ffe_770x984.png)

[![](https://substackcdn.com/image/fetch/$s_!FmRk!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F80c01f87-53c0-406e-b133-b02c0da17068_755x1317.png)](https://substackcdn.com/image/fetch/$s_!FmRk!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F80c01f87-53c0-406e-b133-b02c0da17068_755x1317.png)

[![](https://substackcdn.com/image/fetch/$s_!FvHk!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F958aa40e-81a1-443e-9b29-afec52feaf4a_781x1142.png)](https://substackcdn.com/image/fetch/$s_!FvHk!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F958aa40e-81a1-443e-9b29-afec52feaf4a_781x1142.png)

[![](https://substackcdn.com/image/fetch/$s_!QgW0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3af152da-53a2-4e6e-a701-51b14efa7432_765x1190.png)](https://substackcdn.com/image/fetch/$s_!QgW0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3af152da-53a2-4e6e-a701-51b14efa7432_765x1190.png)

MICRO-LED WILL NEVER WORK.

ELECTRICAL CROSSTALK ALONE KILLS THIS IDIOTIC TECHNOLOGY.

PHASE NOISE FROM THE INCOHERENT LIGHT OF AN LED MAKES THIS TECH EXTRA DEAD.

[![](https://substackcdn.com/image/fetch/$s_!CBw5!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F05550592-51ae-480a-acb4-d15a9a3eefee_805x495.png)](https://substackcdn.com/image/fetch/$s_!CBw5!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F05550592-51ae-480a-acb4-d15a9a3eefee_805x495.png)

 **ALL THE MICRO-LED EFFORTS HAVE MASSIVE COPE ON WHAT BER IS ACTUALLY NEEDED FOR A VIABLE LINK. YOUR PJ/BIT NUMBERS DON’T COUNT FOR JACK SHIT IF YOU EXCLUDE THE MASSIVE POWER YOU HAVE TO BURN MASSIVE POWER ON SUPER HEAVY FEC AND VERY HIGH NUMBER OF LANES.**

[![Brainlet Meme - Meme - Posters and Art Prints | TeePublic](https://substackcdn.com/image/fetch/$s_!vmME!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F039d9c9b-8d62-4624-b692-46bd7caf9aff_630x630.jpeg)](https://substackcdn.com/image/fetch/$s_!vmME!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F039d9c9b-8d62-4624-b692-46bd7caf9aff_630x630.jpeg)

* * *

I am willing to give VCSEL NPO/CPO the benefit of the doubt. Don’t like it but it could work if done well.

Micro-LED is an ultra retarded version of VCSEL NPO/CPO. 

### [1.h] Optics Reach and Credo Dilemma

[![Optical Communication Band - FiberLabs Inc.FiberLabs Inc.](https://substackcdn.com/image/fetch/$s_!t0bz!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2a064c0f-68b3-4897-a07d-8507181fd466_541x272.jpeg)](https://substackcdn.com/image/fetch/$s_!t0bz!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2a064c0f-68b3-4897-a07d-8507181fd466_541x272.jpeg)

Optical fiber is wonderful. Incredibly low loss. Kinda the entire point of optics.

It takes great pain and suffering to get your data onto a fiber, but once you make it there, distance does not matter much.

In O-band (datacom standard band), there is effectively zero practical difference between 1-meter, 10-meter, and 30-meter reach.

Arguably, even up to 100-meter is the same but chromatic dispersion might have a small effect so trying to hedge a bit here.

Credo operates in a niche of 3-7 meter. This niche dies as advanced optics such as LPO, XPO, NPO, and CPO proliferate.

You could argue that Credo has a great optical DSP and are trying to diversify.

[![](https://substackcdn.com/image/fetch/$s_!VnHH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F88feae11-e13b-4999-a96f-1464953c6235_1738x1219.png)](https://substackcdn.com/image/fetch/$s_!VnHH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F88feae11-e13b-4999-a96f-1464953c6235_1738x1219.png)

[![](https://substackcdn.com/image/fetch/$s_!k3kk!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd471b0f6-6499-40f8-a9c7-ce79341e4065_960x548.png)](https://substackcdn.com/image/fetch/$s_!k3kk!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd471b0f6-6499-40f8-a9c7-ce79341e4065_960x548.png)

They had an extremely impressive interopt demo. Amusingly, this is not bullish Credo because they are entering a shrinking market with questionable terminal value. Credo optical DSP being really good is hyper-bearish Marvell, neutral Credo lol.

Also I despise micro-LED in all forms. Go read that section for the takedown. 

### [1.i] Marvell Seems Panicked: Anti-DSP Jihad Response?

There is a jihad (holy war) against optical DSP.

We have the usual suspects (LPO, CPO, NPO) but now Arista has XPO too. Everyone fucking hates optical DSP. Everyone hates Marvell’s most important franchise.

What’s worse is the optical DSP market is getting lots of new entrants. 

We going from Marvell 80%, Broadcom 20% to…

Broadcom much higher share.

Credo take significant share.

Cisco, Maxlinear, and a few others I am forgetting going from zero to something.

And the entire market is fleeing re-timed optical DSP systems anyway.

I’m not sure what Marvell is doing. They seem to be throwing everything at the wall and seeing what sticks. The only reason I am not screaming for everyone to short Marvell into oblivion is Celestial. 

(I am short right now for hedging purposes… sorry Celestial friends…)

### [1.j] Tower vs GloFo Sipho: NOT EVEN CLOSE

It is said that a picture is worth a thousand words.

I present to you my latest artwork.

[![](https://substackcdn.com/image/fetch/$s_!KFrW!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4ad4f361-69d5-4c35-918b-28e6ea367b36_799x640.png)](https://substackcdn.com/image/fetch/$s_!KFrW!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4ad4f361-69d5-4c35-918b-28e6ea367b36_799x640.png)

Quick history detour.

A long time ago (5-10 years ago), it was thought that the best way to integrate electronics and photonics would be using a monolithic approach.

You see, photonics modulators need (in general) very high voltage swing. Around 2-5 volt pk-pk. Unfortunately, SerDes is typically around 400-800 mV, with a peak of 1200 mV in rare corner cases. (this varies based on standard and process node)

So you need some electronics to boost the signal before the photonics, but you don’t want to eat reflections or other channel impairments from packaging.

Thus, GloFo created the monolithic “fusion” node.

[![](https://substackcdn.com/image/fetch/$s_!M700!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc4e03cbe-d393-46a8-b4b5-4d897f05cde0_1680x934.png)](https://substackcdn.com/image/fetch/$s_!M700!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc4e03cbe-d393-46a8-b4b5-4d897f05cde0_1680x934.png)

[![](https://substackcdn.com/image/fetch/$s_!JrWq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F07db749a-fe19-4243-a21e-d96c95a742bd_1597x906.png)](https://substackcdn.com/image/fetch/$s_!JrWq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F07db749a-fe19-4243-a21e-d96c95a742bd_1597x906.png)

Imagine a standalone SiPho node and standalone electronics node each have ~30-60 process layers.

The GloFo fusion node has 100-150 layers. Amusingly, the cycle time is over 6 months (similar to 3nm-class nodes) even though the structures are 45nm-class and would usually take 2-3 months to fab.

* * *

I talk to many engineers from dayjobs and through this newsletter. There is always a spread of opinions. Even topics with extreme consensus have 5% of people taking the other side.

 **Except for GloFo fusion node.**

Not a single person has ever said something nice to me about this monolithic PIC+EIC node. ZERO. Universally derided. 

So many problems. Thermal crosstalk. Electrical crosstalk. Low-quality SiN performance. Painful cycle time and design rules. Poor bandwidth. Poor linearity. Can go on and on.

Ayar Labs and Lightmatter were both using GloFo fusion but have now aggressively pivoted to TSMC COUPE (hybrid bonded). Genuinely looking forward to seeing what those two can accomplish without the crazy process-node handicap they have been suffering through all these years.

There is only one chart you need to see to understand why GloFo fusion is so bad.

[![](https://substackcdn.com/image/fetch/$s_!0XFo!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6057e0be-11ec-4f8b-b92c-06d95ea20e2e_1484x888.png)](https://substackcdn.com/image/fetch/$s_!0XFo!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6057e0be-11ec-4f8b-b92c-06d95ea20e2e_1484x888.png)

Let’s zoom in and make direct comparisons.

[![](https://substackcdn.com/image/fetch/$s_!UEGd!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4ac3dd62-dade-4596-bcd4-0a3c2a626c82_1416x1038.png)](https://substackcdn.com/image/fetch/$s_!UEGd!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4ac3dd62-dade-4596-bcd4-0a3c2a626c82_1416x1038.png)

I made a poor attempt to scale the plots such that the y-axis is roughly similar.

As you can see, the (correct) hybrid-bonding approach delivers ~110 GHz of bandwidth while GloFo fusion only gives 40-75 GHz of bandwidth. Even then, the frequency response becomes super noisy after 30GHz. 

(also for some reason GloFo did not normalize their data… whatever)

Those of you with the appropriate engineering background know what the charts and numbers mean. You will also notice Tower marketing screwed up and labeled their chart S_11 instead of S_21. This is a typo. Silly mistake. Let it go.

Those of you who don’t know what the fuck I am talking about… you can easily recognize that one of these charts is not like the other two and looks really ugly.

* * *

 **Global Foundries has made the wrong technology choice and are still refusing to pivot. Tower saw what TSMC did with COUPE and quickly brought their own (HYBRID BONDED) solution to market less than a year later.**

[![](https://substackcdn.com/image/fetch/$s_!ku_t!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb822172d-3095-4969-aa49-30fdd79123ed_1664x961.png)](https://substackcdn.com/image/fetch/$s_!ku_t!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb822172d-3095-4969-aa49-30fdd79123ed_1664x961.png)

[![](https://substackcdn.com/image/fetch/$s_!jCsx!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Facaab5d2-a3c2-47b7-a923-4182177287af_1706x982.png)](https://substackcdn.com/image/fetch/$s_!jCsx!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Facaab5d2-a3c2-47b7-a923-4182177287af_1706x982.png)

[![](https://substackcdn.com/image/fetch/$s_!2PTv!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F06651a45-7d44-4c30-ac78-0a625d9b7bd1_607x1111.png)](https://substackcdn.com/image/fetch/$s_!2PTv!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F06651a45-7d44-4c30-ac78-0a625d9b7bd1_607x1111.png)

* * *

Tower also has several other nice features on their excellent SiPho platform.

[![](https://substackcdn.com/image/fetch/$s_!lF4Y!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2f98674b-ef9e-40ec-bf38-a6d0ecd82549_1507x841.png)](https://substackcdn.com/image/fetch/$s_!lF4Y!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2f98674b-ef9e-40ec-bf38-a6d0ecd82549_1507x841.png)

 **Worlds best silicon nitride.**

* * *

InP hybrid integration via Openlight. (PDK abstracted!)

[![](https://substackcdn.com/image/fetch/$s_!Jnxt!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6006af9b-774e-4776-8652-a833889d02f9_1520x812.png)](https://substackcdn.com/image/fetch/$s_!Jnxt!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6006af9b-774e-4776-8652-a833889d02f9_1520x812.png)

[![](https://substackcdn.com/image/fetch/$s_!UNaH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9a90c415-69e9-4d4d-9dd6-9db58cf25d3f_1360x875.png)](https://substackcdn.com/image/fetch/$s_!UNaH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9a90c415-69e9-4d4d-9dd6-9db58cf25d3f_1360x875.png)

Up to ~ 11 dBm integrated DFB lasers, 20 mW (13 dBm) integrated SOA, and quite high quality EAM modulators as well. BEAUTIFUL. 

* * *

[![](https://substackcdn.com/image/fetch/$s_!RJPi!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F13ec203d-5979-4f3f-a3d8-13f4b952d7b4_1604x955.png)](https://substackcdn.com/image/fetch/$s_!RJPi!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F13ec203d-5979-4f3f-a3d8-13f4b952d7b4_1604x955.png)

Great dark-current performance and PD bandwidth but the peaking between 20-50 GHz is a mild annoyance. Gotta nitpick this.

Also the ESD tolerance/reliability of Tower PDs has room for improvement.

* * *

[![](https://substackcdn.com/image/fetch/$s_!U8_-!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdc739a35-34e8-4236-9092-46b72247d861_1440x1063.jpeg)](https://substackcdn.com/image/fetch/$s_!U8_-!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdc739a35-34e8-4236-9092-46b72247d861_1440x1063.jpeg)

[![Metal Gear Solid Salute GIFs | Tenor](https://substackcdn.com/image/fetch/$s_!Sf7I!,w_1456,c_limit,f_auto,q_auto:good,fl_lossy/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa04000a2-128a-460b-a12b-065f57d21eb1_220x124.gif)](https://substackcdn.com/image/fetch/$s_!Sf7I!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa04000a2-128a-460b-a12b-065f57d21eb1_220x124.gif)

In Russell we trust.

### [1.k] Apology to Zephyr on Furukawa Laser

Ok so the Furukawa high-power laser is real. They had a live demo.

[![](https://substackcdn.com/image/fetch/$s_!upe3!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa59cac58-b247-45ce-ab2f-00063d35bbf1_1570x912.png)](https://substackcdn.com/image/fetch/$s_!upe3!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa59cac58-b247-45ce-ab2f-00063d35bbf1_1570x912.png)

Claims to have good noise performance but I asked the guy what the RIN is and he gave a very evasive answer. Facial expression told me “fuck fuck dont answer this fuck”.

He did answer my question on if this is a normal DFB or a MOPA.

<https://www.coherent.com/news/glossary/mopa-technology>

[![mopa-principle.jpg](https://substackcdn.com/image/fetch/$s_!dPcq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8f729a16-3f25-41cf-a2d4-eaadffd038de_950x470.jpeg)](https://substackcdn.com/image/fetch/$s_!dPcq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8f729a16-3f25-41cf-a2d4-eaadffd038de_950x470.jpeg)

There are two ways of making a high-power laser.

The normal way is to make big laser. This is difficult as you have to control noise very well. Only Lumentum knows how to do this at 400+ mW class.

The other way is to have a smaller laser (~100 mW) seed a SOA (semiconductor optical amplifier). Both elements are on the same InP chip. (monolithic)

MOPAs are nice because it is much easier to get good noise performance. The drawback is cost (larger InP chip) and mode-hop risk.

Here is a random chart that illustrates mode hops well.

[![Thorlabs · Low-Noise, Narrow-Linewidth Laser Systems, 1550 nm](https://substackcdn.com/image/fetch/$s_!VVf8!,w_1456,c_limit,f_auto,q_auto:good,fl_lossy/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F45b7b927-335c-40fb-9f35-36325dbf26a0_780x512.gif)](https://substackcdn.com/image/fetch/$s_!VVf8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F45b7b927-335c-40fb-9f35-36325dbf26a0_780x512.gif)

Lasers like to jump around in frequency and power at specific drive currents and temperatures. MOPAs are **much more prone** to mode hops because of the cavity between the SOA and the seed DFB. Also much more prone to back-reflection.

It is impossible to know if this Furukawa laser has been sufficiently hardened against mode hops without detailed testing in a laboratory environment. 

But… at least Furukawa has something.

Coherent is playing catch-up, trying to pivot to a MOPA for UHP laser market. Maybe Furukawa is worth a bid over this possible CPO laser upside. 

### [1.l] AAOI Booth

I stopped by the AAOI booth to see if their transceivers are legit and… looking good.

~e-12 pre-fec all lanes for 800G. Good.

[![](https://substackcdn.com/image/fetch/$s_!zYPu!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe22d0742-72fc-48db-8c33-dec975cb7c22_1325x1220.png)](https://substackcdn.com/image/fetch/$s_!zYPu!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe22d0742-72fc-48db-8c33-dec975cb7c22_1325x1220.png)

For 1.6T the performance is a touch lower than I would like but still decent.

[![](https://substackcdn.com/image/fetch/$s_!p5NS!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F45c08242-5ea7-42bd-b717-fc1ba35eb0a7_1558x1216.png)](https://substackcdn.com/image/fetch/$s_!p5NS!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F45c08242-5ea7-42bd-b717-fc1ba35eb0a7_1558x1216.png)

Until I realize the low BER lanes are actually RTLR/LRO.

[![](https://substackcdn.com/image/fetch/$s_!ZmSS!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6e244f8d-08c6-407d-9bb4-c8bb80c465e8_1720x841.png)](https://substackcdn.com/image/fetch/$s_!ZmSS!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6e244f8d-08c6-407d-9bb4-c8bb80c465e8_1720x841.png)

Yea this is pretty good. Test was running for over 2 hours so it’s not cheesed. 

Also have some high power lasers for CPO but no info on linewidth or RIN. No noise performance == messa not interested.

[![](https://substackcdn.com/image/fetch/$s_!m0Gz!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F07ca4e57-a5e8-49c0-8ba5-c8cf32731bdc_1598x1117.png)](https://substackcdn.com/image/fetch/$s_!m0Gz!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F07ca4e57-a5e8-49c0-8ba5-c8cf32731bdc_1598x1117.png)

11% wall-plug efficiency probably at 30C TEC setpoint given case temp is 44.4C. A 15-ish C delta between case and TEC cold side temp seems reasonable.

So worse efficiency than Lumentum’s 13% at similar target TEC setpoint.

### [1.m] 400G EML vs SiPho

Many have asked me about 400G situation for EML vs SiPho.

Some are SiPho bulls, others are EML bulls.

The answer is you should stop over-thinking things and everything goto the moon.

Yes, EML is much better at 400G than SiPho. So what? More of the 200G market will transition to SiPho and precious InP capacity will still be slammed by 400G EML and CPO/CW ultra-high-power lasers.

[![The Lumentum Series | Part 1: Transceivers](https://substackcdn.com/image/fetch/$s_!TMt9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F22a3f8d9-38b1-4409-86c7-1fdd042f8e20_1024x599.png)](https://substackcdn.com/image/fetch/$s_!TMt9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F22a3f8d9-38b1-4409-86c7-1fdd042f8e20_1024x599.png)

Some generations of speed (100G, 40G) are not popular. Honestly, 40G was dead on arrival.

800G, 1.6T, and 3.2T will all have wonderful lifecycles and explosive growth. 

You think those 400G EML InP chips are small? No! Need way more laser power and modulator die size to hit SNR requirements at much higher baud rate.

Everything is fine finance friends. Stop trying to find excuses to be worried about your sipho or EML holdings. 

Here is the excellent Coherent demo. They put a (almost) apples-to-apples comparison of EML vs SiPHo at 400G.

[![](https://substackcdn.com/image/fetch/$s_!_c_2!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F20182bec-9880-4300-869c-d947a40756e3_1213x1185.png)](https://substackcdn.com/image/fetch/$s_!_c_2!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F20182bec-9880-4300-869c-d947a40756e3_1213x1185.png)

 **Notice that the EML demo has 2 km of fiber while the sipho demo has a short patch loopback.**

That is a good 1-1.7 dB delta depending on the band! 

Despite this favorable fudging to try and make sipho look good, we get drastically different histogram results.

[![](https://substackcdn.com/image/fetch/$s_!apNH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fde9eb3c1-a208-413d-b7f9-513d7b233548_787x323.png)](https://substackcdn.com/image/fetch/$s_!apNH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fde9eb3c1-a208-413d-b7f9-513d7b233548_787x323.png)

SiPho histogram is ass. Obvious bandwidth limitation.

EML clear winner at 400G and that is fine. Just means that 200G/lane products will get even more rapid SiPho adoption.

As an aside, 400G modulation is possible with rings and COUPE using clever co-design. So CPO 400G/lane is all good. Rejoice sipho bulls.

* * *

Here is Lumentum’s 400G EML demo.

[![](https://substackcdn.com/image/fetch/$s_!Aj98!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5a79cebb-25b0-4474-8ced-1dba5e1e9f69_1786x1325.png)](https://substackcdn.com/image/fetch/$s_!Aj98!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5a79cebb-25b0-4474-8ced-1dba5e1e9f69_1786x1325.png)

They used scope averaging. This is a big no-no. Called out Nvidia for using averaging in their ISSCC 2026 presentation and gona call out Lumentum here. 

[![](https://substackcdn.com/image/fetch/$s_!KmED!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7b31c2fd-7c6a-4fb7-976a-3d57e0930634_1641x948.png)](https://substackcdn.com/image/fetch/$s_!KmED!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7b31c2fd-7c6a-4fb7-976a-3d57e0930634_1641x948.png)

Annoying they stopped the FEC tail at symbol 6. My guess (from looking at many FEC tails) is they are well past symbol 8. Probably some hits on symbol 10/11.

### [1.n] Impressive Ciena Presentation

[![](https://substackcdn.com/image/fetch/$s_!ykhA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fce52bf63-829b-4021-a78e-9d216d071c23_1601x890.png)](https://substackcdn.com/image/fetch/$s_!ykhA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fce52bf63-829b-4021-a78e-9d216d071c23_1601x890.png)

I would argue that the nasty loss at 80-85GHz means PAM8 is the best but whatever. 

IMO min requirement should be 1e-7.

[![](https://substackcdn.com/image/fetch/$s_!nzMF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7e68b955-ba21-4af9-86e5-685c2681c039_1456x971.png)](https://substackcdn.com/image/fetch/$s_!nzMF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7e68b955-ba21-4af9-86e5-685c2681c039_1456x971.png)

You can hit > 28 dB SNDR with great difficulty electrically but yes Ciena is right you cant hit that optically.

[![](https://substackcdn.com/image/fetch/$s_!jYMU!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa9979386-2776-4ae7-8f5e-6782f0b8eb1c_1605x912.png)](https://substackcdn.com/image/fetch/$s_!jYMU!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa9979386-2776-4ae7-8f5e-6782f0b8eb1c_1605x912.png)

Agree that gearboxing is dogshit solution.

Samtech and TE have good connectors that make PAM4 400G electrically viable. Ciena themselves have a custom connector and package that makes this viable…

Did you guys not talk to each other internally…?

(I am just ribbing them… that connector is for long-haul pluggable InP transceiver, not sipho NPO/CPO)

[![](https://substackcdn.com/image/fetch/$s_!Sf2T!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5a4f98c3-7d35-4333-bffd-db501d075dcb_1743x1231.png)](https://substackcdn.com/image/fetch/$s_!Sf2T!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5a4f98c3-7d35-4333-bffd-db501d075dcb_1743x1231.png)

8 dB CTLE gain. Pretty good given how they were probably VERY limited on die area.

[![](https://substackcdn.com/image/fetch/$s_!8BTd!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F75b5ec7b-7000-4da7-b339-633ba7662c65_1710x1101.png)](https://substackcdn.com/image/fetch/$s_!8BTd!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F75b5ec7b-7000-4da7-b339-633ba7662c65_1710x1101.png)

Many people were asking why Ciena has 65 FFE taps (massive power and area burn) given that the channel impulse response only has a far out reflection at tap 38.

Presenter did not do a good job answering this question so let me help him out.

You always over-build FFE taps in the first generation design. Taps can be disabled for a 90% power reduction.

Further iterations you remove taps or switch to a floating/programmable tap system.

[![](https://substackcdn.com/image/fetch/$s_!5zoJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fee83b3ab-d403-4583-8dd9-3352290e9cf4_1728x1021.png)](https://substackcdn.com/image/fetch/$s_!5zoJ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fee83b3ab-d403-4583-8dd9-3352290e9cf4_1728x1021.png)

Excellent results. 

[![](https://substackcdn.com/image/fetch/$s_!pn05!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F724513c7-dfe0-4416-a5fc-1385f7dffa54_1667x830.png)](https://substackcdn.com/image/fetch/$s_!pn05!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F724513c7-dfe0-4416-a5fc-1385f7dffa54_1667x830.png)

Interesting study on how nonlinearity (low RLM) murders performance. Hear that micro-LED and VCSEL CPO bulls...? LINEARITY IS IMPORTANT.

[![](https://substackcdn.com/image/fetch/$s_!S9_5!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9130648b-da94-46c0-89ee-373534ffeb84_1741x989.png)](https://substackcdn.com/image/fetch/$s_!S9_5!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9130648b-da94-46c0-89ee-373534ffeb84_1741x989.png)

Great performance across all channels. Kudos for showing data with all lanes active, max crosstalk.

[![](https://substackcdn.com/image/fetch/$s_!zeXr!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F59e7085c-05a8-4141-a188-9841e4f09eaa_1645x951.png)](https://substackcdn.com/image/fetch/$s_!zeXr!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F59e7085c-05a8-4141-a188-9841e4f09eaa_1645x951.png)

This is correct. Higher electrical loss means higher random errors so DFB or MLSE helps more.

[![](https://substackcdn.com/image/fetch/$s_!1UK6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1111ddf7-3197-4de7-ba2d-1fc0250ae4f0_1651x968.png)](https://substackcdn.com/image/fetch/$s_!1UK6!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1111ddf7-3197-4de7-ba2d-1fc0250ae4f0_1651x968.png)

Multi-path interference (reflections or chromatic dispersion) kills the link which is expected. 

[![](https://substackcdn.com/image/fetch/$s_!R9bA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0f058e0c-95d6-4170-8e8a-c6a37d601a3f_1597x877.png)](https://substackcdn.com/image/fetch/$s_!R9bA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0f058e0c-95d6-4170-8e8a-c6a37d601a3f_1597x877.png)

Overall great stuff. Really enjoyed this presentation.

### [1.o] Incredible Santec Tunable Laser

I am familiar with the excellent TSL-570. 

They had a demo of the new TSL-580 and holy shit.

[![](https://substackcdn.com/image/fetch/$s_!4mnD!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa6823047-bc6b-4c15-ba36-23911683de9e_870x1039.png)](https://substackcdn.com/image/fetch/$s_!4mnD!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa6823047-bc6b-4c15-ba36-23911683de9e_870x1039.png)

How the fuck did they hit 20 KHz linewidth????

They must be using injection locking in some form.

Incredible product.

### [1.p] Arista Super LPO (XPO)

Arista has a new super LPO MSA and it’s beautiful.

[![](https://substackcdn.com/image/fetch/$s_!0Mtk!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd94ea006-22c7-47cd-b943-e907aa6d8b15_1607x1101.png)](https://substackcdn.com/image/fetch/$s_!0Mtk!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd94ea006-22c7-47cd-b943-e907aa6d8b15_1607x1101.png)

[![](https://substackcdn.com/image/fetch/$s_!BBCA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F20d836a0-df37-486c-96a8-30aa1c2fb4bd_1639x1173.png)](https://substackcdn.com/image/fetch/$s_!BBCA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F20d836a0-df37-486c-96a8-30aa1c2fb4bd_1639x1173.png)

Look at all that tasty content for Semtech! Gona need a lot of analog amplifiers (CTLE, TIA, driver) to make these giant LPO transceivers work.

Fully liquid cooled. This helps performance and power efficiency a lot. Lasers hate heat. Hell, analog amplifiers also perform better at lower temperatures. You generally lose gain at higher die temp.

## [2] Cool Shit

There were many papers that were quite interesting to me but rather useless for investment purposes. 

Everyone wave to the pod monkeys who just scrolled past this section.

[![](https://substackcdn.com/image/fetch/$s_!V6fZ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F45ab192e-e219-411b-8c85-1257c32c5be4_499x515.png)](https://substackcdn.com/image/fetch/$s_!V6fZ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F45ab192e-e219-411b-8c85-1257c32c5be4_499x515.png)

There are 35+ papers and zero planning, ordering, or organization. Don’t have time to make this section readable. Good luck.

* * *

[![](https://substackcdn.com/image/fetch/$s_!mh7r!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffdf9f493-5332-4320-9ce6-0ff37ac19784_794x323.png)](https://substackcdn.com/image/fetch/$s_!mh7r!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffdf9f493-5332-4320-9ce6-0ff37ac19784_794x323.png)

[![](https://substackcdn.com/image/fetch/$s_!UE8A!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbb0f4aec-68e9-4828-870d-31a307848796_1303x927.png)](https://substackcdn.com/image/fetch/$s_!UE8A!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbb0f4aec-68e9-4828-870d-31a307848796_1303x927.png)

Arrayed waveguides (AWG) are neat photonic structures that have lots of filtering applications. These academics made a rather large router using AWGs.

The insertion loss is bad…

[![](https://substackcdn.com/image/fetch/$s_!OE_6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fef87933e-db43-48cd-bcdb-298ba8704e21_1340x878.png)](https://substackcdn.com/image/fetch/$s_!OE_6!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fef87933e-db43-48cd-bcdb-298ba8704e21_1340x878.png)

I give Coherent shit for having 2.7+ dB insertion loss on their OCS and the best this AWGR can do is 3.9 dB.

So… useless but very cool research. Great job.

* * *

[![](https://substackcdn.com/image/fetch/$s_!A9-C!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0d9b036a-4ddf-4f17-b9f2-0d9fe0d74f90_774x200.png)](https://substackcdn.com/image/fetch/$s_!A9-C!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0d9b036a-4ddf-4f17-b9f2-0d9fe0d74f90_774x200.png)

One of the Nvidia people has a great paper and presentation on micro-rings. Some of the diagrams are best I have seen. Saving this for future reference.

[![](https://substackcdn.com/image/fetch/$s_!G_gs!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F18c4de8b-0b4f-48c9-8bf9-d3254b1d1768_2012x654.png)](https://substackcdn.com/image/fetch/$s_!G_gs!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F18c4de8b-0b4f-48c9-8bf9-d3254b1d1768_2012x654.png)

[![](https://substackcdn.com/image/fetch/$s_!-FCs!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff6b25105-5c82-470d-b8d9-841aa0244529_483x361.png)](https://substackcdn.com/image/fetch/$s_!-FCs!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff6b25105-5c82-470d-b8d9-841aa0244529_483x361.png)

[![](https://substackcdn.com/image/fetch/$s_!W-TP!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F34f173f0-cc11-421b-842e-2194ac4fbe0f_2112x1067.png)](https://substackcdn.com/image/fetch/$s_!W-TP!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F34f173f0-cc11-421b-842e-2194ac4fbe0f_2112x1067.png)

Best diagram of OFC 2026. Never seen pole/zero analysis like this. Super helpful for someone with my DSP background. Need more time to play with these transfer functions in MATLAB.

[![](https://substackcdn.com/image/fetch/$s_!cS1r!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdc1a8711-6f2a-41fb-bd3a-50702d11c34a_1667x911.png)](https://substackcdn.com/image/fetch/$s_!cS1r!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdc1a8711-6f2a-41fb-bd3a-50702d11c34a_1667x911.png)

[![](https://substackcdn.com/image/fetch/$s_!iUJA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffac045d7-fa80-4191-9e05-6e4660c2f16d_1512x861.png)](https://substackcdn.com/image/fetch/$s_!iUJA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffac045d7-fa80-4191-9e05-6e4660c2f16d_1512x861.png)

Inductive peaking is absolutely crucial. Process variation kills you. If you avoid that, poor shielding kills you.

Inductors act as antennas. Pick up shit you dont want. MANY problems happen because something dumps noise into an important inductor, say the inductor responsible for CTLE peaking.

[![](https://substackcdn.com/image/fetch/$s_!-Zi9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F110aa9ee-499f-4858-bc4e-d49d5c452e97_868x494.png)](https://substackcdn.com/image/fetch/$s_!-Zi9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F110aa9ee-499f-4858-bc4e-d49d5c452e97_868x494.png)

This is true. Self-heating effect on detuning is particularly painful.

[![](https://substackcdn.com/image/fetch/$s_!Np4i!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9724bb4e-3917-4f67-8b8c-ecc763bda3ca_1675x976.png)](https://substackcdn.com/image/fetch/$s_!Np4i!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9724bb4e-3917-4f67-8b8c-ecc763bda3ca_1675x976.png)

You want the laser wavelengths and ring resonance to be as close as possible to save thermal tuning/shift power.

Fab variation usually makes this impossible but there are clever ways of adjusting ring resonance after fabrication.

These involve FiconTec machines outfitted with a special add-on from a private Canadian company called Femtum.

Basically blast the SiPho chip with a laser to permanently warp the Si/SiN waveguide, shifting refractive index. 

[![](https://substackcdn.com/image/fetch/$s_!rFvt!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb3a1a99f-8cab-4d10-bc6e-a4b5e8674274_1690x942.png)](https://substackcdn.com/image/fetch/$s_!rFvt!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb3a1a99f-8cab-4d10-bc6e-a4b5e8674274_1690x942.png)

I don’t think anyone is using these wider/strange dimension rings. Laser trimming is straight up better.

[![](https://substackcdn.com/image/fetch/$s_!kyL2!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff827a75c-237d-4c1c-97e0-69f1dd1647a5_1710x970.png)](https://substackcdn.com/image/fetch/$s_!kyL2!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff827a75c-237d-4c1c-97e0-69f1dd1647a5_1710x970.png)

Parasitic capacitance kills bandwidth and linearity.

* * *

[![](https://substackcdn.com/image/fetch/$s_!n2Su!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F119650c5-65e6-4b44-b57e-a0c2bb9d212c_1069x635.png)](https://substackcdn.com/image/fetch/$s_!n2Su!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F119650c5-65e6-4b44-b57e-a0c2bb9d212c_1069x635.png)

Injection-locking is a strategy that greatly reduces noise of lasers. Basically, shove some of the laser output back in a controlled manner. 

This is very difficult to do in an economically viable manner.

(notice they are using 100 mm SiN wafers)

[![](https://substackcdn.com/image/fetch/$s_!Mfay!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1d2d5cd2-1ff9-4ddc-84b6-5d475ed40446_1890x776.png)](https://substackcdn.com/image/fetch/$s_!Mfay!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1d2d5cd2-1ff9-4ddc-84b6-5d475ed40446_1890x776.png)

[![](https://substackcdn.com/image/fetch/$s_!is-P!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7e2b6729-0282-43e5-bab4-4b6df5ef7aad_1256x1020.png)](https://substackcdn.com/image/fetch/$s_!is-P!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7e2b6729-0282-43e5-bab4-4b6df5ef7aad_1256x1020.png)

I am annoyed they only have intrinsic linewidth. Effective linewidth is what actually matters. Whatever moving on.

* * *

[![](https://substackcdn.com/image/fetch/$s_!9mCk!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fed30b668-4dce-434b-8a54-935af2789b12_860x376.png)](https://substackcdn.com/image/fetch/$s_!9mCk!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fed30b668-4dce-434b-8a54-935af2789b12_860x376.png)

Samsung Foundry has sipho now. This is news to me. Let’s see what you got!

[![](https://substackcdn.com/image/fetch/$s_!mWxC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F27d3c402-bc4d-48b3-b9a3-c2a1f269da93_1330x863.png)](https://substackcdn.com/image/fetch/$s_!mWxC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F27d3c402-bc4d-48b3-b9a3-c2a1f269da93_1330x863.png)

SiN and MIM cap support. Good.

[![](https://substackcdn.com/image/fetch/$s_!r2aT!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa78f39f1-6be5-4a69-8825-d332b982e862_1286x785.png)](https://substackcdn.com/image/fetch/$s_!r2aT!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa78f39f1-6be5-4a69-8825-d332b982e862_1286x785.png)

SiN waveguide loss a little higher than I would like to see but still pretty good.

None of the chats have properly labeled y-axis. :(

Honestly, Samsung Foundry sipho is probably better than GloFo. LOL

* * *

[![](https://substackcdn.com/image/fetch/$s_!HgT5!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F047e21d0-93fe-4e41-a69e-43fdc4e9a6bf_836x301.png)](https://substackcdn.com/image/fetch/$s_!HgT5!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F047e21d0-93fe-4e41-a69e-43fdc4e9a6bf_836x301.png)

First Nokia paper. Low voltage is a big deal. Most photonic modulators really need > 2 V swing to work properly.

[![](https://substackcdn.com/image/fetch/$s_!QtIE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff63cf768-b55a-42f3-beb3-6a9353c94b3c_1859x965.png)](https://substackcdn.com/image/fetch/$s_!QtIE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff63cf768-b55a-42f3-beb3-6a9353c94b3c_1859x965.png)

The drawback of monolithic InP is high cost.

But at least they shove a ton of SOA into this PIC lol. Helps a lot with perofmrance.

[![](https://substackcdn.com/image/fetch/$s_!ltgk!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1f06ae19-04db-464f-8521-176529b93519_1896x1125.png)](https://substackcdn.com/image/fetch/$s_!ltgk!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1f06ae19-04db-464f-8521-176529b93519_1896x1125.png)

Guys you are supposed to report RIN in dBc/Hz

Let me quickly do that math for you.

[![](https://substackcdn.com/image/fetch/$s_!_92u!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2fecc65c-31aa-45b1-ba06-2f10c4ea91d5_787x694.png)](https://substackcdn.com/image/fetch/$s_!_92u!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2fecc65c-31aa-45b1-ba06-2f10c4ea91d5_787x694.png)

-150.5 dBc/Hz

Wow pretty good!

[![](https://substackcdn.com/image/fetch/$s_!4UUY!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F08065a33-e006-4026-ab37-2d7d7c95f6ff_1886x530.png)](https://substackcdn.com/image/fetch/$s_!4UUY!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F08065a33-e006-4026-ab37-2d7d7c95f6ff_1886x530.png)

Very impressive that boosting SOA current has effectively zero impact on TDECQ. Excellent!

* * *

[![](https://substackcdn.com/image/fetch/$s_!8nyU!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3c64d2a5-89d0-4121-8c89-89824d0c888d_866x366.png)](https://substackcdn.com/image/fetch/$s_!8nyU!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3c64d2a5-89d0-4121-8c89-89824d0c888d_866x366.png)

Calculating Fourier transform using phased arrays?

This is completely useless and FUCKING AWESOME. 

I love phased arrays. 

[![](https://substackcdn.com/image/fetch/$s_!Fah2!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1b860fd3-35ef-48a4-aed8-46a599fc53a6_1892x724.png)](https://substackcdn.com/image/fetch/$s_!Fah2!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1b860fd3-35ef-48a4-aed8-46a599fc53a6_1892x724.png)

[![](https://substackcdn.com/image/fetch/$s_!wfSm!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6962b9f6-1800-462f-b116-48770042bea4_1316x1136.png)](https://substackcdn.com/image/fetch/$s_!wfSm!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6962b9f6-1800-462f-b116-48770042bea4_1316x1136.png)

The sync functions look pretty clean but this is a simulation of course.

[![](https://substackcdn.com/image/fetch/$s_!6otU!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb7c8c035-ed88-4248-8267-95b1a5ca705d_1920x1002.png)](https://substackcdn.com/image/fetch/$s_!6otU!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb7c8c035-ed88-4248-8267-95b1a5ca705d_1920x1002.png)

Honestly not bad. Don’t like the asymmetry but better than I expected.

* * *

[![](https://substackcdn.com/image/fetch/$s_!_oM2!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbb467eeb-febe-44a2-bb25-65c247dcefe3_809x256.png)](https://substackcdn.com/image/fetch/$s_!_oM2!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbb467eeb-febe-44a2-bb25-65c247dcefe3_809x256.png)

[![](https://substackcdn.com/image/fetch/$s_!cODQ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe0ff7bab-c54d-495c-9b44-3b1ab34ff7ed_1891x1257.png)](https://substackcdn.com/image/fetch/$s_!cODQ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe0ff7bab-c54d-495c-9b44-3b1ab34ff7ed_1891x1257.png)

[![](https://substackcdn.com/image/fetch/$s_!ZoKd!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3b21c56a-3c2e-4f96-bac6-1fea43ddce17_1818x1196.png)](https://substackcdn.com/image/fetch/$s_!ZoKd!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3b21c56a-3c2e-4f96-bac6-1fea43ddce17_1818x1196.png)

Excellent repeatability results for both grading and edge coupler characterization.

* * *

[![](https://substackcdn.com/image/fetch/$s_!ZG2w!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd8d93702-65f8-4745-bd4a-e61a90f238ad_823x326.png)](https://substackcdn.com/image/fetch/$s_!ZG2w!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd8d93702-65f8-4745-bd4a-e61a90f238ad_823x326.png)

[![](https://substackcdn.com/image/fetch/$s_!_uL-!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fffb262e8-c2f0-44c5-b245-675d53d43815_1306x771.png)](https://substackcdn.com/image/fetch/$s_!_uL-!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fffb262e8-c2f0-44c5-b245-675d53d43815_1306x771.png)

Never seen something like this before. Hybrid integration of directly modulated (not VCSEL) laser. Very unique.

[![](https://substackcdn.com/image/fetch/$s_!cfjM!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5f9e231a-b7eb-4acb-bf1a-68170010bf4a_1297x790.png)](https://substackcdn.com/image/fetch/$s_!cfjM!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5f9e231a-b7eb-4acb-bf1a-68170010bf4a_1297x790.png)

Yea… 15 FFE taps is rather heavy for this style of link. Power is super low though.

(does not matter because the FFE taps burn crazy power lol)

[![](https://substackcdn.com/image/fetch/$s_!P5Ky!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F39012b28-660c-4476-929e-dacda10daad3_1292x894.png)](https://substackcdn.com/image/fetch/$s_!P5Ky!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F39012b28-660c-4476-929e-dacda10daad3_1292x894.png)

Guys your driver electronics probably contribute 2-4 pj/bit lmao. 

* * *

[![](https://substackcdn.com/image/fetch/$s_!C17_!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F52ed1e28-174b-4e84-937a-abe490419546_830x336.png)](https://substackcdn.com/image/fetch/$s_!C17_!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F52ed1e28-174b-4e84-937a-abe490419546_830x336.png)

Impressive numbers. Let’s see the details.

[![](https://substackcdn.com/image/fetch/$s_!bMpS!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbc4cb94a-6b82-4d15-b758-26328308f7f2_1955x694.png)](https://substackcdn.com/image/fetch/$s_!bMpS!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbc4cb94a-6b82-4d15-b758-26328308f7f2_1955x694.png)

Very impressive ER and bandwidth.

[![](https://substackcdn.com/image/fetch/$s_!OowG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F74ecf576-8315-4d75-895a-14aa4aacd3c8_1917x898.png)](https://substackcdn.com/image/fetch/$s_!OowG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F74ecf576-8315-4d75-895a-14aa4aacd3c8_1917x898.png)

PD has some undesirable response at 80 GHz but overall pretty good.

FFE can fix this.

[![](https://substackcdn.com/image/fetch/$s_!_pT0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F39edd3ef-3273-4bd5-923c-39b0986225b1_1314x156.png)](https://substackcdn.com/image/fetch/$s_!_pT0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F39edd3ef-3273-4bd5-923c-39b0986225b1_1314x156.png)

I won’t ding them for using PDFA. Grating couplers great for R&D. In reality this tech would be used with edge coupling in high-performance transceivers.

[![](https://substackcdn.com/image/fetch/$s_!kzBo!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4a3bfb74-3493-4132-b21e-ed2cfc2d3947_1282x1031.png)](https://substackcdn.com/image/fetch/$s_!kzBo!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4a3bfb74-3493-4132-b21e-ed2cfc2d3947_1282x1031.png)

Impressive results. Could be better if they add a DFE tap.

* * *

[![](https://substackcdn.com/image/fetch/$s_!xFYp!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F876f022a-8d7e-490a-a709-801282a1ce43_856x347.png)](https://substackcdn.com/image/fetch/$s_!xFYp!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F876f022a-8d7e-490a-a709-801282a1ce43_856x347.png)

RLM calibration is what caught my eye.

[![](https://substackcdn.com/image/fetch/$s_!iXAX!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F80d32a6a-3d0a-4144-a1fb-80e82441a610_1345x981.png)](https://substackcdn.com/image/fetch/$s_!iXAX!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F80d32a6a-3d0a-4144-a1fb-80e82441a610_1345x981.png)

[![](https://substackcdn.com/image/fetch/$s_!mG_8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbab8cc44-dcd2-4f0f-a1ae-8ebcff5f0250_1291x276.png)](https://substackcdn.com/image/fetch/$s_!mG_8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbab8cc44-dcd2-4f0f-a1ae-8ebcff5f0250_1291x276.png)

[![](https://substackcdn.com/image/fetch/$s_!v9-O!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F39f4afef-d194-44f3-b59a-c965eb67ec93_1303x603.png)](https://substackcdn.com/image/fetch/$s_!v9-O!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F39f4afef-d194-44f3-b59a-c965eb67ec93_1303x603.png)

[![](https://substackcdn.com/image/fetch/$s_!TTZU!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa40fb0f9-323c-4bfd-b643-866e1a564477_1193x1044.png)](https://substackcdn.com/image/fetch/$s_!TTZU!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa40fb0f9-323c-4bfd-b643-866e1a564477_1193x1044.png)

This strategy almost reminds me of channel sounding. Very clever.

[![](https://substackcdn.com/image/fetch/$s_!RdTk!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa9ced67e-8af6-43da-be3f-a47fc793deaf_1208x1144.png)](https://substackcdn.com/image/fetch/$s_!RdTk!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa9ced67e-8af6-43da-be3f-a47fc793deaf_1208x1144.png)

Most wireless systems use Zaddoph-Chu sequences and autocorrelation. These Samsung guys use much simpler codes.

 **Absolutely massive improvement in RLM.**

Very impressed by this. 

* * *

[![](https://substackcdn.com/image/fetch/$s_!dgot!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9a376848-6a1e-4112-8032-6e548a32b1eb_660x403.png)](https://substackcdn.com/image/fetch/$s_!dgot!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9a376848-6a1e-4112-8032-6e548a32b1eb_660x403.png)

Speaking of channel sounding…

[![](https://substackcdn.com/image/fetch/$s_!JdrT!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd7046813-fe8f-4dcf-8dbd-c9fa082a1751_1863x700.png)](https://substackcdn.com/image/fetch/$s_!JdrT!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd7046813-fe8f-4dcf-8dbd-c9fa082a1751_1863x700.png)

Surprising how nasty hollow-core fiber impulse response is. Good thing Nokia people spent the time to properly characterize.

* * *

[![](https://substackcdn.com/image/fetch/$s_!NjDO!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faef0c3a2-8089-4a33-b164-45b91fec9e94_853x316.png)](https://substackcdn.com/image/fetch/$s_!NjDO!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faef0c3a2-8089-4a33-b164-45b91fec9e94_853x316.png)

[![](https://substackcdn.com/image/fetch/$s_!nL_G!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1bbd603f-d482-4347-b7a3-9844db13b761_1284x764.png)](https://substackcdn.com/image/fetch/$s_!nL_G!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1bbd603f-d482-4347-b7a3-9844db13b761_1284x764.png)

This is IMEC, not TSMC, process node.

[![](https://substackcdn.com/image/fetch/$s_!JVpw!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8893cb6e-a8a3-49bc-aba3-093abfb0b097_1830x1369.png)](https://substackcdn.com/image/fetch/$s_!JVpw!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8893cb6e-a8a3-49bc-aba3-093abfb0b097_1830x1369.png)

Good matching between simulation and measurement. Marginal pass on TDECQ for 224G.

[![](https://substackcdn.com/image/fetch/$s_!APV1!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7a3816f6-607a-4c2c-9258-cea2b18f1daa_1159x971.png)](https://substackcdn.com/image/fetch/$s_!APV1!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7a3816f6-607a-4c2c-9258-cea2b18f1daa_1159x971.png)

Weird how much worse the 224G result is compared to the 200G result. 

Taking another look…

[![](https://substackcdn.com/image/fetch/$s_!epPX!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F72985950-fa37-4251-abbf-36320eb31edc_749x679.png)](https://substackcdn.com/image/fetch/$s_!epPX!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F72985950-fa37-4251-abbf-36320eb31edc_749x679.png)

The test setup is completely different. All that nasty noise in the 224G eye is probably coming from the discrete 11 dB electronic amplifier.

They did not disclose the model numbers for the 11dB or 22 dB electronic amplifiers. My guess is that 11 dB amp is either lower quality or was over-saturated.

* * *

[![](https://substackcdn.com/image/fetch/$s_!vT3n!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa88db605-5b95-45cf-a2b7-0449bcf7c6ea_649x357.png)](https://substackcdn.com/image/fetch/$s_!vT3n!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa88db605-5b95-45cf-a2b7-0449bcf7c6ea_649x357.png)

Avoiding PM fiber for ELS is great. Suffering 1.9 dB of loss to achieve this is unacceptable.

Very cool but quite useless. Solution looking for a problem.

[![](https://substackcdn.com/image/fetch/$s_!w-gt!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faaf13aee-0340-4692-8855-aebbcb0a8574_1311x937.png)](https://substackcdn.com/image/fetch/$s_!w-gt!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faaf13aee-0340-4692-8855-aebbcb0a8574_1311x937.png)

[![](https://substackcdn.com/image/fetch/$s_!kGeq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1270c80e-f8d4-4a31-a44b-b6956dca2957_1876x555.png)](https://substackcdn.com/image/fetch/$s_!kGeq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1270c80e-f8d4-4a31-a44b-b6956dca2957_1876x555.png)

The loss is still way too high. Just co-locate the damn ELS and have a short run of PMF. 

[![Cat On Chair GIFs | Tenor](https://substackcdn.com/image/fetch/$s_!WOfj!,w_1456,c_limit,f_auto,q_auto:good,fl_lossy/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3b9d07a1-0999-4b7c-9a16-078d7dba0d05_220x220.gif)](https://substackcdn.com/image/fetch/$s_!WOfj!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3b9d07a1-0999-4b7c-9a16-078d7dba0d05_220x220.gif)

* * *

[![](https://substackcdn.com/image/fetch/$s_!Zn2m!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F73a87f93-6995-4b94-8e01-95326bb5e56d_682x307.png)](https://substackcdn.com/image/fetch/$s_!Zn2m!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F73a87f93-6995-4b94-8e01-95326bb5e56d_682x307.png)

1.5 dB is not great TBH. You can get ~1 dB loss with a well-designed 2-lense system on an optical bench.

But obviously cost of active alignments very high.

[![](https://substackcdn.com/image/fetch/$s_!dgRr!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2a92df8c-b40c-4e03-af43-12666b4940b7_1836x718.png)](https://substackcdn.com/image/fetch/$s_!dgRr!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2a92df8c-b40c-4e03-af43-12666b4940b7_1836x718.png)

[![](https://substackcdn.com/image/fetch/$s_!ySoP!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd0b7ac72-52c3-491a-b880-f02564f6b5c3_1832x848.png)](https://substackcdn.com/image/fetch/$s_!ySoP!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd0b7ac72-52c3-491a-b880-f02564f6b5c3_1832x848.png)

So your specialty, unproven/exotic process is meaningfully (more than 0.5 dB) worse than lensed fiber.

* * *

[![](https://substackcdn.com/image/fetch/$s_!AhQP!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fac79d697-ed03-42ed-afaf-123b074352c9_807x339.png)](https://substackcdn.com/image/fetch/$s_!AhQP!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fac79d697-ed03-42ed-afaf-123b074352c9_807x339.png)

[![](https://substackcdn.com/image/fetch/$s_!3oHl!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcd9afdbc-c4dc-4d51-b305-84c14437cbef_1278x578.png)](https://substackcdn.com/image/fetch/$s_!3oHl!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcd9afdbc-c4dc-4d51-b305-84c14437cbef_1278x578.png)

A FFE, LMS block, and even a LUT for calibrating ADC interleaves. 

Looks expensive in terms of power and area.

[![](https://substackcdn.com/image/fetch/$s_!5Ls5!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F969aa185-b34a-45d5-ae7d-ee2ec1fd5b95_1852x642.png)](https://substackcdn.com/image/fetch/$s_!5Ls5!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F969aa185-b34a-45d5-ae7d-ee2ec1fd5b95_1852x642.png)

Decent performance gains, but at what cost?

[![](https://substackcdn.com/image/fetch/$s_!ExXB!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F20b833f5-d87d-45be-bcc1-9989f3b87356_1338x1208.png)](https://substackcdn.com/image/fetch/$s_!ExXB!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F20b833f5-d87d-45be-bcc1-9989f3b87356_1338x1208.png)

110-tap FIR per ADC interleave.

[![Risitas GIFs | Tenor](https://substackcdn.com/image/fetch/$s_!4tyC!,w_1456,c_limit,f_auto,q_auto:good,fl_lossy/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe2068782-0163-4b97-ae1a-e78727cfc2c8_220x165.gif)](https://substackcdn.com/image/fetch/$s_!4tyC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe2068782-0163-4b97-ae1a-e78727cfc2c8_220x165.gif)

* * *

[![](https://substackcdn.com/image/fetch/$s_!CjSw!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd64ded45-005a-4f2b-ab57-9ee8f4178fd3_646x505.png)](https://substackcdn.com/image/fetch/$s_!CjSw!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd64ded45-005a-4f2b-ab57-9ee8f4178fd3_646x505.png)

[![](https://substackcdn.com/image/fetch/$s_!rlnc!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff6ee231e-9784-481a-8f48-d00ed9df80f3_1873x809.png)](https://substackcdn.com/image/fetch/$s_!rlnc!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff6ee231e-9784-481a-8f48-d00ed9df80f3_1873x809.png)

Ge PDs are usually built with thin film epi. This paper shows an unusual deep-recess process.

[![](https://substackcdn.com/image/fetch/$s_!QQdz!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fef671b06-a211-4479-99f2-08d20c799cc4_1692x1003.png)](https://substackcdn.com/image/fetch/$s_!QQdz!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fef671b06-a211-4479-99f2-08d20c799cc4_1692x1003.png)

Exceptional bandwidth at very low voltage.

[![](https://substackcdn.com/image/fetch/$s_!SemF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F88d93aa7-4c55-44bf-8930-891603c4146c_1933x980.png)](https://substackcdn.com/image/fetch/$s_!SemF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F88d93aa7-4c55-44bf-8930-891603c4146c_1933x980.png)

Exceptional dark-current performance as well.

* * *

[![](https://substackcdn.com/image/fetch/$s_!EscF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6718038f-34ad-49c8-92ff-f4086340f334_687x305.png)](https://substackcdn.com/image/fetch/$s_!EscF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6718038f-34ad-49c8-92ff-f4086340f334_687x305.png)

Downconversion with zero tuning? Tell me more.

[![](https://substackcdn.com/image/fetch/$s_!JUS2!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F39218c96-bb0c-4bd3-907e-44c258a19188_769x517.png)](https://substackcdn.com/image/fetch/$s_!JUS2!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F39218c96-bb0c-4bd3-907e-44c258a19188_769x517.png)

[![](https://substackcdn.com/image/fetch/$s_!uSI3!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc90fd516-f9b8-478a-8d40-675b26d15a99_1864x872.png)](https://substackcdn.com/image/fetch/$s_!uSI3!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc90fd516-f9b8-478a-8d40-675b26d15a99_1864x872.png)

[![](https://substackcdn.com/image/fetch/$s_!v3RP!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F150fc74f-6d4d-427e-916d-a5b47a471391_1383x919.png)](https://substackcdn.com/image/fetch/$s_!v3RP!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F150fc74f-6d4d-427e-916d-a5b47a471391_1383x919.png)

[![](https://substackcdn.com/image/fetch/$s_!D2sb!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4de8f697-8349-48be-bd3f-1f5dbc89d40c_1248x836.png)](https://substackcdn.com/image/fetch/$s_!D2sb!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4de8f697-8349-48be-bd3f-1f5dbc89d40c_1248x836.png)

Interesting way of creating a frequency comb. Not clear how they calibrate the spacing.

[![](https://substackcdn.com/image/fetch/$s_!Njbm!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fca805289-f1a8-424e-99d6-a38034406eec_1816x847.png)](https://substackcdn.com/image/fetch/$s_!Njbm!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fca805289-f1a8-424e-99d6-a38034406eec_1816x847.png)

SNR of 28.1 dB on QAM64 is exceptional.

(they are using a 201-tap FFE so it better be good lmao)

* * *

[![](https://substackcdn.com/image/fetch/$s_!2kQh!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3fabb571-a386-441f-8e85-948023854566_776x400.png)](https://substackcdn.com/image/fetch/$s_!2kQh!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3fabb571-a386-441f-8e85-948023854566_776x400.png)

[![](https://substackcdn.com/image/fetch/$s_!gT8a!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3c2c985e-34c0-4837-a91b-42e99f595eb9_1406x957.png)](https://substackcdn.com/image/fetch/$s_!gT8a!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3c2c985e-34c0-4837-a91b-42e99f595eb9_1406x957.png)

QD comb lasers are neat but yield, power per line, and SMSR are big issues. How are you filtering?

[![](https://substackcdn.com/image/fetch/$s_!JEKr!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F489baab0-b49e-4a49-95d8-fa791dd9b135_1285x342.png)](https://substackcdn.com/image/fetch/$s_!JEKr!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F489baab0-b49e-4a49-95d8-fa791dd9b135_1285x342.png)

Aha bandpass external filter. So you have no plan for the nasty QD comb laser sidemodes.

[![](https://substackcdn.com/image/fetch/$s_!fGFS!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F15c8b59f-2515-48c6-9f8f-2579304ad3bf_1332x963.png)](https://substackcdn.com/image/fetch/$s_!fGFS!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F15c8b59f-2515-48c6-9f8f-2579304ad3bf_1332x963.png)

(individual channels one at a time… no crosstalk, no SMSR impact… )

* * *

[![](https://substackcdn.com/image/fetch/$s_!_HaA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbd488ee9-c552-44d5-b1df-a2f63c2d431c_836x276.png)](https://substackcdn.com/image/fetch/$s_!_HaA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbd488ee9-c552-44d5-b1df-a2f63c2d431c_836x276.png)

400G linear drive? Fancy CTLE? Interesting…

[![](https://substackcdn.com/image/fetch/$s_!6o1A!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F36f5474d-ce49-42f6-82c3-ae4bcd34c038_1315x446.png)](https://substackcdn.com/image/fetch/$s_!6o1A!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F36f5474d-ce49-42f6-82c3-ae4bcd34c038_1315x446.png)

[![](https://substackcdn.com/image/fetch/$s_!XvHe!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F206bbdfc-2af3-45de-929f-cb6d38c7b5de_1879x516.png)](https://substackcdn.com/image/fetch/$s_!XvHe!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F206bbdfc-2af3-45de-929f-cb6d38c7b5de_1879x516.png)

Very low Vpi. Excellent.

[![](https://substackcdn.com/image/fetch/$s_!9SiW!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F077f17b5-bc47-4e36-9a59-850d26ec10af_1291x791.png)](https://substackcdn.com/image/fetch/$s_!9SiW!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F077f17b5-bc47-4e36-9a59-850d26ec10af_1291x791.png)

Amazing results. 

[![](https://substackcdn.com/image/fetch/$s_!RnUm!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbabede59-cedb-40f7-ba1f-5c4ce9470cde_1333x635.png)](https://substackcdn.com/image/fetch/$s_!RnUm!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbabede59-cedb-40f7-ba1f-5c4ce9470cde_1333x635.png)

How the fuck did they get 9 dB of gain at 100+ GHz from a CTLE. What black magic is this?

[![](https://substackcdn.com/image/fetch/$s_!pmCR!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcc51a968-815e-49ec-a41c-8b4c91cc4c4c_1298x759.png)](https://substackcdn.com/image/fetch/$s_!pmCR!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcc51a968-815e-49ec-a41c-8b4c91cc4c4c_1298x759.png)

Oh this is just a simulation.

Well it’s neat that they are arguing for a CTLE at the Tx. This is very unusual and their simulations and logic make sense.

Great stuff really enjoyed this one.

* * *

[![](https://substackcdn.com/image/fetch/$s_!UH1J!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe96c48f8-1479-4062-8c37-de20459e18a5_718x300.png)](https://substackcdn.com/image/fetch/$s_!UH1J!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe96c48f8-1479-4062-8c37-de20459e18a5_718x300.png)

[![](https://substackcdn.com/image/fetch/$s_!TP9u!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F75071368-20ae-4b1b-921c-08b04beb35ba_1303x531.png)](https://substackcdn.com/image/fetch/$s_!TP9u!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F75071368-20ae-4b1b-921c-08b04beb35ba_1303x531.png)

Testing one channel at a time (bad) but at least they added gaussian noise to the other channels. In the real-world, there will be some correlated noise across channels but this is a reasonable compromise. Otherwise, testing this would be extraordinarily expensive.

[![](https://substackcdn.com/image/fetch/$s_!avT3!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Feb45d525-59b3-4d64-b8e4-1632b75bd2e1_1306x666.png)](https://substackcdn.com/image/fetch/$s_!avT3!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Feb45d525-59b3-4d64-b8e4-1632b75bd2e1_1306x666.png)

Thats a lot of cable lol.

[![](https://substackcdn.com/image/fetch/$s_!4jHH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Feea85bad-179a-4305-b4b5-ba31252315f4_1283x490.png)](https://substackcdn.com/image/fetch/$s_!4jHH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Feea85bad-179a-4305-b4b5-ba31252315f4_1283x490.png)

2.8 watt launch power per channel. Welp, yea this is undersea long-haul. Not sure what I was expecting.

* * *

[![](https://substackcdn.com/image/fetch/$s_!mbaz!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F75d4ae62-32ef-44fc-a11e-b63e60fba1fc_806x336.png)](https://substackcdn.com/image/fetch/$s_!mbaz!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F75d4ae62-32ef-44fc-a11e-b63e60fba1fc_806x336.png)

2 dB loss is a lot, but if this strategy massively reduces manufacturing/assembly cost, then it might be worth it.

[![](https://substackcdn.com/image/fetch/$s_!shha!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F94676123-c26d-495e-845c-28654d09572a_1304x1092.png)](https://substackcdn.com/image/fetch/$s_!shha!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F94676123-c26d-495e-845c-28654d09572a_1304x1092.png)

[![](https://substackcdn.com/image/fetch/$s_!hC-W!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff1941404-4af2-46eb-8f97-98ab86c6843a_1299x1121.png)](https://substackcdn.com/image/fetch/$s_!hC-W!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff1941404-4af2-46eb-8f97-98ab86c6843a_1299x1121.png)

[![](https://substackcdn.com/image/fetch/$s_!rBXJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F73ee8bc2-b912-4687-aec5-740d930f3fa0_1307x1185.png)](https://substackcdn.com/image/fetch/$s_!rBXJ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F73ee8bc2-b912-4687-aec5-740d930f3fa0_1307x1185.png)

Oh lol the loss is much worse. 2 dB is the best case scenario. 

Also the impedance variation across electrical bumps is… unacceptably high.

Very cool but far from being economically viable.

* * *

[![](https://substackcdn.com/image/fetch/$s_!35EY!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd74592de-9058-4c25-94e2-5ca062fda978_781x257.png)](https://substackcdn.com/image/fetch/$s_!35EY!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd74592de-9058-4c25-94e2-5ca062fda978_781x257.png)

2.4 dB insertion loss is indeed quite low. Normally MZI insertion loss is 5 dB ish. 

Then again, normal MZI modulators are 1000-2500 micron in length.

[![](https://substackcdn.com/image/fetch/$s_!tMTt!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F086fe154-f585-45c2-b780-0f661914ee6a_1870x1092.png)](https://substackcdn.com/image/fetch/$s_!tMTt!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F086fe154-f585-45c2-b780-0f661914ee6a_1870x1092.png)

Pretty good. Glad they showed waver-level data.

[![](https://substackcdn.com/image/fetch/$s_!gVfo!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb99378ae-2bbb-4f1a-b5c2-2b0010d74b2b_1282x937.png)](https://substackcdn.com/image/fetch/$s_!gVfo!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb99378ae-2bbb-4f1a-b5c2-2b0010d74b2b_1282x937.png)

Exceptional results. 

I have no clue how they achieved such good results. If anyone who knows physics things can explain, please send me an email.

[![](https://substackcdn.com/image/fetch/$s_!o9cY!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3b82f894-a548-4c22-b79d-4d4cfd591a0c_1308x650.png)](https://substackcdn.com/image/fetch/$s_!o9cY!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3b82f894-a548-4c22-b79d-4d4cfd591a0c_1308x650.png)

[![](https://substackcdn.com/image/fetch/$s_!RVF_!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3e29d18f-f326-4468-8f07-30553ab88405_1309x999.png)](https://substackcdn.com/image/fetch/$s_!RVF_!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3e29d18f-f326-4468-8f07-30553ab88405_1309x999.png)

* * *

[![](https://substackcdn.com/image/fetch/$s_!AADa!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9ac8fa6f-6188-4db2-8354-a65075de2964_716x237.png)](https://substackcdn.com/image/fetch/$s_!AADa!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9ac8fa6f-6188-4db2-8354-a65075de2964_716x237.png)

[![](https://substackcdn.com/image/fetch/$s_!ha26!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F03d8a4a6-976f-40b2-9357-b709ff83216e_1304x895.png)](https://substackcdn.com/image/fetch/$s_!ha26!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F03d8a4a6-976f-40b2-9357-b709ff83216e_1304x895.png)

Inverse design is a computational method that uses simulations to work backwards. It typically leads to weird shapes. 

The problem with inverse designs is they often violate PDK DRC, violently.

[![](https://substackcdn.com/image/fetch/$s_!Inip!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbb517cbc-806d-44ce-9d5e-387567c6813a_1297x241.png)](https://substackcdn.com/image/fetch/$s_!Inip!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbb517cbc-806d-44ce-9d5e-387567c6813a_1297x241.png)

I am 95% confident the “commercial CMOS foundry” that fabed these weird inverse-designed rings is NOT TSMC. 

Don’t get me wrong, inverse design is very cool and sometimes it even works in commercial applications, but more often then not the weird shapes aggressively violate design rules, leading to the foundry saying “no we absolutely will not accept this GDS go away.”

* * *

[![](https://substackcdn.com/image/fetch/$s_!OV9m!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F67269b78-c815-476d-a6df-cf693f322c8d_824x351.png)](https://substackcdn.com/image/fetch/$s_!OV9m!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F67269b78-c815-476d-a6df-cf693f322c8d_824x351.png)

Locking rings at < 100 GHz channel spacing is incredibly difficult. 

[![](https://substackcdn.com/image/fetch/$s_!hqbq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffe3bffce-361c-42c9-9669-e3e8a09abf0b_1301x1139.png)](https://substackcdn.com/image/fetch/$s_!hqbq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffe3bffce-361c-42c9-9669-e3e8a09abf0b_1301x1139.png)

Here is the normal locking method. (baseline)

[![](https://substackcdn.com/image/fetch/$s_!068q!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F30b8e18d-9a0a-4b2f-bfb4-78d7645d79a2_1854x768.png)](https://substackcdn.com/image/fetch/$s_!068q!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F30b8e18d-9a0a-4b2f-bfb4-78d7645d79a2_1854x768.png)

And here is the fancy derivative sum method.

[![](https://substackcdn.com/image/fetch/$s_!4W_L!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd3677fab-14fa-4683-b406-55f963e7ae2f_1874x665.png)](https://substackcdn.com/image/fetch/$s_!4W_L!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd3677fab-14fa-4683-b406-55f963e7ae2f_1874x665.png)

Massive improvement!

* * *

[![](https://substackcdn.com/image/fetch/$s_!oXxc!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7282ffaf-1e5a-493a-a004-2954a23cb156_820x281.png)](https://substackcdn.com/image/fetch/$s_!oXxc!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7282ffaf-1e5a-493a-a004-2954a23cb156_820x281.png)

Hmmm AMD CWDM mux with MMI. Interesting…

Why would you need this mux if you are using Ayar Labs rings? Is this the backup plan?

[![](https://substackcdn.com/image/fetch/$s_!MkdC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0db69539-56d7-4f06-a27a-f9b6b096225c_1341x799.png)](https://substackcdn.com/image/fetch/$s_!MkdC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0db69539-56d7-4f06-a27a-f9b6b096225c_1341x799.png)

This diagram screams “massive insertion loss” but ok lets wait.

[![](https://substackcdn.com/image/fetch/$s_!uozr!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0def6593-0461-4191-a467-a4fdf7d0b31a_1284x1260.png)](https://substackcdn.com/image/fetch/$s_!uozr!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0def6593-0461-4191-a467-a4fdf7d0b31a_1284x1260.png)

Guys where is the insertion loss. Sure you got good rejection of unwanted bands but come on you cant leave IL out.

[![](https://substackcdn.com/image/fetch/$s_!NckH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd7e07e06-b0ed-4fec-b668-b7f3eff68cea_1291x996.png)](https://substackcdn.com/image/fetch/$s_!NckH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd7e07e06-b0ed-4fec-b668-b7f3eff68cea_1291x996.png)

Honestly not bad. Way better than I expected.

Dare I say… 5 dB insertion loss of the entire system is pretty good.

* * *

[![](https://substackcdn.com/image/fetch/$s_!zHIQ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5088a576-ad33-456a-b047-9906be11d586_804x316.png)](https://substackcdn.com/image/fetch/$s_!zHIQ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5088a576-ad33-456a-b047-9906be11d586_804x316.png)

[![](https://substackcdn.com/image/fetch/$s_!-sPM!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F79a992ba-f96f-4095-a540-7ebf26139765_1284x606.png)](https://substackcdn.com/image/fetch/$s_!-sPM!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F79a992ba-f96f-4095-a540-7ebf26139765_1284x606.png)

[![](https://substackcdn.com/image/fetch/$s_!sDuo!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6a3f6d47-d5ac-4840-b136-f02636af2ff2_1292x989.png)](https://substackcdn.com/image/fetch/$s_!sDuo!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6a3f6d47-d5ac-4840-b136-f02636af2ff2_1292x989.png)

[![](https://substackcdn.com/image/fetch/$s_!vqT9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fef22256e-40df-4176-99e3-9113d0ea75cf_1286x346.png)](https://substackcdn.com/image/fetch/$s_!vqT9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fef22256e-40df-4176-99e3-9113d0ea75cf_1286x346.png)

“Standard” 40 KHz linewidth laser lol.

[![](https://substackcdn.com/image/fetch/$s_!drfD!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd016923b-8513-425c-ac1d-a9693c449957_1288x851.png)](https://substackcdn.com/image/fetch/$s_!drfD!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd016923b-8513-425c-ac1d-a9693c449957_1288x851.png)

“standard digital signal processing”

» 601-tap FFE

[![Risitas GIFs | Tenor](https://substackcdn.com/image/fetch/$s_!_ZnS!,w_1456,c_limit,f_auto,q_auto:good,fl_lossy/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6712892b-3599-4940-9ca9-7ae2ea602398_220x220.gif)](https://substackcdn.com/image/fetch/$s_!_ZnS!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6712892b-3599-4940-9ca9-7ae2ea602398_220x220.gif)

## [3] Public Markets: Re[tail]-Tard and Pod Monkey Summary

Are you so brain-damaged you need a color-coded chart with simple words to make investment decisions?

This section is for you.

[![](https://substackcdn.com/image/fetch/$s_!M1bv!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F19c567f1-4e87-44b4-ad6f-b91226a36415_1058x805.png)](https://substackcdn.com/image/fetch/$s_!M1bv!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F19c567f1-4e87-44b4-ad6f-b91226a36415_1058x805.png)

## [4] Trading Account 3/27/2026 Snapshot

I will be publishing full trading record (all transactions, monthly account statements) for Q1 2026 next week. Will also re-build my shit manually updated spreadsheet that consolidates the long-only accounts.

 ~~Are you having fun with the increased levels of KABOOM in the middle east yet?~~

[![smug but crying inside wojak mask meme Art Print](https://substackcdn.com/image/fetch/$s_!DsyG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7a5e8493-5738-4376-8f05-64f2c6d4f2e7_360x360.jpeg)](https://substackcdn.com/image/fetch/$s_!DsyG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7a5e8493-5738-4376-8f05-64f2c6d4f2e7_360x360.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!NQJa!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff24d31dd-94be-4a81-93bd-1c2da3751f28_1510x894.png)](https://substackcdn.com/image/fetch/$s_!NQJa!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff24d31dd-94be-4a81-93bd-1c2da3751f28_1510x894.png) One of the classic memes I found while searching for the “wojak committing double suicide”.

Check out my tourist overview of liquified natural gas.

Here is the trading account at the time of writing. 

[![](https://substackcdn.com/image/fetch/$s_!AKOp!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffbdce255-983e-4a76-9c68-0e6b3948e475_704x1041.webp)](https://substackcdn.com/image/fetch/$s_!AKOp!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffbdce255-983e-4a76-9c68-0e6b3948e475_704x1041.webp)

Barely meeting my performance target of +30% over SMH/benchmark.

[![](https://substackcdn.com/image/fetch/$s_!6MkN!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6f815820-1292-49eb-a409-1c749a4021e9_1305x1041.webp)](https://substackcdn.com/image/fetch/$s_!6MkN!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6f815820-1292-49eb-a409-1c749a4021e9_1305x1041.webp)

[![](https://substackcdn.com/image/fetch/$s_!uD-Y!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F361823dc-8ffc-469c-9202-a85ae4c14a0d_670x1041.webp)](https://substackcdn.com/image/fetch/$s_!uD-Y!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F361823dc-8ffc-469c-9202-a85ae4c14a0d_670x1041.webp)

[![](https://substackcdn.com/image/fetch/$s_!8Mdg!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F14548af3-0982-40ac-a8a4-b3dd07c6347a_1440x971.webp)](https://substackcdn.com/image/fetch/$s_!8Mdg!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F14548af3-0982-40ac-a8a4-b3dd07c6347a_1440x971.webp)

Subscribe for engineering-driven investment analysis.

Subscribe

Share?

[Share](https://irrationalanalysis.substack.com/p/ofc-2026-irrational-recap?utm_source=substack&utm_medium=email&utm_content=share&action=share)
