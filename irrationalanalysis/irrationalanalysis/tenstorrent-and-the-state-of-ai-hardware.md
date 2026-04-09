# Tenstorrent and the State of AI Hardware Startups

## Semi-custom silicon is a bigger problem than Nvidia.

**Dec 15, 2024**

**Likes:** 0

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Please check the [‘about’ page](https://irrationalanalysis.substack.com/about) for a list of active positions.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice, and readers should **always do their own research before investing in any security.**

  * Feel free to contact me via email at: _irrational_analysis@proton.me_




* * *

I wrote some negative things after seeing Tenstorrent’s Hot Chips 2024 presentation.

[![Hot Chips 2024: Irrational Recap](https://substackcdn.com/image/fetch/$s_!HPuv!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe1c7faec-bb00-4052-a4e4-0be3f604b0d1_1024x1024.jpeg)

#### Hot Chips 2024: Irrational Recap

[Irrational Analysis](https://substack.com/profile/135313705-irrational-analysis)·September 2, 2024[Read full story](https://irrationalanalysis.substack.com/p/hot-chips-2024-irrational-recap)](https://irrationalanalysis.substack.com/p/hot-chips-2024-irrational-recap)

[![](https://substackcdn.com/image/fetch/$s_!DpBl!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6220436e-a311-4b51-9a16-f8299d48c867_753x226.png)](https://substackcdn.com/image/fetch/$s_!DpBl!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6220436e-a311-4b51-9a16-f8299d48c867_753x226.png)

A lot of Tenstorrent employees subscribed because of this post.

Surprisingly, David Bennet (Chief Customer Officer) invited me to meet senior software, architecture, and customer relations leadership for an open discussion.

The meeting lasted 1.5 hours and was a ton of fun. 

Before going over the actual content of this post, I would like to discuss the topic of bias.

Am I biased? Yes! This is why I regularly post all > 1% positions with average price.

The Tenstorrent people are very nice, and it was a lot of fun talking to them. This writeup is largely positive because Tenstorrent did a very good job of answering my questions with honest, technical answers. It’s up to you to decide for yourself if what I write is trustworthy.

  * I hold no economic interest in Tenstorrent.

  * Tenstorrent did not pay me any money or provide gifts of significant value.

    * I ate one cookie and drank a bottle of water.

    * Got a (branded) swag bag containing a hat, thermos, and cable carrying/travel bag.

  *  **No Tenstorrent staff have reviewed or edited this post. They will read it at the same time as everyone else.**




[![](https://substackcdn.com/image/fetch/$s_!DeL_!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff7384a4d-645d-4a09-a615-f00850e0a41a_3000x4000.jpeg)](https://substackcdn.com/image/fetch/$s_!DeL_!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff7384a4d-645d-4a09-a615-f00850e0a41a_3000x4000.jpeg) Behold, my conflicts of interest.

Made a framework for thinking about AI hardware startups at the end so this post has value to people who are not interested in Tenstorrent.

## Contents:

  1. Tenstorrent Technical Overview

  2. Discussion Summary 

    1. Register Spilling and v_

    2. Baby RISC-V Fragmentation

    3. Baby RISC-V Capabilities 

    4. History of the Software Stacks

    5. Latency

  3. Davor Capalija Whiteboard Diagram

  4. Tenstorrent Opinion and Valuation Framework

  5. Broader AI Hardware Startup Framework




* * *

## [1] Tenstorrent Technical Overview

[![](https://substackcdn.com/image/fetch/$s_!Dw1U!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F46f054ca-7d5a-4011-8c29-7c990cd97e4c_1508x719.jpeg)](https://substackcdn.com/image/fetch/$s_!Dw1U!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F46f054ca-7d5a-4011-8c29-7c990cd97e4c_1508x719.jpeg)This image is outdated. Grendel will be built on Samsung Foundry SF4X, a process node that is worse than TSMC N5.

Blackhole (gen 2) has detailed information and will be the focus of discussion.

Main takeaways for Grendel (gen 3):

  1. Move to chiplet architecture.

  2. Separate high-performance RISC-V CPU cores and AI cores into separate chiplets.




[![](https://substackcdn.com/image/fetch/$s_!ZjAK!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0b0cac18-83fa-410b-8763-f570a432553e_1431x747.png)](https://substackcdn.com/image/fetch/$s_!ZjAK!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0b0cac18-83fa-410b-8763-f570a432553e_1431x747.png)

Tenstorrent architecture is a mesh topology with a variety of blocks.

[![](https://substackcdn.com/image/fetch/$s_!Ed8i!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fec02e50b-3e46-4ed1-93e2-74f14c185296_1586x803.png)](https://substackcdn.com/image/fetch/$s_!Ed8i!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fec02e50b-3e46-4ed1-93e2-74f14c185296_1586x803.png)

The 16 big RISC-V CPU cores are for general purpose code. You can run Linux on them.

Baby RISC-V cores are super tiny embedded CPU cores. **The 725 baby RISC-V cores take up less than 1% of die area.**

[![](https://substackcdn.com/image/fetch/$s_!a24i!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F86170128-ccc3-4f11-9a0a-763e222a33c7_1568x739.png)](https://substackcdn.com/image/fetch/$s_!a24i!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F86170128-ccc3-4f11-9a0a-763e222a33c7_1568x739.png)

The point of these baby RISC-V cores is to launch kernels. They are basically the control logic. 

[![](https://substackcdn.com/image/fetch/$s_!PaG1!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd501919b-a4ff-4561-8a4a-9dfc24ec66ff_1487x732.png)](https://substackcdn.com/image/fetch/$s_!PaG1!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd501919b-a4ff-4561-8a4a-9dfc24ec66ff_1487x732.png)

Tensix cores are the AI compute building blocks. Each has five baby RISC-V to handle kernel launches. “Compute” is vector and matrix math engines.

Note that two of these baby RISC-V cores are dedicated to router nodes. Data-movement model is important for understanding a lot of the decisions made in this architecture.

[![](https://substackcdn.com/image/fetch/$s_!9i2w!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcdc184e2-5175-4899-90fd-14e5eb03a26a_1488x725.png)](https://substackcdn.com/image/fetch/$s_!9i2w!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcdc184e2-5175-4899-90fd-14e5eb03a26a_1488x725.png)

The compiler for these baby RSIC-V cores is a lightly modified GCC. Users do not need to plan kernel splitting for the three compute-assigned baby RISC-V as the compiler automatically does this. In other works, you only need to write one compute kernel, in theory.

[![](https://substackcdn.com/image/fetch/$s_!rPiF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6d227fdf-2527-4076-a0ea-13c91a9f8311_1521x839.png)](https://substackcdn.com/image/fetch/$s_!rPiF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6d227fdf-2527-4076-a0ea-13c91a9f8311_1521x839.png)

[![](https://substackcdn.com/image/fetch/$s_!DKTO!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F27eba209-0754-4fed-b86b-5c67a38da468_1538x792.png)](https://substackcdn.com/image/fetch/$s_!DKTO!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F27eba209-0754-4fed-b86b-5c67a38da468_1538x792.png)

[![](https://substackcdn.com/image/fetch/$s_!MJ4e!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9252cf48-fec1-4ab3-9f02-6b06a91f191e_1544x806.png)](https://substackcdn.com/image/fetch/$s_!MJ4e!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9252cf48-fec1-4ab3-9f02-6b06a91f191e_1544x806.png)

Baby RISC-V in DRAM and Ethernet “cores” are just router nodes.

[![](https://substackcdn.com/image/fetch/$s_!JExo!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4801d40a-538d-4e91-a620-4eafde011c6c_1548x792.png)](https://substackcdn.com/image/fetch/$s_!JExo!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4801d40a-538d-4e91-a620-4eafde011c6c_1548x792.png)

[![](https://substackcdn.com/image/fetch/$s_!egm7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F54ec588e-5cbb-4483-a523-5ae95fd6b7e2_1276x714.png)](https://substackcdn.com/image/fetch/$s_!egm7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F54ec588e-5cbb-4483-a523-5ae95fd6b7e2_1276x714.png)

## [2] Discussion Summary

I have tried to organize the 90 minutes of discussion into something readable. Only have my illegible notes, mediocre memory, and a few pictures of whiteboard drawings to work with.

Converting a free-form conversation amongst ~10 people into a coherent written summary is surprisingly difficult. If you have feedback, please share.

* * *

### [2.a] Register Spilling and v_

To prepare, I browsed the [Tenstorrent documentation](https://docs.tenstorrent.com/tt-metalium/) to see if anything jumped out.

[![](https://substackcdn.com/image/fetch/$s_!JBzU!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2ebf8c4e-11be-4475-b028-ca3736405264_1143x672.png)](https://substackcdn.com/image/fetch/$s_!JBzU!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2ebf8c4e-11be-4475-b028-ca3736405264_1143x672.png)

[![](https://substackcdn.com/image/fetch/$s_!vtbG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F25d26f23-05db-4c1b-815f-81cd81a3adb0_1164x559.png)](https://substackcdn.com/image/fetch/$s_!vtbG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F25d26f23-05db-4c1b-815f-81cd81a3adb0_1164x559.png)

Initially, I thought that register spilling was a super important feature. Tenstorrent responded that the baby RISC-V cores are so small, it does not make sense to have register spilling given the intended programming model.

Cores are either dedicated to data movement (router node control) or the compute units. In the case of compute, three baby RISC-V are assigned as a group. The higher-level compiler calls GCC 5 (five) times for each Tensix core.

[![](https://substackcdn.com/image/fetch/$s_!2JWM!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F52dd14f3-9c5c-4062-b184-d4e8f5ee23d0_1486x731.png)](https://substackcdn.com/image/fetch/$s_!2JWM!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F52dd14f3-9c5c-4062-b184-d4e8f5ee23d0_1486x731.png)

So the user compute kernel is already spitted before three instances of GCC get called.

Given the intended programming model, this seems fine. Still looks like a challenge for kernel writers but nothing unsurmountable. 

* * *

[![](https://substackcdn.com/image/fetch/$s_!KGTq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe0f12d52-69c2-4ab8-8c8d-c3ab8a0ebbc8_913x212.png)](https://substackcdn.com/image/fetch/$s_!KGTq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe0f12d52-69c2-4ab8-8c8d-c3ab8a0ebbc8_913x212.png)

These “v_” things showed up a lot and one line jumped out. It almost looked like this was some kind of sparsity support?

Turns out, this is the Tenstorrent RSIC-V way of implementing masking features from [AVX-512](https://travisdowns.github.io/blog/2020/05/26/kreg2.html) (x86) and [SVE](https://developer.arm.com/documentation/102476/latest/SVE-architecture-fundamentals) (aarch64). 

Masking features help with power saving. 

### [2.b] Baby RISC-V Fragmentation

At Hot Chips 2024, there was a moment in Q&A that I mis-interpreted. 

Incorrectly thought that the baby RISC-V cores have different ISAs.

Tenstorrent clarified that this is not correct. All 752 baby RSIC-V cores have the same ISA. The ones assigned to NOC (data movement) have structural optimizations for that workload (physical design…?) but no ISA difference.

One of my major concerns was RSIC-V ISA fragmentation and they clarified that this is not a problem. The same modified GCC gets called for everything.

### [2.c] Baby RISC-V Capabilities

[One of the programming examples on GitHub caught my interest.](https://github.com/tenstorrent/tt-metal/blob/main/tech_reports/prog_examples/add_2_integers_in_riscv/add_2_integers_in_riscv.md)

[![](https://substackcdn.com/image/fetch/$s_!v8zv!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8ec575cb-8cde-4af5-a514-a28f698b5102_1025x140.png)](https://substackcdn.com/image/fetch/$s_!v8zv!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8ec575cb-8cde-4af5-a514-a28f698b5102_1025x140.png)

I was curious on the compute capabilities of these baby RISC-V cores. Can users weave in some branchy logic or niche calculations in? Is anyone using this capability?

They were honest in answering this question. Yes, it is possible to have complex control flow in the data movement baby RISC-V assigned cores, but it is likely that users will encounter a bottleneck. These tiny cores are meant for kernel launches. 

Given the open-source nature of everything Tenstorrent, I still have hope some cracked programmer figures out how to make something cool happen along these lines.

### [2.d] History of the Software Stacks

There are a wide variety of software stacks supported by Tenstorrent.

[![](https://substackcdn.com/image/fetch/$s_!4y20!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4787ce24-0362-4481-bb2f-4c51fb36679b_2682x1310.webp)](https://substackcdn.com/image/fetch/$s_!4y20!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4787ce24-0362-4481-bb2f-4c51fb36679b_2682x1310.webp)

[![](https://substackcdn.com/image/fetch/$s_!H3HJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F36f6cde9-71ae-4041-bcdd-a436f18eebd5_2682x1492.webp)](https://substackcdn.com/image/fetch/$s_!H3HJ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F36f6cde9-71ae-4041-bcdd-a436f18eebd5_2682x1492.webp)

[![](https://substackcdn.com/image/fetch/$s_!pzbM!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1b61c5d7-7510-47e3-85a0-55455b98b325_1432x800.png)](https://substackcdn.com/image/fetch/$s_!pzbM!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1b61c5d7-7510-47e3-85a0-55455b98b325_1432x800.png)

The current software stack is attempt #6. A lot of good stuff but was curious what happened to attempts 1 thru 5.

Apparently, the old way was re-build the software stack with each new hardware revision and target workloads. 

They literally had the RTL engineers write software kernels… lol.

But the new method is to build unified software from the ground up and down. Let people come in from the top (ML model —> graph —> netlist) via Buda or from the bottom (low-level kernels), or somewhere in-between (Metalium, TT-NN, TT-MLIR). 

Entry points for everyone. **Maximum open-source and transparency.** Easy access to developer kits/hardware.

These days, some of the best kernels for Tenstorrent hardware are written by new grads and hobbyists on the [official Discord.](https://discord.gg/tenstorrent)

### [2.e] Latency

One major concern I have (and still have to an extent) is latency effecting the mesh topology of Tenstorrent scale-out. Latency kills inference performance. 

The first argument provided by Tenstorrent is their scale-out is much lighter than standard [RDMA over Converged Ethernet ](https://en.wikipedia.org/wiki/RDMA_over_Converged_Ethernet)(RoCE).

Apparently, they stripped a lot of features out. No TCP/IP. 

Other strategies they have been working on:

  1. Overlapping of data prefetch.

    1. Enabled by pipelining.

    2. Runs on DRAM baby RSIC-V cores.

  2. Z-shortcut very important for latency optimization.




[![](https://substackcdn.com/image/fetch/$s_!C8_4!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F22e4af46-d601-4fc5-baa6-ba296e3ee650_1507x832.png)](https://substackcdn.com/image/fetch/$s_!C8_4!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F22e4af46-d601-4fc5-baa6-ba296e3ee650_1507x832.png)

Tenstorrent showed me some internal-only slides on their recent latency reduction progress including performance progression of Llama 3.1 70B inference. Non-public slides and the ~10 minutes of conversation related to this topic were compelling.

 _(still a huge amount of work to be done to be clear)_

They claim the slides will eventually be published as a case-study on their GitHub. 

¯\\_(ツ)_/¯

### [2.F] Mixed Intelligence

Jim Keller (CEO of Tenstorrent) has previously worked on Tesla FSD. In multiple public talks, he has brought up an interesting line of thinking.

The anecdote is simple. Jim Keller says he taught his daughters to drive with two hours of practice. He did not need to feed his daughters exabytes of video data and spend months having them pour over all that video.

* * *

Tenstorrent has an implicate view that the future of AI is mixed-workload, not pure linear algebra spam. Yes, MATMUL go BRRRRRR is valuable, but CPU workloads will be needed in the future. That is the hope.

 **So far, this has not played out.** Nvidia Grace is an overpriced memory controller. AMD had mixed CPU and GPU chiplets in MI300A (almost no sales outside of two traditional HPC supercomputers) but is going all GPU chiplets in future generations. The vast majority of AMD datacenter GPU volume is the pure-GPU MI300X.

What’s interesting is that Tenstorrent is the last standing company that is working on AI and has a good CPU microarchitecture team. If future AI workloads need CPU integration, they are the only well positioned vendor.

I brought this up and asked Tenstorrent if they have customers moving towards or interested in a more mixed AI workload and they said not yet.

## [3] Davor Capalija Whiteboard Diagram

[![](https://substackcdn.com/image/fetch/$s_!C0ia!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F54eff9c2-02a4-4f81-8aa5-14f8a83df693_858x639.png)](https://substackcdn.com/image/fetch/$s_!C0ia!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F54eff9c2-02a4-4f81-8aa5-14f8a83df693_858x639.png)

Davor (Senior Software+Architecture Fellow) spent the majority of the meeting drawing stuff on a whiteboard and explaining the Tenstorrent architecture in great detail. He even went beyond and made direct comparisons to Nvidia/GPU (rip AMD), Google TPU, Groq, SambaNova, and Cerebras.

I found his framework so compelling that all this material needed to be broken out into a dedicated section.

Took pictures of the whiteboard (with permission) and re-created everything in Visio.

His arguments are very good. Going to tell you all up-front that I agree with 80% of what he said/drew.

 _A paraphrased summary of Davor’s arguments will be written in italics._ I will add my comments (including disagreements) afterward in regular (non-italicized) font.

* * *

[![](https://substackcdn.com/image/fetch/$s_!8ULs!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F341f54d8-c780-4070-bdb2-e807cdce57f2_583x1073.png)](https://substackcdn.com/image/fetch/$s_!8ULs!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F341f54d8-c780-4070-bdb2-e807cdce57f2_583x1073.png)Adaptation of Davor whiteboard drawings. **Note that all the arguments text is italicized. These are his arguments, not mine.**

 _CPU workloads are designed around cache hierarchy._

 _GPUs are originally built for graphics and designed for thread-based scaling. Each CUDA core is really an ALU. The streaming multiprocessor (SM) is the real GPU “core”. GPUs have fewer cache levels (only L1 and L2) compared to CPUs._

 _AI workloads need many cores and a DMA engine. Including L2 does not make sense._

 _Tenstorrent architecture is essentially a GPU, but better._

  *  _Cores are correct size in terms of compute and SRAM (2MB)._

  *  _No L2 cache._

  *  _Using baby RISC-V CPU cores for kernel launching, data movement, and scheduling._

    *  _All the flexibility of a CPU (it is literally a CPU with full ISA)._

    *  _No legacy structures to support. (graphics)_

  *  _TT architecture built around DMA from ground up._

    *  _Nvidia Tensor Memory Accelerator is “bolted-on”._

    *  _CUDA software has to support TMA and legacy memory models._




 _With respect to the non-Nvidia competition, Tenstorrent is also better._

  *  _Google TPU has large cores that make utilization problematic._

  *  _Exotic “kernel-less” startups like Groq, Cerebras, and SambaNova place enormous burden on ahead-of-time compilation._

    *  _Cores have kilobytes of memory._

    *  _Schedule stuff at compile time or get severe underutilization._




* * *

I find Davor’s arguments compelling. 

(Reminder that [NVDA 0.00%↑](https://substack.com/discover/stocks/NVDA) is my largest position at an average price of $16/share.)

Architecture design philosophy may be “correct”, but the existing CUDA moat does not care. Nvidia has way more resources and can easily support all the legacy stuff, various hacks, and win even if the architecture is sub-optimal. I know people who work in the Nvidia software performance optimization teams. They are very smart and there are way more of them than Tenstorrent has employees in total.

More on this in section [5].

The other disagreement I have is Davor lumping Groq, Cerebras, and SambaNova into a single category. These three architectures are wildly different.

Groq is 144-wide VLIW and has to compile everything ahead of time in a cycle-accurate manner. It is retarded.

[![\[V\]ery \[L\]ong \[I\]ncoherent \[W\]riteup](https://substackcdn.com/image/fetch/$s_!lVhT!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1335e244-45bb-4add-a677-d9ab1ed74702_875x957.png)

#### [V]ery [L]ong [I]ncoherent [W]riteup

[Irrational Analysis](https://substack.com/profile/135313705-irrational-analysis)·February 24, 2024[Read full story](https://irrationalanalysis.substack.com/p/very-long-incoherent-writeup)](https://irrationalanalysis.substack.com/p/very-long-incoherent-writeup)

I genuinely believe Groq is a fraud. There is no way their private inference cloud has positive gross margins. 

Cerebras is a wafer full of tiny cores. Massive scheduling issues but not in the same way as Groq. If Davor just compared Cerebras with Tenstorrent then I would agree with all his whiteboard arguments.

[![Cerebras \($CBRS.O\) Equity Research Report](https://substackcdn.com/image/fetch/$s_!GZ40!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3f4ca575-d79f-4002-987d-2e9c0cc467b8_780x834.png)

#### Cerebras ($CBRS.O) Equity Research Report

[Irrational Analysis](https://substack.com/profile/135313705-irrational-analysis)·October 14, 2024[Read full story](https://irrationalanalysis.substack.com/p/cerebras-cbrso-equity-research-report)](https://irrationalanalysis.substack.com/p/cerebras-cbrso-equity-research-report)

Looking forward to the Cerebras IPO so I can trade the crap out of this stock. 

[![](https://substackcdn.com/image/fetch/$s_!nxC0!,w_1456,c_limit,f_auto,q_auto:good,fl_lossy/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F56b98ab8-e942-4387-ac32-332b7546db93_520x298.gif)](https://substackcdn.com/image/fetch/$s_!nxC0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F56b98ab8-e942-4387-ac32-332b7546db93_520x298.gif)

SambaNova is a CGRA (very cool super-FPGA) that is in its own category. Compiler is more like FPGA logic synthesis. 

## [4] Tenstorrent Opinion and Valuation Framework

I went into the meeting thinking Tenstorrent is just another Nvidia-roadkill company doomed to death.

Left the meeting genuinely hopeful. 

Every question I had got a good, well-explained, credible answer/counterargument. The only remaining technical concern I have is latency as that is a difficult problem. 

What impressed me is that every single Tenstorrent person I talked to was smart and (more importantly) **reasonable.** It is very common for smart engineers to become delusionally optimistic, blinded by hubris.

This is not Tenstorrent. They are reasonable, realistic, and rational. If any AI hardware startup can break through the Nvidia and semi-custom (Google TPU, Amazin Trainium, Microsoft Maia, Meta <whatever the fuck it’s called>) silicon moats, it’s them.

Tenstorrent is the open-source champion of AI hardware. Everything about their developer strategy is correct. Multiple open software tools. Excellent (A+) community and developer engagement. Easy access to purchasing sample hardware.

Many technical/engineering problems need to be solved but this team can get it done. Very excited to see how next-gen Grendel plays out.

* * *

Now for the valuation question.

[Tenstorrent recently closed a series D venture capital raise at a $2B valuation.](https://tenstorrent.com/en/vision/tenstorrent-closes-693m-of-series-d-funding-led-by-samsung-securities-and-afw-partners)

Earlier this year, I heard chatter that Tenstorrent was pivoting to selling RISC-V IP. This was a sign of weakness and desperation… until ARM decided to engage in moronic behavior.

[![ARM's Chernobyl Moment](https://substackcdn.com/image/fetch/$s_!Rabd!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd6ee1a26-41cf-4029-b3a3-934b355b7b1a_1023x1158.png)

#### ARM's Chernobyl Moment

[Irrational Analysis](https://substack.com/profile/135313705-irrational-analysis)·October 23, 2024[Read full story](https://irrationalanalysis.substack.com/p/arms-chernobyl-moment)](https://irrationalanalysis.substack.com/p/arms-chernobyl-moment)

Let’s take a look at the ARM stock chart.

[![](https://substackcdn.com/image/fetch/$s_!zfgp!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff486a6a6-dc47-4bcc-a670-4cc06841e4f5_767x651.png)](https://substackcdn.com/image/fetch/$s_!zfgp!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff486a6a6-dc47-4bcc-a670-4cc06841e4f5_767x651.png)

Many (basically all) of my finance-land friends think the [ARM 0.00%↑](https://substack.com/discover/stocks/ARM) valuation is nuts. Yes, there is low float and a crazy multiple but… it’s been trading for quite a while. 

Given that ARM is aggressively raising license prices and royalty rates and has (metaphorically) nuked Qualcomm, RISC-V CPU IP clearly has a bright future.

I think it is reasonable to say Tenstorrent is worth 1% of ARM’s market cap ($1.6B) just from the IP business. 

**There are no other high-performance RISC-V IP providers.** All other options are for low-end stuff. Tenstorrent has Jim Keller (CPU design living legend) and many other great CPU micro architects. 

The only other competition (SiFive) decided to commit seppuku. Fired the entire high-performance team.

[![](https://substackcdn.com/image/fetch/$s_!RI28!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F25c40f1a-ff04-44b3-aac4-b4e80088bf20_800x564.png)](https://substackcdn.com/image/fetch/$s_!RI28!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F25c40f1a-ff04-44b3-aac4-b4e80088bf20_800x564.png)

Tenstorrent could completely fail at AI and the company is still worth at least 1% of ARM.O market cap!

* * *

The other valuation method I have is against Cerebras who is attempting to IPO and unload equity on un-informed retail investors.

First, let’s compare the CEOs.

[![](https://substackcdn.com/image/fetch/$s_!KaBR!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb374e545-5e37-4b64-9f01-bdca9c8dfb42_690x957.png)](https://substackcdn.com/image/fetch/$s_!KaBR!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb374e545-5e37-4b64-9f01-bdca9c8dfb42_690x957.png)

Now let’s compare the companies themselves.

[![](https://substackcdn.com/image/fetch/$s_!ecGb!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F530338ce-5fc8-40b1-896c-7cbd50fa99b8_764x955.png)](https://substackcdn.com/image/fetch/$s_!ecGb!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F530338ce-5fc8-40b1-896c-7cbd50fa99b8_764x955.png)

[![](https://substackcdn.com/image/fetch/$s_!ouMS!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1b487fed-5abb-4fc8-9e98-8ac284d5cf5a_507x540.png)](https://substackcdn.com/image/fetch/$s_!ouMS!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1b487fed-5abb-4fc8-9e98-8ac284d5cf5a_507x540.png)

I think Tenstorrent should be worth more than Cerebras. Either Tenstorrent is comically undervalued or Cerebras is comically overvalued. 

## [5] Broader AI Hardware Startup Framework

AI Hardware startups have a problem. A customer problem.

Who is going to buy horizontally supplied AI chips from a startup?

There are many options:

  1. Nvidia

    1. Buy latest generation.

    2. Rent latest generation from Azure, AWS, or GCP

    3. Rent old generation GPUs at comically cheap prices from a neocloud that is about to go bankrupt.

  2. AMD (they keep lowering prices)

  3.  **Build your own semi-custom chip.**

    1. Amazon Trainium, Google TPU, Microsoft Maia, Meta ???

    2. Use Broadcom, Marvell, Alchip, MediaTek, or GUC as a design partner.

  4. Rent semi-custom chips (TPU, Trainium) from GCP or AWS.




 **Who are all these AI hardware startups going to sell to?**

Mega-corps are making their own chips in partnership with five design companies for semi-custom solutions.

AMD makes a meh product, but it is cheap and has lots of HBM.

Smaller companies can easily rent old Nvidia gear from a wide variety of shitcos (sorry “Neoclouds”) at rock bottom prices. **H100 hourly rental prices have already collapsed, and Blackwell has not even ramped yet!**

* * *

Horizontally supplied training hardware is a dead market. Nvidia and the semi-custom hyperscaler chips crowd everyone else out.

Bluntly, I believe every AI hardware startup should give up on training and exclusively focus on inference. There is no hope. Pivot now, maybe live. Keep working on training, definitely die.

As for inference, there is hope but only if cost is insanely low **or** the performance is insanely high from some exotic strategy. If your chip uses HBM and is built on TSMC N3, it probably won’t be cheap enough to compete with all those depreciated H100s and heavily subsidized Trainiums. 

Tenstorrent is using Samsung Foundry SF4X, a dirt-cheap process node. Samsung Ventures have also invested in them, so I assume they got a good deal on tape-out. Finally, Tenstorrent is not using HBM. If demand materializes for Tenstorrent hardware, they can achieve healthy 60% gross margins while deeply undercutting the competition on price.

If Tenstorrent executes on their next generation and spend another 18-36 months on improving the software stack, they have a credible chance of meaningful sales into the rapidly growing inference market. **I believe Tenstorrent is the only investment-grade AI hardware startup.**

With that said, there are two AI hardware startups that I would like to positively mention.

 **SambaNova** has a crazy CGRA architecture that is really cool. It’s so crazy it might work.

 **Positron** has a galaxy brain founder+CEO.

[![](https://substackcdn.com/image/fetch/$s_!Eg19!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcb917e46-67c3-48fa-9416-65f21b2cfa16_2105x1092.png)](https://substackcdn.com/image/fetch/$s_!Eg19!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcb917e46-67c3-48fa-9416-65f21b2cfa16_2105x1092.png)

[![](https://substackcdn.com/image/fetch/$s_!UJwF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8af129b9-3c08-4f27-8ec0-f3d8db3f6a71_2102x1172.png)](https://substackcdn.com/image/fetch/$s_!UJwF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8af129b9-3c08-4f27-8ec0-f3d8db3f6a71_2102x1172.png)

[![](https://substackcdn.com/image/fetch/$s_!vCOV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe820b6ca-e712-402e-9797-4689a6fae670_2089x1089.png)](https://substackcdn.com/image/fetch/$s_!vCOV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe820b6ca-e712-402e-9797-4689a6fae670_2089x1089.png)

[![](https://substackcdn.com/image/fetch/$s_!WmrH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1ce1a9f2-c328-4578-9d71-967a2a74a9b6_2082x1109.png)](https://substackcdn.com/image/fetch/$s_!WmrH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1ce1a9f2-c328-4578-9d71-967a2a74a9b6_2082x1109.png)

[![](https://substackcdn.com/image/fetch/$s_!KiGq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fed1b16b9-d0e2-426b-a9c4-a1ad7e3731d4_2095x1101.png)](https://substackcdn.com/image/fetch/$s_!KiGq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fed1b16b9-d0e2-426b-a9c4-a1ad7e3731d4_2095x1101.png)

 **I cannot recommend enough for you to watch the incredible 15-minute AI and economics presentation by Positron AI CEO Thomas Sohmers.**

There are lots of smart engineers out there. It is very rare for someone to be a top 0.1% engineer **AND** smart in other topics such as economics, history, game theory, and philosophy. 

**The investment case for Positron AI is a galaxy brain Founder in Founder mode.**

(I hold no economic interest in any private company. Only invest in public markets)

If you enjoyed this content, please consider subscribing.

Subscribe

Already subscribed? Thanks! Please consider sharing.

[Share](https://irrationalanalysis.substack.com/p/tenstorrent-and-the-state-of-ai-hardware?utm_source=substack&utm_medium=email&utm_content=share&action=share)
