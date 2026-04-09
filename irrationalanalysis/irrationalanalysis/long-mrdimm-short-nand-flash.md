# Long MRDIMM, Short NAND Flash

## Bonus: Samsung DS-Memory epic fail coverage.

**Jan 05, 2025**

**Likes:** 0

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Please check the [‘about’ page](https://irrationalanalysis.substack.com/about) for a list of active positions.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice, and readers should **always do their own research before investing in any security.**

  * Feel free to contact me via email at: _irrational_analysis@proton.me_




* * *

Consider this an extended submission to the 2025 L/S fintwit contest.

[![](https://substackcdn.com/image/fetch/$s_!0Fpa!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9942c93f-01b0-44dc-bc8e-9d00f9c5255d_590x283.png)](https://substackcdn.com/image/fetch/$s_!0Fpa!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9942c93f-01b0-44dc-bc8e-9d00f9c5255d_590x283.png)https://x.com/schaudenfraud/status/1873859809285726262

[![](https://substackcdn.com/image/fetch/$s_!ywgm!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5da351fa-a0f1-4b56-a292-b9b971cf4d12_644x346.png)](https://substackcdn.com/image/fetch/$s_!ywgm!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5da351fa-a0f1-4b56-a292-b9b971cf4d12_644x346.png)

I have a [small] long [RMBS 0.00%↑](https://substack.com/discover/stocks/RMBS), short [WDC 0.00%↑](https://substack.com/discover/stocks/WDC) position right now. This is more out of intellectual interest than a desire to actually make money. Good learning opportunity. My track record with shorting is… not good.

 **Bonus:** Samsung DS-Memory epic fail coverage, Galaxy S25 edition.

# Contents:

  1. Long MRDIMM

    1. What are MRDIMMs?

    2. Individual Component Deep-Dive

      1. PMIC

      2. Temperature Sensor

      3. SPD Hub

      4. MDB

      5. MRDC

    3. Rambus: A pure-play levered to MRDIMM

  2. Short NAND Flash

    1. What is NAND Flash?

    2. Industry Vibe and Players

    3. Target: Western Digital

  3. History, charts, and a loose plan.

  4. Bonus: Samsung Internal Violence




* * *

## [1] Long MRDIMM

[![](https://substackcdn.com/image/fetch/$s_!BeIO!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fafd88b5f-7fe8-4bbd-8cdd-fd05006a7af9_2145x1040.png)](https://substackcdn.com/image/fetch/$s_!BeIO!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fafd88b5f-7fe8-4bbd-8cdd-fd05006a7af9_2145x1040.png)

MRDIMM is a special type of memory supported by the latest Intel x86 CPU platform, Granit Rapids.

Volume ramp is happening soon. AMD’s next generation (whatever is after Turin) will support MRDIMM now that the tech is making it into official JEDEC spec.

There is one publicly traded company that is (surprisingly) and epic pure-play specifically for MRDIMM.

Rambus.

[![server memory sticks falling down a fantasy rabbit hole](https://substackcdn.com/image/fetch/$s_!Spu5!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fceb52725-39c3-4a08-a2bf-b489d8312a90_1024x1024.jpeg)](https://substackcdn.com/image/fetch/$s_!Spu5!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fceb52725-39c3-4a08-a2bf-b489d8312a90_1024x1024.jpeg)

Follow me down the MRDIMM rabbit-hole.

### [1.a] What are MRDIMMs?

[![](https://substackcdn.com/image/fetch/$s_!K7Ap!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4371873e-582e-481e-a60b-8e9ac3afd97a_1485x835.png)](https://substackcdn.com/image/fetch/$s_!K7Ap!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4371873e-582e-481e-a60b-8e9ac3afd97a_1485x835.png)

MRDIMMs are special memory sticks that act as like two fake memory channels on the same stick.

 **Benefits:**

  1. Saves space on the motherboard.

  2. ~Doubles bandwidth assuming same base speed.

    1. This is not true for current (1st) generation MRDIMM.

    2. Regular DIMM runs at 6000-6400MT/s.

    3. MRDIMM gen1 runs at 2x 4400MT/s = 8800MT/s effective.

    4. MRDIMM gen2 will be at the full 12800MT/s effective speed.

  3. More density per RAM stick.




[![](https://substackcdn.com/image/fetch/$s_!qzbC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F186d55b3-1e1b-42c6-93b8-dc15a6009732_678x362.png)](https://substackcdn.com/image/fetch/$s_!qzbC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F186d55b3-1e1b-42c6-93b8-dc15a6009732_678x362.png)

[![](https://substackcdn.com/image/fetch/$s_!doxM!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe522b16a-7c31-4ff7-a352-4a2466c8a905_678x359.png)](https://substackcdn.com/image/fetch/$s_!doxM!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe522b16a-7c31-4ff7-a352-4a2466c8a905_678x359.png)

[![](https://substackcdn.com/image/fetch/$s_!6vdv!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbe84f26f-a456-4cb8-80e9-9a2a2853614e_678x355.png)](https://substackcdn.com/image/fetch/$s_!6vdv!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbe84f26f-a456-4cb8-80e9-9a2a2853614e_678x355.png)

### [1.b] Individual Component Deep-Dive

[Rambus had a press release](https://investor.rambus.com/press-releases/press-release-details/2024/Rambus-Unveils-Industry-First-Complete-Chipsets-for-Next-Generation-DDR5-MRDIMMs-and-RDIMMs-to-Deliver-Breakthrough-Performance-for-Data-Center-and-AI/default.aspx) less than three months ago:

[![](https://substackcdn.com/image/fetch/$s_!FiuO!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6c63df5f-e271-436d-b276-de2956644947_1251x657.png)](https://substackcdn.com/image/fetch/$s_!FiuO!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6c63df5f-e271-436d-b276-de2956644947_1251x657.png)

[![](https://substackcdn.com/image/fetch/$s_!FZnl!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F07d45334-55c1-43d5-94bc-8f6f109a5d41_480x241.jpeg)](https://substackcdn.com/image/fetch/$s_!FZnl!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F07d45334-55c1-43d5-94bc-8f6f109a5d41_480x241.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!tHbu!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc67e4bc4-3ef0-4f30-8400-ebec488e240e_1126x630.png)](https://substackcdn.com/image/fetch/$s_!tHbu!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc67e4bc4-3ef0-4f30-8400-ebec488e240e_1126x630.png)

[![](https://substackcdn.com/image/fetch/$s_!sFAb!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F435f50ba-c347-423d-829c-551d92eef21c_1113x613.png)](https://substackcdn.com/image/fetch/$s_!sFAb!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F435f50ba-c347-423d-829c-551d92eef21c_1113x613.png)

There are five categories of component needed for an MRDIMM. Rambus makes them all. 

#### [1.b.i] PMIC

Power-Managment ICs are not unique to MRDIMM.

[![Primer: Switching Regulators and VRMs](https://substackcdn.com/image/fetch/$s_!LGLi!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F830b151b-11ef-4aca-8523-7aba620c9276_1439x2822.jpeg)

#### Primer: Switching Regulators and VRMs

[Irrational Analysis](https://substack.com/profile/135313705-irrational-analysis)·November 15, 2024[Read full story](https://irrationalanalysis.substack.com/p/primer-switching-regulators-and-vrms)](https://irrationalanalysis.substack.com/p/primer-switching-regulators-and-vrms)

What makes a MRDIMM PMIC special is that it needs to be very small (not much room on the RAM stick) and it needs to deliver power to MANY chips.

The usual tactic of “just add more phases and bypass caps” is not viable.

Designing such an unusually dense PMIC is challenging. It is also a niche market so the usual suspects either don’t have a solution or made a lazy (low-quality) solution.

 _(speculation on my part. to know for sure I would need to probe RAM sticks with a multimeter)_

#### [1.b.ii] Temperature Sensor

[![](https://substackcdn.com/image/fetch/$s_!zzgF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe8caaf13-3664-4993-badd-772b9ee4828f_606x279.png)](https://substackcdn.com/image/fetch/$s_!zzgF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe8caaf13-3664-4993-badd-772b9ee4828f_606x279.png)

Temperature sensors are typically built with diodes or thermistors. Designing an accurate temperature sensor is not difficult. I am not sure why Rambus investor materials highlight this so much. 

#### [1.b.iii] SPD Hub

The Serial Presence Detect (SPD) hub is essentially a glorified I2C/I3C (basic debug IO) controller. This is easy to make. Boring.

#### [1.b.iv] MDB

Memory Data Buffer chips (MDB) are not storage devices. They are high-speed multiplexers.

[![](https://substackcdn.com/image/fetch/$s_!rCh0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0a2f5739-1f9b-40a6-be20-be525a65755d_1600x1171.jpeg)](https://substackcdn.com/image/fetch/$s_!rCh0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0a2f5739-1f9b-40a6-be20-be525a65755d_1600x1171.jpeg)

Trapezoid = Mux = Multiplexor

[![](https://substackcdn.com/image/fetch/$s_!z7CU!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fabcbaf0c-71a3-44e0-a802-6d91faed6469_419x350.png)](https://substackcdn.com/image/fetch/$s_!z7CU!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fabcbaf0c-71a3-44e0-a802-6d91faed6469_419x350.png)

[![](https://substackcdn.com/image/fetch/$s_!h7vS!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb760d49d-7608-47ce-bc59-a9e131acfc53_297x176.png)](https://substackcdn.com/image/fetch/$s_!h7vS!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb760d49d-7608-47ce-bc59-a9e131acfc53_297x176.png)

These are very simple devices, only 7-9 transistors.

The tricky part is how fast these transistors need to switch.

[![](https://substackcdn.com/image/fetch/$s_!6XZ2!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F76017b3a-c4f3-4f23-9217-69a33bca78f3_1652x798.jpeg)](https://substackcdn.com/image/fetch/$s_!6XZ2!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F76017b3a-c4f3-4f23-9217-69a33bca78f3_1652x798.jpeg)

MRDIMMs effectively operate at QDR. This means four data symbols per clock cycle.

Designing high-speed MUXes (~6GHz in this case) is non-trivial. Especially if there are power constraints.

It is likely that these MDB chips have buffer circuits or even a basic transimpedance amplifier to isolate impedance mis-match between the DDR chips on the module and the load (motherboard PCB + CPU package).

#### [1.b.v] MRCD

To understand the MRDC, we must first understand the vanilla registered clock driver (RCD).

[![](https://substackcdn.com/image/fetch/$s_!O-ZO!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6672dc85-24a8-490f-9485-c4fefc4fd746_950x506.jpeg)](https://substackcdn.com/image/fetch/$s_!O-ZO!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6672dc85-24a8-490f-9485-c4fefc4fd746_950x506.jpeg)

The RCD chip routes commands (requests from the host CPU) to the appropriate row of memory chips. Thus, only half of the memory chips on the stick are active at any one time.

A MRDC chip is the same concept except both of the memory “ranks” are active. This leads to a speedup in addition to capacity benefits of a regular RCD chip.

Imagine you have two plates of food in front of you. You could use one hand to eat from every other plate sequentially, or you could use both hands (one assigned to each plate) to shovel food into your mouth at twice the speed.

Rambus has a great video that explains this.

[![](https://substackcdn.com/image/fetch/$s_!0Peg!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc9757b69-d24b-4aa1-ab54-ffacb49657d9_454x401.png)](https://substackcdn.com/image/fetch/$s_!0Peg!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc9757b69-d24b-4aa1-ab54-ffacb49657d9_454x401.png)Foreshadowing… lol

At a high level, designing a MRDC chip has two primary challenges:

  1. Unusually fast switching frequency requirements for the transistors.

  2. Strict 1-cycle latency limit.




### [1.c] Rambus: A pure-play levered to MRDIMM

There are a few companies that make the various (non-DRAM) chips needed for an MRDIMM. Renesas (very diversified company) has a few relevant products for example.

What makes Rambus so interesting to me is that it is a pure-play just for MRDIMM. Their recent decisions have been an attempt to **financially engineer leverage to this factor.**

[![](https://substackcdn.com/image/fetch/$s_!ylcH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2579fe22-e67e-47d6-b793-8304eae68edf_767x1083.png)](https://substackcdn.com/image/fetch/$s_!ylcH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2579fe22-e67e-47d6-b793-8304eae68edf_767x1083.png)<https://www.rambus.com/cadence/>

A little over a year ago, Rambus sold their PHY IP assets to Cadence. This move was surprising to me at the time. Why sell PHY IP business but keep the controller IP?

Synopsys and Cadence both have controller IP they can bundle with PHY IP and EDA SaaS contracts/seats.

[![](https://substackcdn.com/image/fetch/$s_!hzpI!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff7180047-b62a-4373-af21-2d237eb163ad_889x596.png)](https://substackcdn.com/image/fetch/$s_!hzpI!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff7180047-b62a-4373-af21-2d237eb163ad_889x596.png)<https://www.synopsys.com/dw/ipdir.php?ds=dwc_hbm3_controller>

[![](https://substackcdn.com/image/fetch/$s_!tBbj!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F91ba3da6-bee0-4737-9822-2e3988b3089e_1114x957.png)](https://substackcdn.com/image/fetch/$s_!tBbj!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F91ba3da6-bee0-4737-9822-2e3988b3089e_1114x957.png)<https://www.cadence.com/en_US/home/tools/silicon-solutions/protocol-ip.html>

Rambus severely weakened their IP sales strength when they sold-off the PHY group. 

It is clear that they want to hard pivot to MRDIMM silicon and have tacitly abandoned IP altogether.

Simple digital IP is easy to port across process nodes. Low capital intensity. This is in stark contrast with analog IP (PHY) that needs new tape-outs (silicon) for each process node.

Rambus can easily use emulation platforms to keep porting their digital IP and make minor speed improvements. It’s a low-effort, high ROI strategy that will likely decay revenue slowly as the two EDA majors win sockets from bundling and integration.

Let’s take a more high-level overview of Rambus.

* * *

[![](https://substackcdn.com/image/fetch/$s_!fvT4!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffaf4c5bc-fff2-47a5-8beb-956f1facad05_1049x636.png)](https://substackcdn.com/image/fetch/$s_!fvT4!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffaf4c5bc-fff2-47a5-8beb-956f1facad05_1049x636.png)

We already discussed MRDIMM and what’s left of the IP business.

As the top comment on the Rambus YouTube video implied, Rambus has a history of patent trolling.

[![](https://substackcdn.com/image/fetch/$s_!iDdw!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F110b7791-7bba-465b-a177-51ff734f0870_1171x527.png)](https://substackcdn.com/image/fetch/$s_!iDdw!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F110b7791-7bba-465b-a177-51ff734f0870_1171x527.png)<https://www.rambus.com/rambus-files-patent-infringement-suit-against-nvidia/>

[![](https://substackcdn.com/image/fetch/$s_!jRJK!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F06736e72-89a9-482e-9fc2-4106b4529718_1176x751.png)](https://substackcdn.com/image/fetch/$s_!jRJK!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F06736e72-89a9-482e-9fc2-4106b4529718_1176x751.png)<https://www.rambus.com/court-declares-rambus-patents-in-suit-unenforceable-in-micron-delaware-case/>

[![](https://substackcdn.com/image/fetch/$s_!B3E6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F14ed8536-3b73-41bd-bc8f-df6761c7cd3f_1166x575.png)](https://substackcdn.com/image/fetch/$s_!B3E6!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F14ed8536-3b73-41bd-bc8f-df6761c7cd3f_1166x575.png)<https://www.rambus.com/rambus-wins-patent-infringement-trial-against-hynix/>

[![](https://substackcdn.com/image/fetch/$s_!YCEy!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Feb41fc06-d33e-42f2-a742-9a1190b5e4ac_878x980.png)](https://substackcdn.com/image/fetch/$s_!YCEy!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Feb41fc06-d33e-42f2-a742-9a1190b5e4ac_878x980.png)<https://www.reuters.com/article/us-rambus-patent-idUSTRE80Q24E20120127/>

[![](https://substackcdn.com/image/fetch/$s_!sRJj!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F13c9a772-e974-4733-a5bd-809cecd9b639_848x769.png)](https://substackcdn.com/image/fetch/$s_!sRJj!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F13c9a772-e974-4733-a5bd-809cecd9b639_848x769.png)<https://nvidianews.nvidia.com/news/u-s-patent-office-rejects-all-17-claims-in-three-rambus-patents-asserted-against-nvidia-in-international-trade-commission-action>

[![](https://substackcdn.com/image/fetch/$s_!s4xI!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9b47fb25-d29f-4017-aee6-7be62de27bf7_1210x1080.png)](https://substackcdn.com/image/fetch/$s_!s4xI!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9b47fb25-d29f-4017-aee6-7be62de27bf7_1210x1080.png)You know it’s bad when a Georg Bush Republican administration unanimously declares you has a monopoly.[ https://www.ftc.gov/news-events/news/press-releases/2006/08/ftc-finds-rambus-unlawfully-obtained-monopoly-power](https://www.ftc.gov/news-events/news/press-releases/2006/08/ftc-finds-rambus-unlawfully-obtained-monopoly-power)

[![](https://substackcdn.com/image/fetch/$s_!3XL3!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F17bd5d0d-686b-42c4-9654-6c4caba06b21_891x1051.png)](https://substackcdn.com/image/fetch/$s_!3XL3!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F17bd5d0d-686b-42c4-9654-6c4caba06b21_891x1051.png)<https://www.reuters.com/article/business/rambus-loses-antitrust-lawsuit-shares-plunge-idUSTRE7AF1XM/>

I am not going to bother making a nice Visio timeline of Rambus legal nonsense. They have a long track record and the business as it stands today will not grow. 

Let’s look at the most recent 10-Q filing. You know things are getting obscure when I bother to bring up official SEC filings lol.

[![](https://substackcdn.com/image/fetch/$s_!wl7M!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9a57b459-00d5-409d-9109-3fd00e537ad1_1023x418.png)](https://substackcdn.com/image/fetch/$s_!wl7M!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9a57b459-00d5-409d-9109-3fd00e537ad1_1023x418.png)

“Contract and other revenue” is the digital IP business Rambus has kept. The EDA majors will be leveraging PHY and SaaS contract bundling to win controller IP sockets from Rambus over time. For “security” IP, ARM will likely join the EDA majors in bundling and taking sockets from Rambus too. **Rambus management appears to be aware of this and has made a conscious decision to YOLO into MRDIMM chips (product revenue).**

Look at cost of revenue. The digital IP business is basically pure profit at 95% gross margin. Royalties (patent trolling) has zero cost of revenue as there is no line item.

So there is a super interesting situation now. The historical ultra-high gross margin businesses are either flat or decaying over time.

The product/MRDIMM chip business has 63% gross margins and is going to explode as Intel Granit Rapids ramps production and will explode again in ~12-18 months when Intel and AMD (and presumably ARM-based hyperscaler CPU chips) support next-gen 12800 MT/s MRDIMM.

This is a strange combination of businesses of an obscure small-cap company. Most financial analysts and professional investors probably don’t know what they are looking at here.

The tell is in how Rambus is presenting themselves in quarterly slide decks.

[![](https://substackcdn.com/image/fetch/$s_!BWap!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9462e4ca-5121-4ce0-b426-4a753edd28d1_1646x859.png)](https://substackcdn.com/image/fetch/$s_!BWap!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9462e4ca-5121-4ce0-b426-4a753edd28d1_1646x859.png)

[![](https://substackcdn.com/image/fetch/$s_!K6bi!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5bdcfbd9-2952-4d43-9853-abca55e46320_1668x930.png)](https://substackcdn.com/image/fetch/$s_!K6bi!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5bdcfbd9-2952-4d43-9853-abca55e46320_1668x930.png)

[![](https://substackcdn.com/image/fetch/$s_!Itjh!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5160602d-6bc5-4d4a-99e4-b4b7f8d61ef7_1647x931.png)](https://substackcdn.com/image/fetch/$s_!Itjh!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5160602d-6bc5-4d4a-99e4-b4b7f8d61ef7_1647x931.png)

They wont shut up about this 42% CAGR number. It’s as if Rambus investor relations is trying to scream the play right at you.

[![](https://substackcdn.com/image/fetch/$s_!JRUA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6f48aff8-50d1-46cf-b79f-1a25ab3e56d2_478x530.png)](https://substackcdn.com/image/fetch/$s_!JRUA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6f48aff8-50d1-46cf-b79f-1a25ab3e56d2_478x530.png)

## [2] Short NAND Flash

For the short leg of the fintwit stupid ideas long/short contest, I have chosen NAND flash. It is still memory but the worst, most degenerate segment of memory. 

### [2.a] What is NAND Flash?

[![Is NAND Flash a hidden AI play?](https://substackcdn.com/image/fetch/$s_!WuJ7!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8ab1fb22-5092-4682-8f7f-0c202f35c50e_800x450.jpeg)

#### Is NAND Flash a hidden AI play?

[Irrational Analysis](https://substack.com/profile/135313705-irrational-analysis)·July 8, 2024[Read full story](https://irrationalanalysis.substack.com/p/is-nand-flash-a-hidden-ai-play)](https://irrationalanalysis.substack.com/p/is-nand-flash-a-hidden-ai-play)

I have an old shitpost on this. To be clear, this thesis was intentionally bad and just a vector for me to use the “stressed Mira Murati” meme as a thumbnail.

Practically, you need to understand two concepts.

  1. NAND Flash has many layers. (we are at 150-300 layers right now)

  2. NAND Flash needs special equipment to print very deep high-aspect ratio holes.




[![](https://substackcdn.com/image/fetch/$s_!bRWb!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8d8d18b6-fcac-477e-8179-d62bd66790a0_700x383.jpeg)](https://substackcdn.com/image/fetch/$s_!bRWb!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8d8d18b6-fcac-477e-8179-d62bd66790a0_700x383.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!8xrg!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff70f563e-d9d0-4908-a0cb-94bd058dd6cf_1280x760.jpeg)](https://substackcdn.com/image/fetch/$s_!8xrg!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff70f563e-d9d0-4908-a0cb-94bd058dd6cf_1280x760.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!n6F2!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff150223b-b858-42dd-a7e6-0cf53d01dd1f_871x361.jpeg)](https://substackcdn.com/image/fetch/$s_!n6F2!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff150223b-b858-42dd-a7e6-0cf53d01dd1f_871x361.jpeg)High aspect ratio hole means deep and narrow with minimal deformities.

I try to avoid writing about semicap because Fabricated Knowledge and Semianalysis are much better. No value for me to add here.

Regardless, NAND semicap is in a much better position than the NAND manufacturers. To understand why, lets take a quick tour.

### [2.b] Industry Vibe and Players

[![](https://substackcdn.com/image/fetch/$s_!q0LC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F573ef460-0dff-49ac-9390-966f6c66804b_503x325.png)](https://substackcdn.com/image/fetch/$s_!q0LC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F573ef460-0dff-49ac-9390-966f6c66804b_503x325.png)

All three of the DRAM players make NAND flash too. YMTC (PRC company) is in “others” and is rapidly growing.

Given the recent Micron earnings, someone is clearly dumping NAND right now.

I thought YMTC was the offender, but it might be Samsung. Frankly, it does not matter.

[![](https://substackcdn.com/image/fetch/$s_!7hiZ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd6542c65-be1c-4bf5-b8c5-7fd357313462_598x605.png)](https://substackcdn.com/image/fetch/$s_!7hiZ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd6542c65-be1c-4bf5-b8c5-7fd357313462_598x605.png)https://x.com/Jukanlosreve/status/1873976316086936022 // https://www.trendforce.com/presscenter/news/20241231-12427.html

NAND is in a death spiral right now. Somebody is aggressively dumping into a cyclical downcycle driven by weak smartphone and PC markets. 

You know the situation is bad because Enterprise (datacenter) SSD has also peaked… as datacenter capex keeps getting revised up.

There are two pure-play-ish (its complicated) NAND companies, Western Digital and Kioxia.

[WDC 0.00%↑](https://substack.com/discover/stocks/WDC) has been desperately trying to merge with Kioxia for years. Due to a variety of reasons, this has not happened.

Instead, we are on the interesting timeline where Bain Capital (private equity bagholders) finally IPO-ed Kioxia. Simultaneously, Western digital is trying to split the NAND flash business from the (more stable and less masochistic) HDD business.

These two companies have a complicated relationship. [So complicated that there is a dedicated slide deck for this shit.](https://investor.wdc.com/static-files/324a167f-4256-4e06-9423-312136dbb4c2)

[![](https://substackcdn.com/image/fetch/$s_!048r!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F399e438d-1aa7-46d5-a446-578eccbb75fe_1658x921.png)](https://substackcdn.com/image/fetch/$s_!048r!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F399e438d-1aa7-46d5-a446-578eccbb75fe_1658x921.png)

[![](https://substackcdn.com/image/fetch/$s_!5LL8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Febaa608c-84c8-4d8d-bcf5-af6bad6e620b_1646x938.png)](https://substackcdn.com/image/fetch/$s_!5LL8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Febaa608c-84c8-4d8d-bcf5-af6bad6e620b_1646x938.png)

[![](https://substackcdn.com/image/fetch/$s_!cCs3!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9782af79-cf65-4e52-8188-b0dc002fea43_1661x932.png)](https://substackcdn.com/image/fetch/$s_!cCs3!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9782af79-cf65-4e52-8188-b0dc002fea43_1661x932.png)

[![](https://substackcdn.com/image/fetch/$s_!3-m3!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F28d17507-6344-4ad0-9c77-096b7503d505_1641x932.png)](https://substackcdn.com/image/fetch/$s_!3-m3!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F28d17507-6344-4ad0-9c77-096b7503d505_1641x932.png)

[![](https://substackcdn.com/image/fetch/$s_!MlJR!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2c2e1525-b351-4d02-9871-3f710c3cf4b9_1644x839.png)](https://substackcdn.com/image/fetch/$s_!MlJR!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2c2e1525-b351-4d02-9871-3f710c3cf4b9_1644x839.png)

This is financial engineering. I neither have the skillset nor motivation to parse this bullshit.

### [2.c] Target: Western Digital

There are three reasons why I chose to short [WDC 0.00%↑](https://substack.com/discover/stocks/WDC) over Kioxia.

  1. My trading account (Webull) does not have access to Japanese equities.

  2. I think enabling margin trading on Interactive Brokers significantly increases the probability I go bankrupt.

  3. Western Digital had a hilarious investor presentation (“New Era of NAND”) that **reeked of desperation and “loser energy”.**




[I have previously covered the WDC event. ](https://irrationalanalysis.substack.com/p/is-nand-flash-a-hidden-ai-play)Here is an updated/abridged version with superior entertainment value.

[![](https://substackcdn.com/image/fetch/$s_!7mfs!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F10134cf9-4502-42e1-9c7a-0858b4b156a9_969x1073.png)](https://substackcdn.com/image/fetch/$s_!7mfs!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F10134cf9-4502-42e1-9c7a-0858b4b156a9_969x1073.png)

 **June 10th, 2024:** Western Digital declares the layers race is over and they don’t need to spend more money on CapEx.

 **December 4th, 2024:** [Semiengineering article on how innovators](https://semiengineering.com/nand-flash-targets-1000-layers/) (not losers like Western Digital) are moving to 1,000 (~4-5x) layers within the next ~2 years.

## [3] History, charts, and a loose plan.

My goal for this contest is to construct an interesting and thematic long/short strategy. Plan is to learn. Making money off this would be nice but honestly mostly interested in learning more about how markets work for this one.

Pure-Play Memory Investment Vectors:

  * Good (balanced risk/reward)

    * HBM Advanced Packaging: [ONTO 0.00%↑](https://substack.com/discover/stocks/ONTO) and [CAMT 0.00%↑](https://substack.com/discover/stocks/CAMT)

    * Rambus via MRDIMM YOLO. **(selected for long)**

  * Dangerous (extreme risk/reward)

    * HBM manufacturers: [MU 0.00%↑](https://substack.com/discover/stocks/MU) and SK Hynix.

  * Neutral

    * Semicap majors with memory exposure such as [LRCX 0.00%↑](https://substack.com/discover/stocks/LRCX) and Tokyo Electron.

    * I try to avoid writing about semicap because Fabricated Knowledge and Semianalysis are much better. No value for me to add here.

  * Bad (short candidates)

    * Anyone with exposure to NAND flash lol.

    * Kioxia finally IPO after Bain Capital has been bagholding for years.

    *  **I choose[WDC 0.00%↑](https://substack.com/discover/stocks/WDC) for my short leg.**

    * Short-selling is illegal in South Korea.




[![](https://substackcdn.com/image/fetch/$s_!tEdM!,w_56,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2Fac6587ae-db17-41fa-b25f-7dc0b7c601be_1000x1000.png)Fabricated KnowledgeA Pure Play on Datacenter Memory and CXLRead more4 years ago · 8 likes · 8 comments · Doug O'Laughlin](https://www.fabricatedknowledge.com/p/a-pure-play-on-datacenter-memory?utm_source=substack&utm_campaign=post_embed&utm_medium=web)

[![](https://substackcdn.com/image/fetch/$s_!L6vM!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3d17e9d2-f2f0-4d76-a65e-5b044b3c30f2_1439x2822.jpeg)](https://substackcdn.com/image/fetch/$s_!L6vM!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3d17e9d2-f2f0-4d76-a65e-5b044b3c30f2_1439x2822.jpeg)Horizontal line based on Fabricated Knowledge coverage date.

[![](https://substackcdn.com/image/fetch/$s_!d8LZ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7e10768f-5cf9-49bd-a340-442432833a99_1440x3088.jpeg)](https://substackcdn.com/image/fetch/$s_!d8LZ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7e10768f-5cf9-49bd-a340-442432833a99_1440x3088.jpeg)

Charts look good. Only problem is that Western Digital is spinning out their NAND flash division soon. Not sure what happens to my borrowed shares in that case. If I have to cover and re-short the new garbage then so be it. Whatever.

## [4] Bonus: Samsung Internal Violence

Very surprised by this news TBH.

[![](https://substackcdn.com/image/fetch/$s_!G10c!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F43d1c1b2-5544-48a0-94ac-0a43163ee6ee_592x306.png)](https://substackcdn.com/image/fetch/$s_!G10c!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F43d1c1b2-5544-48a0-94ac-0a43163ee6ee_592x306.png)https://x.com/Jukanlosreve/status/1874756484493717774

The source material from Korean-language news sites is hilarious.

(obviously I used Google translate)

<https://dealsite.co.kr/articles/134327>

<https://mbiz.heraldcorp.com/article/10381688?ref=naver>

[![](https://substackcdn.com/image/fetch/$s_!lC7u!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1364d7ad-9467-4472-855c-a8624777db0e_836x373.png)](https://substackcdn.com/image/fetch/$s_!lC7u!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1364d7ad-9467-4472-855c-a8624777db0e_836x373.png)

[![](https://substackcdn.com/image/fetch/$s_!tRQS!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd8e9eb1e-9f2b-4cfe-ba82-a051a01f54d8_647x441.png)](https://substackcdn.com/image/fetch/$s_!tRQS!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd8e9eb1e-9f2b-4cfe-ba82-a051a01f54d8_647x441.png)

[![](https://substackcdn.com/image/fetch/$s_!pb2T!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6711467c-cbf4-405e-a741-fc1ee922f321_664x519.png)](https://substackcdn.com/image/fetch/$s_!pb2T!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6711467c-cbf4-405e-a741-fc1ee922f321_664x519.png)

[![](https://substackcdn.com/image/fetch/$s_!vvvw!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc94dafe5-f673-4df1-a327-6670e95123b1_502x246.png)](https://substackcdn.com/image/fetch/$s_!vvvw!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc94dafe5-f673-4df1-a327-6670e95123b1_502x246.png)

[![](https://substackcdn.com/image/fetch/$s_!KP7A!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0fbb874f-b6a0-48de-9bd5-feb689e6546b_478x229.png)](https://substackcdn.com/image/fetch/$s_!KP7A!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0fbb874f-b6a0-48de-9bd5-feb689e6546b_478x229.png)

This is hilarious. 

Obviously, Samsung DS-Memory knew that there was a risk of DX/MX moving volume to Micron. **What is incredible is that they played a game of chicken and lost.**

I think this news in a strong indicator that Samsung Electronics is finally at a breaking point.

  1. DX/MX cannot use overpriced DS LPDDRx because Qualcomm is raising application processor prices so much they would have **negative operating margins on the Galaxy Smartphones.**

  2. DS-Memory **cannot lower LPDDR5X prices further** because the product quality is terrible, and they are hemorrhaging DRAM share to CXMT.

  3. DS-LSI (Exynos) cannot deliver a product to balance Qualcomm’s price hikes because DS-Logic-Foundry has catastrophically failed multiple years in a row.




[![](https://substackcdn.com/image/fetch/$s_!8ksG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9d16849d-f17e-449e-a1a4-a740f1e5541e_220x165.gif)](https://substackcdn.com/image/fetch/$s_!8ksG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9d16849d-f17e-449e-a1a4-a740f1e5541e_220x165.gif)

Check out this piece by Jukanlosreve for more info on the drama.

<https://www.sammobile.com/opinion/dont-blame-tm-roh-hes-the-guardian-of-samsungs-galaxy/>

Subscribe for engineering-driven investment-analysis.

Subscribe

Share?

[Share](https://irrationalanalysis.substack.com/p/long-mrdimm-short-nand-flash?utm_source=substack&utm_medium=email&utm_content=share&action=share)
