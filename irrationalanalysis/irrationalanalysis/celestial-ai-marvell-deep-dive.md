# Celestial AI // Marvell Deep Dive

## Fascinating situation.

**Dec 07, 2025**

**Likes:** 0

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice, and readers should **always do their own research before investing in any security.**

  * Feel free to contact me via email at: _irrational_analysis@proton.me_




* * *

For a while, I have been making fun of Marvell as “co-packed optics losers”.

This is one of my favorite artworks.

[![](https://substackcdn.com/image/fetch/$s_!QFvJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe4ca3fd4-c30c-4a72-83de-7d5449f1adaf_812x579.png)](https://substackcdn.com/image/fetch/$s_!QFvJ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe4ca3fd4-c30c-4a72-83de-7d5449f1adaf_812x579.png)“Co-Packed Optics Losers” — Original Artwork

That has been true for most of this year, until they bought Celestial AI.

Everything they already had (DR-MZI based light engines) is getting thrown out in favor of Celestial AI germanium EAM tech stack.

Matt Murphy really does have an ace up his sleeve now. 

But with any gamble, there is considerable risk.

This situation is truly fascinating. Only extreme outcomes are possible.

Lets get started!

# Contents:

  1. The Lame (Normal) Investor-Relations Overview

  2. What if I told you Celestial AI is either Inphi/Mellanox or a zero?

  3. Thermal Stability == Shitting on Rings

    1. Celestial is Right, but also Wrong

    2. How Ring Modulators Work: TSMC COUPE Paper Walkthrough

    3. Thermal [CROSSTALK] Stability is Solvable, but Very Difficult

  4. Germanium EAM: The Core of Celestial Technology Stack

    1. Electro-Absorption Modulator Crash Course

    2. Rockley Photonics Patent Rabbit-Hole

  5. Do you notice something…? 

  6. Detour: Germanium Photodiode

  7. Detour: Public Germanium EAM Research

  8. Bullshit Detector Calibration (for financial analysts)




* * *

## [1] The Lame (Normal) Investor-Relations Overview

Marvell has a slide deck on the Celestial AI deal. It is mostly useless so let me quickly cover it.

[![](https://substackcdn.com/image/fetch/$s_!BiPL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F520751c0-b4d9-4fcc-b54f-5169a28afc83_1408x784.png)](https://substackcdn.com/image/fetch/$s_!BiPL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F520751c0-b4d9-4fcc-b54f-5169a28afc83_1408x784.png)

How many McKinsey consultants did you pay to make this useless slide?

[![](https://substackcdn.com/image/fetch/$s_!oyY_!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1ca7d21c-e80e-452c-8de8-a8df3ebf5077_1369x779.png)](https://substackcdn.com/image/fetch/$s_!oyY_!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1ca7d21c-e80e-452c-8de8-a8df3ebf5077_1369x779.png)

There is an earnout clause that depends on Celestial AI delivering a minimum of $500M of revenue in Calander year 2028.

Very telling. It is effectively an admission that meaningful revenue in CY 2026 and 2027 is unlikely.

Kinda expected given GR-468 reliability qualification timelines.

Amazon also got more warrants at $87/share. Because of course they got more warrants.

## [2] What if I told you Celestial AI is either Inphi/Mellanox or a zero?

In 2019, Nvidia acquired Mellanox. Nvidia’s dominance in high-end networking stems in large part from this legendary deal.

In 2020, Marvell acquired Inphi. Another legendary/transformative deal.

[![](https://substackcdn.com/image/fetch/$s_!eHY0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F89a1673d-4d86-4aad-8d51-7264d3c81596_573x247.png)](https://substackcdn.com/image/fetch/$s_!eHY0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F89a1673d-4d86-4aad-8d51-7264d3c81596_573x247.png)

He is right. Celestial AI easily has more potential than Inphi deal back in 2020.

Or… it could be a zero.

* * *

There are only two possible outcomes:

  1. Celestial AI smashes the revenue guidance provided by Marvell, transforms the company, and has the same strategic impact as Mellanox+Inphi deals simultaneously.

  2. Catastrophic failure. Zero revenue.




## [3] Thermal Stability == Shitting on Rings

Throughout many Celestial AI and Marvell personations, you will see the phrase “thermal stability”.

This key phrase is basically taking shots at ring modulator technology.

[![](https://substackcdn.com/image/fetch/$s_!dLS4!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffecc12e1-bfe9-46a1-9763-66dac4699cd9_534x532.png)](https://substackcdn.com/image/fetch/$s_!dLS4!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffecc12e1-bfe9-46a1-9763-66dac4699cd9_534x532.png)

There are three companies who have publicly talked about ring modulator tech. Only Nvidia is going to ship high-volume transceivers and CPO switches next year using rings.

There are at least two large-cap and three mega-cap publicly traded companies who are seriously evaluating ring modulators on TSMC COUPE and will have something within the next 2 years.

Not going to give you these four names as I will get in trouble.

### [3.a] Celestial is Right, but also Wrong

Celestial has a slide they like to show from time to time.

I have made some subtle edits and corrections.

[![](https://substackcdn.com/image/fetch/$s_!ykDz!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F37da340b-988d-4136-836f-f6a7e616e9a2_811x661.png)](https://substackcdn.com/image/fetch/$s_!ykDz!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F37da340b-988d-4136-836f-f6a7e616e9a2_811x661.png)

Amusingly, Celestial is right that ring modulators are thermally unstable. And yet, they have completely failed to explain WHY this is the case.

If you know why rings are unstable, you can figure out if this is a solvable problem or not.

Spoiler… this problem is solvable but very difficult. Only Nvidia has demonstrated success by ramping up huge ring-based transceiver and CPO switch volume next year.

### [3.b] How Ring Modulators Work: TSMC COUPE Paper Walkthrough

Here is an amazing TSMC paper on COUPE silicon photonics.

First, a full re-publishing of the paper because IEEE paywall can fuck off. 

[![](https://substackcdn.com/image/fetch/$s_!yNe6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5c7589ea-cc43-4d56-9109-9c6677c3a97f_941x1205.png)](https://substackcdn.com/image/fetch/$s_!yNe6!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5c7589ea-cc43-4d56-9109-9c6677c3a97f_941x1205.png)

[![](https://substackcdn.com/image/fetch/$s_!poEd!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fed38d8f3-bbae-4cf5-a42d-358b78c12b08_923x1205.png)](https://substackcdn.com/image/fetch/$s_!poEd!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fed38d8f3-bbae-4cf5-a42d-358b78c12b08_923x1205.png)

[![](https://substackcdn.com/image/fetch/$s_!Hf1b!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3b31a2f5-5f4b-46f9-8e03-fd6fa6e70db0_958x1099.png)](https://substackcdn.com/image/fetch/$s_!Hf1b!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3b31a2f5-5f4b-46f9-8e03-fd6fa6e70db0_958x1099.png)

[![](https://substackcdn.com/image/fetch/$s_!YGMm!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8a2a8372-0596-4add-a524-ed56520bab8b_953x1153.png)](https://substackcdn.com/image/fetch/$s_!YGMm!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8a2a8372-0596-4add-a524-ed56520bab8b_953x1153.png)

Before explaining the paper, let’s go over some industry history.

Ring modulators have been an academic fantasy for quite a long time. On paper, there are massive benefits. 

In practice…

  * Designing and reliably manufacturing ring modulators **WAS** a nightmare.

  * Controlling hundreds of these thermally unstable things is a nightmare that only Nvidia has solved at economically viable scale.




For many years, various researchers and companies worked with silicon photonics foundries to develop customer process nodes to design their own rings.

Nvidia partnered with TSMC to jointly develop ring tech on the COUPE platform. Now, rings are just a fucking PDK element!

[![](https://substackcdn.com/image/fetch/$s_!XtRf!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1edc0f6a-7f88-4124-920f-4a7b7a9e7fc7_900x348.png)](https://substackcdn.com/image/fetch/$s_!XtRf!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1edc0f6a-7f88-4124-920f-4a7b7a9e7fc7_900x348.png)

And the nightmarish process variation? Solved.

[![](https://substackcdn.com/image/fetch/$s_!PIoV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F90b5f737-ea4d-4883-bc76-b17b69811291_1448x369.png)](https://substackcdn.com/image/fetch/$s_!PIoV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F90b5f737-ea4d-4883-bc76-b17b69811291_1448x369.png)

TSMC+Nvidia have solved most of the tricky things and made this tech available for anyone to use. 

It is a win-win for both.

Nvidia gets high-volume manufacturing and rapid supply-chain development. They also get a ~18-month head start over everyone else and can drive TSMC’s roadmap to suit Nvidia needs.

TSMC deepens their moat and poaches customers who have been struggling to get proprietary rings on GloFo derivative nodes working at scale.

### [3.c] Thermal [CROSSTALK] Stability is Solvable, but Very Difficult

This chart is all you need to understand why rings are thermally unstable.

[![](https://substackcdn.com/image/fetch/$s_!Iw-O!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffa8b161e-48da-426c-b012-6cb44d753002_436x385.png)](https://substackcdn.com/image/fetch/$s_!Iw-O!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffa8b161e-48da-426c-b012-6cb44d753002_436x385.png)

Let’s break it down.

Suppose we transmit an electrical signal where 0 volt is a logical “0” and -3.5 volt is a logical “1”.

Ring modulators are thermally tuned and very sensitive. 

If the ring is PERFECTLY thermally tuned, it will look like this:

[![](https://substackcdn.com/image/fetch/$s_!Jys8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F316a7e4a-d60c-4e46-9013-d176e6a82bd4_436x385.png)](https://substackcdn.com/image/fetch/$s_!Jys8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F316a7e4a-d60c-4e46-9013-d176e6a82bd4_436x385.png)

The optical difference between a logical “0” and “1” is 15 dB. This is a lot. Thus the receiver can easily figure out what the transmitter is sending.

Now, what if the ring is not at the correct thermal setpoint…?

[![](https://substackcdn.com/image/fetch/$s_!YEQW!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4fd5b6b6-6f96-4edf-96f2-ea9ba40d86e7_436x385.png)](https://substackcdn.com/image/fetch/$s_!YEQW!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4fd5b6b6-6f96-4edf-96f2-ea9ba40d86e7_436x385.png)

Now the difference is only 4 dB. Receiver is gona struggle to tell the difference between a 0 and a 1.

[![](https://substackcdn.com/image/fetch/$s_!QTmT!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F359b9dee-5155-4a03-bfd5-e10f11338c84_484x481.png)](https://substackcdn.com/image/fetch/$s_!QTmT!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F359b9dee-5155-4a03-bfd5-e10f11338c84_484x481.png)

  * Laser wavelength thermally drifts too!

  * Neighboring rings will dump thermal noise into each other.

  * Rings absorb some light and self-heat.

    * Now laser power fluctuations can also kill your system.




Honestly this is only the tip of the thermally-unstable iceberg.

 **Point is, Celestial is right. Rings are VERY thermally unstable.**

 **But their argument that rings are un-viable for scale-up CPO is completely wrong.**

Nvidia and many others are going to get DWDM rings working on TSMC COUPE + CoWoS-L within the next two years.

Remind me, when is the earnout clause triggered for Celestial revenue?

Oh ya…. 2028.

Race is on. 

(Nvidia is way ahead.)

## [4] Germanium EAM: The Core of Celestial Technology Stack

Celestial has a lot of interesting IP but everything revolves around germanium EAM. 

### [4.a] Electro-Absorption Modulator Crash Course

Electro-Absorption modulators use an electrical signal to absorb light. Simple!

[![](https://substackcdn.com/image/fetch/$s_!IMNU!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa7bdddfd-337c-4bfd-b4c4-4115cf9b2a6e_1696x1281.png)](https://substackcdn.com/image/fetch/$s_!IMNU!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa7bdddfd-337c-4bfd-b4c4-4115cf9b2a6e_1696x1281.png)

[![](https://substackcdn.com/image/fetch/$s_!cpA4!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F476bda2f-ce32-432e-88c1-8cf3554af72a_1686x1269.png)](https://substackcdn.com/image/fetch/$s_!cpA4!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F476bda2f-ce32-432e-88c1-8cf3554af72a_1686x1269.png)

EAM is very popular in traditional transceivers. When you hear EML, think a DFB Laser + EAM on same InP substrate.

[![](https://substackcdn.com/image/fetch/$s_!5xsE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F76189e70-d399-44a9-b270-f3fdc92f79c8_1677x1278.png)](https://substackcdn.com/image/fetch/$s_!5xsE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F76189e70-d399-44a9-b270-f3fdc92f79c8_1677x1278.png)

 **Celestial does not use traditional InP-based EAM.**

 **They use germanium based EAM.**

### [4.b] Rockley Photonics Patent Rabbit-Hole

[![](https://substackcdn.com/image/fetch/$s_!9l7F!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F373900da-d0dc-4e22-8630-f6c29efe6926_1413x345.png)](https://substackcdn.com/image/fetch/$s_!9l7F!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F373900da-d0dc-4e22-8630-f6c29efe6926_1413x345.png)

Back in October 2024, Celestial bough a patent portfolio from Rockley Photonics.

Around two years earlier, in January 2023, Rockley Photonics filed for chapter 11 bankruptcy.

[![](https://substackcdn.com/image/fetch/$s_!Hh8v!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe6a2ca06-e918-4a49-986b-0302e53efb19_653x495.png)](https://substackcdn.com/image/fetch/$s_!Hh8v!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe6a2ca06-e918-4a49-986b-0302e53efb19_653x495.png)

There is a very amusing side story related to this. Ask around.

Anyway, let’s take a look at two of these patents!

[https://patents.google.com/patent/US10838240B2 ](https://patents.google.com/patent/US10838240B2)

[![](https://substackcdn.com/image/fetch/$s_!s68D!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbe0efc68-b9a1-466a-b73f-cec338b2f388_382x593.png)](https://substackcdn.com/image/fetch/$s_!s68D!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbe0efc68-b9a1-466a-b73f-cec338b2f388_382x593.png)

[![](https://substackcdn.com/image/fetch/$s_!RBTI!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F26e6d28d-da0f-4bf5-8a3d-50407908420f_1616x847.png)](https://substackcdn.com/image/fetch/$s_!RBTI!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F26e6d28d-da0f-4bf5-8a3d-50407908420f_1616x847.png)

[![](https://substackcdn.com/image/fetch/$s_!WcVp!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6519c1de-ee4d-45ec-889b-483caf954945_961x871.png)](https://substackcdn.com/image/fetch/$s_!WcVp!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6519c1de-ee4d-45ec-889b-483caf954945_961x871.png)

<https://patents.google.com/patent/US10788688B2>

[![](https://substackcdn.com/image/fetch/$s_!6EoE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6eaa2a67-5d84-4aa1-a6e1-314eb579f1f2_1067x628.png)](https://substackcdn.com/image/fetch/$s_!6EoE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6eaa2a67-5d84-4aa1-a6e1-314eb579f1f2_1067x628.png)

[![](https://substackcdn.com/image/fetch/$s_!8KwV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F952d4fa8-c655-48d0-881b-01681c5b0450_1130x568.png)](https://substackcdn.com/image/fetch/$s_!8KwV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F952d4fa8-c655-48d0-881b-01681c5b0450_1130x568.png)

[![](https://substackcdn.com/image/fetch/$s_!IlJw!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2edfc7d5-c3a3-41e4-91ac-e92d3a609b20_920x889.png)](https://substackcdn.com/image/fetch/$s_!IlJw!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2edfc7d5-c3a3-41e4-91ac-e92d3a609b20_920x889.png)

SiGe (silicon-germanium) seems important. 

[![](https://substackcdn.com/image/fetch/$s_!PIeh!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1500068d-1a03-4b55-82d3-8ddd2bb30d4a_480x360.gif)](https://substackcdn.com/image/fetch/$s_!PIeh!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1500068d-1a03-4b55-82d3-8ddd2bb30d4a_480x360.gif)

## [5] Do you notice something…? 

If you look at all the public material (slides, presentations, press releases) Celestial and Marvell put out, you will find something missing.

[![](https://substackcdn.com/image/fetch/$s_!Lr1y!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F999d18cc-9ea8-4701-9960-553139b50c1e_811x655.png)](https://substackcdn.com/image/fetch/$s_!Lr1y!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F999d18cc-9ea8-4701-9960-553139b50c1e_811x655.png)

[![](https://substackcdn.com/image/fetch/$s_!AnZZ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff7b86e45-2a09-4f05-85e3-d999845d480b_790x644.png)](https://substackcdn.com/image/fetch/$s_!AnZZ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff7b86e45-2a09-4f05-85e3-d999845d480b_790x644.png)

[![](https://substackcdn.com/image/fetch/$s_!ZP0M!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F12d5b751-f1e3-4772-8e13-08aa2fd93301_647x805.png)](https://substackcdn.com/image/fetch/$s_!ZP0M!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F12d5b751-f1e3-4772-8e13-08aa2fd93301_647x805.png)

Not once have they mentioned the word “germanium”.

There is a reason why they are avoiding this word.

To understand why, we must embark on a quick detour.

## [6] Detour: Germanium Photodiode

Within silicon photonics, there is a component called a photodiode.

It is the inverse of an LED.

Light go in, electricity come out.

Photodiodes (PDs) are absolutely critical for two main functions:

  1. Converting light data signal back into data electrical signal so the SerDes can recover information.

  2. Monitoring what is going on in the SiPho chip to actively tune components.




A PD typically looks like this.

[![](https://substackcdn.com/image/fetch/$s_!ymel!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff91d363e-5f56-46ab-8e41-fa5be69aea3a_738x246.png)](https://substackcdn.com/image/fetch/$s_!ymel!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff91d363e-5f56-46ab-8e41-fa5be69aea3a_738x246.png)

As you can see, there is a layer of Ge on top of the Si. This is accomplished by a process known as epitaxial growth.

[![](https://substackcdn.com/image/fetch/$s_!kgR0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa92a0af3-3246-44b6-87f9-7146c3611e35_677x426.png)](https://substackcdn.com/image/fetch/$s_!kgR0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa92a0af3-3246-44b6-87f9-7146c3611e35_677x426.png)

In short, Ge and Si have different crystal structures. Getting the crystals to play nice with each other is challenging.

[![](https://substackcdn.com/image/fetch/$s_!trq_!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fae520752-68d8-4b2d-9db8-b089a5b5ea0a_665x812.png)](https://substackcdn.com/image/fetch/$s_!trq_!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fae520752-68d8-4b2d-9db8-b089a5b5ea0a_665x812.png)

[![](https://substackcdn.com/image/fetch/$s_!iiG7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9c121d77-942e-418a-8ef4-9eccef76c80d_977x550.webp)](https://substackcdn.com/image/fetch/$s_!iiG7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9c121d77-942e-418a-8ef4-9eccef76c80d_977x550.webp)

Because of chemistry and physics reasons, there is going to be stress between the two layers. Managing this stress is a yield and reliability problem.

Within GR-468, the industry-standard optical reliability standard, photodiodes get a lot of attention.

[![](https://substackcdn.com/image/fetch/$s_!_qrb!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff57eafbc-481f-4b85-a79c-640f24ca26fe_627x575.png)](https://substackcdn.com/image/fetch/$s_!_qrb!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff57eafbc-481f-4b85-a79c-640f24ca26fe_627x575.png)

[![](https://substackcdn.com/image/fetch/$s_!gmIF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9b374e28-c039-4e50-82b0-bb7c4699e512_703x819.png)](https://substackcdn.com/image/fetch/$s_!gmIF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9b374e28-c039-4e50-82b0-bb7c4699e512_703x819.png)

10000 hours = 417 days = 1.14 years

 **Reminder… the earnout clause is based on Celestial delivering $500M in revenue in CY 2028.**

## [7] Public Germanium EAM Research

Here is a 2022 paper from IMEC on the exact topic we are interested in.

<https://imec-publications.be/bitstreams/6d7ee36c-efdc-48e3-acef-35ea7ca7e58a/download>

[![](https://substackcdn.com/image/fetch/$s_!gZEH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F20836253-7080-4af2-ad9f-c93def592766_451x277.png)](https://substackcdn.com/image/fetch/$s_!gZEH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F20836253-7080-4af2-ad9f-c93def592766_451x277.png)

[![](https://substackcdn.com/image/fetch/$s_!W4ib!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe68061cf-25ae-4daa-a72b-056945a29cb2_452x322.png)](https://substackcdn.com/image/fetch/$s_!W4ib!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe68061cf-25ae-4daa-a72b-056945a29cb2_452x322.png)

[![](https://substackcdn.com/image/fetch/$s_!7REh!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F983e2823-82d8-4cf3-8775-bc5f0e50a6c6_455x139.png)](https://substackcdn.com/image/fetch/$s_!7REh!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F983e2823-82d8-4cf3-8775-bc5f0e50a6c6_455x139.png)

[![](https://substackcdn.com/image/fetch/$s_!u9NZ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F50c6f721-d90f-4d59-9009-274d731389b0_475x600.png)](https://substackcdn.com/image/fetch/$s_!u9NZ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F50c6f721-d90f-4d59-9009-274d731389b0_475x600.png)

[![](https://substackcdn.com/image/fetch/$s_!NK_7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffc9527a5-c333-485e-be50-b334cd1fc16f_460x676.png)](https://substackcdn.com/image/fetch/$s_!NK_7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffc9527a5-c333-485e-be50-b334cd1fc16f_460x676.png)

## [8] Bullshit Detector Calibration (for financial analysts)

Germanium EAM reliability/longevity and GR-468 qualification is the only real problem Celestial has yet to solve. 

The 2028 earnout coincidentally lines up with roughly how long it takes to complete reliability testing.

Friendly advice to help finance people calibrate your bullshit detectors.

* * *

 **Claim:** Germanium photodiodes are in all transceivers and SiPho. Nothing to see here.

 **Counterargument:** Germanium EAM is a fundamentally different structure that exhibits different failure modes.

* * *

If you want to sound dangerous, try weaving the following phrases into your question.

  * Lattice mismatch.

  * Dark current.

  * GR-468 qualification.

  * SNR and extinction ratio degradation.




Have fun!

[![](https://substackcdn.com/image/fetch/$s_!XGa8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F24f2ce08-b1b7-4628-adee-9c00d92a45ae_420x314.gif)](https://substackcdn.com/image/fetch/$s_!XGa8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F24f2ce08-b1b7-4628-adee-9c00d92a45ae_420x314.gif)

Subscribe for engineering-driven investment analysis.

Subscribe

Share?

[Share](https://irrationalanalysis.substack.com/p/celestial-ai-marvell-deep-dive?utm_source=substack&utm_medium=email&utm_content=share&action=share)
