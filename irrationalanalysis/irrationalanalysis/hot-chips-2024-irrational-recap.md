# Hot Chips 2024: Irrational Recap

## Remember this conference. Bubble gets bigger.

**Sep 02, 2024**

**Likes:** 0

# IMPORTANT:

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Please check the [‘about’ page](https://irrationalanalysis.substack.com/about) for a list of active positions.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice, and readers should **always do their own research before investing in any security.**

  * Feel free to contact me via email at: _irrational_analysis@proton.me_




* * *

[Hot Chips](https://hotchips.org) is an annual semiconductor engineering conference. A three-day event with lots of exciting presentations from large companies, academia, and startups.

I will cover all interesting portions of the conference in this post, loosely grouping and ordering presentations by sentiment.

 **Note:** _You should probably read this one from a web browser. Email will almost certainly be clipped._

  1. Excellent

    1. Broadcom Co-Packaged Optics

    2. Meta Recommendation Inference ASIC

    3. Tesla Transport Protocol — Ultra-Dumb NIC

  2. Good

    1. Qualcomm Oryon CPU

    2. IBM Telum 2

    3. Tutorial: AI for Hardware Design

    4. Tutorial: Liquid Cooling

    5. Poster: Radix-8 FFT Accelerator

  3. Meh

    1. Intel Lunar Lake

    2. Intel Edge Xeon

    3. Enfabrica 

    4. Intel Silicon Photonics

    5. SambaNova

    6. FuriosaAI RNGD

    7. Frore AirJet

  4. Bad

    1. Tenstorrent 

    2. Nvidia Blackwell Advertisement Re-run

    3.  **Literally Every Single AMD Presentation**

    4. Cerebras Inference Pipedreams

    5. Microsoft Maia

    6. Intel Gaudi 3 (is already dead)

    7. Tutorial: Qualcomm On-Device AI

    8. Phononic Solid-State Cooling

  5. Dumpster Fire

    1. Ampere Computing

    2. SK Hynix In-Memory Compute

  6. Terrifying — Trevor Cai, the OpenAI Guy

    1. Excellent Technical Material

    2. “Sometimes lines really do go up” 

      1. Solar Panels

      2. Moore’s Law

    3. Surreal Bubble Inflation

  7. Winners and Losers




* * *

## [1] Excellent:

Excellent presentations deserve special commendation for a combination of rich technical material, high-impact products, and overall delivery.

### [1.a] Broadcom Co-Packaged Optics

[![](https://substackcdn.com/image/fetch/$s_!h9tC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fefef4c31-c92e-4506-b8b8-705a7be11455_2364x1307.png)](https://substackcdn.com/image/fetch/$s_!h9tC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fefef4c31-c92e-4506-b8b8-705a7be11455_2364x1307.png)

Prior to this presentation, co-packaged optics were a 2028 technology in my opinion. Broadcom’s incredible presentation changes everything. It looks like 2026 high-volume production is highly likely.

Reliability and serviceability have always been a major concern with CPO. Broadcom has moved the laser source to a pluggable front-end as that is the most failure-prone component. It also has temperature sensitivity which can be adequately controlled/cooled in the front panel. The presenter exuded confidence that this form of CPO (front panel laser, everything else integrated) is meets reliability and serviceability requirements for massive scale deployments.

[![](https://substackcdn.com/image/fetch/$s_!vu1b!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3733372d-4df8-486a-bea6-38cb865fe777_2397x1337.png)](https://substackcdn.com/image/fetch/$s_!vu1b!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3733372d-4df8-486a-bea6-38cb865fe777_2397x1337.png)

All the photonic components are integrated into a photonics IC (PIC) and hybrid-bonded to the electrical IC using Fan-out Wafer-level Packaging. Yields are apparently very good.

[![](https://substackcdn.com/image/fetch/$s_!kKcv!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffba7ad71-7cc4-4126-9fab-2040bbc6e2a6_2371x1283.png)](https://substackcdn.com/image/fetch/$s_!kKcv!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffba7ad71-7cc4-4126-9fab-2040bbc6e2a6_2371x1283.png)

Importantly, **everything on the package is silicon.** The process node for the PIC and EIC are of course different, but both are silicon-based processes. Manufacturing, packaging, and test are all mature, leading to high yields.

[![](https://substackcdn.com/image/fetch/$s_!GsWF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F21204375-fb03-4b5b-a6ed-d3d28ec40226_1547x876.png)](https://substackcdn.com/image/fetch/$s_!GsWF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F21204375-fb03-4b5b-a6ed-d3d28ec40226_1547x876.png)

Look at how clean these SEM cross-sections are!

[![](https://substackcdn.com/image/fetch/$s_!o_Bh!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2fe6a5cc-2fe8-4f67-9772-5bc223eb2857_1563x859.png)](https://substackcdn.com/image/fetch/$s_!o_Bh!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2fe6a5cc-2fe8-4f67-9772-5bc223eb2857_1563x859.png)

CPO enables much higher radix (number of ports per switch chip), allowing for simpler network topologies. Less layers in the network means massive cost and power savings.

[![](https://substackcdn.com/image/fetch/$s_!-0F3!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F617b2d96-ddd5-4470-a397-6e2776692f59_1555x861.png)](https://substackcdn.com/image/fetch/$s_!-0F3!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F617b2d96-ddd5-4470-a397-6e2776692f59_1555x861.png)

The demo is incredible. They did not try to hide minor flaws. **Transmitter linearity is failing (needs to be >= 0.95) and they still showed the results! **Eye is super clean considering every lane is in loopback and active, acting as aggressors dumping noise into the lane under test. Power of 4.8 watts per lane is super amazing.

[![](https://substackcdn.com/image/fetch/$s_!_Hfo!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F605ab480-5b53-4238-b62a-c3ddd22a85ca_1561x868.png)](https://substackcdn.com/image/fetch/$s_!_Hfo!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F605ab480-5b53-4238-b62a-c3ddd22a85ca_1561x868.png)

FEC data for every single port on a production-quality part!

[![](https://substackcdn.com/image/fetch/$s_!Lbmg!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa691677a-974d-44e2-91e7-9683ef8f152b_1554x863.png)](https://substackcdn.com/image/fetch/$s_!Lbmg!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa691677a-974d-44e2-91e7-9683ef8f152b_1554x863.png)

They even showed some optimized in-progress lab results where they almost have threshold 3 error free. 

[![](https://substackcdn.com/image/fetch/$s_!xWAH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F34f9606f-499b-40f7-8cc9-c348ee8dc1c2_730x400.png)](https://substackcdn.com/image/fetch/$s_!xWAH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F34f9606f-499b-40f7-8cc9-c348ee8dc1c2_730x400.png)

Suppose you have a link with a raw bit-error-rate (BER) of 1e-8. With forward-error-correction, you want to get that to 0, error free, even if there are burst errors in the system. This is very difficult. High-speed Ethernet SerDes typically use [Reed-Solomon error correction](https://en.wikipedia.org/wiki/Reed%E2%80%93Solomon_error_correction) which can be configured.

A heavy FEC configuration adds more parity data, reducing use-space data transmission but enabling greater error detection and correction capabilities.

Ideally, you want the physical layer (PHY) to be as error-free as possible to enable running a lighter FEC config, providing more usable data bandwidth. 

Broadcom has shown that with some lab optimizations, they only have two ports with uncorrectable errors at symbol threshold 4, with the rest at symbol threshold 3.

 **This is very good.** If they get all ports to 0 uncorrectable (error free) at symbol threshold 3 then this product is ready for high-volume production.

I cannot overstate how kickass this is. They are showing real, high-quality, raw data and saying, _“yea we gona fix this in ~1 year and crush all you fools”_.

[![](https://substackcdn.com/image/fetch/$s_!mS37!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F186f5371-54b9-4425-b9f3-84d49b0ee1b4_1097x623.jpeg)](https://substackcdn.com/image/fetch/$s_!mS37!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F186f5371-54b9-4425-b9f3-84d49b0ee1b4_1097x623.jpeg)

This news is terrifying for [MRVL 0.00%↑](https://substack.com/discover/stocks/MRVL) , who is heavily dependent on oDSP revenue. 

[![](https://substackcdn.com/image/fetch/$s_!9MIa!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fba83f2d6-e80d-436e-b9f6-0339dc5be828_1558x871.png)](https://substackcdn.com/image/fetch/$s_!9MIa!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fba83f2d6-e80d-436e-b9f6-0339dc5be828_1558x871.png)Marvell DSP revenue goes bye bye in 2026. 😈

[![](https://substackcdn.com/image/fetch/$s_!LQ96!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F953f3de0-d4d0-4c9c-b352-738f0b30b8d5_371x395.png)](https://substackcdn.com/image/fetch/$s_!LQ96!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F953f3de0-d4d0-4c9c-b352-738f0b30b8d5_371x395.png)

### [1.b] Meta Recommendation Inference ASIC

This chip is designed to accelerate recommendation network inference. A major feature of recommendation networks is the large embedding tables. Basically, this Meta chip is a true ASIC, extremely cost-optimized, high-performance inference of once specific flavor of neural network, not that good for anything else.

[![](https://substackcdn.com/image/fetch/$s_!JiiQ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F60c22d21-d1d1-49f0-a526-fead6e72cd35_2357x1213.png)](https://substackcdn.com/image/fetch/$s_!JiiQ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F60c22d21-d1d1-49f0-a526-fead6e72cd35_2357x1213.png)

Notice the LPDDR5. They have a brilliant solution to this bandwidth bottleneck while maintaining the cost and power savings enabled by LPDDR vs HBM.

[![](https://substackcdn.com/image/fetch/$s_!Wivd!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd56dd0de-5644-4635-bf85-101f62201c53_2363x1260.png)](https://substackcdn.com/image/fetch/$s_!Wivd!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd56dd0de-5644-4635-bf85-101f62201c53_2363x1260.png)

Very heavy on the SRAM. Custom mesh.

[![](https://substackcdn.com/image/fetch/$s_!LXE8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F113064d3-1d6f-4445-b294-73b2f88fd1db_2378x1263.png)](https://substackcdn.com/image/fetch/$s_!LXE8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F113064d3-1d6f-4445-b294-73b2f88fd1db_2378x1263.png)

Cheapo RSIC-V control cores to save money and avoid paying the ARM tax. Good move for such a cost-optimized, internal-only chip.

Both the PCIe PMA and RISC_V CPU cores get a nice chunk of dedicated SRAM to make sure workloads are configured quickly.

[![](https://substackcdn.com/image/fetch/$s_!ZSWJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5133126d-0312-4a31-9c10-4d17177c1ed0_2379x1264.png)](https://substackcdn.com/image/fetch/$s_!ZSWJ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5133126d-0312-4a31-9c10-4d17177c1ed0_2379x1264.png)

There are two networks-on-chip (NoC), one for data and another for configuration. This is surprising. Never seen this before. Physical design routing of these two NoCs (both have to connect to each processing element) must have been challenging. 

Dedicated data and config NoCs probably help a lot with the programming model. Don’t have to worry about collisions between kernels and data.

[![](https://substackcdn.com/image/fetch/$s_!F5hn!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbc254697-ffef-40b4-b4a4-494ae99d7f50_2370x1278.png)](https://substackcdn.com/image/fetch/$s_!F5hn!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbc254697-ffef-40b4-b4a4-494ae99d7f50_2370x1278.png)

RISC-V again for maximum customization, power saving, and not paying money to [ARM 0.00%↑](https://substack.com/discover/stocks/ARM) in a cost-optimized, internal-only project.

[![](https://substackcdn.com/image/fetch/$s_!64DF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc4f3b850-5340-4b01-baeb-c3ef4b4cf9ff_2372x1263.png)](https://substackcdn.com/image/fetch/$s_!64DF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc4f3b850-5340-4b01-baeb-c3ef4b4cf9ff_2372x1263.png)

There is hardware-level support for some micro-quantization. It is unclear if these are MX compliant. In Q&A the presenters admitted that none of these fancy quantization methods are currently in use within Meta’s production datacenters even though the chip was put into production in Q1 2024.

[![](https://substackcdn.com/image/fetch/$s_!TSFt!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F65eb7cab-faba-4afa-bf6b-8cc5478f57d4_2337x1274.png)](https://substackcdn.com/image/fetch/$s_!TSFt!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F65eb7cab-faba-4afa-bf6b-8cc5478f57d4_2337x1274.png)GPUs are very bad at Huffman-code based decompression due to variable-length codewords.

[![](https://substackcdn.com/image/fetch/$s_!FZOI!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa8d7fe8e-f9e2-4d68-aa14-0d4bb91d6e59_2312x1250.png)](https://substackcdn.com/image/fetch/$s_!FZOI!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa8d7fe8e-f9e2-4d68-aa14-0d4bb91d6e59_2312x1250.png)

In order to compensate for the mediocre bandwidth of LPDDR5, Meta added a dedicated on-die decompression engine. Super-lossless compression at a 50% ratio.

[![](https://substackcdn.com/image/fetch/$s_!gEOy!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F09698f6a-09a0-417f-865f-fd611d3c2560_2346x1257.png)](https://substackcdn.com/image/fetch/$s_!gEOy!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F09698f6a-09a0-417f-865f-fd611d3c2560_2346x1257.png)

Accelerators and compress, transmit, and decompress data to one another at lightning speed over PCIe because of the hardware compression engines. CXL-based memory expansion adds an additional giant pool of memory.

[![](https://substackcdn.com/image/fetch/$s_!povT!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F17af5bd1-1566-4a86-b599-112d61bd5361_2340x1259.png)](https://substackcdn.com/image/fetch/$s_!povT!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F17af5bd1-1566-4a86-b599-112d61bd5361_2340x1259.png)

Some hand-optimization of data blocking within SRAM partitions is needed to squeeze all the performance out of this chip. This is likely why the control and data are on dedicated NoCs. 

### [1.c] Tesla Transport Protocol — Ultra-Dumb NIC

Before getting into the presentation, I want to take a moment to call out the speaker himself, Eric Quinnell.

Without a doubt, he was the best presenter at Hot Chips 2024.

  * High energy delivery.

  * Comedy routine.

    * Multiple really funny jokes that got audible laughter from the audience.

    * Self-deprecation that hammers-home the objective of TTPoE.

  * Brought props on a table to show everyone what the hardware looks like.

  * Excellent technical explanation.




[![](https://substackcdn.com/image/fetch/$s_!NSvK!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6745c506-fb8d-4d78-a53d-48f5f84a0a30_2391x1327.png)](https://substackcdn.com/image/fetch/$s_!NSvK!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6745c506-fb8d-4d78-a53d-48f5f84a0a30_2391x1327.png)

[![](https://substackcdn.com/image/fetch/$s_!ACwL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbe417ceb-d66b-425d-9fa1-a2eef5b5856a_2385x1335.png)](https://substackcdn.com/image/fetch/$s_!ACwL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbe417ceb-d66b-425d-9fa1-a2eef5b5856a_2385x1335.png)

A hardware-based TCP implementation… interesting. How?

[![](https://substackcdn.com/image/fetch/$s_!2I15!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F46cf577b-dd40-4712-9546-6df4def9d86f_1646x928.png)](https://substackcdn.com/image/fetch/$s_!2I15!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F46cf577b-dd40-4712-9546-6df4def9d86f_1646x928.png)

[![](https://substackcdn.com/image/fetch/$s_!rMpc!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fce4ee248-cc3c-452d-8478-26dd48e6deff_1677x947.png)](https://substackcdn.com/image/fetch/$s_!rMpc!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fce4ee248-cc3c-452d-8478-26dd48e6deff_1677x947.png)

A state-machine implemented with physical memory only on a cheap-ass FPGA. 

Some banger lines from the talk:

  * Dojo lost its Mojo.

  * We want the dumbest NIC. No OS, no CPU cores, no nothing.

  * PCIe Gen3 x16 is enough to push 100Gbps Ethernet and is cheap. We love cheap.

  * DDR4 is cheap. Cheap is great.

  * We want to sprinkle these dumb NICs everywhere. SO CHEAP!!!!




This solution is cost optimized, awesome, and hilarious. 

[![](https://substackcdn.com/image/fetch/$s_!R6P7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe2b4abe2-039f-4a30-ba2f-16debde6280b_1659x931.png)](https://substackcdn.com/image/fetch/$s_!R6P7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe2b4abe2-039f-4a30-ba2f-16debde6280b_1659x931.png)

These ultra-dumb NICs act as nodes on the DIP (Dojo interface processor) network to allow flexible scaling.

[![](https://substackcdn.com/image/fetch/$s_!N6Co!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1518cdb2-f2d0-47e1-8155-eb75a3c67c0f_1661x934.png)](https://substackcdn.com/image/fetch/$s_!N6Co!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1518cdb2-f2d0-47e1-8155-eb75a3c67c0f_1661x934.png)

They have a 4 exaflop engineering/testing system. LOL

[![](https://substackcdn.com/image/fetch/$s_!1iFY!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3260ef19-a80a-4f98-ab51-080b36445f52_1652x926.png)](https://substackcdn.com/image/fetch/$s_!1iFY!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3260ef19-a80a-4f98-ab51-080b36445f52_1652x926.png)

Donating the spec to Ultra Ethernet! Bravo!

[![](https://substackcdn.com/image/fetch/$s_!epID!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F585f5a93-5f32-4d3a-a057-5fefb02cefe2_1659x931.png)](https://substackcdn.com/image/fetch/$s_!epID!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F585f5a93-5f32-4d3a-a057-5fefb02cefe2_1659x931.png)

The latency bar chart is on log scale. Absolutely crushed the design goals. Congratulations to every person who worked on this feat of engineering.

[![](https://substackcdn.com/image/fetch/$s_!dhd4!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbcf7f81f-3f1f-4e52-b391-e491ae4cce7d_893x912.png)](https://substackcdn.com/image/fetch/$s_!dhd4!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbcf7f81f-3f1f-4e52-b391-e491ae4cce7d_893x912.png)

## [2] Good

Good presentations offered useful information and/or shared technical details on quality products. 

### [2.a] Qualcomm Oryon CPU

[![](https://substackcdn.com/image/fetch/$s_!vRME!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa845aeba-fd0b-4c3d-908e-1a962577ee32_1262x691.png)](https://substackcdn.com/image/fetch/$s_!vRME!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa845aeba-fd0b-4c3d-908e-1a962577ee32_1262x691.png)

One neat tidbit is one of the CPU clusters is “different in its physical construction” to enable better power efficiency. 

Seems like efficiency-focused transistor libraries and standard cells were used for the efficiency cluster, even though the higher-level RTL is the same.

[![](https://substackcdn.com/image/fetch/$s_!ujx9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc03ec94e-dd0e-4915-b9df-3ada3eaea57b_594x274.webp)](https://substackcdn.com/image/fetch/$s_!ujx9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc03ec94e-dd0e-4915-b9df-3ada3eaea57b_594x274.webp)

Use different physical design blocks, sacrifice FMAX for better power efficiency.

[![](https://substackcdn.com/image/fetch/$s_!ozNv!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F51d14a74-cf5e-4c6d-a902-ab30488cf06a_1031x665.png)](https://substackcdn.com/image/fetch/$s_!ozNv!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F51d14a74-cf5e-4c6d-a902-ab30488cf06a_1031x665.png)

The inner workings of this forwarding mux would be interesting.

[![](https://substackcdn.com/image/fetch/$s_!MrNZ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F201def8b-b8f6-4ebb-aa15-b5e401fd6cdf_1226x691.png)](https://substackcdn.com/image/fetch/$s_!MrNZ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F201def8b-b8f6-4ebb-aa15-b5e401fd6cdf_1226x691.png)

Each core typically uses 3-4MB of L2 at runtime but can use more if needed. Latency of 15-20 cycles.

### [2.b] IBM Telum 2

Why do mainframes still exist?

[![](https://substackcdn.com/image/fetch/$s_!A-Fm!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F595b5d59-26d4-4d10-b58a-6fc88f938b62_943x336.png)](https://substackcdn.com/image/fetch/$s_!A-Fm!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F595b5d59-26d4-4d10-b58a-6fc88f938b62_943x336.png)

To process financial transactions in real-time with ultra-low latency and absurd uptime/reliability.

[![](https://substackcdn.com/image/fetch/$s_!1-T6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1e7b2ee4-9b12-4aaf-8817-959e3a9e79d0_1462x786.png)](https://substackcdn.com/image/fetch/$s_!1-T6!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1e7b2ee4-9b12-4aaf-8817-959e3a9e79d0_1462x786.png)

Previously, IBM would include extra cores to improve yield. In this generation, they decided to remove two extra/spare cores and plop in a dedicated DPU. There is some dead space (blue squiggle) which is unfortunate but overall smart design choices. 

[![](https://substackcdn.com/image/fetch/$s_!6zyL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F28bbde63-2830-48ba-a06f-b910bda6c4af_1661x904.png)](https://substackcdn.com/image/fetch/$s_!6zyL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F28bbde63-2830-48ba-a06f-b910bda6c4af_1661x904.png)

[![](https://substackcdn.com/image/fetch/$s_!53gk!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3be1b3a1-c3db-464c-aa22-5a4b94fba56a_1655x887.png)](https://substackcdn.com/image/fetch/$s_!53gk!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3be1b3a1-c3db-464c-aa22-5a4b94fba56a_1655x887.png)

[![](https://substackcdn.com/image/fetch/$s_!HlM3!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F77e740f8-45b5-4661-bc19-4c743e1edc96_1652x906.png)](https://substackcdn.com/image/fetch/$s_!HlM3!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F77e740f8-45b5-4661-bc19-4c743e1edc96_1652x906.png)

This built-in DPU is pretty nice. Enables L2 coherence across 32 Telum II chips. IBM chips have a fancy virtual L3 and L4 system. Speaking of virtual cache…

[![](https://substackcdn.com/image/fetch/$s_!Kv6G!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9510055e-5ecd-476d-bbeb-376f093a2a7c_1541x912.png)](https://substackcdn.com/image/fetch/$s_!Kv6G!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9510055e-5ecd-476d-bbeb-376f093a2a7c_1541x912.png)

Each CPU core can access all the other L2s as a virtual L3. They can even access other chips L2 as a virtual L4. This feature is unique to IBM chips and is very cool, especially given all of these virtual cache accesses support cross-node encryption.

Unfortunately, IBM did not share the expected latency for DDR5 hits. Presumably, the latency would be somewhere in the 80-120ns range so a virtual L4 hit is still better than a local DDR hit.

[![](https://substackcdn.com/image/fetch/$s_!_GZq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe7ee1841-6c70-43da-839b-72039a7a4534_1610x843.png)](https://substackcdn.com/image/fetch/$s_!_GZq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe7ee1841-6c70-43da-839b-72039a7a4534_1610x843.png)

The previous generation had an on-chip AI accelerator, and it has gotten significant upgrades. Note that the LLM commentary is marketing hype. Nobody is gona use this thing for LLMs lol. 

Interesting that they have choses a CISC uarch and rely on ML op fusion. Can’t think of anyone else who has gone this route.

One important new feature that was verbally mentioned is each CPU core can access every AI accelerator within the same drawer, with a latency penalty of course. Only one CPU core can use the AI accelerator at a time and customer use has steadily increased. To mitigate congestion issues, cross-chip AI accelerator access was added. It’s a good sign. IBM’s customers (banks, credit card processors) are actually using the accelerator. 

[![](https://substackcdn.com/image/fetch/$s_!Dnak!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fae1bcdff-9bac-4611-b562-b676b73b9112_1625x762.png)](https://substackcdn.com/image/fetch/$s_!Dnak!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fae1bcdff-9bac-4611-b562-b676b73b9112_1625x762.png)

[![](https://substackcdn.com/image/fetch/$s_!RSO0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc940e97a-ae25-4bd1-8894-4c90d9b6ef11_1578x841.png)](https://substackcdn.com/image/fetch/$s_!RSO0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc940e97a-ae25-4bd1-8894-4c90d9b6ef11_1578x841.png)

They put 32 copies of this AI accelerator on a dedicated chip. Not sure who is going to buy this.

[![](https://substackcdn.com/image/fetch/$s_!LOgR!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F54c3f8a9-5b64-4e11-8f86-dde5f0f7edd9_1309x928.png)](https://substackcdn.com/image/fetch/$s_!LOgR!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F54c3f8a9-5b64-4e11-8f86-dde5f0f7edd9_1309x928.png)

[![](https://substackcdn.com/image/fetch/$s_!m0B9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fde48c00b-39f1-468b-8982-50ffe7d44f0b_1346x848.png)](https://substackcdn.com/image/fetch/$s_!m0B9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fde48c00b-39f1-468b-8982-50ffe7d44f0b_1346x848.png)

Marketed as a genAI solution. Hard doubt on this one. Maybe some of the financial institution customers will buy some of these to make bizzarro AI trading bots. The software stack and architecture are too bespoke (painful to program) for anyone outside of IBM’s existing customer base to bother with. Accumulation and activation ops seem to be handled in a rather rigid manner, especially in the context of data precision. When you see “scratchpad” think programmer-managed memory… AKA painful programming model that has a high-skill ceiling to achieve advertised performance. Someone at Citadel is gona have a lot of fun with this Spyre chip.

### [2.c] Tutorial: AI for Hardware Design

There were multiple, excellent talks on using AI for chip design that I will lump together in this section.

[![](https://substackcdn.com/image/fetch/$s_!OWpg!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F298b7d62-448c-4be1-9167-fad0469f13e4_1531x820.png)](https://substackcdn.com/image/fetch/$s_!OWpg!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F298b7d62-448c-4be1-9167-fad0469f13e4_1531x820.png)

Cross-stage analysis and optimization is very important, given how complexity of leading-edge chiplet systems has exploded.

[![](https://substackcdn.com/image/fetch/$s_!if1N!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F361744a6-fe1f-4bb5-9410-d36982706896_1534x827.png)](https://substackcdn.com/image/fetch/$s_!if1N!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F361744a6-fe1f-4bb5-9410-d36982706896_1534x827.png)Look at the sick productivity gains!

Physical design optimization is well-suited for conv-nets. Simulating IR drop (intrinsic resistance/impedance of each sub-circuit) is very slow. AI helps by estimating where problems are likely and allow experienced designers to target EDA analysis tools on specific portions of the chip. 

[![](https://substackcdn.com/image/fetch/$s_!AkTE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F363eaecc-e4a0-41de-a857-6c88b170f1c3_1534x816.png)](https://substackcdn.com/image/fetch/$s_!AkTE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F363eaecc-e4a0-41de-a857-6c88b170f1c3_1534x816.png)

Analog circuit design is typically in two discrete stages:

  1. Make a schematic of the circuit.

  2. Implement the schematic on a physical design.




“Parasitics” refers to unwanted attributes. Typically, resistance and capacitance. 

Examples:

  1. Wires have intrinsic resistance. If you don’t account for this, the voltage drop might be too high resulting in bit-flips/errors.

  2. Devices (transistors, diodes, flip-flps,…) have intrinsic capacitance that can easily mess up your transient response.




[![](https://substackcdn.com/image/fetch/$s_!bhej!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6ce04eb7-0294-4baf-b19f-0a763344083a_741x300.png)](https://substackcdn.com/image/fetch/$s_!bhej!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6ce04eb7-0294-4baf-b19f-0a763344083a_741x300.png)Higher parasitics mean you have to wait longer for the current to settle. Lower clock speed.

[![](https://substackcdn.com/image/fetch/$s_!VcKy!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F11856469-87eb-4e13-903d-589539404232_1108x526.png)](https://substackcdn.com/image/fetch/$s_!VcKy!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F11856469-87eb-4e13-903d-589539404232_1108x526.png)You can model this by adding fake capacitors into a simulator, but decisions made by the physical designer effect the underlying assumptions.

The normal way to handle these problems involves a lot of back-and-forth. It is somewhat challenging to have physical designers and circuit/schematic designers bounce design revisions across their fields. Using AI to predict possible parasitic issues is a great productivity boost for both departments.

[![](https://substackcdn.com/image/fetch/$s_!4vKo!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fed4cba36-dc88-42b4-91b3-4b96e08b0a52_1537x838.png)](https://substackcdn.com/image/fetch/$s_!4vKo!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fed4cba36-dc88-42b4-91b3-4b96e08b0a52_1537x838.png)

Commercial EDA tools have macro placement tools but the configuration parameters for said tools have a huge impact on output quality. The baseline is for experienced designers to guesstimate what parameters to choose, run the tool, analyze the results, then try again.

AI once again provides a massive productivity boost. More coverage of a wider search space and faster iteration to a better end-result.

[![](https://substackcdn.com/image/fetch/$s_!B685!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F21dc173c-d4a5-428d-9eef-f089d63edfb8_1543x874.png)](https://substackcdn.com/image/fetch/$s_!B685!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F21dc173c-d4a5-428d-9eef-f089d63edfb8_1543x874.png)

Modern process nodes have many design rules. A reinforcement-learning AI agent can automatically play a “game” that removes DRC violations. 

[![](https://substackcdn.com/image/fetch/$s_!IhwL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fba4b1b1f-2212-4ee4-9b67-eaafbfbcaac1_1542x860.png)](https://substackcdn.com/image/fetch/$s_!IhwL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fba4b1b1f-2212-4ee4-9b67-eaafbfbcaac1_1542x860.png)

Reinforcement-learning has many other uses. Any optimization problem with a clearly defined environment, reward mechanism, and large search space is quite well suited for RL.

[![](https://substackcdn.com/image/fetch/$s_!s5Dz!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fadfab66d-8bfe-48d1-8c0f-2c0ae3b5d7b7_1537x846.png)](https://substackcdn.com/image/fetch/$s_!s5Dz!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fadfab66d-8bfe-48d1-8c0f-2c0ae3b5d7b7_1537x846.png)

[![](https://substackcdn.com/image/fetch/$s_!_3KQ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2c8abb8a-84ed-4a98-adce-6b905efcc247_1540x853.png)](https://substackcdn.com/image/fetch/$s_!_3KQ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2c8abb8a-84ed-4a98-adce-6b905efcc247_1540x853.png)

On to the modern (bleeding-edge) techniques. Generative AI (transformers) is very good at compressing massive search spaces into an intermediate representation, latent space, allowing for efficient analysis of pre-filtered optimization points.

One example is logic gate sizing. The search space for optimizing power, area, and performance (delay) for individual logic gates is massive. By tokenizing each gate in a circuits critical path, the transformer optimizer can quickly find optimization opportunities. **An incredible 2-3 order of magnitude speedup** was achieved compared to traditional EDA optimization tools.

At this point, the Nvidia presenter not so subtly took a jab at the EDA vendors for being too slow to implement new features. If a customer can develop a 100x to 1000x faster optimizer, you might be innovating too slow.

[![](https://substackcdn.com/image/fetch/$s_!8kZN!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F653011c9-7536-4947-a504-e932402d36c5_1548x828.png)](https://substackcdn.com/image/fetch/$s_!8kZN!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F653011c9-7536-4947-a504-e932402d36c5_1548x828.png)

Once again, the latent space of a transformer model is very good at choosing optimizations of complex designs with very large search spaces. A dimension-reducing function to search faster and find better local minima/maxima.

[![](https://substackcdn.com/image/fetch/$s_!FCSR!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb727cca0-70dc-4e96-a4ac-c45d92aa12f4_1513x825.png)](https://substackcdn.com/image/fetch/$s_!FCSR!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb727cca0-70dc-4e96-a4ac-c45d92aa12f4_1513x825.png)

[![](https://substackcdn.com/image/fetch/$s_!U2n6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffdab5e81-5b39-4609-90bd-8ee2d0a88c1b_1537x868.png)](https://substackcdn.com/image/fetch/$s_!U2n6!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffdab5e81-5b39-4609-90bd-8ee2d0a88c1b_1537x868.png)

[![](https://substackcdn.com/image/fetch/$s_!PRlZ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F239a297d-5678-48b6-9c80-9f4a23591565_1498x840.png)](https://substackcdn.com/image/fetch/$s_!PRlZ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F239a297d-5678-48b6-9c80-9f4a23591565_1498x840.png)

LLM agents are generalists that can be RAG-ed onto internal proprietary data. Simulations, custom standard cells, past chip designs, …

Most of the focus has been on RTL generation but the presenter went out of his way to highlight that LLM agents are super useful across a wide variety of domains. Bug report analyst, testbench assistance, EDA script generation, … we have only scratched the surface of chip design productivity improvements with LLMs.

* * *

On to the Synopsys presentation.

[![](https://substackcdn.com/image/fetch/$s_!inhI!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2fb723d4-11e3-4b1f-8156-e526b7bb71d5_1226x670.png)](https://substackcdn.com/image/fetch/$s_!inhI!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2fb723d4-11e3-4b1f-8156-e526b7bb71d5_1226x670.png)

[![](https://substackcdn.com/image/fetch/$s_!Dh3U!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcabead66-aeb3-43d2-819f-03f7919af34d_1234x691.png)](https://substackcdn.com/image/fetch/$s_!Dh3U!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcabead66-aeb3-43d2-819f-03f7919af34d_1234x691.png)

Design search space is massive and gets exponentially larger at each step of the process.

[![](https://substackcdn.com/image/fetch/$s_!ZfOB!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F35e2e220-3b17-48a2-8a5f-538df9ba3ad2_1232x677.png)](https://substackcdn.com/image/fetch/$s_!ZfOB!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F35e2e220-3b17-48a2-8a5f-538df9ba3ad2_1232x677.png)

Complexity harms productivity, and thus cost. 

[![](https://substackcdn.com/image/fetch/$s_!_pDu!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb5958f00-4183-4a92-9f52-4ad3ec665af9_1239x700.png)](https://substackcdn.com/image/fetch/$s_!_pDu!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb5958f00-4183-4a92-9f52-4ad3ec665af9_1239x700.png)

Identifying cross-layer optimization opportunities is very difficult but critical to squeezing out every competitive advantage possible.

[![](https://substackcdn.com/image/fetch/$s_!RePU!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F274e1260-10df-4842-9544-f19ba514c714_1221x681.png)](https://substackcdn.com/image/fetch/$s_!RePU!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F274e1260-10df-4842-9544-f19ba514c714_1221x681.png)

Reinforcement learning once again comes in to save the day. In this plot, the bottom left is desirable. Goal is to minimize leakage (wasted) power and TNS (total negative slack), a measure of timing violations. **The RL/AI agent out-performed months of human work by 30%.**

[![](https://substackcdn.com/image/fetch/$s_!pimU!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff4cfb05b-4e33-4839-9d2d-f66a943fab2f_1222x701.png)](https://substackcdn.com/image/fetch/$s_!pimU!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff4cfb05b-4e33-4839-9d2d-f66a943fab2f_1222x701.png)

In this example, the yellow triangle is the human-designed baseline. AI/RL floor planning **found multiple solutions** that not only improve on the human design but also **offer optionality**. Could optimize for area (cost) or performance or both. Regardless, these new options are enabled by the RL agent. Many engineer-hours of human work missed all these options because the design space is simply too big.

[![](https://substackcdn.com/image/fetch/$s_!GlE9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9148a11d-3fcc-436b-818c-a0eff4f8d339_1238x681.png)](https://substackcdn.com/image/fetch/$s_!GlE9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9148a11d-3fcc-436b-818c-a0eff4f8d339_1238x681.png)

Multiple RL agents can be trained with different reward mechanisms, leading to different results. Lots of way to set up the game.

### [2.d] Tutorial: Liquid Cooling

Fun-fact, one of the circuit breakers at Stanford tripped as the Supermicro presenter was talking about power limitations. The market happened to crash on that day. No correlation. 

[![](https://substackcdn.com/image/fetch/$s_!_YOS!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa16419ca-ff32-4dd5-8d70-8f7ef5e709d0_1572x827.png)](https://substackcdn.com/image/fetch/$s_!_YOS!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa16419ca-ff32-4dd5-8d70-8f7ef5e709d0_1572x827.png)

IIRC, the efficiency record is held by a Meta datacenter at a PUE of 1.02 but don’t quote me on that.

[![](https://substackcdn.com/image/fetch/$s_!6HO8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4abc558b-9be7-419b-a234-8a1bf3c8e560_1566x828.png)](https://substackcdn.com/image/fetch/$s_!6HO8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4abc558b-9be7-419b-a234-8a1bf3c8e560_1566x828.png)

Wasting water to evaporation is a sustainability problem. Credit to the presenter for bringing this up and not dodging the topic.

[![](https://substackcdn.com/image/fetch/$s_!tG8Y!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7b67e4d3-7b78-4b78-81f4-850a7b932e06_1576x829.png)](https://substackcdn.com/image/fetch/$s_!tG8Y!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7b67e4d3-7b78-4b78-81f4-850a7b932e06_1576x829.png)

Cold plate design is a fun topic that was unfortunately not discussed in depth. 

[![](https://substackcdn.com/image/fetch/$s_!2lYM!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F21259791-bf89-476a-a892-739c85a568fe_871x690.jpeg)](https://substackcdn.com/image/fetch/$s_!2lYM!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F21259791-bf89-476a-a892-739c85a568fe_871x690.jpeg)

Fin shape, size, positioning, count, and offset are all important variables. 

[![](https://substackcdn.com/image/fetch/$s_!HtRi!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F13340adc-7378-4b1f-9aef-1c652fa5f0eb_1572x835.png)](https://substackcdn.com/image/fetch/$s_!HtRi!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F13340adc-7378-4b1f-9aef-1c652fa5f0eb_1572x835.png)

Direct liquid cooling has a massive advantage because high-powered fans in traditional air-cooling systems burn a lot of power. A 2U server that draws 2KW from compute can easily have 200W+ burned just from the fans.

* * *

[![](https://substackcdn.com/image/fetch/$s_!nOx6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F12ede85a-d03e-45e6-96ee-e83d57fa672f_1268x711.png)](https://substackcdn.com/image/fetch/$s_!nOx6!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F12ede85a-d03e-45e6-96ee-e83d57fa672f_1268x711.png)

[![](https://substackcdn.com/image/fetch/$s_!jWq_!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3c98f29e-5340-4904-8013-cb23892b1f37_1241x705.png)](https://substackcdn.com/image/fetch/$s_!jWq_!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3c98f29e-5340-4904-8013-cb23892b1f37_1241x705.png)

A major limitation of direct liquid cooling is erosion. Fluid flow-rate cannot just arbitrarily go up. The cold plate micro-fins will erode, destroying thermal dissipation.

In Q&A, the topic of future scaling came up. Phase-change cooling (pressurized liquid go in, gas go out) was brought up and it seems to be the path forward.

[![](https://substackcdn.com/image/fetch/$s_!0CEU!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8f05c0df-825b-4f71-b7a0-2391b4f24946_2480x1548.png)](https://substackcdn.com/image/fetch/$s_!0CEU!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8f05c0df-825b-4f71-b7a0-2391b4f24946_2480x1548.png)

A large amount of energy (heat) is dissipated from phase changes. There are obvious problems with the fluid composition as most liquid cooling loops use a mixture of 60% water, 40% glycol compounds, and minor quantity of anti-microbial and anti-corrosive additives. Each of these fluids have their own boiling points.

[![](https://substackcdn.com/image/fetch/$s_!TncW!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F64331ee5-92a9-4adf-8cb5-781bb1edae3c_1237x698.png)](https://substackcdn.com/image/fetch/$s_!TncW!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F64331ee5-92a9-4adf-8cb5-781bb1edae3c_1237x698.png)

Nvidia is working on it though. “Two-phase” is the keyword.

[![](https://substackcdn.com/image/fetch/$s_!Oo4L!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F48d9e2de-5c5d-47cb-b845-f52ed1b136fc_1230x691.png)](https://substackcdn.com/image/fetch/$s_!Oo4L!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F48d9e2de-5c5d-47cb-b845-f52ed1b136fc_1230x691.png)

One neat idea shared is a waste-heat recycling project. Use warm fluid from a datacenter to heat up a neighboring agricultural facility such as a greenhouse or hydroponic farm. Waste heat electricity generation is also a possibility but seems much more difficult.

### [2.e] Poster: Radix-8 FFT Accelerator

Here is the full poster. I will walk you through it in chunks.

[![](https://substackcdn.com/image/fetch/$s_!8A0B!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F79bb85b9-36c2-4f82-b807-4032e3e2a942_1823x1341.png)](https://substackcdn.com/image/fetch/$s_!8A0B!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F79bb85b9-36c2-4f82-b807-4032e3e2a942_1823x1341.png)

Optimizing assembly code for FFT engines is difficult…

[![](https://substackcdn.com/image/fetch/$s_!KRum!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F24dd77f7-0052-4bbf-bf20-396762533c20_578x703.png)](https://substackcdn.com/image/fetch/$s_!KRum!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F24dd77f7-0052-4bbf-bf20-396762533c20_578x703.png)

…because the engine is standalone. FFT operations are often mixed with other companion operations such as circular shift, windowing, and [spectral density](https://en.wikipedia.org/wiki/Spectral_density) processing. The designers chose to create a codelet intermediate representation and optimize the hardware to that.

[![](https://substackcdn.com/image/fetch/$s_!ivHM!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff3258926-ef45-4fa3-8f4e-d94a5bd0091e_637x1052.png)](https://substackcdn.com/image/fetch/$s_!ivHM!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff3258926-ef45-4fa3-8f4e-d94a5bd0091e_637x1052.png)

Essentially there is a flexible 8-point FFT engine paired with some complex multipliers that can be configured according to codelet instructions.

Neat poster.

## [3] Meh

“Meh” presentations are somewhat interesting but are not compelling from a commercial perspective.

### [3.a] Intel Lunar Lake

All the major chiplets on Lunar Lake are on TSMC N3B. Only the passive interposer is on an Intel process node. This product is great, but COGS is up 80-100%. This laptop chip is SO MUCH MORE expensive to manufacture compared to its predecessor, Metero Lake.

Lunar Lake might bankrupt Intel. Not joking. 

[![Obfuscation Inside](https://substackcdn.com/image/fetch/$s_!-eDN!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff4d0dce9-f70b-4145-a0ec-bf74ea2c76ce_1280x1455.jpeg)

#### Obfuscation Inside

[Daud's Scout](https://substack.com/profile/135313705-dauds-scout)·August 9, 2024[Read full story](https://irrationalanalysis.substack.com/p/obfuscation-inside)](https://irrationalanalysis.substack.com/p/obfuscation-inside)

Sell-side is modeling gross-margins going UP sequentially. This assumption makes no sense and is very wrong!

I will cover the recent [INTC 0.00%↑](https://substack.com/discover/stocks/INTC) news, from board member resignations to activist defense prep to possible “strategic actions” next week. Subscribe so you get a notification/email as soon as it goes live.

Subscribe

With that pre-amble out of the way, let’s go over the presentation itself.

[![](https://substackcdn.com/image/fetch/$s_!34FD!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F853a951f-b37a-4b15-a8eb-e90f1597100d_1198x634.png)](https://substackcdn.com/image/fetch/$s_!34FD!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F853a951f-b37a-4b15-a8eb-e90f1597100d_1198x634.png)

Nvidia applies their 70-80% gross-margin to on-package (HBM) memory. Intel’s CFO explicitly stated that they would be applying 0% margin on the on-package LPDDR5x in last quarter’s earnings call.

[![](https://substackcdn.com/image/fetch/$s_!8JNM!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F694f36b9-bdf2-4167-9c5e-07d0277ee765_1170x469.png)](https://substackcdn.com/image/fetch/$s_!8JNM!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F694f36b9-bdf2-4167-9c5e-07d0277ee765_1170x469.png)

Memory side cache is analogous to the system-level cache (SLC) that smartphone SoC vendors have been using for years. Interesting that Intel chose to adopt this strategy for the first time. Perhaps it is to help the NPU and GPU not choke on the LPDDR5x bus.

[![](https://substackcdn.com/image/fetch/$s_!Nn7t!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff8de6376-9bfc-4d81-8775-c46fd7b6c675_1180x446.png)](https://substackcdn.com/image/fetch/$s_!Nn7t!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff8de6376-9bfc-4d81-8775-c46fd7b6c675_1180x446.png)

[![](https://substackcdn.com/image/fetch/$s_!8LbQ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9517e131-e2a8-4315-a915-0ae3ad557b71_1177x427.png)](https://substackcdn.com/image/fetch/$s_!8LbQ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9517e131-e2a8-4315-a915-0ae3ad557b71_1177x427.png)

[![](https://substackcdn.com/image/fetch/$s_!A-c0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcd67bba2-da7d-4ddd-97fe-3e89714d521d_1193x398.png)](https://substackcdn.com/image/fetch/$s_!A-c0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcd67bba2-da7d-4ddd-97fe-3e89714d521d_1193x398.png)

[![](https://substackcdn.com/image/fetch/$s_!A-uJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc7466741-0568-419c-ab40-fc9f2cac9fe0_1198x402.png)](https://substackcdn.com/image/fetch/$s_!A-uJ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc7466741-0568-419c-ab40-fc9f2cac9fe0_1198x402.png)

E-core cluster gets its own power-delivery. They even made custom PMICs to support many separate power rails. Perhaps I was too critical of the Qualcomm PMIC situation. Nah. Qualcomm should have designed a new PMIC like Intel, instead of re-using PMICs designed for mobile chipset power levels (<5W) on a 55W part, running way outside of the efficiency zone and placing a comical number of PMICs in parallel and paying a hefty apology subsidy to laptop OEMs.

[![Dell Mega Leak Analysis](https://substackcdn.com/image/fetch/$s_!DmRp!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1ffcbb23-7f8c-4022-9a35-358dd1d87d05_1797x1139.png)

#### Dell Mega Leak Analysis

[Daud's Scout](https://substack.com/profile/135313705-dauds-scout)·May 15, 2024[Read full story](https://irrationalanalysis.substack.com/p/dell-mega-leak-analysis)](https://irrationalanalysis.substack.com/p/dell-mega-leak-analysis)

Anyway, back to Intel. The ML-based power management was vigorously roasted in Slack Q&A. These “ML models” don’t run on the NPU, obviously, because that would burn a ton of power spinning up the NPU…

[![](https://substackcdn.com/image/fetch/$s_!J7ki!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F09406586-0275-49fc-94a8-d3be1ba8007d_292x297.png)](https://substackcdn.com/image/fetch/$s_!J7ki!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F09406586-0275-49fc-94a8-d3be1ba8007d_292x297.png)This pissed off the entire audience.

Write this off as a marketing snafu. It’s fine.

[![](https://substackcdn.com/image/fetch/$s_!29sA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7cb6baa3-0e77-4fa7-9e4c-da6e1edad98a_443x289.png)](https://substackcdn.com/image/fetch/$s_!29sA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7cb6baa3-0e77-4fa7-9e4c-da6e1edad98a_443x289.png)

The P-cores have much finer clock scheduling. Traditional Intel cores only have granularity in 100MHz steps. Very interesting development. Probably helps with idle and light-use power consumption. Splitting the out-of-order engine for vector and integer is also interesting. Sacrifices area but likely gives a meaningful performance boost.

[![](https://substackcdn.com/image/fetch/$s_!Hkgn!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9bcce695-6bcf-45ce-8fec-de9497e94772_498x602.png)](https://substackcdn.com/image/fetch/$s_!Hkgn!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9bcce695-6bcf-45ce-8fec-de9497e94772_498x602.png)

Who is running VNNI/vector workloads on E-cores? This seems like a waste of area.

[![](https://substackcdn.com/image/fetch/$s_!17RA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9c9e396b-4fd7-4581-bd41-16f0c1aeaa58_1226x637.png)](https://substackcdn.com/image/fetch/$s_!17RA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9c9e396b-4fd7-4581-bd41-16f0c1aeaa58_1226x637.png)WHY? Who asked for this?

[![](https://substackcdn.com/image/fetch/$s_!txoL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd625d1f0-a94e-429b-97ee-a16fed215532_220x220.gif)](https://substackcdn.com/image/fetch/$s_!txoL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd625d1f0-a94e-429b-97ee-a16fed215532_220x220.gif)

[![](https://substackcdn.com/image/fetch/$s_!Uvai!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa31f4fc5-2fbf-49aa-bd13-21d3069944d0_1238x677.png)](https://substackcdn.com/image/fetch/$s_!Uvai!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa31f4fc5-2fbf-49aa-bd13-21d3069944d0_1238x677.png)

Integer performance boost of 1.38x gen-on-gen is great.

[![](https://substackcdn.com/image/fetch/$s_!zG4m!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdd38ea48-ad2b-4a5a-ad5f-e39644c88743_1232x694.png)](https://substackcdn.com/image/fetch/$s_!zG4m!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdd38ea48-ad2b-4a5a-ad5f-e39644c88743_1232x694.png)

Power-efficiency is much more important, and they crushed it. Excellent job to the entire Skymont team! Looking forward to the server variant, Clearwater Forest.

[![](https://substackcdn.com/image/fetch/$s_!3zWa!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F86e5cae2-16ae-404a-ab97-df4fb1d04b8d_1259x657.png)](https://substackcdn.com/image/fetch/$s_!3zWa!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F86e5cae2-16ae-404a-ab97-df4fb1d04b8d_1259x657.png)

Awesome latency improvements. The Windows scheduler should have a much easier time spreading applications across P and E cores.

[![](https://substackcdn.com/image/fetch/$s_!BguX!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdbcd4f80-3056-485d-ac27-284756005c68_945x1071.png)](https://substackcdn.com/image/fetch/$s_!BguX!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdbcd4f80-3056-485d-ac27-284756005c68_945x1071.png)

Great data visualization. I hope my employer gives me a laptop refresh to Lunar Lake as the battery life of my 12th-gen, Alder Lake unit sucks.

### [3.b] Intel Edge Xeon

These Xeon products are intended for edge operation, typically Telco, security systems, traffic systems, …

[![](https://substackcdn.com/image/fetch/$s_!TAap!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3ecfe83b-708f-421a-bb9d-888fb8b406b8_1122x640.png)](https://substackcdn.com/image/fetch/$s_!TAap!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3ecfe83b-708f-421a-bb9d-888fb8b406b8_1122x640.png)

Lots of goodies are now integrated on-package, greatly improving throughput and power efficiency. Full CXL 2.0 support. Awesome.

[![](https://substackcdn.com/image/fetch/$s_!ypOA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F615c1f2d-e863-4ef0-ab34-224d63c99c22_1154x651.png)](https://substackcdn.com/image/fetch/$s_!ypOA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F615c1f2d-e863-4ef0-ab34-224d63c99c22_1154x651.png)

[![](https://substackcdn.com/image/fetch/$s_!rsSN!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb8554557-b2d2-4857-9040-4e6c0fd0a7ed_1154x637.png)](https://substackcdn.com/image/fetch/$s_!rsSN!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb8554557-b2d2-4857-9040-4e6c0fd0a7ed_1154x637.png)

AMX is very useful for CPU-based AI. It is a real workload believe it or not. 

[![](https://substackcdn.com/image/fetch/$s_!DVGX!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff8d3056a-d3c7-46b4-8ea2-16b6a7e11b5c_1178x631.png)](https://substackcdn.com/image/fetch/$s_!DVGX!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff8d3056a-d3c7-46b4-8ea2-16b6a7e11b5c_1178x631.png)

A bunch of Intel proprietary accelerators are on the IO chiplet. The ones I highlighted are actually useful and broadly utilized by customers. Intel is… not in a good place right now so customers are not excited to write code to use most of these proprietary accelerators. 

### [3.c] Enfabrica 

Weird, self-proclaimed “super-NIC”. Not sure why this chip exists or who would want to buy it… but it is super cool so worth covering.

[![](https://substackcdn.com/image/fetch/$s_!dwUF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb85c309d-50a3-495a-afa1-26ed44693fbb_1260x704.png)](https://substackcdn.com/image/fetch/$s_!dwUF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb85c309d-50a3-495a-afa1-26ed44693fbb_1260x704.png)

[![](https://substackcdn.com/image/fetch/$s_!uqMj!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5d4b6c25-ada4-4ff4-bc51-22f87b8e88a6_1268x717.png)](https://substackcdn.com/image/fetch/$s_!uqMj!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5d4b6c25-ada4-4ff4-bc51-22f87b8e88a6_1268x717.png)

If you don’t understand these slides… that’s ok. I don’t either. Only makes sense once we take a look at the chip block diagram.

[![](https://substackcdn.com/image/fetch/$s_!YHqx!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F457f8b94-6dd0-4818-b2e1-7f14e0e1cfe0_1263x706.png)](https://substackcdn.com/image/fetch/$s_!YHqx!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F457f8b94-6dd0-4818-b2e1-7f14e0e1cfe0_1263x706.png)

[![](https://substackcdn.com/image/fetch/$s_!RCeP!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7d98a29c-85ec-420e-bace-2db4b33467e3_1259x702.png)](https://substackcdn.com/image/fetch/$s_!RCeP!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7d98a29c-85ec-420e-bace-2db4b33467e3_1259x702.png)

[![](https://substackcdn.com/image/fetch/$s_!NWWH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb4d180b4-7a15-4628-bf26-ded71e13e8dc_1258x686.png)](https://substackcdn.com/image/fetch/$s_!NWWH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb4d180b4-7a15-4628-bf26-ded71e13e8dc_1258x686.png)

Ok so this chip is a bizzarro, hybrid Ethernet + PCIe switch. Highly programmable, fully buffered, and extremely configurable from a radix perspective.

Again, not sure who would want to buy this, but it is very cool lol.

[![](https://substackcdn.com/image/fetch/$s_!NAc3!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1a379a6d-f1bf-4646-a98c-b2671f7caf4a_1260x709.png)](https://substackcdn.com/image/fetch/$s_!NAc3!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1a379a6d-f1bf-4646-a98c-b2671f7caf4a_1260x709.png)

Great… burst absorption… but uh… wont the latency suck?

### [3.d] Intel Silicon Photonics

This presentation was good but the [AVGO 0.00%↑](https://substack.com/discover/stocks/AVGO) one on the exact same topic was much better. Broadcom will commercialize their silicon photonics solution in 2025/2026 at high-volume while the team behind this Intel project is at high risk of getting cut in the impending layoffs. Really unfortunate. Wish the best for them. 

[![](https://substackcdn.com/image/fetch/$s_!QP5X!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F82a714b5-630f-4140-9597-7e1c30bbff37_1267x711.png)](https://substackcdn.com/image/fetch/$s_!QP5X!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F82a714b5-630f-4140-9597-7e1c30bbff37_1267x711.png)

No RDL layer. Probably results in better power efficiency compared to the Broadcom method at the cost of packaging complexity, and thus yield.

[![](https://substackcdn.com/image/fetch/$s_!nR0C!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd2dffabb-d0bd-42eb-a52e-e16f171c67e8_1258x705.png)](https://substackcdn.com/image/fetch/$s_!nR0C!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd2dffabb-d0bd-42eb-a52e-e16f171c67e8_1258x705.png)

The lasers are on the photonic IC (PIC). Broadcom went out of their way to move the lasers off-die to external pluggable modules for serviceability and reliability. 

[![](https://substackcdn.com/image/fetch/$s_!d6R_!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F66e1f90b-189b-4941-a044-fe19c38442c2_1261x706.png)](https://substackcdn.com/image/fetch/$s_!d6R_!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F66e1f90b-189b-4941-a044-fe19c38442c2_1261x706.png)

Intel claims that their solution is reliable from field data testing. 

[![](https://substackcdn.com/image/fetch/$s_!wK8U!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fed7c0140-325f-4e77-97fa-8f11f24360f0_1397x530.png)](https://substackcdn.com/image/fetch/$s_!wK8U!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fed7c0140-325f-4e77-97fa-8f11f24360f0_1397x530.png)

Resolution of the plot is not great… but sure it looks like their reliability claims can be taken at face value. The presenter did not say how they accomplished this other than highlighting the quality of their photonic process node.

### [3.e] SambaNova

Sambanova was my most anticipated presentation and… it was fine. The architecture is a CGRA, which is something in-between an FPGA and an ASIC.

Let’s unpack that.

ASIC is just a purpose-built chip that can be programmed with software but has rigid hardware features.

An FPGA is highly programmable using truth-tables (LUTs).

[![](https://substackcdn.com/image/fetch/$s_!CU2w!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa5a5aece-cb3c-40a9-86cf-9e62418ac629_932x461.webp)](https://substackcdn.com/image/fetch/$s_!CU2w!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa5a5aece-cb3c-40a9-86cf-9e62418ac629_932x461.webp)

[![](https://substackcdn.com/image/fetch/$s_!YnDc!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0473d994-69f8-4b22-96ce-842b15910448_1024x492.webp)](https://substackcdn.com/image/fetch/$s_!YnDc!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0473d994-69f8-4b22-96ce-842b15910448_1024x492.webp)

Imagine if you could create any chip design and flash it in under 90-seconds instead of spending $20-100M on tape-out and waiting 3-6 months for the chip to be printed. This is what an FPGA enables, at the cost of horrendous PPA.

CGRAs are somewhere in-between. A rare anomaly of computer architecture.

[![](https://substackcdn.com/image/fetch/$s_!aFiJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdbea990f-2e7d-4aee-aa26-86ab8137ee86_1176x669.png)](https://substackcdn.com/image/fetch/$s_!aFiJ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdbea990f-2e7d-4aee-aa26-86ab8137ee86_1176x669.png)

The ‘P’ in PCU and PMU stands for ‘pattern’. Idea of this architecture is to identify patterns in the workload, map them to weird, configurable SIMD things, and link them up in a uniform mesh switch grid. Sort of like the MUX trees of an FPGA.

[![](https://substackcdn.com/image/fetch/$s_!y81R!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1d1fcac8-f48b-4ac7-af12-6876c2a40493_1189x674.png)](https://substackcdn.com/image/fetch/$s_!y81R!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1d1fcac8-f48b-4ac7-af12-6876c2a40493_1189x674.png)

Compute can be configured as a systolic array or SIMD vector unit; the former uses the broadcast buffer and the latter does not.

[![](https://substackcdn.com/image/fetch/$s_!FnKl!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2c6a3cbc-c940-4e14-8fa6-0f2779239ab9_1195x672.png)](https://substackcdn.com/image/fetch/$s_!FnKl!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2c6a3cbc-c940-4e14-8fa6-0f2779239ab9_1195x672.png)

Remember friends, when you hear “programmer managed scratchpad”, think “pain, suffering, high skill-ceiling, and impossible compiler complexity”.

[![](https://substackcdn.com/image/fetch/$s_!99mC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffa4e21f4-86df-47c4-a531-ca840fab26e2_1189x666.png)](https://substackcdn.com/image/fetch/$s_!99mC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffa4e21f4-86df-47c4-a531-ca840fab26e2_1189x666.png)

SambaNova decided to one-up Meta and make three separate mesh interconnects for their chip. Physical design and routing must have been particularly challenging… so congratulations to the engineers to pulled this off.

[![](https://substackcdn.com/image/fetch/$s_!Qf6d!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fee243ab0-5e9c-4723-a6da-b6e3b3f21df2_1193x668.png)](https://substackcdn.com/image/fetch/$s_!Qf6d!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fee243ab0-5e9c-4723-a6da-b6e3b3f21df2_1193x668.png)

A mesh-ring hybrid top-level interconnect. Graph compiler team must have so much fun trying to make this work.

[![](https://substackcdn.com/image/fetch/$s_!Z4P0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffb033740-185c-41e3-8b6a-c80c66e0eaff_1187x661.png)](https://substackcdn.com/image/fetch/$s_!Z4P0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffb033740-185c-41e3-8b6a-c80c66e0eaff_1187x661.png)

The main draw of this architecture is how it maps complex compute operations directly to the highly configurable hardware, enabling lots of neat optimizations.

Here is a more complicated example:

[![](https://substackcdn.com/image/fetch/$s_!Kjr_!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F019bc6d7-7276-42fd-9687-0f3a36d5ad66_943x1078.png)](https://substackcdn.com/image/fetch/$s_!Kjr_!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F019bc6d7-7276-42fd-9687-0f3a36d5ad66_943x1078.png)

[![](https://substackcdn.com/image/fetch/$s_!wW2u!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa6c3a0ce-15e2-427e-89cd-d5c15e9d6703_952x1081.png)](https://substackcdn.com/image/fetch/$s_!wW2u!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa6c3a0ce-15e2-427e-89cd-d5c15e9d6703_952x1081.png)

They straight-up map this entire complicated transformer block directly to the hardware. Data just flows thru…

Lots of op fusion… opportunities.

[![](https://substackcdn.com/image/fetch/$s_!Oqzq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F136a042d-1693-4524-bf8c-4f246f5ccb7a_948x532.png)](https://substackcdn.com/image/fetch/$s_!Oqzq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F136a042d-1693-4524-bf8c-4f246f5ccb7a_948x532.png)

[![](https://substackcdn.com/image/fetch/$s_!nIKc!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F940766f4-44f3-4866-9bcf-ca0f5c8cc1bd_955x535.png)](https://substackcdn.com/image/fetch/$s_!nIKc!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F940766f4-44f3-4866-9bcf-ca0f5c8cc1bd_955x535.png)

Which lets them collapse kernel launch overhead (pink) and compute (dark green) very efficiently. 

[![](https://substackcdn.com/image/fetch/$s_!wJ-w!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6f94b0b2-065c-46be-bd3f-b2b623992a84_454x404.png)](https://substackcdn.com/image/fetch/$s_!wJ-w!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6f94b0b2-065c-46be-bd3f-b2b623992a84_454x404.png)Apologies for the reflections. I suck at photography.

I am a big fan of how batshit insane this chip is. Want to believe it can be a real player in low-latency, high-throughput inference.

The engineers who attended claim that it only took a few hours to get Llama 3.1 working on the chip. They claim the compiler is good.

Wish them all the best. Out of all the AI hardware startups, SambaNova is my favorite but frankly, Nvidia and vertically integrated custom silicon will be very difficult to compete with.

### [3.f] FuriosaAI RNGD

Why does this company exist?

[![](https://substackcdn.com/image/fetch/$s_!zzls!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe8b9967f-6d55-4453-a4a5-47354c8f6f70_1853x998.png)](https://substackcdn.com/image/fetch/$s_!zzls!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe8b9967f-6d55-4453-a4a5-47354c8f6f70_1853x998.png)

To sell export-control compliant AI chips to China. Comparing yourself Nvidia L40S and Intel Gaudi 2 gives away your target market pretty decisivly.

[![](https://substackcdn.com/image/fetch/$s_!2IMY!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd230d018-0720-45a4-b23c-b8f621044425_1421x774.png)](https://substackcdn.com/image/fetch/$s_!2IMY!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd230d018-0720-45a4-b23c-b8f621044425_1421x774.png)

This slide is why I bothered to cover them. Really awesome signal integrity and power integrity plots. Beautifull stuff.

### [3.g] Frore AirJet

[![](https://substackcdn.com/image/fetch/$s_!1slo!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9a7214bc-9506-4000-a575-f1a3ff3b4cac_1545x825.png)](https://substackcdn.com/image/fetch/$s_!1slo!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9a7214bc-9506-4000-a575-f1a3ff3b4cac_1545x825.png)

A solid-state, active cooling, MEMS chip. Super cool (pun intended). Very narrow market where they can sell this thing. Embedded IoT where thermal stability is important?

[![](https://substackcdn.com/image/fetch/$s_!RNOp!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9cea4c6b-4cb0-4173-a71d-fb361a8313a8_889x764.png)](https://substackcdn.com/image/fetch/$s_!RNOp!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9cea4c6b-4cb0-4173-a71d-fb361a8313a8_889x764.png)

The MEMS vibrate in such a way that air is pushed out of the hollow inside of the chip. Allegedly, the vibrations are at a frequency that is not audible to humans. Dogs maybe, lol?

[![](https://substackcdn.com/image/fetch/$s_!Tq67!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F741a9c1f-9daf-4324-90bf-ebe98e10c36b_1567x730.png)](https://substackcdn.com/image/fetch/$s_!Tq67!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F741a9c1f-9daf-4324-90bf-ebe98e10c36b_1567x730.png)

They have a custom non-silicon Fab which is interesting… not sure how they are paying for this given the limited commercial applications of the product.

[![](https://substackcdn.com/image/fetch/$s_!cJs7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc72779bf-f513-492f-b9d8-6ad7cf0550b9_845x908.png)](https://substackcdn.com/image/fetch/$s_!cJs7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc72779bf-f513-492f-b9d8-6ad7cf0550b9_845x908.png)

[![](https://substackcdn.com/image/fetch/$s_!quzM!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff0e47d87-a00f-42ca-90bb-04327a9e1cb1_838x468.png)](https://substackcdn.com/image/fetch/$s_!quzM!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff0e47d87-a00f-42ca-90bb-04327a9e1cb1_838x468.png)

All of these applications have strict battery limits. Burning 1W for active cooling seems like a terrible design tradeoff.

[![](https://substackcdn.com/image/fetch/$s_!-xDK!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fff08af23-bcb0-4b30-9909-e42e955da2bb_837x939.png)](https://substackcdn.com/image/fetch/$s_!-xDK!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fff08af23-bcb0-4b30-9909-e42e955da2bb_837x939.png)

AirJet makes a lot of sense for embedded and industrial applications where any moving parts are a liability. Both of these use-cases have DC power inputs so burning 1W on active cooling is fine.

## [4] Bad

This section is dedicated to two types of presentations:

  1. Unviable products.

  2. Delivery/content was so bad that attendees learned almost nothing new on excellent products/engineering.




### [4.a] Tenstorrent 

I am a Jim Keller fanboi but this presentation… did not inspire confidence in Tenstorrent’s future.

[![](https://substackcdn.com/image/fetch/$s_!n0wL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1cbb5b42-216d-462c-83c4-631d48dd8e58_1415x741.png)](https://substackcdn.com/image/fetch/$s_!n0wL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1cbb5b42-216d-462c-83c4-631d48dd8e58_1415x741.png)

[![](https://substackcdn.com/image/fetch/$s_!l53W!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe0afb565-cdd4-4efa-88a4-8bd8b405b443_1417x786.png)](https://substackcdn.com/image/fetch/$s_!l53W!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe0afb565-cdd4-4efa-88a4-8bd8b405b443_1417x786.png)

[![](https://substackcdn.com/image/fetch/$s_!nKG0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3900920b-4673-4fee-a782-78cb354289cc_1556x809.png)](https://substackcdn.com/image/fetch/$s_!nKG0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3900920b-4673-4fee-a782-78cb354289cc_1556x809.png)

This architecture is “RSIC-V” to the max. Literally everything is controlled and managed by a baby RISC-V (super tiny) CPU core. Even DRAM and Ethernet control.

[![](https://substackcdn.com/image/fetch/$s_!rRXW!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9c0ca5a3-f9e1-48ea-96aa-a64d19f7b974_1556x710.png)](https://substackcdn.com/image/fetch/$s_!rRXW!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9c0ca5a3-f9e1-48ea-96aa-a64d19f7b974_1556x710.png)

[![](https://substackcdn.com/image/fetch/$s_!V4yL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdd3b62b2-1777-4f94-bf09-cc57e679c874_1508x733.png)](https://substackcdn.com/image/fetch/$s_!V4yL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdd3b62b2-1777-4f94-bf09-cc57e679c874_1508x733.png)

The compute cores have five baby RISC-V cores calling the shots.

[![](https://substackcdn.com/image/fetch/$s_!6VD9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb4cafbcb-6416-4320-9623-3ff5eafc33f5_1554x866.png)](https://substackcdn.com/image/fetch/$s_!6VD9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb4cafbcb-6416-4320-9623-3ff5eafc33f5_1554x866.png)

Some mapping of neural network structures to the hardware is possible but not nearly to the degree of flexibility as SambaNova. 

[![](https://substackcdn.com/image/fetch/$s_!YmbK!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff26d304b-f583-4b9c-b49f-ae880aad1cd3_1529x780.png)](https://substackcdn.com/image/fetch/$s_!YmbK!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff26d304b-f583-4b9c-b49f-ae880aad1cd3_1529x780.png)

[![](https://substackcdn.com/image/fetch/$s_!gAEV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Feb5f6245-a7d1-4c35-ab71-e948d162e12c_1267x707.png)](https://substackcdn.com/image/fetch/$s_!gAEV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Feb5f6245-a7d1-4c35-ab71-e948d162e12c_1267x707.png)

Here is a very important fact that was revealed in Q&A:

 **The baby RISC-V cores are heterogeneous** depending on which higher level core they reside in. Each has it’s own ISA extensions.

RISC-V toolchain was already lacking and now Tenstorrent has multiple flavors and custom ISA extensions sprinkled throughout one chip. Compiler and programmer nightmare.

[![](https://substackcdn.com/image/fetch/$s_!ZM2v!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffb3789af-196e-458e-9dab-4ce33652c475_1562x878.png)](https://substackcdn.com/image/fetch/$s_!ZM2v!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffb3789af-196e-458e-9dab-4ce33652c475_1562x878.png)

[![](https://substackcdn.com/image/fetch/$s_!zwBz!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F72a08f09-1590-4b96-8677-2905d75a41b4_1523x817.png)](https://substackcdn.com/image/fetch/$s_!zwBz!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F72a08f09-1590-4b96-8677-2905d75a41b4_1523x817.png)

From a high-level, their scaling system seems elegant at first. Once core is one chip is one system. The programming model just extends outward to bigger and bigger systems because everything is Ethernet.

Latency non-uniformity almost certainly kills their chances with inference. 

[![](https://substackcdn.com/image/fetch/$s_!N5Ti!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F55eac78a-e072-4797-867d-c364ea819009_1536x804.png)](https://substackcdn.com/image/fetch/$s_!N5Ti!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F55eac78a-e072-4797-867d-c364ea819009_1536x804.png)

I spoke with someone (not Tenstorrent employee) at the conference and he said this TT-Metalium software stack is their 6th attempt. Credit to Tenstorrent for realizing the first five attempts were unsalvageable and starting from scratch.

They are way behind on the software front and the current (6th iteration) software stack delivers… not great performance. Thankfully, Tenstorrent is selling developer kits, and the open-source freaks are working hard on propping them up. **They have a path forward, only because of the excellent, developer-first mindset.**

### [4.b] Nvidia Blackwell Advertisement Re-Run

Almost nothing in this presentation was new. Only the Quazar (brand name for OCP MX micro-scaling) stuff was new and worth covering.

[![](https://substackcdn.com/image/fetch/$s_!RpW6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffeda8578-3e8e-4d27-b61f-e0a337fed55d_1173x656.png)](https://substackcdn.com/image/fetch/$s_!RpW6!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffeda8578-3e8e-4d27-b61f-e0a337fed55d_1173x656.png)

Fine granularity quantization of individual rows.

[![](https://substackcdn.com/image/fetch/$s_!GbvE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4e6ed6b5-0b54-4cee-bf07-1fb1d9729592_1279x685.png)](https://substackcdn.com/image/fetch/$s_!GbvE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4e6ed6b5-0b54-4cee-bf07-1fb1d9729592_1279x685.png)

Speedup depends on compute utilization and how the workload response to micro-scaling so take this table with a large crystal of salt.

[![](https://substackcdn.com/image/fetch/$s_!av2o!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F407b5f92-d7ce-46f1-9ae2-b722aba6736b_1098x676.png)](https://substackcdn.com/image/fetch/$s_!av2o!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F407b5f92-d7ce-46f1-9ae2-b722aba6736b_1098x676.png)

Ah yes, the moat just got 10 feet deeper. Nice.

[![](https://substackcdn.com/image/fetch/$s_!H5eY!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3c53c29f-fdc9-49fd-9754-1c3b30e73fdf_1239x722.png)](https://substackcdn.com/image/fetch/$s_!H5eY!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3c53c29f-fdc9-49fd-9754-1c3b30e73fdf_1239x722.png)

In Q&A, Dr. Ian Cutress absolutely roasted Nvidia, repeatedly asking if the Bluefield product line was dead. There is no BF4 on the roadmap. It is dead. The presenters sort of panicked and kept pointing to BF3 being on this slide. Very funny exchange.

###  **[4.c] Literally Every Single AMD Presentation**

AMD showed up to this conference determined to not share any new information and bore the audience into a coma. The content was bad. The presenters read from notes in the most boring, monotone manner possible, and nobody learned anything new.

There are only two slides I want to include, both from Victor (retired) Peng’s presentation.

[![](https://substackcdn.com/image/fetch/$s_!Vtgf!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2dcce442-2714-46bc-878b-65d363e3faa7_1903x1060.png)](https://substackcdn.com/image/fetch/$s_!Vtgf!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2dcce442-2714-46bc-878b-65d363e3faa7_1903x1060.png)

Years from now when this bubble pops and we are all in economic ruin, the symbol of said bubble will be a fucking llama wearing blue sunglasses. Why are the sunglasses always blue? An anthropologist needs to answer this critical question.

[![](https://substackcdn.com/image/fetch/$s_!PPqP!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0443cc48-fd6c-4154-94ba-118b8c3f104f_853x456.png)](https://substackcdn.com/image/fetch/$s_!PPqP!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0443cc48-fd6c-4154-94ba-118b8c3f104f_853x456.png)

One of the AI applications he highlighted is using AI to identify if fish are healthy.

HEDGE FUND, INVESTMENT BANKING, AND FINANCE SUBSCRIBERS, WE HAVE FOUND THE MISSING AI REVENUE. BUBBLE NO MORE.

 _Jokes aside, this is a real edge AI use-case._

### [4.d] Cerebras Inference Pipedreams

[![](https://substackcdn.com/image/fetch/$s_!bBUM!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F12cfa411-bc58-49a1-b228-fb193095692b_857x566.png)](https://substackcdn.com/image/fetch/$s_!bBUM!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F12cfa411-bc58-49a1-b228-fb193095692b_857x566.png)

[![](https://substackcdn.com/image/fetch/$s_!iAq_!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F78b35b97-b20b-4b5b-9b80-97ffc9487e40_1266x710.png)](https://substackcdn.com/image/fetch/$s_!iAq_!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F78b35b97-b20b-4b5b-9b80-97ffc9487e40_1266x710.png)

[![](https://substackcdn.com/image/fetch/$s_!gW1L!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F283ff302-4163-4293-af4a-130e3b7e6188_1103x690.png)](https://substackcdn.com/image/fetch/$s_!gW1L!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F283ff302-4163-4293-af4a-130e3b7e6188_1103x690.png)

Cerebras makes chips the size of a wafer. They have developed incredible, breakthrough technologies to enable this.

  * Cross-reticle die stitching. 

  * Cooling an entire wafer that burns like 20 KW at peak.

  * Power delivery.

  * PVT auto-management in firmware for stable clocks and high yield.




I am a huge fan of this company but will still mercilessly attack the false narratives they are pushing with respect to their AI capabilities. 

This is an amazing HPC company. Biopharma, oil/gas, supercomputing, thermo/fluid simulations, nuclear simulations, bleeding edge science.

[![](https://substackcdn.com/image/fetch/$s_!HWPF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff6837c9b-0186-48e1-861b-6980554b21ff_937x521.png)](https://substackcdn.com/image/fetch/$s_!HWPF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff6837c9b-0186-48e1-861b-6980554b21ff_937x521.png)

You have 44GB of SRAM on one chip. I would hope the performance of a tiny 8B parameter model is much higher than this.

[![](https://substackcdn.com/image/fetch/$s_!7npP!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7afd856a-1ec5-4ecd-8a01-41e8f14c5350_938x523.png)](https://substackcdn.com/image/fetch/$s_!7npP!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7afd856a-1ec5-4ecd-8a01-41e8f14c5350_938x523.png)

[![](https://substackcdn.com/image/fetch/$s_!7Z8H!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F539e590c-32ec-4349-90f9-90e1bf6d7ae7_931x524.png)](https://substackcdn.com/image/fetch/$s_!7Z8H!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F539e590c-32ec-4349-90f9-90e1bf6d7ae7_931x524.png)

The bandwidth and power efficiency is great… a **s long as you stay on one Wafer Scale Engine.**

Llama3.1-70B is too large to fit.

[![](https://substackcdn.com/image/fetch/$s_!IJui!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7db5685a-a434-4efa-92ee-5779fb15acb4_938x528.png)](https://substackcdn.com/image/fetch/$s_!IJui!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7db5685a-a434-4efa-92ee-5779fb15acb4_938x528.png)

Naturally? You hit massive latency problems because of the proprietary parallel-port, memI/O style interconnect for moving data from the wafer to Ethernet.

[![](https://substackcdn.com/image/fetch/$s_!ub8p!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6477ccd3-ee38-4593-8178-73278db51bd4_915x515.png)](https://substackcdn.com/image/fetch/$s_!ub8p!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6477ccd3-ee38-4593-8178-73278db51bd4_915x515.png)

There are no Llama3.1-405B results in the presentation because they suck. This solution is not scalable. Cerebras managed to cobble together a few toy demos with small models and don’t have anything commercially viable.

[![](https://substackcdn.com/image/fetch/$s_!-_CX!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F492317d1-7a3a-4221-8f79-f3d045791f17_511x306.png)](https://substackcdn.com/image/fetch/$s_!-_CX!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F492317d1-7a3a-4221-8f79-f3d045791f17_511x306.png)

[SRAM area scaling](https://fuse.wikichip.org/news/7343/iedm-2022-did-we-just-witness-the-death-of-sram/) is super dead. When Cerebras moves from N5 to N3P, they will get effectively zero scaling SRAM, only logic. There is a one-time innovation possible in which they slap an SRAM-only wafer on top with hybrid bonding.

[![](https://substackcdn.com/image/fetch/$s_!yHZw!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa3ae2c9d-b73a-477e-acb4-b987a7723902_1024x706.jpeg)](https://substackcdn.com/image/fetch/$s_!yHZw!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa3ae2c9d-b73a-477e-acb4-b987a7723902_1024x706.jpeg)

There are several factors that conflict with each other when trying to estimate the effective SRAM scaling of such a system.

  * Both wafers need significant area dedicated to TSVs.

  * The logic/normal wafer might be thermally limited.

  * Minor latency penalty for communication hits to the SRAM wafer.

  * I have no idea what the area ratio is for SRAM/logic on the existing WSE because none of the diagrams are to scale and the wafer images are too uniform.




Let’s be generous and say a next-generation WSE with a hybrid-bonded SRAM wafer will achieve 1.8x SRAM capacity scaling. After that, it’s over.

Cerebras loves to talk about a “GPU/HBM wall” but they have a wall too, a SRAM wall.

### [4.e] Microsoft Maia

Frankly, this presentation was just bad. Out of all the hypsercalers working on custom AI accelerators, Microsoft is dead last. The only nice thing I have to say is at least the Maia team showed up and presented, unlike Amazon Trainium/Inferentia.

[![](https://substackcdn.com/image/fetch/$s_!texa!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F58f5f80c-6cda-4322-98c6-eb9bdc7863a1_1518x857.png)](https://substackcdn.com/image/fetch/$s_!texa!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F58f5f80c-6cda-4322-98c6-eb9bdc7863a1_1518x857.png)

Two generations of HBM behind… and why is provisioned TDP 200W lower than designed TDP? Did they realize the performance is so bad that underclocking is the only way to salvage the project?

No performance data. Generic information. They don’t have anything.

### [4.f] Intel Gaudi 3 (is already dead)

The Gaudi products are from an acquisition Intel made back in 2019, Habana Labs. As is tradition, Intel mis-managed the acquired company into oblivion and has discontinued their products.

Gaudi 3 is the last Gaudi. The next product is a GPU called Falcon Shores that will use the OneAPI software framework. None of the Gaudi chips support OneAPI. Falcon Shores will not support the Gaudi software stack. **Zero forward compatibility.**

[![](https://substackcdn.com/image/fetch/$s_!Z_q3!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F137c9235-fd50-4db1-af89-fd16a1c52374_1266x712.png)](https://substackcdn.com/image/fetch/$s_!Z_q3!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F137c9235-fd50-4db1-af89-fd16a1c52374_1266x712.png)

VLIW compute units. None of the software stack is gona make it into OneAPI or Falcon Shores.

[![\[V\]ery \[L\]ong \[I\]ncoherent \[W\]riteup](https://substackcdn.com/image/fetch/$s_!lVhT!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1335e244-45bb-4add-a677-d9ab1ed74702_875x957.png)

#### [V]ery [L]ong [I]ncoherent [W]riteup

[Daud's Scout](https://substack.com/profile/135313705-dauds-scout)·February 24, 2024[Read full story](https://irrationalanalysis.substack.com/p/very-long-incoherent-writeup)](https://irrationalanalysis.substack.com/p/very-long-incoherent-writeup)

### [4.g] Tutorial: Qualcomm On-Device AI

This presentation was a copeium advertisement for [QCOM 0.00%↑](https://substack.com/discover/stocks/QCOM) irrelevance in the genAI era. 

[![](https://substackcdn.com/image/fetch/$s_!-D6h!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F959db962-b01c-4759-a21d-2b926a507a99_926x488.png)](https://substackcdn.com/image/fetch/$s_!-D6h!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F959db962-b01c-4759-a21d-2b926a507a99_926x488.png)No it’s not.

[![](https://substackcdn.com/image/fetch/$s_!NxVY!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6b83dcda-dcc8-48a3-a4fc-55905e9c77f0_1285x985.png)](https://substackcdn.com/image/fetch/$s_!NxVY!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6b83dcda-dcc8-48a3-a4fc-55905e9c77f0_1285x985.png)Source: Evercore discussions with Qualcomm investor relations.

[![](https://substackcdn.com/image/fetch/$s_!dzqu!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F07ecf2f5-de9e-4b27-849f-332d5800a37d_935x536.png)](https://substackcdn.com/image/fetch/$s_!dzqu!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F07ecf2f5-de9e-4b27-849f-332d5800a37d_935x536.png)The vast majority of quantization efforts are on FP4 and various floating-point MX standards, not INT4.

Sub-10B LLMs suck. Why have a bad experience when a much better experience is less than 150ms latency away in the cloud?

[![](https://substackcdn.com/image/fetch/$s_!whPb!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4ce6811c-c3e9-4f30-8bdc-1d684442b869_932x527.png)](https://substackcdn.com/image/fetch/$s_!whPb!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4ce6811c-c3e9-4f30-8bdc-1d684442b869_932x527.png)

LLM models also burn through all the user’s battery when run on a smartphone, turning the device into a hand warmer. Why should anyone generate images locally on their phone when much higher quality images can be generated in the cloud using **industry-leading wireless connectivity?**

[![](https://substackcdn.com/image/fetch/$s_!JJZ-!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0a389b71-478c-4914-92cd-1bbaa6a3ab77_925x456.png)](https://substackcdn.com/image/fetch/$s_!JJZ-!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0a389b71-478c-4914-92cd-1bbaa6a3ab77_925x456.png)

I bought one of these Snapdragon X Elite laptops and struggled to get the NPU to activate at all. After hours of trying, I found one workload that only activated the NPU to 3% utilization according to task manager.

[![\[1/3\] Dell XPS \(TributoQC\) 13 Review](https://substackcdn.com/image/fetch/$s_!xPDW!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb4ecb4fc-5e71-46b2-995b-66adecffbac0_842x614.png)

#### [1/3] Dell XPS (TributoQC) 13 Review

[Daud's Scout](https://substack.com/profile/135313705-dauds-scout)·July 27, 2024[Read full story](https://irrationalanalysis.substack.com/p/13-dell-xps-tributoqc-13-review)](https://irrationalanalysis.substack.com/p/13-dell-xps-tributoqc-13-review)

### [4.h] Phononic Solid-State Cooling

Here is another solid-state cooling solution but with an utterly implausible commercial pitch. This device was designed to control the temperature of optical engines and other highly sensitive loads. Use a lot of power to make sure the target device stays in a narrow temperature band.

[![](https://substackcdn.com/image/fetch/$s_!A7lY!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fece06751-6bfb-4821-9aac-74561516d21c_1250x713.png)](https://substackcdn.com/image/fetch/$s_!A7lY!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fece06751-6bfb-4821-9aac-74561516d21c_1250x713.png)

They have made a product that has no reason to exist. A tower air cooler that can have solid-state active cooling kick-in to dynamically increase thermal dissipation. 

Why is this better than just spinning the fans at a higher RPM?

Does the efficiency of this system make sense? (No!)

## [5] Dumpster Fire

No redeeming qualities. 

[![](https://substackcdn.com/image/fetch/$s_!qzuG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2a135781-3d6d-45c7-a72c-2424a33e1f78_584x584.webp)](https://substackcdn.com/image/fetch/$s_!qzuG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2a135781-3d6d-45c7-a72c-2424a33e1f78_584x584.webp)

### [5.a] Ampere Computing

Ampere Computing is a company that made a niche product, cloud-optimized ARM (ISA) CPUs, and has since been abandoned by every single customer they had except [ORCL 0.00%↑](https://substack.com/discover/stocks/ORCL) who only buys chips from Ampere Computing because they have massive bags. 

[![](https://substackcdn.com/image/fetch/$s_!IH_O!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fadd10fec-7d8d-42ec-833f-249ce19b12fb_768x1182.png)](https://substackcdn.com/image/fetch/$s_!IH_O!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fadd10fec-7d8d-42ec-833f-249ce19b12fb_768x1182.png)Source: [Reuters](https://www.reuters.com/technology/oracle-spends-more-than-100-million-ampere-chips-2023-09-22/)

<COUGH COUGH> RELATED-PARTY ROUND-TRIPPED REVENUE <COUGH COUGH>

I will be adding some subtle enhancements to the slides. See if you can spot them.

[![](https://substackcdn.com/image/fetch/$s_!InWF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8422ff3f-b51a-4866-ad96-3711222b1788_926x576.png)](https://substackcdn.com/image/fetch/$s_!InWF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8422ff3f-b51a-4866-ad96-3711222b1788_926x576.png)

There is a paradigm shift, to an army of competitors that do your niche better. Competitors who have real 3rd-party customers.

It’s not just the ARM semi-custom chips cloud hyperscalers have made. Intel and AMD both have compelling x86 products in this cloud-optimized market segment. Intel Clearwater Forrest looks incredible. 

[![](https://substackcdn.com/image/fetch/$s_!pCTi!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe134be12-9cdf-4cef-a53f-3fe1c2322266_837x453.png)](https://substackcdn.com/image/fetch/$s_!pCTi!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe134be12-9cdf-4cef-a53f-3fe1c2322266_837x453.png)

[![](https://substackcdn.com/image/fetch/$s_!Kq4V!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4cc7bdb6-61f0-451b-86f3-a84a525530be_1027x556.png)](https://substackcdn.com/image/fetch/$s_!Kq4V!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4cc7bdb6-61f0-451b-86f3-a84a525530be_1027x556.png)

There are rumors that the mesh is licensed from ARM. Last generation, they had a custom mesh. 

[![](https://substackcdn.com/image/fetch/$s_!BEz9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8ac81950-32dd-4e47-a33a-37482a9556a8_1252x686.png)](https://substackcdn.com/image/fetch/$s_!BEz9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8ac81950-32dd-4e47-a33a-37482a9556a8_1252x686.png)

They compare perf/watt against Genoa (not the real competing product) when Bergamo data is literally on the same slide!

Let’s fix that.

[![](https://substackcdn.com/image/fetch/$s_!skwj!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6257a2b9-ad92-4977-8bdf-b418cc08021d_870x822.png)](https://substackcdn.com/image/fetch/$s_!skwj!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6257a2b9-ad92-4977-8bdf-b418cc08021d_870x822.png)

Intel Clearwater Forest and AMD Turin dense (2025 release) will beat Ampere Computing to market and annihilate them in perf/watt.

[![](https://substackcdn.com/image/fetch/$s_!dVom!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F33e18067-9f76-4822-b355-f8f6867f7d98_1242x682.png)](https://substackcdn.com/image/fetch/$s_!dVom!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F33e18067-9f76-4822-b355-f8f6867f7d98_1242x682.png)

Nobody is running these inference workloads on CPUs. The actual CPU inference workloads (tabular data, heavy financial inference) run on Intel Xeon because of the excellent AMX extensions, accompanying software stack, and broad x86 ecosystem.

[![](https://substackcdn.com/image/fetch/$s_!sHoJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb9caf353-38ac-47f4-b57b-7c9f11645602_860x473.png)](https://substackcdn.com/image/fetch/$s_!sHoJ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb9caf353-38ac-47f4-b57b-7c9f11645602_860x473.png)

Indeed, the ecosystem is ready. All your customers (excluding Oracle) bought your chips to port their software to ARM and have now gone vertical. 

### [5.b] SK Hynix In-Memory Compute

Every in-memory compute project has the same problem. The process node for memory is very bad if you try to add logic. PPA of complex transistor structures is really bad on a process designed for highly uniform capacitor banks.

This SK presentation did not address any of this process tech stuff.

[![](https://substackcdn.com/image/fetch/$s_!yyyK!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fea20e6a7-aa02-490f-b11c-dda4f47ee677_1261x704.png)](https://substackcdn.com/image/fetch/$s_!yyyK!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fea20e6a7-aa02-490f-b11c-dda4f47ee677_1261x704.png)

To evaluate these compute-in-memory GDDR6 chips, they needed a FPGA host, purely for testing.

Except none of the test results are real. It’s all simulations as the prototype they are presenting has not been brought up yet. 

In Q&A, they were absolutely roasted. It was argued that spending R&D effort on reducing the energy cost of memory interfaces to main logic would be far more productive than trying to fuse compute into the memory die itself. 

This idea does not work (no test data) and has no commercial future.

## [6] Terrifying — Trevor Cai, the OpenAI Guy

This presentation is so special, it deserves its own category. 

### [6.a] Excellent Technical Material

[![](https://substackcdn.com/image/fetch/$s_!WCzy!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F71aeffe4-da28-4655-97c2-4540c4b35617_1016x317.png)](https://substackcdn.com/image/fetch/$s_!WCzy!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F71aeffe4-da28-4655-97c2-4540c4b35617_1016x317.png)

Silent data corruption (SDC) is a problem that got a lot of attention. I wonder if the source of these SDCs is GPU SRAM or logic/timing faults.

[![](https://substackcdn.com/image/fetch/$s_!o3nb!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffaa13f64-a53c-4b47-92cf-5ffb0802993d_1156x438.png)](https://substackcdn.com/image/fetch/$s_!o3nb!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffaa13f64-a53c-4b47-92cf-5ffb0802993d_1156x438.png)

[![](https://substackcdn.com/image/fetch/$s_!ZN1p!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F12058555-2508-4a85-b19f-74b3f043a21c_1156x419.png)](https://substackcdn.com/image/fetch/$s_!ZN1p!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F12058555-2508-4a85-b19f-74b3f043a21c_1156x419.png)

Wonder if he thinks the new Blackwell RAS engine is enough. What gaps are still there in self-test coverage.

Link-flaps on one port effecting neighboring network ports is very difficult to mitigate. Bad links effectively behave like sinusoidal noise sources, dumping jitter/noise into neighbors. The SerDes CDR needs to be more robust.

[![](https://substackcdn.com/image/fetch/$s_!0S-s!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcb4ea5a5-99e2-4622-8e98-5d2a803d28d7_418x286.png)](https://substackcdn.com/image/fetch/$s_!0S-s!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcb4ea5a5-99e2-4622-8e98-5d2a803d28d7_418x286.png)A flapping link can dump noise into neighbors that is outside the official IEEE tolerance spec.

[![](https://substackcdn.com/image/fetch/$s_!4iA-!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4e537dcd-0855-4808-b60b-d198936e61ad_600x249.webp)](https://substackcdn.com/image/fetch/$s_!4iA-!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4e537dcd-0855-4808-b60b-d198936e61ad_600x249.webp)Depending on the receiver design, a degraded link (aggressor) may dump deterministic jitter (phase interpolator constant rotation), or random jitter (multiple blocks randomly searching for a re-lock).

[![](https://substackcdn.com/image/fetch/$s_!uOFy!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F987dee69-f05e-4440-b919-76e04500bb5a_1103x445.png)](https://substackcdn.com/image/fetch/$s_!uOFy!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F987dee69-f05e-4440-b919-76e04500bb5a_1103x445.png)

Induced noise from a degraded link depends on the CDR design. The commonality is an oscillator dumping asynchronous noise via electromagnetic coupling and/or supply/ground pollution.

[![](https://substackcdn.com/image/fetch/$s_!vKG9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd1b2eacc-6222-4471-a5a0-e12c63232521_1072x286.png)](https://substackcdn.com/image/fetch/$s_!vKG9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd1b2eacc-6222-4471-a5a0-e12c63232521_1072x286.png)

Interesting that transient power response is becoming problematic for cluster stability.

OOB power management is possible by using firmware and board-level PMICs, shunt resistors, ADCs, and so on.

Making that OOB power telemetry both accurate and low latency is uh… extremely difficult. Manufacturing variances in silicon, PCB material, and analog surface-mount components make current measurements surprisingly inaccurate. Synchronizing thousands of I2C-triggered measurements is a challenge by itself, to say nothing of the latency issues. 

Wonder what the latency requirement would be. 10 ms? 200 ms? 

### [6.b] “Sometimes lines really do go up”

[![](https://substackcdn.com/image/fetch/$s_!vyN-!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff448be20-c1b3-44ea-a3cb-2c8dee2332c5_992x605.png)](https://substackcdn.com/image/fetch/$s_!vyN-!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff448be20-c1b3-44ea-a3cb-2c8dee2332c5_992x605.png)Curve-fitting works.

We can curve-fit observations to predict future scaling!

[![](https://substackcdn.com/image/fetch/$s_!4-1J!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F33fab7a6-d5b2-45a5-bf35-406004ee19e1_1005x605.png)](https://substackcdn.com/image/fetch/$s_!4-1J!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F33fab7a6-d5b2-45a5-bf35-406004ee19e1_1005x605.png)Except when it does not.

But actually no. Scaling went from 6.7x to 4.2x per year.

So… which is it? Can we arbitrarily curve-fit empirical data and extrapolate to infinity or not? 

Trevor Cai, the OpenAI guy, tried to make an economic argument that I strongly disagree with. 

“Sometimes lines really do go up.”

Both of the examples he gave have decisive counterarguments.

#### [6.b.i] Solar Panels

[![](https://substackcdn.com/image/fetch/$s_!qsE6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff28b2071-e2bb-4457-a358-fc89f83e8af8_905x614.png)](https://substackcdn.com/image/fetch/$s_!qsE6!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff28b2071-e2bb-4457-a358-fc89f83e8af8_905x614.png)

Oh, wow the International Energy Agency repeatedly mis-predicted solar-power capacity expansion trends. Well… they did not predict **China state-run economic policy** encouraging massive un-economic capacity expansions and **dumping solar panels below COGS!**

[![](https://substackcdn.com/image/fetch/$s_!_uFh!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F10d3dab2-207e-4cf1-8604-c02660e0fcb6_1387x784.png)](https://substackcdn.com/image/fetch/$s_!_uFh!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F10d3dab2-207e-4cf1-8604-c02660e0fcb6_1387x784.png) Source: $FSLR 1Q2024 Earnings Slides

[![](https://substackcdn.com/image/fetch/$s_!c0DX!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F77de1aa8-d736-407c-9df4-73827d01ffc4_762x1140.png)](https://substackcdn.com/image/fetch/$s_!c0DX!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F77de1aa8-d736-407c-9df4-73827d01ffc4_762x1140.png)Source: [Reuters](https://www.reuters.com/business/energy/china-solar-industry-faces-shakeout-rock-bottom-prices-persist-2024-04-03/)

Ironically, this example of why we should not be worried about a massive genAI bubble demonstrates why we would be terrified!

What happens if all these datacenters produce nothing more than 10 duplicative chatbots of similar performance with no meaningful demand? 

Massive. Compute. Overcapacity.

#### [6.b.ii] Moore’s Law

[![](https://substackcdn.com/image/fetch/$s_!IgaP!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdec0cecd-0068-40ab-9352-4ff00210e7fd_968x593.png)](https://substackcdn.com/image/fetch/$s_!IgaP!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdec0cecd-0068-40ab-9352-4ff00210e7fd_968x593.png)

Funny how Moore’s law is brough up as a defense for lines go up. 

**Moore’s law has always been an economic law.** It makes sense to move to a new, denser process node because the economic value of the product goes up.

Huge up-front CapEx spend for Fabs is justified because the demand will be there for the latest node.

Except this has changed. The latest nodes are too expensive.

Chiplets are being used as a cost-saving strategy. Everyone is trying to minimize content on 3nm-class nodes. 

Some products that would traditionally be launched on the latest node are instead choosing N-1.

[![](https://substackcdn.com/image/fetch/$s_!KV37!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F47f80863-f897-4b21-9fd2-2e9271d1fb7a_588x337.png)](https://substackcdn.com/image/fetch/$s_!KV37!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F47f80863-f897-4b21-9fd2-2e9271d1fb7a_588x337.png)[Source](https://x.com/dnystedt/status/1829341138471596341?t=99BIl2QRcIDc_Owr98Mw5A)

Many products will not move past the 3nm-class (TSMC N3E/P/X, Samsung SF2, Intel 18A) generation. This era of process technology represents a cost wall. 

Moore’s law is dead, not because transistor scaling is dead. Chiplets and advanced packaging will keep density scaling alive. 

**The economic facet of Moore’s law is dead.**

It no longer makes sense to move every product to the latest node.

It’s over. Line no longer go up.

### [6.c] Surreal Bubble Inflation

Sitting in the audience listening to this presentation was surreal. It was like watching a bubble inflate in real time.

Someone in Q&A asked about ROI. You know shit has gone off the rails when engineers are asking about ROI at a technical conference.

To demonstrate the absurdity of where we are, I have created a meme using one of my favorite films, “The Big Short (2015)”.

[![](https://substackcdn.com/image/fetch/$s_!fRrR!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff72c4a1e-03ac-43b1-a25d-a39ddad0ee5e_768x4129.jpeg)](https://substackcdn.com/image/fetch/$s_!fRrR!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff72c4a1e-03ac-43b1-a25d-a39ddad0ee5e_768x4129.jpeg)

We are going so much higher. DotCom and tulips got nothing on genAI.

[![](https://substackcdn.com/image/fetch/$s_!HPuv!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe1c7faec-bb00-4052-a4e4-0be3f604b0d1_1024x1024.jpeg)](https://substackcdn.com/image/fetch/$s_!HPuv!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe1c7faec-bb00-4052-a4e4-0be3f604b0d1_1024x1024.jpeg)

## [7] Winners and Losers

Ok, investment time!

Here are the winners and losers (with runners up) divided amongst public and private companies.

 **Public Winner:** [AVGO 0.00%↑](https://substack.com/discover/stocks/AVGO)

The co-packaged optics presentation was incredible. High-quality test data shared with maximum confidence. Excellent technical details. Bravo. 

**Public Winner Runner-Up:** [NVDA 0.00%↑](https://substack.com/discover/stocks/NVDA)

Galaxy-brain researchers work at Nvidia, developing innovative AI-based chip design techniques that yield massive productivity boosts and performance improvements.

 **Private Winner:** OpenAI

Thier chip-design and infrastructure team is kickass. Very excited to see what they put together in the coming years. They are going to raise a new funding round at $100-125B valuation and dump that money into making breakthrough chips.

[![](https://substackcdn.com/image/fetch/$s_!UhKV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd57552a0-bba6-434b-97de-4e2083b68ad4_866x542.png)](https://substackcdn.com/image/fetch/$s_!UhKV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd57552a0-bba6-434b-97de-4e2083b68ad4_866x542.png)

Bubble is inflating but that is a problem for the future. 

[![](https://substackcdn.com/image/fetch/$s_!RgFW!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F47684aed-fce5-4c8d-afc8-541cc3961861_638x795.png)](https://substackcdn.com/image/fetch/$s_!RgFW!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F47684aed-fce5-4c8d-afc8-541cc3961861_638x795.png)

**Private Winner Runner-Up:** Cerebras

Many poorly informed investors are going to fall for the inference story Cerebras concocted. IPO will pop. Try to get allocation on the way up, then find an opportune moment to short them aggressively.

[![](https://substackcdn.com/image/fetch/$s_!7amK!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F193a12cf-9bd5-4242-b4f9-1ba757be7ae4_564x473.png)](https://substackcdn.com/image/fetch/$s_!7amK!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F193a12cf-9bd5-4242-b4f9-1ba757be7ae4_564x473.png)

DO NOT SHORT THEM WITHIN THE FIRST MONTH OF TRADING.

Cerebras is a good company that makes a niche HPC solution. Quality engineering that deserves some valuation, just not an AI hype valuation.

I admire the incredible engineering Cerebras has and would love to own shares long-term once the bubble pops and they are appropriately valued as a breakthrough HPC company, rather than an AI head fake.

 **Public Loser:** [MRVL 0.00%↑](https://substack.com/discover/stocks/MRVL)

Broadcom is going to crush this company. CPO will destroy the oDSP business. The incredible new custom-silicon platform will poach Marvell customers over time.

[![Harlan Sur's \(JPM\) Massive $AVGO Scoop](https://substackcdn.com/image/fetch/$s_!3n3l!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F60b0a260-4747-4755-9612-6bcc98814be3_1024x1024.jpeg)

#### Harlan Sur's (JPM) Massive $AVGO Scoop

[Daud's Scout](https://substack.com/profile/135313705-dauds-scout)·August 23, 2024[Read full story](https://irrationalanalysis.substack.com/p/harlan-surs-jpm-massive-avgo-scoop)](https://irrationalanalysis.substack.com/p/harlan-surs-jpm-massive-avgo-scoop)

 **To be clear, the short-term outlook for Marvell is amazing.** Amazon orders, oDSP, and (hate to admit this) telco market recovery are all going to hit at once and make this ticker moon. 

DO NOT INVEST IN THIS COMPANY LONG TERM.

PLAN TO BE OUT BY SUMMER 2025.

[![](https://substackcdn.com/image/fetch/$s_!Gp1Z!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F21d58619-43a0-4839-b661-ce8f991c0dff_775x433.png)](https://substackcdn.com/image/fetch/$s_!Gp1Z!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F21d58619-43a0-4839-b661-ce8f991c0dff_775x433.png)

 **Public Loser Runner-up:** [INTC 0.00%↑](https://substack.com/discover/stocks/INTC)

Lunar Lake is going to annihilate gross margins. Sell-side and the finance community have no idea what is coming.

 **Private Loser:** Ampere Computing

They have no customers other than Oracle, who have heavily invested in them. 

****The vast majority of revenue is related party revenue.****

If they ever make it to the public markets, I will short them in size and write a detailed short report in LaTeX. 

**Day one short.** Long [ARM 0.00%↑](https://substack.com/discover/stocks/ARM) for the most concentrated alpha trade of all time. 

[![](https://substackcdn.com/image/fetch/$s_!t0yI!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6d753849-8f43-4b2d-80c0-91f4b43befd2_1019x463.png)](https://substackcdn.com/image/fetch/$s_!t0yI!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6d753849-8f43-4b2d-80c0-91f4b43befd2_1019x463.png)

[![](https://substackcdn.com/image/fetch/$s_!LK-u!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff9fad275-3207-43d3-98be-8f45f1cb061a_889x886.png)](https://substackcdn.com/image/fetch/$s_!LK-u!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff9fad275-3207-43d3-98be-8f45f1cb061a_889x886.png)

**Private Loser Runner-Up:** Tenstorrent

This architecture is too damn complicated. No human can hope to program this PHD science project that somehow has a $2B valuation. 

Someday, Artificial Super-Intelligence (ASI) will be created on someone else’s chip and only ASI will be able to effectively program Tenstorrent architecture.

* * *

I have an earnings post coming late next week that includes [NVDA 0.00%↑](https://substack.com/discover/stocks/NVDA) [MRVL 0.00%↑](https://substack.com/discover/stocks/MRVL) [AVGO 0.00%↑](https://substack.com/discover/stocks/AVGO) a special [INTC 0.00%↑](https://substack.com/discover/stocks/INTC) update, and an update on all my portfolio holdings. The spreadsheet I made years ago was never designed to keep track of short positions, hence the re-build from scratch and delay. 

Subscribe so you don’t miss it.

Subscribe

Already subscribed? Thanks! Please consider feeding my unhinged narcissism by sharing.

[Share](https://irrationalanalysis.substack.com/p/hot-chips-2024-irrational-recap?utm_source=substack&utm_medium=email&utm_content=share&action=share)
