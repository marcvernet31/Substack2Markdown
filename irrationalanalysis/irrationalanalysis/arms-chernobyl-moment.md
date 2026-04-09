# ARM's Chernobyl Moment

## Incredibly self-destructive cancelation of Qualcomm's v8 ALA.

**Oct 23, 2024**

**Likes:** 0

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Please check the [‘about’ page](https://irrationalanalysis.substack.com/about) for a list of active positions.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice, and readers should **always do their own research before investing in any security.**

  * Feel free to contact me via email at: _irrational_analysis@proton.me_




* * *

The Chernobyl nuclear disaster was driven by the impatience of one man, [Anatoly Dyatlov](https://en.wikipedia.org/wiki/Anatoly_Dyatlov). Reactor number 4 was scheduled to be taken partially offline to test a safety feature. Dyatlov, an arrogant and overbearing man, was impatient. This test had already been delayed several times prior. On the early morning of April 26th, 1986, Dyatlov showed up to supervise.

Procedures called for a gradual reduction in power output. Unfortunately, this sequence was interrupted as [grid operators indicated they needed reactor #4’s power for a while longer.](https://world-nuclear.org/information-library/appendices/chernobyl-accident-appendix-1-sequence-of-events)

Dyatlov arrived at a reactor that was in a state unsuitable for the test he was determined to complete. He should have just waited.

[![Radioactive Survival Lessons from the Chernobyl Nuclear Disaster](https://substackcdn.com/image/fetch/$s_!kIcM!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faf894022-4e97-402e-91dc-44181ae62743_1100x914.jpeg)](https://substackcdn.com/image/fetch/$s_!kIcM!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faf894022-4e97-402e-91dc-44181ae62743_1100x914.jpeg)

* * *

On October 22nd, 2024, [Bloomberg reported](https://www.bloomberg.com/news/articles/2024-10-23/arm-to-cancel-qualcomm-chip-design-license-in-escalation-of-feud) that ARM has decided to cancel Qualcomm’s architectural license. From my reading and analysis of public court documents, it seemed clear that [ARM 0.00%↑](https://substack.com/discover/stocks/ARM) was going to win their lawsuit against [QCOM 0.00%↑](https://substack.com/discover/stocks/QCOM). 

Canceling the architectural license of your largest customer is extraordinarily destructive. Batshit insane. 

ARM had so many positive catalysts. A bright future where they control a robust earned monopoly in CPU with 98% gross margins. It’s all gone now. Contaminated in the fallout of a nuclear disaster of their own making. A disaster driven by impatience and hubris.

[![](https://substackcdn.com/image/fetch/$s_!Rabd!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd6ee1a26-41cf-4029-b3a3-934b355b7b1a_1023x1158.png)](https://substackcdn.com/image/fetch/$s_!Rabd!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd6ee1a26-41cf-4029-b3a3-934b355b7b1a_1023x1158.png)

RISC-V was in disarray, fragmented beyond recognition. [INTC 0.00%↑](https://substack.com/discover/stocks/INTC) and [AMD 0.00%↑](https://substack.com/discover/stocks/AMD) recently announced a hilarious x86 “advisory committee” out of fear and desperation. 

Why has ARM done this? 

* * *

# Contents:

  1. Background

  2. Impact to Qualcomm

  3. Impact to ARM

  4. A Gift from the Heavens to RISC-V

  5. Investment Thoughts




* * *

## [1] Background

If you want to understand what x86, RISC-V, and ARM (ISA) are, please read this old post.

[![Instruction Sets For Investors](https://substackcdn.com/image/youtube/w_728,c_limit/QMiubC6LdTA)

#### Instruction Sets For Investors

[Irrational Analysis](https://substack.com/profile/135313705-irrational-analysis)·October 7, 2023[Read full story](https://irrationalanalysis.substack.com/p/instruction-sets-for-investors)](https://irrationalanalysis.substack.com/p/instruction-sets-for-investors)

Based on Bloomberg reporting and my own understanding of the legal and technical aspects of this situation, I believe ARM has cancelled Qualcomm’s v8 ALA. This license was purchased well before the Nuvia acquisition.

Many companies purchase architectural licenses (ALA) from ARM even if they have no intention of using it to design their own CPU cores/microarchitectures. The purchase provides optionality and insurance… against getting sued.

Based on public information, it appears that Qualcomm had no serious CPU design activity from 2017 through 2021, despite the ALA. With the Nuvia acquisition, Qualcomm now had two ALAs (their own and Nuvia’s). According to public court documents, ARM quickly moved to cancel the Nuvia ALA.

We now have two distinct legal issues.

  1. Is the Nuvia IP (design, RTL code) transferable and valid under Qualcomm’s ALA?

  2. Does ARM have the right to cancel Qualcomm’s ALA due to breach of contract?




 **These orthogonal legal questions are the key to understanding what has motivated ARM to use the nuclear option on Qualcomm.**

## [2] Impact to Qualcomm

Qualcomm’s stock is probably going to tank tomorrow. Business will be unaffected so long as ARM does not gain an injunction.

The 2017-2019 legal battel between Qualcomm and Apple/Intel is instructive. Qualcomm accused Apple and Intel of modem IP theft and successfully got an injunction against iPhones with Intel modems in the EU and China. This means that Apple was banned from selling iPhones equipped with Intel chips in those regions.

If ARM gets such an injunction, it would be DEVESTATING. Revenue for the jurisdiction(s) goes to zero overnight.

Given that the trial is set to start in December anyway, I doubt any court would decide in favor of a ARM injunction. Disruption would be massive, and the trail is moving along anyway.

## [3] Impact to ARM

Devastating self-own. Every customer (excluding Nvidia and Apple) is going to start working on RISC-V migration with vigor.

Frankly, I still cannot believe ARM has done this. Canceling Qualcomm’s ALA two months before the trial is set to start is insane. They are probably (95% chance) going to win the trial!

 **Why have they done this?**

My original theory was that the new Snapdragon Elite smartphone chips (Nuvia Oryon V2 cores) were going to hit ARM’s upcoming quarterly result and guide. Qualcomm is ARM’s largest customer by royalty revenue. The previous smartphone chip (Snapdragon 8 Gen3) used ARM v9 Cortex cores under a TLA. Going from a v9 TLA to a v8 ALA is a double royalty hit. Based on public information and my own research, Qualcomm’s royalty rate per chip would drop from 4-5.5% down to 2-2.5%.

But a quarter or two of misses can’t possibly justify the radioactive hellfire ARM has unleashed tonight. 

There is a much better theory. Credit to [Ravi_711](https://x.com/ravi_711?lang=en) for bringing this idea to my attention. Oryon v2 is very good.

[![](https://substackcdn.com/image/fetch/$s_!wbQL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F69ee4cfc-7e3b-488b-a2e1-f9fbb3d89dc0_2694x1230.png)](https://substackcdn.com/image/fetch/$s_!wbQL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F69ee4cfc-7e3b-488b-a2e1-f9fbb3d89dc0_2694x1230.png)

So good that it seems to be a completely new microarchitecture. These power and performance numbers don’t look like a simple port from TSMC N4P to N3E. It can’t be just a minor design evolution of Oryon v1.

 **Oryon v2 appears to be a clean-sheet design by the Nuvia team after they joined Qualcomm.** If true, this implies this CPU IP is theoretically not covered in the lawsuit.

Here are the two orthogonal legal questions again:

  1. Is the Nuvia IP (design, RTL code) transferable and valid under Qualcomm’s ALA?

  2. Does ARM have the right to cancel Qualcomm’s ALA due to breach of contract?




If Oryon v2 was developed from the ground up without using any Nuvia IP, that would make it theoretically immune to legal question #1. 

Presumably, Qualcomm are not morons. They probably sequestered all Nuvia IP and started a clean-slate design sometime in 2021. Oryon v2 launching now (Jan 2025 really) would match a typical semiconductor product life cycle.

ARM seems to have realized this. They have plenty of discovery documents. Winning the lawsuit is now a moot point. So what if a < $200M worth of laptop chips with Oryon v1 are violating license terms. Tens of billions of dollars worth of smartphone chips with Oryon v2 are going to ship next year…. at a v8 ALA royalty rate!

ARM has apparently decided that legal question #1 does not matter anymore. Proving question #2 is the key to their strategy going forward.

## [4] A Gift from the Heavens to RISC-V

RISC-V has a serious fragmentation problem. Today was historic for two reasons:

  1. RISC-V adopted the RVA23 standard in an attempt to get their shit together.

  2. ARM lit themselves on fire.




There are several startups working on RISC-V who are subscribers here.

ARM HAS GIVEN YOU AN INCREDIBLE GIFT.

YOUR NUMBER ONE PRIORITY TOMORROW IS LEVERAGE THE CRAP OUT OF THIS NEWS AND MARKET LIKE CRAZY.

YOU WILL NEVER GET AN OPPERTUNITY LIKE THIS EVER AGAIN.

## [5] Investment Thoughts

I still own a tiny number of ARM shares in my long-only accounts. It’s less than 0.2% so not gona bother. Will be interesting to see what happens to those shares 10 years from now.

Doug from Fabricated knowledge at an excellent post this morning on Qualcomm

[![](https://substackcdn.com/image/fetch/$s_!tEdM!,w_56,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2Fac6587ae-db17-41fa-b25f-7dc0b7c601be_1000x1000.png)Fabricated KnowledgeIdea in SmartphonesRead morea year ago · 14 likes · 4 comments · Doug O'Laughlin](https://www.fabricatedknowledge.com/p/idea-in-smartphones?utm_source=substack&utm_campaign=post_embed&utm_medium=web)

Unfortunately, he got super unlucky with the timing lamo.

I was considering buying some QCOM call options last night for many of the same reasons and Doug’s post gave me the last push to initiate a small position this morning.

[![](https://substackcdn.com/image/fetch/$s_!-kvx!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F681abb07-37c4-49b5-b27f-e52e4cfe2c79_1439x287.jpeg)](https://substackcdn.com/image/fetch/$s_!-kvx!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F681abb07-37c4-49b5-b27f-e52e4cfe2c79_1439x287.jpeg)

Probably going to be down 60% tomorrow at open. 

Genuinely no idea what I am going to do. Cut losses or double down.

Setup is still good but ARM decided to blow everything up.

If you enjoyed this content, please consider subscribing. 

Subscribe

Already subscribed? Thanks! Please consider sharing.

[Share](https://irrationalanalysis.substack.com/p/arms-chernobyl-moment?utm_source=substack&utm_medium=email&utm_content=share&action=share)
