# Is NAND Flash a hidden AI play?

## Video models could drive explosive growth.

**Jul 08, 2024**

**Likes:** 0

# IMPORTANT:

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Please check the [‘about’ page](https://irrationalanalysis.substack.com/about) for a list of active positions.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice and readers should **always do their own research before investing in any security.**




* * *

Remember when Joanna Stern (WSJ) [interviewed](https://www.wsj.com/video/series/joanna-stern-personal-technology/openai-made-me-crazy-videosthen-the-cto-answered-most-of-my-questions/) OpenAI CTO Mira Murati on their ‘Sora’ video generative AI model?

[![](https://substackcdn.com/image/fetch/$s_!WuJ7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8ab1fb22-5092-4682-8f7f-0c202f35c50e_800x450.jpeg)](https://substackcdn.com/image/fetch/$s_!WuJ7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8ab1fb22-5092-4682-8f7f-0c202f35c50e_800x450.jpeg)

This glorious meme was inspirational… for a niche investment idea: NVMe SSDs.

* * *

# Contents:

  1. Why video model training may cause a NAND demand spike.

  2. What is NAND flash memory?

  3. State of the industry, featuring WDC’s lame 2024 investor event.

  4. NVMe: Components and Key Attributes

  5. The Players (Investment Vectors)

    1. Companies that also make DRAM

    2. WDC + Kioxia + Bain Capital Clown Show

    3. The Merchant Silicon Providers

  6. Conclusion and Risks

* * *




### [1] Why video model training may cause a NAND demand spike.

Why are we here (this particular corner of the public internet) today?

The answer is OpenAI Sora and the hilarious face CTO Mira Murati made when asked if the model was trained on YouTube video data.

 _(they definitely used YouTube data to train Sora)_

Also inspired by a discussion with [Pytorch to Atoms](https://open.substack.com/users/227854567-pytorch-to-atoms?utm_source=mentions). Check out their great content.

How though? YouTube has an API but data cannot be pulled live during training. Latency from pinging public Google datacenters would kill efficiency and MFU.

Full-resolution video also cannot be used effectively. OpenAI must have created a local repository of pre-processed YouTube data. Compressed, quantized, and (most importantly) **local.**

### [2] What is NAND flash memory?

NAND flash is non-volatile memory. This means when it loses power, the memory retains data. USB flash drives, SATA SSDs, NVMe SSDs, SD cards, and eMMC storage are all based on NAND flash.

[![](https://substackcdn.com/image/fetch/$s_!UJ_T!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe1ed96a6-b7ef-440e-add1-40f9b7270d12_1381x747.webp)](https://substackcdn.com/image/fetch/$s_!UJ_T!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe1ed96a6-b7ef-440e-add1-40f9b7270d12_1381x747.webp)

Essentially, a long string of transistors are used to store data. This data remains in the absence of a supply power because some transistors are in depletion mode.

[![](https://substackcdn.com/image/fetch/$s_!WBkX!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc86bff70-fb2d-4bfc-8918-6266b44666bc_602x452.jpeg)](https://substackcdn.com/image/fetch/$s_!WBkX!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc86bff70-fb2d-4bfc-8918-6266b44666bc_602x452.jpeg)

This means the transistor behaves like a short-circuit in the absence of a gate voltage. So always on without any power.

For more detailed information on the tech itself, check out this [excellent resource.](https://embeddedhardwaredesign.com/what-is-nand-flash-memory/#The_Architecture_of_NAND_Flash_Memory)

I don’t want to dwell on the technical details of NAND because of how degenerate this industry is. NAND truly is the bottom-feeding, shitco pity party of semiconductor. 

Key Concepts:

  * NAND is the most commoditized corner of semiconductor-land.

  * COST BASE IS EVERYTHING.

  * In general, more layers is better because it reduces cost.

  * Bit’s per cell (SLC, MLC, TLC, QLC) has interesting tradeoffs that you need to understand to follow industry presentations.

    * More bits per memory cell mean higher density (good) but lower write cycle endurance (bad) but much lower price (good).

    * Almost everything these days (2024) TLC with some QLC penetration.

    * Many drives have SLC caches to improve responsiveness. 

  * There is a huge difference between SATA and NVMe SSDs.

  * Components other than the NAND itself (logic controller, DRAM cache) have an outsized impact on drive performance.




### [3] State of the industry, featuring WDC’s lame 2024 investor event.

On June 10th, 2024, Western Digital ( [WDC 0.00%↑](https://substack.com/discover/stocks/WDC) ) held an [investor webinar](https://edge.media-server.com/mmc/p/w9a9b7wq/) titled _‘The New Era of NAND’._

A brief summary of the event is as follows:

We are a bunch of bottom-feeding losers and intend to not be losers in the future.

[![](https://substackcdn.com/image/fetch/$s_!uT4B!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa482b9fa-3d79-4ff8-b46e-594f84e8cf79_2626x1182.png)](https://substackcdn.com/image/fetch/$s_!uT4B!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa482b9fa-3d79-4ff8-b46e-594f84e8cf79_2626x1182.png)

Thier presentation is a good vector for explaining the state of the NAND industry. 

  * How NAND got here.

  * Why everyone is so malnourished, miserable, and traumatized.

  * Key technology trends over the last decade+.




[![](https://substackcdn.com/image/fetch/$s_!AovQ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F29b4a9be-c5f6-42dc-9da9-7a6dbf0904fe_2563x1173.png)](https://substackcdn.com/image/fetch/$s_!AovQ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F29b4a9be-c5f6-42dc-9da9-7a6dbf0904fe_2563x1173.png)

They last five years have been painful. 

[![](https://substackcdn.com/image/fetch/$s_!HV5u!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F12a028ac-7eff-4be2-9623-99225be0f804_2559x1282.png)](https://substackcdn.com/image/fetch/$s_!HV5u!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F12a028ac-7eff-4be2-9623-99225be0f804_2559x1282.png)

YMTC (China) has been flooding the global market with dirt cheap NAND while retaining profitability. Protectionist sanctions did not do much to slow them down.

[![](https://substackcdn.com/image/fetch/$s_!q46a!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff0fa614c-34e4-4395-85b3-5469211e8cd5_2551x1159.png)](https://substackcdn.com/image/fetch/$s_!q46a!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff0fa614c-34e4-4395-85b3-5469211e8cd5_2551x1159.png)

General complaints on CapEx intensity for the transition to 3D NAND.

[![](https://substackcdn.com/image/fetch/$s_!mqQE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F40c34273-8805-4d79-a555-319c5d886b1c_674x358.jpeg)](https://substackcdn.com/image/fetch/$s_!mqQE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F40c34273-8805-4d79-a555-319c5d886b1c_674x358.jpeg)

3D NAND stacks many layers (we are at 200+ now) to get huge density gains. Printing such complex structures is difficult. Companies like Lam Research, Tokyo Electron, Applied Materials, and so on have made great money selling tools to the bottom feeders. The NAND manufacturers themselves… no lol. 

[![](https://substackcdn.com/image/fetch/$s_!bsl7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa3110bf5-ed56-469e-ad7f-0fc67c414c75_2610x1227.png)](https://substackcdn.com/image/fetch/$s_!bsl7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa3110bf5-ed56-469e-ad7f-0fc67c414c75_2610x1227.png)

WD has been trying to push PLC (5-bit-per-cell) for quite some time. QLC has existing endurance and reliability challenges. 

An intuitive way for understanding why logical scaling harms endurance/durability is as follows.

  * With more bits per cell, you need to much more accuracy to charge and measure the cell voltage.

  * As the same cell is written/read from over time, the transistors degrade. Electrons get “stuck” in the cell. 

  * Eventually, a cell will be unable to reach all the necessary voltage states and must be disabled, permanently reducing product bit capacity.

  * Drive manufacturers must over-provision NAND as a reserve/backup for this inevitability, driving up cost.




[![](https://substackcdn.com/image/fetch/$s_!wuB1!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd9a48a32-dcde-483f-8720-74d2dca9c114_747x1150.png)](https://substackcdn.com/image/fetch/$s_!wuB1!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd9a48a32-dcde-483f-8720-74d2dca9c114_747x1150.png)

I find it amusing that WD spent a third of their presentation complaining about CapEx and promising to reduce future equipment spend while simultaneously hinging most of their technological differentiation on hybrid bonding.

[![](https://substackcdn.com/image/fetch/$s_!XdxQ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4fdfdd53-68e1-43ac-b585-4edc5b6080c5_2445x1168.png)](https://substackcdn.com/image/fetch/$s_!XdxQ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4fdfdd53-68e1-43ac-b585-4edc5b6080c5_2445x1168.png)

Allways nice to see a hyper-commoditized bottom-feeder claiming their business has entered a new era of premium pricing power.

The performance of products that use NAND flash heavily depends on DRAM caching and controller (built on logic node) quality. 

[![](https://substackcdn.com/image/fetch/$s_!3OsZ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F730abecd-980e-4d24-b13d-09ec3d754e57_2476x1183.png)](https://substackcdn.com/image/fetch/$s_!3OsZ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F730abecd-980e-4d24-b13d-09ec3d754e57_2476x1183.png)

EVERYTHING IS NEW EVERYONE. WE WILL NOT EAT SHIT IN THE INEVITABLE, VIOLENT DOWNCYCE. 

**Layers race is over!** WD has declared it so! YMTC, Micron, and Samsung definitely will not continue racing even though we are publicly begging everyone to slow down.

[![](https://substackcdn.com/image/fetch/$s_!j-es!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa7cd3262-b5bc-46de-b8fc-e32050be7efc_736x365.jpeg)](https://substackcdn.com/image/fetch/$s_!j-es!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa7cd3262-b5bc-46de-b8fc-e32050be7efc_736x365.jpeg)

### [4] NVMe: Components and Key Attributes

[![](https://substackcdn.com/image/fetch/$s_!9kti!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F67b73b72-e4d9-446a-9be6-55a8eb07ce84_678x354.png)](https://substackcdn.com/image/fetch/$s_!9kti!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F67b73b72-e4d9-446a-9be6-55a8eb07ce84_678x354.png)

Broadly speaking, there are three primary components to a solid-state drive:

  1. NAND flash chips

  2. DRAM cache

  3. Logic (interface) controller




Cheapo drives skip the DRAM cache and have terrible performance. Mid-tier drives use lower-quality controllers. 

Ironically, the NAND itself tends to have the least impact of the three on performance.

[![](https://substackcdn.com/image/fetch/$s_!i9nz!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F556a38a7-80bc-42d2-a3b9-1e02d0a2b46c_795x507.png)](https://substackcdn.com/image/fetch/$s_!i9nz!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F556a38a7-80bc-42d2-a3b9-1e02d0a2b46c_795x507.png)

Here is an example using two drives I happen to have in my primary machine. Both drives use 64-layer TLC NAND but the performance is widely different. This is due to the following differences:

  1. The NVMe drive is not limited by an ancient standard (SATA) that was designed for hard-drives.

  2. The NVMe drive has **double the ratio of DRAM** (cache) to NAND.

  3. The NVMe drive uses a **custom-made controller** with optimized firmware while the SATA drive uses an off-the-shelf merchant silicon controller.




In general, it is rare for real-world workloads to be sequential in nature. A sequential write is like copying a large file all at once. 

Most workloads are random and low-queue depth. This means the program (operating system, database, web browser, …) reads/writes in small 4-16 KB chunks randomly spread out across the memory. The software/filesystem tries to queue up several small tasks to speed up operation but is somewhat limited. 

Every workload is different. To properly evaluate drives for AI training workloads, it is necessary to profile the workload directly instead of relying on toy benchmarks or manufacturer-provided IOPS specifications.

The key takeaways are:

  1. NVMe is way better than SATA.

  2. The NAND flash itself has less impact compared to the DRAM cache and logic controller.




### [5] The Players (Investment Vectors)

[![](https://substackcdn.com/image/fetch/$s_!31ZE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6d4eef2e-12ef-4ba4-9757-5041e970b5fa_503x325.png)](https://substackcdn.com/image/fetch/$s_!31ZE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6d4eef2e-12ef-4ba4-9757-5041e970b5fa_503x325.png)

Comments on the TrendForce table:

  1. Solidigm was Intel’s Flash business before it got sold to SK Hynix.

  2. Kioxia was Toshiba Flash before it was spun out to Bain Capital.

  3. “Others” is dominated by YMTC who is likely severely undercounted because sanctions.




Broadly speaking, there are three categories the investment… _opportunities_ available to NAND degenerates. 

#### [5.a] Companies that also make DRAM

All memory is a commodity but not all commodities are created equal. DRAM is going through a super-cycle because of HBM supply-destruction via 3-5x area intensity. Samsung, SK, and MU stocks are all moving largely due to DRAM, not NAND. If you want to find an investment vector for NAND as a pure-play, these three are not it. 

[![](https://substackcdn.com/image/fetch/$s_!9Ozw!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1bfa87ab-69ed-46e1-8736-be9f79c15839_896x562.png)](https://substackcdn.com/image/fetch/$s_!9Ozw!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1bfa87ab-69ed-46e1-8736-be9f79c15839_896x562.png)

However, pure-plays are not necessarily the best. All good NVMe drives need DRAM cache. In theory, the companies that make both DRAM and NAND have an intrinsic advantage. 

#### [5.b] WDC + Kioxia + Bain Capital Clown Show

WDC and Kioxia (formerly Toshiba Flash) have a long, complicated history. 

Key Points:

  * Bain Capital owns Kioxia and is in deep ****.

  * SK Hynix is also a private shareholder of Kioxia.

  * WDC and Kioxia have had a technology partnership for many years.

    * BiCS flash.

    * Essentially, R&D is shared amongst these sub-scale shitcos.

  * WDC has been desperately trying to merge with Kioxia for YEARS.

    * Bain wants to unload bags.

    * SK Hynix opposes this merger.

    * WDC and Kioxia are self-aware and realize they are sub-scale.

    * This saga has been going on for so long that Bain is trying to IPO their bags.




> TOKYO, April 16 (Reuters) - Bain Capital has proposed an initial public offering (IPO) of Japan's Kioxia Holdings as part of a plan to allow the money-losing chipmaker to refinance a $5.8 billion loan coming due in June, according to a person familiar with the matter.
> 
> Bain and Kioxia met with a group of banks including Sumitomo Mitsui [(8316.T)](https://www.reuters.com/markets/companies/8316.T), Mizuho [(8411.T),](https://www.reuters.com/markets/companies/8411.T) and Mitsubishi UFJ [(8306.T)](https://www.reuters.com/markets/companies/8306.T), on Monday after the lenders urged Kioxia to come up with a recapitalisation plan because it looks likely to run afoul of the terms of a 900 billion yen ($5.8 billion) syndicated loan, the person said.
> 
> Formerly Toshiba Memory, Kioxia was acquired by a Bain-led group in a $18 billion carve-out in 2018. The maker of memory chips is expected to have posted a loss for the year that ended last month, according to the person. That would mark its second straight annual loss and push its net assets below the roughly 500 billion yen required under the terms of the loan, the person said.
> 
> The banks want the refinancing to pave the way for reviving merger talks with U.S. chipmaker Western Digital [(WDC.O)](https://www.reuters.com/markets/companies/WDC.O), according to the source.
> 
> Talks between the two to merge and create a memory chip powerhouse stalled last year due to opposition from South Korea's SK Hynix [(000660.KS)](https://www.reuters.com/markets/companies/000660.KS), which is an investor in Kioxia.
> 
> The banks had previously pledged to provide a loan of about 1.9 trillion yen on the condition that Kioxia would merge with Western Digital.
> 
> Source: [Reuters](https://www.reuters.com/technology/bain-proposes-ipo-japans-kioxia-clear-way-58-bln-loan-refinance-source-says-2024-04-16/)

#### [5.c] The Merchant Silicon Providers

Most drive manufactures make their own controllers.

[![](https://substackcdn.com/image/fetch/$s_!vMk7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcbd6b462-9eae-46ab-ae5a-7512000ab663_361x144.png)](https://substackcdn.com/image/fetch/$s_!vMk7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcbd6b462-9eae-46ab-ae5a-7512000ab663_361x144.png)Source: Irrational Analysis Mediocre Research

There are two big merchant silicon providers of NVMe controllers, Phison (TPEX:8299) and Silicon Motion ([SIMO 0.00%↑](https://substack.com/discover/stocks/SIMO)). 

A few other tiny players exist (Microchip, Marvell) but are not worth taking seriously for NVMe.

### [6] Conclusion and Risks

[![](https://substackcdn.com/image/fetch/$s_!42QM!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb6ed8c6c-4920-4686-a661-2c0712a1ab00_1436x2171.jpeg)](https://substackcdn.com/image/fetch/$s_!42QM!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb6ed8c6c-4920-4686-a661-2c0712a1ab00_1436x2171.jpeg)

Look at this graph.

NAND is not a good long-term investment. Terrible compared to every other sub-sector within semiconductor.

This chart puts into perspective all the cope WD presented in their “NEW ERA OF NAND” public therapy session.

However, NAND is an interesting opportunity right now because of AI driving almost all attention to HBM/DRAM, historically low bit growth, and a possible incoming **demand-shock driven by video model training.**

Good luck, have fun.

If you enjoyed this content, please consider subscribing.

Subscribe

Already subscribed? Thanks! Please consider sharing.

[Share](https://irrationalanalysis.substack.com/p/is-nand-flash-a-hidden-ai-play?utm_source=substack&utm_medium=email&utm_content=share&action=share)
