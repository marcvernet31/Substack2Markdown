# Qualcomm should not buy any subset of Intel.

## Insane duplication and redundancy. Very little upside.

**Sep 22, 2024**

**Likes:** 0

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Please check the [‘about’ page](https://irrationalanalysis.substack.com/about) for a list of active positions.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice, and readers should **always do their own research before investing in any security.**

  * Feel free to contact me via email at: _irrational_analysis@proton.me_




* * *

We certainly live in interesting times.

[![](https://substackcdn.com/image/fetch/$s_!smCF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe6cc1b79-e31b-42c3-a7b5-39761678c67b_681x498.png)](https://substackcdn.com/image/fetch/$s_!smCF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe6cc1b79-e31b-42c3-a7b5-39761678c67b_681x498.png)

[![](https://substackcdn.com/image/fetch/$s_!o7ov!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe86b5839-cd0f-4ccb-ab3f-b0e56348b6c7_686x503.png)](https://substackcdn.com/image/fetch/$s_!o7ov!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe86b5839-cd0f-4ccb-ab3f-b0e56348b6c7_686x503.png)

The opposing spikes in stock price are because of a Wall Street Journal article published literally minutes before markets closed on a Friday.

[![](https://substackcdn.com/image/fetch/$s_!asKJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F94281265-8d24-466e-9bfc-51dcd8905179_664x374.png)](https://substackcdn.com/image/fetch/$s_!asKJ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F94281265-8d24-466e-9bfc-51dcd8905179_664x374.png)[Source: WSJ](https://www.wsj.com/business/deals/qualcomm-approached-intel-about-a-takeover-in-recent-days-fa114f9d)

[QCOM 0.00%↑](https://substack.com/discover/stocks/QCOM) has does a much smaller deal similar to what WSJ is describing, Veoneer. 

[![](https://substackcdn.com/image/fetch/$s_!24vA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd1450371-da2b-4935-ba34-75d77dc9d7a5_1107x1040.png)](https://substackcdn.com/image/fetch/$s_!24vA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd1450371-da2b-4935-ba34-75d77dc9d7a5_1107x1040.png)[Source](https://www.qualcomm.com/news/releases/2021/10/qualcomm-and-ssw-partners-reach-definitive-agreement-acquire-veoneer)

This was a $4.5B deal that ended up in Qualcomm paying something like $1B for the Arriver business in the end (the part of Veoneer they wanted).

Today’s news on a possible takeover of [INTC 0.00%↑](https://substack.com/discover/stocks/INTC) is literally 20x the size of the Veoneer deal in terms of market cap and several orders of magnitude higher in complexity.

As someone who has a massive short position against Qualcomm, I hope they pursue this crazy, idiotic, value destroying strategy and tank their own stock, allowing me to cover my short position at a hefty profit.

Setting aside financial biases, let’s talk about why I think this is a horrible idea for both Qualcomm and Intel. 

[![](https://substackcdn.com/image/fetch/$s_!T4QL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6c6e9024-de06-4896-9f4e-ea3e69188df8_855x477.png)](https://substackcdn.com/image/fetch/$s_!T4QL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6c6e9024-de06-4896-9f4e-ea3e69188df8_855x477.png)

## Contents:

  1. Most likely mechanics of a theoretical deal.

  2. Insane Redundancy and Anti-Synergy

    1. GPU

    2. DSP/NPU

    3. AI Software

    4. CPU Microarchitecture

    5. Competitive Positioning in PC

    6. Physical Design

    7. WiFi+Bluetooth

    8. O-RAN

  3. Possible Motives

    1. They really are that stupid. (1%)

    2. Public Trolling (99%)

* * *




### [1] Most likely mechanics of a theoretical deal.

There is no way Qualcomm wants to keep the Fabs. So that part of Intel would have to be spun out somehow. Let’s assume it is. (big assumption)

In public reporting, the Wall Street Journal and Bloomberg have implied that Qualcomm only wants to buy Intel’s consumer business (CCG, laptop/PC) and would prefer to sell the datacenter/server buisness.

This is not possible.

Huge portions of IP are used across CCG and DCAI. CPU cores (microarchitectures), NoC (ring/mesh), GPU cores and software (OneAPI), various accelerators like QAT, memory and interface (PCIe, Ethernet, EMIB, UCIe) PHY+PMA, …

 **It is literally impossible for anyone to buy only CCG from Intel and unload DCAI.**

So… with engineering reality in mind, any buyer of Intel Design (Qualcomm included) must buy ALL of Intel Design. Fabs can be sold off, but nothing else.

### [2] Insane Redundancy and Anti-Synergy

If Qualcomm bought Intel Design, the combined company would have crazy redundancy and multiple teams in direct conflict. Almost zero synergy. It’s like mixing an acid and a base. All you get is a violent bubbling, chaotic mess.

#### [2.a] GPU

Qualcomm Adreno is the best mobile GPU (sub 5 watt) on the market. Better than even Apple. With an excellent baseline of highly efficient performance, you would think a larger Adreno for laptops should be great right?

The problem is… Windows GPU drivers are a totally different beast when compared to Android. DirectX support, a wide variety of games, legacy API support, …

At the time of writing, Qualcomm’s Windows GPU drivers are bad. Unusably bad for the vast majority of games and GPU intensive applications.

Buying Intel Design (with the ARC GPU group included) will not fix this deficiency. ARC and Adreno are completely different architectures. There is no synergy!

A sane strategy would be to allocate like $300M in budget to higher as many Intel GPU employees as possible with generous signing RSU grants. Given the disaster that is [INTC 0.00%↑](https://substack.com/discover/stocks/INTC) stock, it would be easy to poach all the useful GPU driver engineers from Intel for cheap. 

#### [2.b] DSP/NPU

Another example where the Qualcomm solution (Hexagon) and Intel solution (Movidius) have completely different architectures.

Both are VLIW DSPs but the inner workings of a VLIW architecture are critical for designing the compiler stack. These complex compilers with vast libraries of hand-written assembly code routines/kernels will not combine into a “greater than the sum of their parts” software ecosystem. 

[![\[V\]ery \[L\]ong \[I\]ncoherent \[W\]riteup](https://substackcdn.com/image/fetch/$s_!lVhT!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1335e244-45bb-4add-a677-d9ab1ed74702_875x957.png)

#### [V]ery [L]ong [I]ncoherent [W]riteup

[Daud's Scout](https://substack.com/profile/135313705-dauds-scout)·February 24, 2024[Read full story](https://irrationalanalysis.substack.com/p/very-long-incoherent-writeup)](https://irrationalanalysis.substack.com/p/very-long-incoherent-writeup)

There is no way the Hexagon and Movidus teams would merge into anything remotely unified or coherant. 

#### [2.c] AI Software

Intel has many products that can target AI workloads.

  * AVX-512 Enabled CPU

  * AMX Enabled CPU

  * AMX Enabled GPU

  * Habana (dead)

  * Movidius DSP/NPU




Everything except Habana (which is dead) uses the OneAPI software framework.

Qualcomm has one hardware IP (Hexagon) that handles the vast majority of their AI acceleration. GPU and CPU occasionally pitch in but the Qualcomm “AI Stack” is mostly for Hexagon.

Merging the Qualcomm AI Stack and Intel OneAPI would be a disaster. These teams would fight and politically bicker to the death. 

#### [2.d] CPU Microarchitecture

Qualcomm bought their CPU microarchitecture team back in 2021 for $1.4B. This is a great team that has finally delivered their first commercial core (after some unfortunate delays from legal issues and other departments) and has a bright future ahead of them.

Intel has several CPU microarchitecture teams for P-cores and E-cores. A combined Qualcomm and Intel Products entity would be comically overstaffed in the CPU uarch department leading to massive OpEx inefficiencies. ARM (ISA) and x86 programs would have to be kept alive in parallel to support existing roadmaps. Very little would be transferable across the cores as the ISA determines how many sub-blocks (decoder, branch predictor, cache hierarchy) should be designed.

#### [2.e] Competitive Positioning in PC

Qualcomm has a slow start into their first real entrance into the laptop/PC market. 

Meanwhile, Intel has been hemorrhaging share to competitors and only recently stemmed the bleeding with Lunar Lake, by using a more expensive and advanced process node from TSMC.

This is something most of the normal media has missed or failed to highlight properly. Qualcomm X Elite and AMD Strix Point both use TSMC N4P (a 5nm-class node) while Intel Lunar Lake has the core compute on TSMC N3B (a much better 3nm-class node).

A lot of the performance and power efficiency delta is because Intel chose a much more expensive and advanced process node from TSMC.

If Qualcomm and AMD were excited to massively dilute their gross margins and not make money, they too would have used TSMC N3-family for medium-sized laptop chips.

 _Note: Qualcomm’s upcoming smartphone chips are on TSMC N3E because these chips are much smaller, and power is so important in that market._

 **Qualcomm does not need to buy Intel Design to supercharge their revenue growth in the laptop/PC market.**

The path forward is very simple and much cheaper than buying Intel design.

  1. Let Microsoft continue to improve their x86-64 emulator, which is already decent from my testing.

  2. Hire some more GPU driver engineers (for cheap from Intel) to fix the Adreno Windows drivers.

  3. Design a proper PMIC chip with the higher power draw of a laptop chip in mind instead of moronically forcing OEMs to place a huge number of inefficient PMIC chips designed for smartphone and paying them a $60 apology “marketing” subsidy that destroys operating margins.




Fix these problems and organic growth with massive shares gains from Intel Design will materialize in the next 18-24 months. 

#### [2.f] Physical Design

Qualcomm has one of the best physical design teams in the entire semiconductor industry. They have pulled of multiple emergency ports from failed Samsung Foundry process nodes to TSMC under enormous time pressure with high stakes. 

For financial and political reasons, Qualcomm will have to continue evaluating Samsung Foundry nodes, even if said nodes are a disaster. Need to throw a bone to your largest customer (Samsung MX) who has strong ties to Samsung DS (SS Foundry is a part of DS).

A company that has to port IP to all three major leading-edge logic foundries (TSMC, Samsung, Intel) would be overloaded. It would not go well!

#### [2.g] WiFi+Bluetooth

Qualcomm’s WiFi and Bluetooth (from a 2011 acquisition of Atheros) is very good. Industry leading in performance, power efficiency, and features with great RFFE synergy. 

The entire Intel Design WiFi+Bluetooth team would be 100% redundant and thus need to be fired in a possible merger.

#### [2.h] O-RAN

Traditional Telco edge processing has been done with FPGA’s and x86 CPUs. Intel has a huge market position with their Altera FPGAs and Xeon D CPUs.

Companies such as Qualcomm and Marvell are rapidly eating Intel Design’s lunch by making custom ASICs that are far more energy efficient, and performant, compared to the legacy Intel Design solutions.

[![](https://substackcdn.com/image/fetch/$s_!8jwA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F31cd207f-6cf1-432d-b1c7-548f5ef6f1be_1114x810.png)](https://substackcdn.com/image/fetch/$s_!8jwA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F31cd207f-6cf1-432d-b1c7-548f5ef6f1be_1114x810.png)

### [3] Possible Motives

In my opinion, there are only two possibilities. Let’s discuss them with an assigned probability for each.

#### [3.a] They really are that stupid. (1%)

Qualcomm management are complete idiots, with a [lower percentage of functional braincells than Samsung’s advanced-node yield at the Taylor, Texas Fab (10-20%).](https://www.trendforce.com/news/2024/09/12/news-samsungs-2nm-yield-rate-at-most-20-withdraws-personnel-from-texas-taylor-plant/)

[![Brainlet Meme Dump - meme post - Imgur](https://substackcdn.com/image/fetch/$s_!kCp6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0982a1ae-c054-4bcd-b4d4-fec88dc8b012_645x729.jpeg)](https://substackcdn.com/image/fetch/$s_!kCp6!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0982a1ae-c054-4bcd-b4d4-fec88dc8b012_645x729.jpeg)

#### [3.b] Public Trolling (99%)

Qualcomm CEO Cristiano Amon has a history of publicly trolling companies he does not like. 

For example, he told the [Financial Times](https://www.ft.com/content/eab1d19d-ab4c-45b7-88b4-f1f5e115d16e) that Qualcomm was interested in investing in ARM, consortium-style, after his company was the leader in sabotaging the sale of ARM to Nvidia.

[![](https://substackcdn.com/image/fetch/$s_!q8Cz!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F337e6891-5071-4fb1-94fc-815b9e024cbd_1087x967.png)](https://substackcdn.com/image/fetch/$s_!q8Cz!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F337e6891-5071-4fb1-94fc-815b9e024cbd_1087x967.png)He looks so happy, triggering ARM as they struggle to IPO while they build a legal case against him.

[![](https://substackcdn.com/image/fetch/$s_!7fdo!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb2a2a2cf-fb0e-44a6-9501-463eb191da5a_1042x171.png)](https://substackcdn.com/image/fetch/$s_!7fdo!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb2a2a2cf-fb0e-44a6-9501-463eb191da5a_1042x171.png)Source: The Financial Times, May, 2022

If you cross-refence the date of this FT article with public court documents, you will realize something really funny.

 **ARM and Qualcomm were already privately fighting each other over Nuvia license assignments when Cristiano Amon went rouge and floated this investment idea to the FT.**

When [ARM 0.00%↑](https://substack.com/discover/stocks/ARM) finally did go public, several companies (including Apple and Intel) did participate in the IPO as anchor investors. Not Qualcomm. 

Cristiano Amon is not a boring, vanilla CEO. He is spicy. He holds grudges. Those of you who follow mobile/wireless know that many Qualcomm executives continue hold a grudge against Intel because of their 4G/5G modems.

Unnamed Qualcomm sources leaking takeover Interest to the press as Intel is in a state of utter chaos is hilarious public trolling. Front-stabbing Intel with a daggar made of salt, coated in pure capsaicin crystals.

[![](https://substackcdn.com/image/fetch/$s_!79wu!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F56851e9a-3e58-45e4-8fca-83dcca3c6585_1048x1185.png)](https://substackcdn.com/image/fetch/$s_!79wu!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F56851e9a-3e58-45e4-8fca-83dcca3c6585_1048x1185.png)

If you enjoyed this content, please consider subscribing.

Subscribe

Already subscribed? Thanks! Please consider sharing.

Subscribe
