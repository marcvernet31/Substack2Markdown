# OCP Global Summit 2025: Irrational Recap

## $TSEM $LITE $SNDK $BE $002281.SZ $AVGO $CIEN $300308.SZ $300502.SZ $MRVL $FN $COHR $AMD $TEL $KEYS $NVDA $ANET $CRDO $PSTG $ALAB

**Oct 24, 2025**

**Likes:** 0

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Please check the [‘about’ page](https://irrationalanalysis.substack.com/about) for a list of active positions.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice, and readers should **always do their own research before investing in any security.**

  * Feel free to contact me via email at: _irrational_analysis@proton.me_




* * *

Messa back with moar conference coverage.

[![](https://substackcdn.com/image/fetch/$s_!4Hlz!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc8d1aa2e-fe4e-48e7-87db-103321636868_536x831.png)](https://substackcdn.com/image/fetch/$s_!4Hlz!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc8d1aa2e-fe4e-48e7-87db-103321636868_536x831.png)

I will group most of the material by theme.

# Contents:

  1. Theme: Co-Packaged Optics

  2. Theme: 400G Electrical SerDes

  3. Theme: Optical Transceivers 

  4. Theme: Scale-Up Protocols, ESUN, and UALink Death

  5. Miscellaneous

    1. Marvell Alaska AEC

    2. Bloom Energy

    3. QLC Storage

    4. Cool Cable Length Measurment

    5. Multilane Test Equipment

    6. Interesting 3D Etched? Copper Coldplates

    7. Point2

    8. Elyian

  6. Funny Shit

  7. Public-Market Investment Corner

    1. Updated Disclosures and Holdings

    2. Opinion by Ticker




* * *

## [1] Theme: Co-Packaged Optics

CPO was huge at OCP. Easily 10+ dedicated talks just on this topic.

Quick high-level summary by company…

 **Broadcom**[AVGO 0.00%↑](https://substack.com/discover/stocks/AVGO) showed incredible data from reliability, performance, and power fronts. Really incredible stuff. They also showed interesting VCSEL based CPO.

 **Nvidia**[NVDA 0.00%↑](https://substack.com/discover/stocks/NVDA) did not show anything new. All material was already presented at GTC and Hot Chips earlier in the year. Complete waste of time. 

**Accelink** $002281.SZ hard a lot of nice presentations. Impressive ELSFP output power for CPO.

 **Marvell**[MRVL 0.00%↑](https://substack.com/discover/stocks/MRVL) showed literally zero data. Some nice block diagrams though.

 **Ciena** [CIEN 0.00%↑](https://substack.com/discover/stocks/CIEN) (Nubis recent acquisition) had an interesting take on DWDM that I strongly disagree with but respect.

 _* Note: Withholding coverage of micro-LED for an upcoming photonics post. I hate micro-LED with the fire of a thousand suns. Will explain later._

* * *

* * *

Many people within industry complain that CPO has worse reliability than transceivers. These people are idiots who have no idea what the hell they talking about. Broadcom showed excellent reliability data that should have put this debate to rest. Unfortunately, stupidity is often difficult to stamp out.

Case in point, this idiot who replied to one of my tweets.

[![](https://substackcdn.com/image/fetch/$s_!e_Pa!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc24a7e9e-55fa-4273-a6be-30be462102d7_593x730.png)](https://substackcdn.com/image/fetch/$s_!e_Pa!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc24a7e9e-55fa-4273-a6be-30be462102d7_593x730.png)

[![](https://substackcdn.com/image/fetch/$s_!ezR7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F307f9497-11d3-48ce-9574-ba75760a1f07_599x627.png)](https://substackcdn.com/image/fetch/$s_!ezR7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F307f9497-11d3-48ce-9574-ba75760a1f07_599x627.png)

[![](https://substackcdn.com/image/fetch/$s_!Ibm3!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F45c07c9b-f806-4062-a836-4904677a0aa3_1366x768.jpeg)](https://substackcdn.com/image/fetch/$s_!Ibm3!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F45c07c9b-f806-4062-a836-4904677a0aa3_1366x768.jpeg)

As a baseline, here are the most common failure modes for traditional pluggable transceivers.

[![](https://substackcdn.com/image/fetch/$s_!Y5yq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1bb8d561-3035-4925-b9fb-fd3fb6f874b8_1638x830.png)](https://substackcdn.com/image/fetch/$s_!Y5yq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1bb8d561-3035-4925-b9fb-fd3fb6f874b8_1638x830.png)

It’s the laser and wirebond/packaging that kills these things.

This is what wirebonds look like:

[![](https://substackcdn.com/image/fetch/$s_!e9Dp!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2bd48927-7417-498f-b3d1-8b6b37f73e72_1600x900.webp)](https://substackcdn.com/image/fetch/$s_!e9Dp!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2bd48927-7417-498f-b3d1-8b6b37f73e72_1600x900.webp)

[![](https://substackcdn.com/image/fetch/$s_!-oVU!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F331e4022-fb3c-4ee7-99a2-866c8e983c21_259x194.jpeg)](https://substackcdn.com/image/fetch/$s_!-oVU!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F331e4022-fb3c-4ee7-99a2-866c8e983c21_259x194.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!d4x_!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F45e2204b-8eb0-4548-9d5c-1ea8d07559d9_259x194.jpeg)](https://substackcdn.com/image/fetch/$s_!d4x_!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F45e2204b-8eb0-4548-9d5c-1ea8d07559d9_259x194.jpeg)

These things look fragile because they are.

 **CPO does not use any wirebonds. COUPE and RDL-based CPO methods are zero-wirebond.**

Next, let’s talk about PCB mounted component errors. 

In general, the most unreliable sub-components are Germanium-based photodiodes (ger-PD).

Think of ger-PDs as a necessary evil. Every optical system (transceiver, CPO, whatever) needs these things.

Germanium PDs are….

  1. Much higher failure rate than any other photonic structure.

  2. Very sensitive to ESD.

  3. Can degrade over time if you are stupid and botch basic design principals.




Here are examples of germanium PD in traditional transceivers…

[![](https://substackcdn.com/image/fetch/$s_!GQsh!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F172230b1-4c47-45bd-b2d3-3a0f8389df4f_723x441.png)](https://substackcdn.com/image/fetch/$s_!GQsh!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F172230b1-4c47-45bd-b2d3-3a0f8389df4f_723x441.png)

[![](https://substackcdn.com/image/fetch/$s_!fXot!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fad597a76-0be8-4b85-9ebc-bfe2f1e8c7a1_601x471.png)](https://substackcdn.com/image/fetch/$s_!fXot!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fad597a76-0be8-4b85-9ebc-bfe2f1e8c7a1_601x471.png)

In general, integrating all germanium PDs into a single SiPho chip greatly reduces the probability of failure over time. Every single PD is tested at wafer level, greatly improving economics. Finally, discrete or partially integrated PDs can be damaged in handling and packaging. Fully integrated PDs within a SiPHo chip are much easier to protect during manufacturing/assembly.

 **Nearly all CPO implementations use integrated PDs and thus have significantly better reliability in this regard.**

Next, we have lasers, the most unreliable component of any optical system. I have a lot more material sitting in my drafts folder so here is a quick summary:

  * Lasers are made of III-V material, typically Indium Phosphide (InP).

    * Shit yield.

    * Shit reliability.

  * Laser diodes are very sensitive to temperature.

    * I am talking +/- 0.1C sensitive in some cases.

    * Often, it is desirable to keep a laser at a specific temperature to ensure no mode hops (jumps in frequency response) and better efficiency.

  * All lasers degrade over time (lower power over time) and need to be burned-in and margined appropriately. 

  * Charge density is the main factor for degradation.




 **All CPO systems use external lasers (ELSFP) that are intrinsically much more reliable than integrated lasers within transceivers.**

This is because temperature can be controlled much more easily and a fewer number of higher power lasers (with larger die size to keep charge density the same) are needed. Fewer points of failure… and PLUGGABLE ANYWAY IN CASE OF FAILURE.

[![](https://substackcdn.com/image/fetch/$s_!lEU3!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9a2527bc-24b3-406e-b84c-08d76aa414e0_555x176.png)](https://substackcdn.com/image/fetch/$s_!lEU3!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9a2527bc-24b3-406e-b84c-08d76aa414e0_555x176.png)

 **CPO (when done right) is intrinsically more reliable than traditional optical transceivers.**

Case in point… Broadcom.

[![](https://substackcdn.com/image/fetch/$s_!EWVY!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa9556b21-d12a-45ea-8141-af698d25ac3c_1657x939.png)](https://substackcdn.com/image/fetch/$s_!EWVY!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa9556b21-d12a-45ea-8141-af698d25ac3c_1657x939.png)

[![](https://substackcdn.com/image/fetch/$s_!7kV2!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F341ab83e-59d0-4db6-8b86-1722ed9eb677_1641x809.png)](https://substackcdn.com/image/fetch/$s_!7kV2!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F341ab83e-59d0-4db6-8b86-1722ed9eb677_1641x809.png)

[![](https://substackcdn.com/image/fetch/$s_!xKfY!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0a770609-8480-4809-8263-96591ebc7385_1643x842.png)](https://substackcdn.com/image/fetch/$s_!xKfY!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0a770609-8480-4809-8263-96591ebc7385_1643x842.png)

This is incredible long-term FEC data. Not a single FEC bin above symbol 12.

In fact, if people were willing to tolerate a very small amount of packet drops, half FEC (8 bits) could be used.

[![](https://substackcdn.com/image/fetch/$s_!va4v!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdaa85d62-56df-4b18-9038-b6b07f2654a1_1614x762.png)](https://substackcdn.com/image/fetch/$s_!va4v!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdaa85d62-56df-4b18-9038-b6b07f2654a1_1614x762.png)

Incredible power savings.

[![](https://substackcdn.com/image/fetch/$s_!yzlZ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2aaa4626-e66f-4a97-a5ef-e64b4f2859a3_1624x860.png)](https://substackcdn.com/image/fetch/$s_!yzlZ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2aaa4626-e66f-4a97-a5ef-e64b4f2859a3_1624x860.png)

Massive improvement in mean-time-between-failure.

Broadcom actually got **ZERO FAILURES** in this 1M device hours of data. They need more data to claim higher MTBF. It is currently unknown how good Broadcom CPO really is. The 2.5-million-hour MTBF number is simply the statistically best they can claim with existing **PERFECT** data.

[![](https://substackcdn.com/image/fetch/$s_!K8sC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe538fa15-54cb-4fa3-abda-c23110cea6e1_1407x801.png)](https://substackcdn.com/image/fetch/$s_!K8sC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe538fa15-54cb-4fa3-abda-c23110cea6e1_1407x801.png)

 **Zero is perfect track record.** What the hell are you smoking, CPO reliability bears?

🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡🤡

* * *

In contrast to Broadcom, Marvell showed literally zero data.

[![](https://substackcdn.com/image/fetch/$s_!6O6I!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F75b0502a-8624-446e-886f-e64f2f3a4e2f_507x257.png)](https://substackcdn.com/image/fetch/$s_!6O6I!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F75b0502a-8624-446e-886f-e64f2f3a4e2f_507x257.png)

I attended the Marvell CPO talk and there was zero data. Just some block diagrams.

[![](https://substackcdn.com/image/fetch/$s_!VVuG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc00e950c-6484-4bcb-961c-29cef75f3cbf_524x524.png)](https://substackcdn.com/image/fetch/$s_!VVuG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc00e950c-6484-4bcb-961c-29cef75f3cbf_524x524.png)

I asked at least four people at the Marvell booth if they could disclose any information similar to what Broadcom has shown repeatedly over the past year.

  * pre-FEC BER.

  * FEC tail

  * MTBF

  * Power consumption vs transceiver.




Literally nothing.

[![](https://substackcdn.com/image/fetch/$s_!7Xdn!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F92675d6a-9c28-4c78-8c6a-b5b19dc5b949_978x1190.png)](https://substackcdn.com/image/fetch/$s_!7Xdn!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F92675d6a-9c28-4c78-8c6a-b5b19dc5b949_978x1190.png)

System looks cool but there is no public evidence all lanes can operate while meeting FEC requirements.

Here is the data Broadcom showed **over a year ago at Hot Chips 2024.**

[![](https://substackcdn.com/image/fetch/$s_!iWfF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F36620d15-fcf4-42e2-ba43-6526f865b089_1555x856.png)](https://substackcdn.com/image/fetch/$s_!iWfF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F36620d15-fcf4-42e2-ba43-6526f865b089_1555x856.png)

[![](https://substackcdn.com/image/fetch/$s_!ZHJA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3e2aa890-4ea0-4311-950a-9d54e5001b2f_1555x846.png)](https://substackcdn.com/image/fetch/$s_!ZHJA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3e2aa890-4ea0-4311-950a-9d54e5001b2f_1555x846.png)

[![](https://substackcdn.com/image/fetch/$s_!GKPy!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F45709397-25aa-4277-8a0f-4118f6019a07_934x496.png)](https://substackcdn.com/image/fetch/$s_!GKPy!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F45709397-25aa-4277-8a0f-4118f6019a07_934x496.png)

Looking forward to public data from Marvell on their CPO solution.

* * *

Next, lets talk about Nubis (now part of Ciena [CIEN 0.00%↑](https://substack.com/discover/stocks/CIEN)) CPO presentation.

[![](https://substackcdn.com/image/fetch/$s_!YFEN!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe13f3232-d900-4ef9-b248-4a39f744e79d_1694x1106.png)](https://substackcdn.com/image/fetch/$s_!YFEN!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe13f3232-d900-4ef9-b248-4a39f744e79d_1694x1106.png)

[![](https://substackcdn.com/image/fetch/$s_!Qfl-!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5fb515e1-cea5-4baa-8f4e-995348dd43f7_1511x1025.png)](https://substackcdn.com/image/fetch/$s_!Qfl-!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5fb515e1-cea5-4baa-8f4e-995348dd43f7_1511x1025.png)

[![](https://substackcdn.com/image/fetch/$s_!6TU1!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1fecca74-3c8f-48cc-a05f-7a5ce53c8ffb_1587x1054.png)](https://substackcdn.com/image/fetch/$s_!6TU1!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1fecca74-3c8f-48cc-a05f-7a5ce53c8ffb_1587x1054.png)

[![](https://substackcdn.com/image/fetch/$s_!Hyen!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe2417e6a-fe3a-4261-ad26-762a87645a34_1290x881.png)](https://substackcdn.com/image/fetch/$s_!Hyen!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe2417e6a-fe3a-4261-ad26-762a87645a34_1290x881.png)

[![](https://substackcdn.com/image/fetch/$s_!SLHW!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F150d0f46-843f-4de5-8649-36d754ff90a7_1454x1019.png)](https://substackcdn.com/image/fetch/$s_!SLHW!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F150d0f46-843f-4de5-8649-36d754ff90a7_1454x1019.png)

[![](https://substackcdn.com/image/fetch/$s_!luyc!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb9dcfa33-95cd-4718-925b-de03cf1f6edf_1554x1035.png)](https://substackcdn.com/image/fetch/$s_!luyc!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb9dcfa33-95cd-4718-925b-de03cf1f6edf_1554x1035.png)

[![](https://substackcdn.com/image/fetch/$s_!Pi_B!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd2827861-3698-4b90-bee8-9b2605b6a2da_1339x921.png)](https://substackcdn.com/image/fetch/$s_!Pi_B!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd2827861-3698-4b90-bee8-9b2605b6a2da_1339x921.png)

Ciena/Nubis presenter argues the following:

  * CPO should use high-speed (200G —> 400G) SerDes.

  * Single-wavelength is enough.

  * Scaling should be via large fiber arrays and grating couplers.




I strongly disagree with these arguments for a variety of reasons:

  * D2D clock-forwarded SerDes (UCIe, NVLink D2D, Broadcom MAX, Marvell 64G D2D, Elyian, …) has far better shoreline density and energy efficiency per bit.

  * Every fiber attach is a point of failure.

  * More fiber attachments reduce yield.

  * Grating coupler alignment is very challenging to scale.

  * DWDM based scaling, driven by D2D NRZ clock-forwarded SerDes is the optimal solution for co-packaged optics.

  * Laser power requirements grow exponentially as datarate and modulation scheme go up. (to maintain SNR/BER targets)




Engineering is about tradeoffs and strategically choosing which problems to solve.

Ciena/Nubis presenter argues for the opposite of my personal beliefs, but I respect his stance because there is logic behind it.

Still strongly disagree.

* * *

Accelink had some nice CPO material and demos, particularly on the laser side.

[![](https://substackcdn.com/image/fetch/$s_!lBD0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F96793e35-e051-423f-abfd-0e58c097f21b_1438x787.png)](https://substackcdn.com/image/fetch/$s_!lBD0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F96793e35-e051-423f-abfd-0e58c097f21b_1438x787.png)

[![](https://substackcdn.com/image/fetch/$s_!Chbl!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F187c907a-f486-4b4c-ad4a-2338d7dc2b10_1697x1009.png)](https://substackcdn.com/image/fetch/$s_!Chbl!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F187c907a-f486-4b4c-ad4a-2338d7dc2b10_1697x1009.png)

[![](https://substackcdn.com/image/fetch/$s_!YtOf!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F03ea8655-50fe-4908-8baa-2f7bf9aea79a_1663x974.png)](https://substackcdn.com/image/fetch/$s_!YtOf!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F03ea8655-50fe-4908-8baa-2f7bf9aea79a_1663x974.png)

The NPO solution is a scaled-up SiPho chip. Same (or at least very similar) MZI modulator system they use in transceivers.

Moar content for [TSEM 0.00%↑](https://substack.com/discover/stocks/TSEM) huehuehuehue.

[![](https://substackcdn.com/image/fetch/$s_!amhS!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F26879773-f318-4a32-bcf2-bd04876b92d4_1470x941.png)](https://substackcdn.com/image/fetch/$s_!amhS!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F26879773-f318-4a32-bcf2-bd04876b92d4_1470x941.png)

Pretty good results but the curve looks too smooth. Perhaps they only used one device to generate this data? 

* * *

Now for the really good Accelink stuff… ultra high-power ELSFP.

[![](https://substackcdn.com/image/fetch/$s_!NQpk!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F793a41bd-91ec-48c0-8ab9-ee26f3a1f027_1644x900.png)](https://substackcdn.com/image/fetch/$s_!NQpk!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F793a41bd-91ec-48c0-8ab9-ee26f3a1f027_1644x900.png)

[![](https://substackcdn.com/image/fetch/$s_!jEvL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7d22cdbd-ee4d-4d1d-b881-8a8542caf82f_1641x904.png)](https://substackcdn.com/image/fetch/$s_!jEvL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7d22cdbd-ee4d-4d1d-b881-8a8542caf82f_1641x904.png)

[![](https://substackcdn.com/image/fetch/$s_!gnXS!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd8fc7d1d-2430-44c1-bf78-9e32d6837046_1677x1176.png)](https://substackcdn.com/image/fetch/$s_!gnXS!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd8fc7d1d-2430-44c1-bf78-9e32d6837046_1677x1176.png)

Excellent optical power and stability. Really kickass data.

Efficiency is a bit low to be honest. But the power flatness is so incredible that efficiency gap does not matter IMO.

* * *

Broadcom also showed VCSEL CPO driving each laser with 100G SerDes.

[![](https://substackcdn.com/image/fetch/$s_!uon9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6b369271-df0f-4546-9094-20347c4b91a1_1323x751.png)](https://substackcdn.com/image/fetch/$s_!uon9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6b369271-df0f-4546-9094-20347c4b91a1_1323x751.png)

[![](https://substackcdn.com/image/fetch/$s_!FXu3!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe3c27495-7639-49c9-afb5-c93728251ba1_1438x745.png)](https://substackcdn.com/image/fetch/$s_!FXu3!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe3c27495-7639-49c9-afb5-c93728251ba1_1438x745.png)

This is an interesting niche solution. Cannot scale past 100G but really good at that speed.

* * *

Lumentum presentation trying to shill thin-film lithium-niobate.

[![](https://substackcdn.com/image/fetch/$s_!Xb0J!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbbf199e9-ad46-43d8-91f6-a6759c6a9db8_1435x816.png)](https://substackcdn.com/image/fetch/$s_!Xb0J!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbbf199e9-ad46-43d8-91f6-a6759c6a9db8_1435x816.png)

I don’t know enough about material science to comment. People tell me that TFLN is very far out.

Lumentum has higher content with InP based modulation solutions. There is a reason they are throwing shade on SiPho. 

## [2] Theme: 400G Electrical SerDes

I have strong opinions about PAM4 400G electrical SerDes.

Systems people look at unreasonably optimistic channel models in pretty MATLAB simulations while handwringing over SNR requirements of PAM8/6.

Myself, and anyone else who has measured real channels with a network analyzer, knows that real channels are shit and PAM4 400G is not going to work for most channels.

[![](https://substackcdn.com/image/fetch/$s_!5sno!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fce04f017-ceda-4fe3-9de4-5366e42241d6_1319x625.png)](https://substackcdn.com/image/fetch/$s_!5sno!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fce04f017-ceda-4fe3-9de4-5366e42241d6_1319x625.png)

[![](https://substackcdn.com/image/fetch/$s_!6kVz!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F21834b26-e875-433c-8499-7a3bdfc5edcf_1118x551.png)](https://substackcdn.com/image/fetch/$s_!6kVz!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F21834b26-e875-433c-8499-7a3bdfc5edcf_1118x551.png)

[![](https://substackcdn.com/image/fetch/$s_!t9MK!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F47ce777c-0a5c-43e1-ab7d-0d1595d1e6f3_1469x857.png)](https://substackcdn.com/image/fetch/$s_!t9MK!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F47ce777c-0a5c-43e1-ab7d-0d1595d1e6f3_1469x857.png)So your reference channel is shit after 85 GHz but you still arguing for Nyquist well over 85 GHz. Nice.

[![](https://substackcdn.com/image/fetch/$s_!dJPb!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd4dc2d8a-e363-45d2-9471-f831dde3d327_1355x765.png)](https://substackcdn.com/image/fetch/$s_!dJPb!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd4dc2d8a-e363-45d2-9471-f831dde3d327_1355x765.png)

COM simulations are already bullshit.

Not including crosstalk in the simulation makes it extra bullshit. LOL

Only way 400G PAM4 SerDes works is if you use exotic channels like co-packaged copper.

Here is the Ciena connector for telco transceivers.

[![](https://substackcdn.com/image/fetch/$s_!9YAm!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5a36ef05-3c68-4631-b634-2f35b13c37d0_1097x707.png)](https://substackcdn.com/image/fetch/$s_!9YAm!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5a36ef05-3c68-4631-b634-2f35b13c37d0_1097x707.png)

And some more notable connectors.

[![](https://substackcdn.com/image/fetch/$s_!4KTo!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbd100629-722a-4f8d-9f93-77bc41fd7c1f_1668x1138.png)](https://substackcdn.com/image/fetch/$s_!4KTo!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbd100629-722a-4f8d-9f93-77bc41fd7c1f_1668x1138.png)

[![](https://substackcdn.com/image/fetch/$s_!Id9N!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2968fd31-787d-47d6-9453-203b81062624_797x838.png)](https://substackcdn.com/image/fetch/$s_!Id9N!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2968fd31-787d-47d6-9453-203b81062624_797x838.png)

[![](https://substackcdn.com/image/fetch/$s_!I5nf!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0b1fb57d-6640-429a-866a-746bc6c294c5_1152x907.png)](https://substackcdn.com/image/fetch/$s_!I5nf!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0b1fb57d-6640-429a-866a-746bc6c294c5_1152x907.png)

[![](https://substackcdn.com/image/fetch/$s_!TKLy!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3ac63881-79c6-42d6-af96-2989909bcd86_1568x1214.png)](https://substackcdn.com/image/fetch/$s_!TKLy!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3ac63881-79c6-42d6-af96-2989909bcd86_1568x1214.png)

Samtech somehow managed to make a magic connector. This shit is mind-blowingly good.

Anyway, PAM4 400G is a dumb idea that should not be standardized. It is too risky to limit official standards to niche CPC channels.

* * *

Ciena’s 400G SerDes is kickass but they have a rather glaring issue that needs to be fixed. Can you spot it?

[![](https://substackcdn.com/image/fetch/$s_!_NPJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4bc39a1e-d4a9-4fb1-9f33-7be9c1987a5b_1530x948.png)](https://substackcdn.com/image/fetch/$s_!_NPJ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4bc39a1e-d4a9-4fb1-9f33-7be9c1987a5b_1530x948.png)

[![](https://substackcdn.com/image/fetch/$s_!VUpu!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa33a2075-f741-42fb-a7f2-9e5440196761_1694x1198.png)](https://substackcdn.com/image/fetch/$s_!VUpu!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa33a2075-f741-42fb-a7f2-9e5440196761_1694x1198.png)

There is a random noise problem. Look between the symbol histograms.

[![](https://substackcdn.com/image/fetch/$s_!qW69!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd2cc0e2d-d156-4faa-a326-02bb1fed20f3_1413x331.png)](https://substackcdn.com/image/fetch/$s_!qW69!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd2cc0e2d-d156-4faa-a326-02bb1fed20f3_1413x331.png)

There is a floor. Not good.

Many possible root causes but one guess would be poor ADC interleave calibration. 

Ciena needs to fix this. Given how great the rest of their data is, I’m sure they will figure this out.

## [3] Theme: Optical Transceivers 

While CPO was super popular, transceivers are not going anywhere. See this Lightcounting data.

[![](https://substackcdn.com/image/fetch/$s_!roYD!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F34570a04-65a5-48f4-a353-052ae6756408_1226x779.png)](https://substackcdn.com/image/fetch/$s_!roYD!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F34570a04-65a5-48f4-a353-052ae6756408_1226x779.png)

I am much more bullish on CPO than Lightcounting. Think CPO market share is much higher in 2029 onwards.

But regardless, CPO is not a universal solution. Transceivers will always have a place in the market.

* * *

Let’s start with the holy war against DSP chips.

[![](https://substackcdn.com/image/fetch/$s_!4Miq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F747423d6-0b3e-480f-8254-147d2fbb34f7_1606x933.png)](https://substackcdn.com/image/fetch/$s_!4Miq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F747423d6-0b3e-480f-8254-147d2fbb34f7_1606x933.png)

[![](https://substackcdn.com/image/fetch/$s_!mffy!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe0a5d81d-ba7b-4aea-9662-4851ac20b0f1_1533x903.png)](https://substackcdn.com/image/fetch/$s_!mffy!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe0a5d81d-ba7b-4aea-9662-4851ac20b0f1_1533x903.png)

Everyone wants to remove the DSP because of two main reasons:

  1. Huge BOM cost contribution.

  2. Large power consumption contribution.




LRO is a silly half-measure in my opinion.

[![](https://substackcdn.com/image/fetch/$s_!T9q1!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F674fcfa2-41f0-47be-acdd-92075a9fbe51_417x200.gif)](https://substackcdn.com/image/fetch/$s_!T9q1!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F674fcfa2-41f0-47be-acdd-92075a9fbe51_417x200.gif)

LPO is the way forward, and it can work great if done right.

[![](https://substackcdn.com/image/fetch/$s_!agYq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F49c0f4d9-1679-44c9-8c76-722c78034222_1491x856.png)](https://substackcdn.com/image/fetch/$s_!agYq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F49c0f4d9-1679-44c9-8c76-722c78034222_1491x856.png)

Channel variation across switch ports is a major issue that needs careful tuning and optical module design to overcome.

Some CTLE, driver, TIA, linear EQ configuration (Semtech, Macom, Marvell) is needed to account for such variation.

[![](https://substackcdn.com/image/fetch/$s_!L_s0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F56477a9c-d2ae-4b3f-8c1f-882a96f7f5c0_1723x1065.png)](https://substackcdn.com/image/fetch/$s_!L_s0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F56477a9c-d2ae-4b3f-8c1f-882a96f7f5c0_1723x1065.png)

Mildly annoyed Accelink did not show FEC tails but whatever.

* * *

Credo has a 1.6T optical DSP now. Heard rumors it was good (perf and power consumption) and rumors were confirmed at the show.

[![](https://substackcdn.com/image/fetch/$s_!JC5z!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0576310a-1fc3-446c-901c-c2ff7037a945_1296x1313.png)](https://substackcdn.com/image/fetch/$s_!JC5z!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0576310a-1fc3-446c-901c-c2ff7037a945_1296x1313.png)

Pre-FEC BER is good. Matches Marvell.

TDECQ is decent. In general, sub 1.5 dB is the target.

[![](https://substackcdn.com/image/fetch/$s_!3FKp!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3009ea90-765f-49ea-8862-1074b26f6233_884x1137.png)](https://substackcdn.com/image/fetch/$s_!3FKp!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3009ea90-765f-49ea-8862-1074b26f6233_884x1137.png)

They are using a low-noise laboratory-grade laser though. Sneaky sneaky.

Next, lets go over Credo’s “zero flap” OCP proposed standard.

[![](https://substackcdn.com/image/fetch/$s_!calk!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0766925e-e34c-408d-abb1-17c6c33c5664_1655x852.png)](https://substackcdn.com/image/fetch/$s_!calk!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0766925e-e34c-408d-abb1-17c6c33c5664_1655x852.png)

[![](https://substackcdn.com/image/fetch/$s_!stzY!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0cbdd734-dc6d-4594-bf7f-825083f19f57_1305x714.png)](https://substackcdn.com/image/fetch/$s_!stzY!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0cbdd734-dc6d-4594-bf7f-825083f19f57_1305x714.png)

It’s mostly laser mode hops due to thermal drift but whatever go on…

[![](https://substackcdn.com/image/fetch/$s_!Y7Qj!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F445e7119-d801-4681-84a9-7ab996018cb4_1166x655.png)](https://substackcdn.com/image/fetch/$s_!Y7Qj!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F445e7119-d801-4681-84a9-7ab996018cb4_1166x655.png)

[![](https://substackcdn.com/image/fetch/$s_!cTfP!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff398a59a-2a39-4b17-8778-4e642901965f_1709x1024.png)](https://substackcdn.com/image/fetch/$s_!cTfP!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff398a59a-2a39-4b17-8778-4e642901965f_1709x1024.png)

[![](https://substackcdn.com/image/fetch/$s_!Ru8N!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F03da3a7b-9961-43c4-b814-48d1fc18e93c_1585x863.png)](https://substackcdn.com/image/fetch/$s_!Ru8N!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F03da3a7b-9961-43c4-b814-48d1fc18e93c_1585x863.png)

[![](https://substackcdn.com/image/fetch/$s_!y1V_!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff37d56b1-13fd-46e5-ac49-c3c95b894598_1313x698.png)](https://substackcdn.com/image/fetch/$s_!y1V_!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff37d56b1-13fd-46e5-ac49-c3c95b894598_1313x698.png)

Credo has developed a nice tool/firmware framework for monitoring optics. They will also donate this work to OCP.

Nice. Kudos.

* * *

Let’s go over OCP NIC standards updates. The optical modules need to plug into something on the host end.

[![](https://substackcdn.com/image/fetch/$s_!0Ucd!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2c7ee167-589c-4a1a-a2a3-410736d20d51_1422x887.png)](https://substackcdn.com/image/fetch/$s_!0Ucd!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2c7ee167-589c-4a1a-a2a3-410736d20d51_1422x887.png)

[![](https://substackcdn.com/image/fetch/$s_!a30v!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F27a13f81-81c4-45a4-9522-637e35f8271c_1454x826.png)](https://substackcdn.com/image/fetch/$s_!a30v!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F27a13f81-81c4-45a4-9522-637e35f8271c_1454x826.png)

[![](https://substackcdn.com/image/fetch/$s_!oHn-!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2629d917-7471-4695-8ddb-05beb3965d8f_1422x862.png)](https://substackcdn.com/image/fetch/$s_!oHn-!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2629d917-7471-4695-8ddb-05beb3965d8f_1422x862.png)

[![](https://substackcdn.com/image/fetch/$s_!d0fj!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F214673f9-c061-4828-b033-179d5b4a3ab3_1398x673.png)](https://substackcdn.com/image/fetch/$s_!d0fj!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F214673f9-c061-4828-b033-179d5b4a3ab3_1398x673.png)

[![](https://substackcdn.com/image/fetch/$s_!G-O8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F547a66f8-ddb6-4649-bd1e-bfbaa7782d83_914x688.png)](https://substackcdn.com/image/fetch/$s_!G-O8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F547a66f8-ddb6-4649-bd1e-bfbaa7782d83_914x688.png)The answer is yes. Please kill Astera Labs.

[![](https://substackcdn.com/image/fetch/$s_!shVj!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2568267e-8f52-4488-b20b-628623a63fd4_1264x786.png)](https://substackcdn.com/image/fetch/$s_!shVj!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2568267e-8f52-4488-b20b-628623a63fd4_1264x786.png)Good. Artificial power limits from standards bodies have been harming NIC innovation.

[![](https://substackcdn.com/image/fetch/$s_!wNmP!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F32f8f3a2-8314-4ce5-a5b6-e8a84b603aca_1261x736.png)](https://substackcdn.com/image/fetch/$s_!wNmP!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F32f8f3a2-8314-4ce5-a5b6-e8a84b603aca_1261x736.png)

Astera Labs probably has the following feedback for 64x-PCIe lane OCP NIC standard.

[![](https://substackcdn.com/image/fetch/$s_!mub7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fce0292d2-f1c5-4d9a-a395-7479bfe4018a_220x179.gif)](https://substackcdn.com/image/fetch/$s_!mub7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fce0292d2-f1c5-4d9a-a395-7479bfe4018a_220x179.gif)

* * *

Finally, lets talk about Marvell’s 1.6T optical DSP.

Three people at the conference told me that Marvell is out from Nvidia transceivers. All three said that Nvidia would dual-source between their internal DSP and Broadcom’s.

When I asked why Nvidia would go to the trouble of dual sourcing the DSP, I did not get very credible answers. If people want supply-chain resilience, they will go buy non-Nvidia transceivers from Innolight, Accelink, Eoptolink, Lumentum, Coherent, or several other players.

How the hell is buying a Broadcom-DSP powered Nvidia transceiver of any strategic value to end customers?

Marvell had a demo of this DSP chip and it is basically useless.

[![](https://substackcdn.com/image/fetch/$s_!X5VF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffb15d7c9-96e3-4090-81cb-0e3b7460cf77_1713x940.png)](https://substackcdn.com/image/fetch/$s_!X5VF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffb15d7c9-96e3-4090-81cb-0e3b7460cf77_1713x940.png)

Oh wow FEC symbol 2. What is the test setup?

[![](https://substackcdn.com/image/fetch/$s_!bV18!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F89b09609-a825-4369-99be-e0586c42006d_1393x1204.png)](https://substackcdn.com/image/fetch/$s_!bV18!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F89b09609-a825-4369-99be-e0586c42006d_1393x1204.png)

[![](https://substackcdn.com/image/fetch/$s_!UcTK!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffb14c602-7618-4aae-8e41-cd7d9699ec09_220x192.gif)](https://substackcdn.com/image/fetch/$s_!UcTK!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffb14c602-7618-4aae-8e41-cd7d9699ec09_220x192.gif)

Only the optical-side SerDes is active and it’s in a synchronous (zero PPM) loopback on a simple 4-5 dB copper channel.

Maybe Marvell was afraid of the Barclays gremlin showing up and nitpicking their optical DSP over 1 watt again.

Regardless, I am tired of trying to figure out if Marvell is in or out of Nvidia 1.6T transceiver.

[![](https://substackcdn.com/image/fetch/$s_!BuRv!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7bff8af6-8377-4a67-a0bd-debaa80491ac_200x120.gif)](https://substackcdn.com/image/fetch/$s_!BuRv!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7bff8af6-8377-4a67-a0bd-debaa80491ac_200x120.gif)

Look at this graph.

[![](https://substackcdn.com/image/fetch/$s_!pTof!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc365b321-61d5-451d-b454-4c70c06c51e2_1292x757.png)](https://substackcdn.com/image/fetch/$s_!pTof!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc365b321-61d5-451d-b454-4c70c06c51e2_1292x757.png)

  * 800G transceivers going to the moon.

  * Nobody is going to bother designing Marvell out of that generation.

  * Yes, massive share loss in 1.6T generation. 

    * So what?

    * Marvell/InPhi gona massively grow.

  * If you are looking for a Marvell short thesis, this isn’t it.

    * Idiots who still expect Maia program to ramp up is why you might want to short Marvell.




## [4] Theme: Scale-Up Protocols, ESUN, and UALink Death

[ALAB 0.00%↑](https://substack.com/discover/stocks/ALAB) stock tanked because of OCP announcements. 

[![](https://substackcdn.com/image/fetch/$s_!I_gC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6839cdc9-4d02-46e8-afbb-0a2cbb26cf2f_595x571.png)](https://substackcdn.com/image/fetch/$s_!I_gC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6839cdc9-4d02-46e8-afbb-0a2cbb26cf2f_595x571.png)

[![](https://substackcdn.com/image/fetch/$s_!lHAA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1dccb7fb-27ca-42c4-a24b-d7f0550f0d3e_1280x720.webp)](https://substackcdn.com/image/fetch/$s_!lHAA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1dccb7fb-27ca-42c4-a24b-d7f0550f0d3e_1280x720.webp)

[![](https://substackcdn.com/image/fetch/$s_!N84H!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff6b398a9-e672-40bf-b4a8-0942267e1afd_588x509.png)](https://substackcdn.com/image/fetch/$s_!N84H!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff6b398a9-e672-40bf-b4a8-0942267e1afd_588x509.png)

Notice who is not on the ESUN supporters list? 

_< whispers… ALAB…>_

UALink was already dead but now this joke of a standard is extra dead. The body has been burned and the ashes dissolved in hydrofluoric acid for good measure.

Here is a rough timeline of what happened in standards politics land.

  1. UALink was formed when **AMD donated their specification to the org.**

  2. Broadcom joined, realized they were the only ones who had a viable SerDes, and left.

  3. Broadcom made SUE.

  4. Meta (and presumably other hyperscalers) panicked and negotiated for Broadcom to re-join the fold… by creating ESUN.




At a high level, ESUN exists to standardize the switch-side digital bits, while leaving client-side digital bits open to customization.

As a starting point, Broadcom SUE has been donated as a default client-side protocol.

<https://www.opencompute.org/wiki/Networking/ESUN>

<https://www.opencompute.org/w/index.php?title=Networking/SUE-T>

[![](https://substackcdn.com/image/fetch/$s_!OGKE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F37f242df-c0d6-4a30-9ad7-eb89693b5c36_714x400.png)](https://substackcdn.com/image/fetch/$s_!OGKE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F37f242df-c0d6-4a30-9ad7-eb89693b5c36_714x400.png)

Two companies were pro-UALink (from the purchaser side of the equation): Amazon and AMD.

Amazon has dual-tracked Trainium 4. There is an NVLink Fusion version and a UALink version.

AMD has also dual-tracked their GPU program. There is a UALink version and an ESUN version.

I believe both Amazon and AMD will abandon UALink.

 **This is really bad for Astera Labs as their switching content will be replaced by Nvidia and Broadcom respectively.**

[![](https://substackcdn.com/image/fetch/$s_!NL3A!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F889e4409-d111-4252-9c8b-bcb23743bfec_1489x812.png)](https://substackcdn.com/image/fetch/$s_!NL3A!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F889e4409-d111-4252-9c8b-bcb23743bfec_1489x812.png) Proud member of a dead standard replaced by the open OCP endorsed ESUN protocol.

[![](https://substackcdn.com/image/fetch/$s_!ZaOH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5afade59-7bbd-4d4d-a086-49fe107419b2_577x1262.png)](https://substackcdn.com/image/fetch/$s_!ZaOH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5afade59-7bbd-4d4d-a086-49fe107419b2_577x1262.png)

Astera Labs had a meme rack on a rotating display trying to claim they are the open standard scale-up leader. Kept talking about PCIe-based scaleup with retimers on every link.

LOL

Broadcom, Nvidia, Marvell, NextHop, and Upscale are going to vaporize these fools.

## [5] Miscellaneous

Random interesting things that don’t fit into any broader theme.

### [5.a] Marvell Alaska AEC

Marvell’s AEC DSP is incredible. Supports up to 9 meters of length.

Look at this FEC histogram! (7 meter version)

[![](https://substackcdn.com/image/fetch/$s_!b46t!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F897eafb4-430d-4fc5-bda3-ff81d7722799_1626x899.png)](https://substackcdn.com/image/fetch/$s_!b46t!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F897eafb4-430d-4fc5-bda3-ff81d7722799_1626x899.png)

This is amazing. FEC symbol 4.

Obviously, some favorable (aggressive) active cooling was used for this demo.

 **Regardless, this demo is so good that it is reasonable to assume that half-FEC operation (half latency) is easily achievable with Marvell Alasca AEC.**

I asked the Marvell people why Credo is getting away with highway robbery given that Marvell has a superior product in terms of reach, performance, latency, and power.

They said some excuses like… _oh no Credo is vertically integrated and we only sell the chip and we have lots of partners and don’t want to compete with them to take content blah blah blah._

[![](https://substackcdn.com/image/fetch/$s_!xJtS!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc5ac1259-4b8e-4b91-895b-9563c115010b_651x473.png)](https://substackcdn.com/image/fetch/$s_!xJtS!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc5ac1259-4b8e-4b91-895b-9563c115010b_651x473.png)

So what?

Design the stupid PCB yourself and give it to each partner for free. Accelerate your time to market.

Credo’s margins are your opportunity!

 **Stop giving me lame excuses and go kill Credo.**

I pitched long [MRVL 0.00%↑](https://substack.com/discover/stocks/MRVL) short [CRDO 0.00%↑](https://substack.com/discover/stocks/CRDO) to every finance person I met up with at OCP and this trade got shot down by every single one of them.

Credo ramp so big oh no messa scared to short this overvalued meme stock. 

### [5.b] Bloom Energy

Bloom energy has a time-to-power advantage. 

The tech is mediocre in basically every other way. Only real advantage is you get datacenter powered up faster.

This alone is enough for considering going long [BE 0.00%↑](https://substack.com/discover/stocks/BE) but given how I missed the rally, been sitting out.

Then I see this…

[![](https://substackcdn.com/image/fetch/$s_!UpxN!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9aec6d08-cc40-4949-8f1e-1c3a9260fe84_1750x1212.png)](https://substackcdn.com/image/fetch/$s_!UpxN!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9aec6d08-cc40-4949-8f1e-1c3a9260fe84_1750x1212.png)

[![](https://substackcdn.com/image/fetch/$s_!SX7Q!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6c60c062-6de3-4081-a2f9-75e946e6d920_1315x709.png)](https://substackcdn.com/image/fetch/$s_!SX7Q!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6c60c062-6de3-4081-a2f9-75e946e6d920_1315x709.png)

Supercapacitors to improve transient ripple for 800V DC direct supply?

[![](https://substackcdn.com/image/fetch/$s_!55-b!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0818ad03-89fb-4565-a7db-45ff79e95023_1167x601.png)](https://substackcdn.com/image/fetch/$s_!55-b!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0818ad03-89fb-4565-a7db-45ff79e95023_1167x601.png)

Configurable and modular reliability scaling?

[![](https://substackcdn.com/image/fetch/$s_!RsRA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc5a0e7da-53c9-4114-a978-2c9c5d6972e1_1515x762.png)](https://substackcdn.com/image/fetch/$s_!RsRA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc5a0e7da-53c9-4114-a978-2c9c5d6972e1_1515x762.png)

[![](https://substackcdn.com/image/fetch/$s_!ZLbB!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5f46fd12-0441-41bd-9a6b-eb2a385eaeb0_1542x815.png)](https://substackcdn.com/image/fetch/$s_!ZLbB!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5f46fd12-0441-41bd-9a6b-eb2a385eaeb0_1542x815.png)

[![](https://substackcdn.com/image/fetch/$s_!XXGK!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff8a3e3b2-283d-4e63-9d5f-11ba9d98ad33_1575x797.png)](https://substackcdn.com/image/fetch/$s_!XXGK!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff8a3e3b2-283d-4e63-9d5f-11ba9d98ad33_1575x797.png)

[![](https://substackcdn.com/image/fetch/$s_!v5ZO!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9aa4de26-60c7-4112-817f-a436aa6edbeb_220x220.gif)](https://substackcdn.com/image/fetch/$s_!v5ZO!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9aa4de26-60c7-4112-817f-a436aa6edbeb_220x220.gif)

I bought some shares. Need to do more research before sizing up the position.

### [5.c] QLC Storage

Meta is deploying QLC flash storage at scale.

[![](https://substackcdn.com/image/fetch/$s_!1wiU!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F818f1c5b-39f6-4392-ab24-e569853151f8_1278x712.png)](https://substackcdn.com/image/fetch/$s_!1wiU!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F818f1c5b-39f6-4392-ab24-e569853151f8_1278x712.png)

[![](https://substackcdn.com/image/fetch/$s_!D0bE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1252d746-d27e-40aa-9d9c-f049ebe26950_1535x868.png)](https://substackcdn.com/image/fetch/$s_!D0bE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1252d746-d27e-40aa-9d9c-f049ebe26950_1535x868.png)

Power and density important.

Shilling Purestorage. (this shall be short lived)

[![](https://substackcdn.com/image/fetch/$s_!9HEw!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F41587292-c730-46e6-b941-9a8841186118_1549x840.png)](https://substackcdn.com/image/fetch/$s_!9HEw!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F41587292-c730-46e6-b941-9a8841186118_1549x840.png)

Ah so you are in the process of designing out Purestraoge. Nice.

[![](https://substackcdn.com/image/fetch/$s_!U7e4!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F01a5e8c7-fbe0-4046-8da5-dc2780149166_1514x859.png)](https://substackcdn.com/image/fetch/$s_!U7e4!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F01a5e8c7-fbe0-4046-8da5-dc2780149166_1514x859.png)

Slide complains about CPUs taking too much power budget. Need to move to next-gen manycore x86 CPU single-socket platform.

The presenter was very… vocal about how much he hates the Intel Saphire Rapids dual-socket power draw. Man was genuinely pissed.

So Meta is either going to use AMD Venice Dense or Intel Clearwater Forrest.

(probably AMD but we shall see… not material to either AMD or Intel stock)

ARM solutions unlikely because Meta seems concerned about CPU core performance in this application.

* * *

[![](https://substackcdn.com/image/fetch/$s_!q9CH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F49c746db-ef17-40b5-a788-45070ae5faca_1470x824.png)](https://substackcdn.com/image/fetch/$s_!q9CH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F49c746db-ef17-40b5-a788-45070ae5faca_1470x824.png)

[![](https://substackcdn.com/image/fetch/$s_!OIoY!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8adf13b5-dade-4934-8ffc-fc968abe63c2_1461x871.png)](https://substackcdn.com/image/fetch/$s_!OIoY!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8adf13b5-dade-4934-8ffc-fc968abe63c2_1461x871.png)

[![](https://substackcdn.com/image/fetch/$s_!Q1d1!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb3a13157-b4fa-4ef0-9493-041c43e8be2a_1327x823.png)](https://substackcdn.com/image/fetch/$s_!Q1d1!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb3a13157-b4fa-4ef0-9493-041c43e8be2a_1327x823.png)

NAND flash naturally wears out over time. 

Overprovisioning is a process where a portion of the total raw storage capacity is set aside for future use.

So your “1 TB” SSD might actually have 1.1 TB of raw capacity for example.

All flash storage devices use this tactic but with varying overprovisioning ratios. Electric cars also overprovision batteries.

Anyway, due to some complicated underlying nuances, the overprovisioning needs to be spread out.

[![](https://substackcdn.com/image/fetch/$s_!Gb3o!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F18a42d18-a362-4fd3-b961-ae5faf5e4ce7_1306x783.png)](https://substackcdn.com/image/fetch/$s_!Gb3o!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F18a42d18-a362-4fd3-b961-ae5faf5e4ce7_1306x783.png)

[![](https://substackcdn.com/image/fetch/$s_!vBAk!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1009b5d2-72ad-4031-a090-f26878dcabca_1264x771.png)](https://substackcdn.com/image/fetch/$s_!vBAk!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1009b5d2-72ad-4031-a090-f26878dcabca_1264x771.png)

[![](https://substackcdn.com/image/fetch/$s_!7fMk!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff911b394-4d48-4b5d-bcf3-6b09d77b74d9_1199x781.png)](https://substackcdn.com/image/fetch/$s_!7fMk!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff911b394-4d48-4b5d-bcf3-6b09d77b74d9_1199x781.png)

[![](https://substackcdn.com/image/fetch/$s_!8uI2!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F98ea0e35-9570-4504-91c2-a41f5aaca6fa_1240x742.png)](https://substackcdn.com/image/fetch/$s_!8uI2!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F98ea0e35-9570-4504-91c2-a41f5aaca6fa_1240x742.png)

[![](https://substackcdn.com/image/fetch/$s_!LULU!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F42df0c5f-a259-40b2-94ee-b516d21f9d17_1233x751.png)](https://substackcdn.com/image/fetch/$s_!LULU!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F42df0c5f-a259-40b2-94ee-b516d21f9d17_1233x751.png)

Very cool.

### [5.d] Cool Cable Length Measurment

Meta has developed a neat software tool that can measure the cable length of any run inside a multi-datacenter network. Inside and outside the datacenter.

[![](https://substackcdn.com/image/fetch/$s_!3HNw!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8e777565-7f13-4c2e-ac5b-7b3d4f09b2eb_1580x928.png)](https://substackcdn.com/image/fetch/$s_!3HNw!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8e777565-7f13-4c2e-ac5b-7b3d4f09b2eb_1580x928.png)

[![](https://substackcdn.com/image/fetch/$s_!x36E!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5e679864-0037-4c50-9f34-bab7e711d91e_1432x778.png)](https://substackcdn.com/image/fetch/$s_!x36E!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5e679864-0037-4c50-9f34-bab7e711d91e_1432x778.png)

[![](https://substackcdn.com/image/fetch/$s_!JbO-!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6e181477-d1b4-40aa-9ff5-dd9f8db0c9a2_1354x788.png)](https://substackcdn.com/image/fetch/$s_!JbO-!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6e181477-d1b4-40aa-9ff5-dd9f8db0c9a2_1354x788.png)

[![](https://substackcdn.com/image/fetch/$s_!2MGV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0338ac34-6bfe-4ecd-9504-a1fc2af2d2b6_1488x838.png)](https://substackcdn.com/image/fetch/$s_!2MGV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0338ac34-6bfe-4ecd-9504-a1fc2af2d2b6_1488x838.png)

[![](https://substackcdn.com/image/fetch/$s_!xlq1!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fee7eb1b3-8566-403e-9595-8402a6d01ae6_1338x749.png)](https://substackcdn.com/image/fetch/$s_!xlq1!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fee7eb1b3-8566-403e-9595-8402a6d01ae6_1338x749.png)

[![](https://substackcdn.com/image/fetch/$s_!Mllw!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdceb7085-f267-4387-b32e-e60e0fb858be_1398x798.png)](https://substackcdn.com/image/fetch/$s_!Mllw!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdceb7085-f267-4387-b32e-e60e0fb858be_1398x798.png)

[![](https://substackcdn.com/image/fetch/$s_!83Gk!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb63e8a71-f3e9-4322-8fc9-b612035dc223_1497x843.png)](https://substackcdn.com/image/fetch/$s_!83Gk!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb63e8a71-f3e9-4322-8fc9-b612035dc223_1497x843.png)

[![](https://substackcdn.com/image/fetch/$s_!sqkw!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdd4f3500-4feb-419b-a9d0-6d59e9ed096c_1556x905.png)](https://substackcdn.com/image/fetch/$s_!sqkw!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdd4f3500-4feb-419b-a9d0-6d59e9ed096c_1556x905.png)

[![](https://substackcdn.com/image/fetch/$s_!3Q8L!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F396207c5-6c63-4807-978f-64d54ac5b8cc_1572x849.png)](https://substackcdn.com/image/fetch/$s_!3Q8L!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F396207c5-6c63-4807-978f-64d54ac5b8cc_1572x849.png)

Very clever distance approximation. Commercial wireless world has used similar tactics since 2018. Delay-based distance estimation is a common military signal-processing challenge.

The most difficult part of what Meta’s system is estimating the switch latency itself. They seem to have collected a small dataset of known-length runs to calibrate out the unique delay of each switch model.

Meta claims to have accuracy of within +/- 10 meters. Really incredible stuff.

### [5.e] Multilane Test Equipment

A small privately held test equipment company you probably have never heard of had a meaningful impact on improving the yields of complex AI scale-up cabled backplanes.

[![](https://substackcdn.com/image/fetch/$s_!Wq8U!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0a30fd49-189b-4304-b960-1f807e5c4dee_1210x702.png)](https://substackcdn.com/image/fetch/$s_!Wq8U!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0a30fd49-189b-4304-b960-1f807e5c4dee_1210x702.png)

The original way these backplanes were tested is via optical inspection and basic continuity tests. (probe pins with a multimeter lol)

No measurement of signal integrity, BER, s-parameters, or TDR pulses.

This strategy did not go well. 

The reason nobody was testing these backplanes properly was the equipment to test so many differential pairs at the same time did not exist.

[![](https://substackcdn.com/image/fetch/$s_!H-mV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc7cb1d95-bae6-45c8-8773-4328c855ed3d_1277x720.png)](https://substackcdn.com/image/fetch/$s_!H-mV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc7cb1d95-bae6-45c8-8773-4328c855ed3d_1277x720.png)

When backplane (rack-integrator) yields were at < 10%, everyone was playing a fun finger-pointing game.

  * This is Amphenol’s fault.

  * No no no it’s FIT/Wistron/Quanta/… fault.

  * No no no the customer does not know how to operate advanced AI racks…

  * No no no the design itself is too complicated and cannot be manufactured at scale.




[![](https://substackcdn.com/image/fetch/$s_!eDVb!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd2fbad41-aef2-40cd-807c-18b284aadc9f_1601x928.png)](https://substackcdn.com/image/fetch/$s_!eDVb!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd2fbad41-aef2-40cd-807c-18b284aadc9f_1601x928.png)

Multilane helped the ecosystem dramatically improve yields (80-90%) by creating a giant 64-lane BERT (bit-error-rate-tester) that can slot entire sections of a backplane in for one giant test.

  * Real hardware FEC BER measurements.

  * Real channel impulse response.

  * Real SNR calculations.

  * Real insertion and return loss.




To give some context, a high-speed BERT capable of testing ONE DIFFERNTIAL PAIR at 200Gbps speeds costs around $700K minimum. 

Buying and wiring up 64x $700K boxes is stupid and unviable. There is a reason the ecosystem took the lame way out (basic continuity tests and optical inspection) and ate shit shortly thereafter.

Multilane found an incredible niche and are serving that market INCREDIBLY well. It’s kinda crazy. I am very familiar with the traditional electrical test equipment market. Keysight, R&S, Tektronix, Anritsu, Spirent, Teledyne, RIGOL, …

Nobody else has what Multilane can offer. The sheer value these guys deliver is crazy. 

[![](https://substackcdn.com/image/fetch/$s_!iN3Z!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0deddb9e-76b1-47f2-951f-78bf65a981e9_1601x911.png)](https://substackcdn.com/image/fetch/$s_!iN3Z!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0deddb9e-76b1-47f2-951f-78bf65a981e9_1601x911.png)

### [5.f] Interesting 3D Etched? Copper Coldplates

Some Chinese company I never heard of made these.

[![](https://substackcdn.com/image/fetch/$s_!TW4t!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdc396e69-457a-4e76-9a17-7fb7f25f8e7a_4000x3000.jpeg)](https://substackcdn.com/image/fetch/$s_!TW4t!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdc396e69-457a-4e76-9a17-7fb7f25f8e7a_4000x3000.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!G_TC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fee73bf6f-1b82-462c-962d-4db48170f566_4000x3000.jpeg)](https://substackcdn.com/image/fetch/$s_!G_TC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fee73bf6f-1b82-462c-962d-4db48170f566_4000x3000.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!QM1T!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1bff22e8-14bb-4b22-8be9-15b18f431884_4000x3000.jpeg)](https://substackcdn.com/image/fetch/$s_!QM1T!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1bff22e8-14bb-4b22-8be9-15b18f431884_4000x3000.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!x73P!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F382500c6-7381-4efc-b6b5-64d64e75bfee_4000x3000.jpeg)](https://substackcdn.com/image/fetch/$s_!x73P!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F382500c6-7381-4efc-b6b5-64d64e75bfee_4000x3000.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!U21R!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F701a999f-0610-4509-b58c-960205efa865_4000x3000.jpeg)](https://substackcdn.com/image/fetch/$s_!U21R!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F701a999f-0610-4509-b58c-960205efa865_4000x3000.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!23wl!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F670d918e-106b-418b-bb30-e3f7ce1104cf_4000x3000.jpeg)](https://substackcdn.com/image/fetch/$s_!23wl!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F670d918e-106b-418b-bb30-e3f7ce1104cf_4000x3000.jpeg)

Held few of these in my hand. They are super solid and sturdy. It’s looks like a deepfake but it’s actually real.

Somehow they use lasers to print these weird shapes. 

Super interesting. 

### [5.g] Point2

Interesting mmWave over plastic tube high-speed connectivity.

[Vikram Sekar](https://open.substack.com/users/124411709-vikram-sekar?utm_source=mentions) has a great writeup.

[![](https://substackcdn.com/image/fetch/$s_!9JlA!,w_56,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa409d69d-ca10-4bfe-a1fc-f8d291690566_185x185.png)Vik's NewsletterPlastic Cables for AI Clusters: Can Point2’s E-Tube Disrupt Copper and Optics?Welcome to a 🔒 subscriber-only deep-dive edition 🔒 of my weekly newsletter. Each week, I help investors, professionals and students stay up-to-date on complex topics, and navigate the semiconductor industry…Read more7 months ago · 25 likes · 6 comments · Vikram Sekar](https://www.viksnewsletter.com/p/plastic-cables-for-ai-clusters-etube?utm_source=substack&utm_campaign=post_embed&utm_medium=web)

[![](https://substackcdn.com/image/fetch/$s_!wnGn!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbb2931cd-1988-4196-b39e-a959bd680587_1260x607.png)](https://substackcdn.com/image/fetch/$s_!wnGn!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbb2931cd-1988-4196-b39e-a959bd680587_1260x607.png)

[![](https://substackcdn.com/image/fetch/$s_!UXYI!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F63b14d13-25f0-4875-a830-5f4b3c7a3b7d_1045x1263.png)](https://substackcdn.com/image/fetch/$s_!UXYI!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F63b14d13-25f0-4875-a830-5f4b3c7a3b7d_1045x1263.png)

Wow these numbers look great for 200G per lane.

Let’s see the eye diagram.

Oh you only have a live demo for the 100G per lane version? Ok let’s see it.

[![](https://substackcdn.com/image/fetch/$s_!91Lb!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc4cc1b01-adb0-4419-8ce8-cf7adcf61f43_1583x1031.png)](https://substackcdn.com/image/fetch/$s_!91Lb!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc4cc1b01-adb0-4419-8ce8-cf7adcf61f43_1583x1031.png)

That is a decisively “mid” eye diagram.

Credit to them for actually showing this publicly.

 _(looking at you Marvell CPO department showing literally zero data)_

Hope Point2 makes improvements and brings 200G per lane product to market. Tech is really cool and wish them the best of luck.

### [5.h] Elyian

It looks great.

Bi-di electrical SerDes works using a precise analog circuit that uses phase shifters to subtract out the local Tx from the Rx.

Nvidia has a nice paper on it.

<https://research.nvidia.com/publication/2022-06_0297-pjbit-504-gbswire-inverter-based-short-reach-simultaneous-bidirectional>

[![](https://substackcdn.com/image/fetch/$s_!xGhm!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd7b46464-5499-4598-97cb-315a0febb03c_1090x873.jpeg)](https://substackcdn.com/image/fetch/$s_!xGhm!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd7b46464-5499-4598-97cb-315a0febb03c_1090x873.jpeg)

Marvell has a 64G D2D PHY that is conceptually very similar to both Nvidia and Elyian’s solutions.

Properly calibrating and controlling all these phase shifters is challenging. 

[![](https://substackcdn.com/image/fetch/$s_!KHIC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F92a786b0-e9be-4674-94d3-3d8646c8de68_1380x815.png)](https://substackcdn.com/image/fetch/$s_!KHIC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F92a786b0-e9be-4674-94d3-3d8646c8de68_1380x815.png)

[![](https://substackcdn.com/image/fetch/$s_!8DTJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe804ba09-424a-4196-92bf-668468011637_1447x848.png)](https://substackcdn.com/image/fetch/$s_!8DTJ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe804ba09-424a-4196-92bf-668468011637_1447x848.png)

[![](https://substackcdn.com/image/fetch/$s_!9n9l!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe10e1a52-e6bc-4433-9b5a-1aa13f353ff1_1239x820.png)](https://substackcdn.com/image/fetch/$s_!9n9l!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe10e1a52-e6bc-4433-9b5a-1aa13f353ff1_1239x820.png)

This is pretty good. Marvell claims higher BW/mm but they need **expensive advanced packaging.**

[![](https://substackcdn.com/image/fetch/$s_!EbPl!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5e817db1-585e-4673-a89f-216e271ef6ab_734x433.png)](https://substackcdn.com/image/fetch/$s_!EbPl!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5e817db1-585e-4673-a89f-216e271ef6ab_734x433.png)

To the best of my knowledge, Elyian’s claim of having industry leading density on standard package is correct.

Eye diagrams look great.

Excited to see these guys get design wins. 

## [6] Funny Shit

AMD had a marketing own-goal at OCP.

[![](https://substackcdn.com/image/fetch/$s_!zucr!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F74ea9459-066f-4ae4-aa52-064d61a20cd2_500x281.gif)](https://substackcdn.com/image/fetch/$s_!zucr!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F74ea9459-066f-4ae4-aa52-064d61a20cd2_500x281.gif)

Proudly on display was the Helios AI rack.

[![](https://substackcdn.com/image/fetch/$s_!dtg9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F43df6645-585e-426f-9a97-28651823b218_869x1271.png)](https://substackcdn.com/image/fetch/$s_!dtg9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F43df6645-585e-426f-9a97-28651823b218_869x1271.png)

But if you look closer… there are… other hardware vendors in this rack.

[![](https://substackcdn.com/image/fetch/$s_!Cctk!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe68d1028-3ba3-46e3-aeba-57a020880663_1694x1175.png)](https://substackcdn.com/image/fetch/$s_!Cctk!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe68d1028-3ba3-46e3-aeba-57a020880663_1694x1175.png)

That’s right… Nvidia 800G optical transceivers.

A hedge fund friend pointed this out to me when I met him. Couldn’t believe it. Went back to the show floor to see for myself. Tweeted out the pictures and it blew up way too much.

Apparently sell-side analysts were congregating in the Hillton hotel lobby trying to decipher what this means. 

Someone emailed me that pod monkeys were bidding up Fabrinet [FN 0.00%↑](https://substack.com/discover/stocks/FN) because of my joke tweet. 

[![](https://substackcdn.com/image/fetch/$s_!HusL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7db59bae-efea-456c-bcfc-7afdd1647b49_715x740.png)](https://substackcdn.com/image/fetch/$s_!HusL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7db59bae-efea-456c-bcfc-7afdd1647b49_715x740.png)

[![](https://substackcdn.com/image/fetch/$s_!HGNq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe07788e8-9dc2-4b3f-b6a8-263ae08305ad_838x840.png)](https://substackcdn.com/image/fetch/$s_!HGNq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe07788e8-9dc2-4b3f-b6a8-263ae08305ad_838x840.png)

What the fuck are you clowns doing?

Look at the transceiver manufacturing dates. 

**September 2022**

Transceivers over 3 years old.

Realistically, here is the most likely chain of events.

  1. AMD needs to put together a non-functional rack for the show floor.

  2. They need transceivers to complete the rack.

  3. Someone at AMD makes the ****hilarious**** mistake of using old Nvidia transceivers from 2022 that were originally purchased for competitive analysis and have been collecting dust for years.




 **This fiasco has zero engineering, investment, or strategic implications.**

 **It is hilarious. That’s it.**

AMD removed all the transceivers the day after my tweet.

[![](https://substackcdn.com/image/fetch/$s_!TBBd!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1b1617e1-c359-4f99-a7b8-e14ee8ff8101_604x1242.png)](https://substackcdn.com/image/fetch/$s_!TBBd!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1b1617e1-c359-4f99-a7b8-e14ee8ff8101_604x1242.png)

To all the tourists who commented saying _“Nvidia bought Mellanox”_ and _“Nvidia networking is good and companies do business with each other all the time.”_

Nvidia bought Mellanox in 2019.

There are at least 6 large and reputable 800G transceiver vendors AMD could have used for their NON FUNCTIONAL SHOWFLOOR DEMO RACK.

  1. Lumentum

  2. Coherent

  3. Accelink

  4. Innolight

  5. Eoptolink

  6. Cisco




All AMD had to do was ask a hyperscaler for a bucket of dead NON-NVIDIA transceivers for their Helios rack demo.

There is no way in hell AMD would ever use Nvidia transceivers in production. 

This is a hilarious marketing own-goal. Nothing more.

* * *

Keynotes and food service were held in a separate nearby building.

[![](https://substackcdn.com/image/fetch/$s_!g2bA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fff5d2835-efab-4ab2-ba43-21b223e6aa6b_1326x778.png)](https://substackcdn.com/image/fetch/$s_!g2bA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fff5d2835-efab-4ab2-ba43-21b223e6aa6b_1326x778.png)

[![](https://substackcdn.com/image/fetch/$s_!GA4C!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5f60074e-3506-4bf6-9f70-09a595fc5078_1612x1267.png)](https://substackcdn.com/image/fetch/$s_!GA4C!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5f60074e-3506-4bf6-9f70-09a595fc5078_1612x1267.png)

[![](https://substackcdn.com/image/fetch/$s_!teZm!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa8e96c1d-2e11-4d24-a152-c56c2bd374a5_1696x1229.png)](https://substackcdn.com/image/fetch/$s_!teZm!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa8e96c1d-2e11-4d24-a152-c56c2bd374a5_1696x1229.png)

A literal Meta GPU tent.

LOL

* * *

[![](https://substackcdn.com/image/fetch/$s_!my2D!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5209a5bc-c42e-4c3c-9810-c2ac7f19d94e_1144x645.png)](https://substackcdn.com/image/fetch/$s_!my2D!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5209a5bc-c42e-4c3c-9810-c2ac7f19d94e_1144x645.png)

Bloom Energy presenter spent 3 minutes giving a weird story about a rabbit riding a tortoise. I timed him. 

[![](https://substackcdn.com/image/fetch/$s_!TVF3!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbb17960b-323e-42ee-902a-df02115dacfc_1200x600.avif)](https://substackcdn.com/image/fetch/$s_!TVF3!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbb17960b-323e-42ee-902a-df02115dacfc_1200x600.avif)

* * *

Finally, we have this slide, which wins the award for “most useless slide of the conference”.

[![](https://substackcdn.com/image/fetch/$s_!TI85!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F75d40560-4578-42fb-a09f-c40e0ac40551_1137x641.png)](https://substackcdn.com/image/fetch/$s_!TI85!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F75d40560-4578-42fb-a09f-c40e0ac40551_1137x641.png)

Completely unreadable lol.

X XXX XX XXXX XXX XXX XX X XXX XX XXXXXX X XXXXXXXXX 

## [7] Public-Market Investment Corner

Shame on any pod monkeys who skipped direct to this section.

### [7.a] Updated Disclosures and Holdings

Reminder that trading account and long-only accounts are disclosed separately because updating manual spreadsheet is painful.

 **Long Only:**

[![](https://substackcdn.com/image/fetch/$s_!ApaU!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb1c4055b-87db-4870-90ae-730a0d578d7f_327x693.png)](https://substackcdn.com/image/fetch/$s_!ApaU!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb1c4055b-87db-4870-90ae-730a0d578d7f_327x693.png)

 **Trading:**

[![](https://substackcdn.com/image/fetch/$s_!DGmM!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fef2c1fc9-8e18-40d7-b75c-4df0f0c1a88f_1440x1058.webp)](https://substackcdn.com/image/fetch/$s_!DGmM!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fef2c1fc9-8e18-40d7-b75c-4df0f0c1a88f_1440x1058.webp)

[![](https://substackcdn.com/image/fetch/$s_!xx-h!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F60d6df97-c7e9-42cd-ba64-daf2fffc6ac4_709x1103.webp)](https://substackcdn.com/image/fetch/$s_!xx-h!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F60d6df97-c7e9-42cd-ba64-daf2fffc6ac4_709x1103.webp)

[![](https://substackcdn.com/image/fetch/$s_!kH-P!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff15c0afa-91d3-4cd0-867c-14bc01a50ec1_807x1102.webp)](https://substackcdn.com/image/fetch/$s_!kH-P!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff15c0afa-91d3-4cd0-867c-14bc01a50ec1_807x1102.webp)

[![](https://substackcdn.com/image/fetch/$s_!AuKn!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fef395e55-7ac9-4441-a602-6fecf399ecb8_1440x915.webp)](https://substackcdn.com/image/fetch/$s_!AuKn!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fef395e55-7ac9-4441-a602-6fecf399ecb8_1440x915.webp)

[![](https://substackcdn.com/image/fetch/$s_!YCNz!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F61710944-245d-4863-8e94-d40188b60a47_652x1103.webp)](https://substackcdn.com/image/fetch/$s_!YCNz!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F61710944-245d-4863-8e94-d40188b60a47_652x1103.webp)

### [7.b] Opinion by Ticker

[![](https://substackcdn.com/image/fetch/$s_!hf4P!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1f5c8957-58b8-4ce0-9ac6-970c40dc8be8_909x1037.png)](https://substackcdn.com/image/fetch/$s_!hf4P!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1f5c8957-58b8-4ce0-9ac6-970c40dc8be8_909x1037.png)

Subscribe for engineering-driven investment analysis.

Subscribe

Share?

[Share](https://irrationalanalysis.substack.com/p/ocp-global-summit-2025-irrational?utm_source=substack&utm_medium=email&utm_content=share&action=share)
