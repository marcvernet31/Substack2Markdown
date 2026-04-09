# Hot Chips 2025: Irrational Recap

## Spicy conference.

**Sep 13, 2025**

**Likes:** 0

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Please check the [‘about’ page](https://irrationalanalysis.substack.com/about) for a list of active positions.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice and readers should **always do their own research before investing in any security.**

  * Feel free to contact me via email at: _irrational_analysis@proton.me_




* * *

Welcome to the second annual Hot Chips Irrational Recap.

[![Hot Chips 2024: Irrational Recap](https://substackcdn.com/image/fetch/$s_!HPuv!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe1c7faec-bb00-4052-a4e4-0be3f604b0d1_1024x1024.jpeg)

#### Hot Chips 2024: Irrational Recap

[Irrational Analysis](https://substack.com/profile/135313705-irrational-analysis)·September 2, 2024[Read full story](https://irrationalanalysis.substack.com/p/hot-chips-2024-irrational-recap)](https://irrationalanalysis.substack.com/p/hot-chips-2024-irrational-recap)

This year, there was a lot of spicy drama.

Jar Jar Binks of semiconductor analysis (MESSA) is here to provide differentiated, entertaining, and somewhat retarded coverage.

[![](https://substackcdn.com/image/fetch/$s_!zsSt!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7a40d49d-569a-4ed7-895a-f763cc3050d1_886x515.png)](https://substackcdn.com/image/fetch/$s_!zsSt!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7a40d49d-569a-4ed7-895a-f763cc3050d1_886x515.png)

Messa only cover presentations that were interesting and on topics Messa can write about.

This means zero coverage of the kernel programming section. Messa stupid and can barely script slow shit code in Python and MATLAB. Tri Dao flash attention 4 interesting but Messa understand nothing. Youssa go elsewhere for that kind of coverage.

[![](https://substackcdn.com/image/fetch/$s_!sxmK!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0486e1ff-3b18-4f0c-9231-bba1f855ec50_1015x394.png)](https://substackcdn.com/image/fetch/$s_!sxmK!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0486e1ff-3b18-4f0c-9231-bba1f855ec50_1015x394.png)

Grouping presentations by section instead of quality like last year because there is a lot of “cross-pollination” of concepts. 

Also sections re-ordered such that topics that interest me are first.

* * *

Due to certain events and perceived conflicts of interest, I have decided to withhold some material.

The original draft still exists. 

[![](https://substackcdn.com/image/fetch/$s_!6mvu!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4d2226de-d4c9-4068-9d8e-f0ca7c05eab3_1116x483.png)](https://substackcdn.com/image/fetch/$s_!6mvu!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4d2226de-d4c9-4068-9d8e-f0ca7c05eab3_1116x483.png)

* * *

# Contents:

  1. <redacted>

  2. Networking

    1. Intel Smart NIC

    2. AMD Smart NIC

    3. Nvidia Fast Smart-ish NIC

    4. Broadcom Switch: Why the fuck does UALink exist?

  3. Machine Learning

    1. Marvell Memory

    2. d-Matrix 

    3. Huawei

    4. Google TPU 6p/7 aka Ironwood

  4. Rack-Scale Roundup

  5. Miscellaneous 

    1. Intel Clearwater Forrest

    2. Strange RISC-V CPUs

    3. Fully Homeomorphic Encryption RISC-V Accelerator

    4. IBM Power 11

    5. Weird 3D Printed Heatsinks

  6. Useless Keynotes




* * *

## [2] Networking

Last year, Eric Quinell won the entire conference with his hilarious and highly informative talk on Tesla Transport Protocol for Dojo.

Dojo is now dead so very sad.

### [2.a] Intel Smart-NIC

[![](https://substackcdn.com/image/fetch/$s_!Mfln!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb6ac1079-f8b0-4597-ac6e-1ab4acdbc77e_957x525.png)](https://substackcdn.com/image/fetch/$s_!Mfln!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb6ac1079-f8b0-4597-ac6e-1ab4acdbc77e_957x525.png)

[![](https://substackcdn.com/image/fetch/$s_!QRa3!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F98464597-4f50-4c1f-ac73-d6456b09f725_949x525.png)](https://substackcdn.com/image/fetch/$s_!QRa3!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F98464597-4f50-4c1f-ac73-d6456b09f725_949x525.png)

I guess x86 is so irrelevant now that all the infrastructure apps support ARM better.

[![](https://substackcdn.com/image/fetch/$s_!40AJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F10cc1ac0-3773-47b9-babc-6cb99d78a4db_1762x983.png)](https://substackcdn.com/image/fetch/$s_!40AJ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F10cc1ac0-3773-47b9-babc-6cb99d78a4db_1762x983.png)

Ah yes, you have an RDMA engine but shared ZERO performance data. Nice.

### [2.b] AMD Smart-NIC

AMD bought Pensando in 2022 for $1.9B and have proceeded to mis-manage it into oblivion. This Pollara NIC is two years behind Nvidia ConntctX, has shit performance, apparently is a semi-custom Broadcom project and thus has shit margins, and nobody wants to use it other than shitco Neoclouds getting fucking debt forgiveness in exchange. LOL

(also Oracle)

[![](https://substackcdn.com/image/fetch/$s_!3rCk!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faca82a9b-521b-4d49-85d3-9de787828ac8_1749x939.png)](https://substackcdn.com/image/fetch/$s_!3rCk!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faca82a9b-521b-4d49-85d3-9de787828ac8_1749x939.png)

Guys you cant just remove the Y-axis completely. I cannot take you jokers seriously when you show bullshit like this.

40% gain can still be shit if the baseline is tiny. 

### [2.c] Nvidia Smart-ish NIC

The real Nvidia smart NIC is called Bluefield and nobody wants to buy it.

Instead, we have ConnectX.

I find it IMMENSLY amusing Nvidia presented this right after AMD. At least three AMD people asked questions and were basically in shock.

[![](https://substackcdn.com/image/fetch/$s_!tZPO!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe31f5f01-e652-4cf4-9c2f-b1b93dd803a0_596x99.png)](https://substackcdn.com/image/fetch/$s_!tZPO!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe31f5f01-e652-4cf4-9c2f-b1b93dd803a0_596x99.png)

The look on their faces was “oh fuck we suck… their numbers are real?”.

AMD Employee: <asks about test setup>

Nvidia Presenter: <confidently explains test setup>

AMD Employee:

[![](https://substackcdn.com/image/fetch/$s_!P5a-!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F98e4145b-f167-4156-ab0d-ed8d641cf17a_300x290.jpeg)](https://substackcdn.com/image/fetch/$s_!P5a-!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F98e4145b-f167-4156-ab0d-ed8d641cf17a_300x290.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!bTpt!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F37b1e674-2041-494d-982d-70f62f799ea7_1863x1045.png)](https://substackcdn.com/image/fetch/$s_!bTpt!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F37b1e674-2041-494d-982d-70f62f799ea7_1863x1045.png)

Once again I am reminded of losing money trying to short Astera Labs, the cockroach of semiconductors.

[![](https://substackcdn.com/image/fetch/$s_!uBQy!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F121e3036-a0d3-4114-94a4-0282f19b43ee_1701x884.png)](https://substackcdn.com/image/fetch/$s_!uBQy!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F121e3036-a0d3-4114-94a4-0282f19b43ee_1701x884.png)

[![](https://substackcdn.com/image/fetch/$s_!JzPE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F85e2e0c3-47b7-4e54-bf5c-4330ad5eb431_1887x838.png)](https://substackcdn.com/image/fetch/$s_!JzPE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F85e2e0c3-47b7-4e54-bf5c-4330ad5eb431_1887x838.png)

[![](https://substackcdn.com/image/fetch/$s_!JYR0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbbc732ff-c660-4e42-b772-277ee026713d_1747x727.png)](https://substackcdn.com/image/fetch/$s_!JYR0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbbc732ff-c660-4e42-b772-277ee026713d_1747x727.png)

Hey AMD jokers, this is what real performance looks like.

### [2.d] Broadcom Switch: Why the fuck does UALink exist?

UALink people like to think that Ethernet has 400 ns of latency and thus they have an intrinsic advantage at around 200 ns.

Broadcom showed off excellent performance data for their Tomahawk 5 Ultra. It is very reasonable that the next spin of the Tomahawk 6 will have this digital logic ported over. So H2 2026 Broadcom will deliver 200G per lane SerDes and all the nice low-latency and collectives features in UEC and SUE while UALink losers struggle to ship anything.

[![](https://substackcdn.com/image/fetch/$s_!QRcn!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F44fd2a9f-58fe-472f-834a-1ed28a52a538_1682x844.png)](https://substackcdn.com/image/fetch/$s_!QRcn!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F44fd2a9f-58fe-472f-834a-1ed28a52a538_1682x844.png)

[![](https://substackcdn.com/image/fetch/$s_!U8OT!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8f9cd368-67ce-4c0d-8abc-5df5a763c658_1701x849.png)](https://substackcdn.com/image/fetch/$s_!U8OT!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8f9cd368-67ce-4c0d-8abc-5df5a763c658_1701x849.png)

Reduced header support for lower latency.

[![](https://substackcdn.com/image/fetch/$s_!v6HZ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4c2b3754-f4ea-4f2c-b046-397c3b6311ab_1738x858.png)](https://substackcdn.com/image/fetch/$s_!v6HZ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4c2b3754-f4ea-4f2c-b046-397c3b6311ab_1738x858.png)

Broadcom already supports collectives in a high-volume shipping product while the UALink losers continue to debate what to include in their worthless joke of a standard.

[![](https://substackcdn.com/image/fetch/$s_!v9uZ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc148d1cd-e08e-456c-bb47-e89e4673fa1e_1723x843.png)](https://substackcdn.com/image/fetch/$s_!v9uZ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc148d1cd-e08e-456c-bb47-e89e4673fa1e_1723x843.png)

Latency is great. What argument does UALink have left?

The 200G SerDes of future (2027 lol) UALink switches will likely need AEC or on-PCB retimers. That immediately causes the latency of a UALink system to be worse than a SUE/UEC Broadcom system.

## [3] Machine Learning

### [3.a] Marvell Memory

I was going to try and be nice to Marvell for once but their hilarious earnings implosion and legendary earnings call make this very difficult.

[![](https://substackcdn.com/image/fetch/$s_!sTL9!,w_1456,c_limit,f_auto,q_auto:good,fl_lossy/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe9b5b6a8-b089-4330-8343-8dc60a7885c9_497x280.gif)](https://substackcdn.com/image/fetch/$s_!sTL9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe9b5b6a8-b089-4330-8343-8dc60a7885c9_497x280.gif)

[![](https://substackcdn.com/image/fetch/$s_!QmIQ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F34785e53-571e-4ca5-b88b-1a478fda7660_604x1295.webp)](https://substackcdn.com/image/fetch/$s_!QmIQ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F34785e53-571e-4ca5-b88b-1a478fda7660_604x1295.webp)

On a whim, I threw out a sell short order for 1K shares at $72 limit and it was surprisingly filled. Made more than a months rent in under two hours, closed the short, and was happy.

Missed out on an extra two months of free rent LMAO.

* * *

This earnings call is without a doubt the worst one I have ever listened to. The entertainment value is incredible. Do yourself a favor and listen to the audio itself. Transcript does not do it justice.

<https://event.choruscall.com/mediaframe/webcast.html?webcastid=Kd2z6aT9>

Let’s start with the Hot Chips presentation, literally days before this earnings call.

[![](https://substackcdn.com/image/fetch/$s_!jGIN!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F80ddc11c-1183-4c96-87f4-284934aa7fbc_1714x959.png)](https://substackcdn.com/image/fetch/$s_!jGIN!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F80ddc11c-1183-4c96-87f4-284934aa7fbc_1714x959.png)

500 mV SRAM! Super impressive.

[![](https://substackcdn.com/image/fetch/$s_!7fx0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F01ef8891-8d98-4b66-a3fe-ff0323832671_1685x943.png)](https://substackcdn.com/image/fetch/$s_!7fx0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F01ef8891-8d98-4b66-a3fe-ff0323832671_1685x943.png)

Shame for pulling an AMD and not including a properly labeled y-axis.

Also, why are you showing performance at -40C? You should show at 90/110/125C for more realistic operation.

[![](https://substackcdn.com/image/fetch/$s_!ruhD!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff4468af9-2133-415f-b625-5f2365d45fa1_1678x952.png)](https://substackcdn.com/image/fetch/$s_!ruhD!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff4468af9-2133-415f-b625-5f2365d45fa1_1678x952.png)

[![](https://substackcdn.com/image/fetch/$s_!YcEj!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3233c367-8efe-4961-9e40-a1823b8fe464_1706x943.png)](https://substackcdn.com/image/fetch/$s_!YcEj!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3233c367-8efe-4961-9e40-a1823b8fe464_1706x943.png)

[![](https://substackcdn.com/image/fetch/$s_!zRVh!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F60c7d7b4-845a-43b2-b5a5-2b74ca1c8a21_1736x947.png)](https://substackcdn.com/image/fetch/$s_!zRVh!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F60c7d7b4-845a-43b2-b5a5-2b74ca1c8a21_1736x947.png)

[![](https://substackcdn.com/image/fetch/$s_!i7uz!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F755603bb-a16e-4a43-8c85-c72719ae6a7e_1778x952.png)](https://substackcdn.com/image/fetch/$s_!i7uz!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F755603bb-a16e-4a43-8c85-c72719ae6a7e_1778x952.png)

This is exceptional data! Great job.

All PVT corners across a reasonably large sample size.

Interesting that the fast -40C condition seems to be the worst.

[![](https://substackcdn.com/image/fetch/$s_!rjbF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fac4bd3ec-fce2-4d77-867f-f252f5af0751_1729x963.png)](https://substackcdn.com/image/fetch/$s_!rjbF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fac4bd3ec-fce2-4d77-867f-f252f5af0751_1729x963.png)

Excellent results. Notice how there is some variation in the bathtub curve across lanes. 

**This Marvell D2D IP puts Synopsys, Cadence and Alphawave UCIe teams to shame.** Congratulations to everyone who worked on this. 

* * *

Allright earnings call time.

Half of the hedge funds already knew Marvell had lost Trainum 3 to Alchip. The other half found out when they saw Marvell’s guidance.

[![](https://substackcdn.com/image/fetch/$s_!oe3g!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6985e98f-f0fe-45c3-aef5-8705fee51f11_220x192.gif)](https://substackcdn.com/image/fetch/$s_!oe3g!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6985e98f-f0fe-45c3-aef5-8705fee51f11_220x192.gif)

[![](https://substackcdn.com/image/fetch/$s_!U3Ua!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6f712685-d5f5-4500-a5d8-fc330bd3fcab_610x225.png)](https://substackcdn.com/image/fetch/$s_!U3Ua!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6f712685-d5f5-4500-a5d8-fc330bd3fcab_610x225.png)

They are consolidating all their half-dead businesses into one segment to obfuscate. Reducing information provided to investors is always a bad thing. I called out AMD when they deleted gaming as a reportable segment and lumped into consumer to obfuscate the ass-whooping from Nvidia/Geforce. What Marvell is doing now is same thing. Hiding bad information.

[![](https://substackcdn.com/image/fetch/$s_!NFPk!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8c04be90-a33e-4f9f-8046-78a1ecb9bc38_572x205.png)](https://substackcdn.com/image/fetch/$s_!NFPk!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8c04be90-a33e-4f9f-8046-78a1ecb9bc38_572x205.png)

Translation: Did you lose Trainum 3?

[![](https://substackcdn.com/image/fetch/$s_!lDQN!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4e4d5f56-646f-40cf-a85a-51a0abf53d4d_605x771.png)](https://substackcdn.com/image/fetch/$s_!lDQN!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4e4d5f56-646f-40cf-a85a-51a0abf53d4d_605x771.png)

Once again they are asked about Trainium 3 and chose to pivot to XPU attach.

[![](https://substackcdn.com/image/fetch/$s_!RJuH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F43ffab60-2ffe-441f-acf6-7028caf1fc56_617x846.png)](https://substackcdn.com/image/fetch/$s_!RJuH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F43ffab60-2ffe-441f-acf6-7028caf1fc56_617x846.png)

[![](https://substackcdn.com/image/fetch/$s_!nIjK!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9dadb404-32cd-48a7-8a9a-6623f4e211d0_940x940.jpeg)](https://substackcdn.com/image/fetch/$s_!nIjK!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9dadb404-32cd-48a7-8a9a-6623f4e211d0_940x940.jpeg)Visual approximation of Alchip employees working on Trainium 3 and 4 in an episodic manner.

[![](https://substackcdn.com/image/fetch/$s_!5Xbu!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbe013bdf-8e7c-4262-9908-f00455d7dd1b_609x776.png)](https://substackcdn.com/image/fetch/$s_!5Xbu!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbe013bdf-8e7c-4262-9908-f00455d7dd1b_609x776.png)

Marvell management appears to not understand that Nvidia Spectrum-XGS competes with Broadcom Jericho. Marvell does not have a product in this category. They are struggling to ship basic Ethernet switches. Forget about the fancy buffered routers that have tons of high-end software features.

[![](https://substackcdn.com/image/fetch/$s_!lZKN!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5b08b37b-46ab-4527-b69c-c80e467a5d66_612x937.png)](https://substackcdn.com/image/fetch/$s_!lZKN!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5b08b37b-46ab-4527-b69c-c80e467a5d66_612x937.png)

Vivek Arya is trying to pin down Marvell and force them to admit they lost Trainium 3.

Matt Murphy chooses to pivot into the half dead carrier and enterprise networking business “recovery”.

Bro if those businesses are doing well why you lumping them all into a single reportable segment?

[![](https://substackcdn.com/image/fetch/$s_!S6AY!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F62d87652-c989-49b5-b4e3-9fa9612146ac_610x788.png)](https://substackcdn.com/image/fetch/$s_!S6AY!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F62d87652-c989-49b5-b4e3-9fa9612146ac_610x788.png)

SORRY I HAVE TO ASK AGAIN. DID YOU LOSE TRAINIUM 3 OR IS THERE A SMALL PAUSE BETWEEN TRAINIUM 2.5 AND 3?

[![](https://substackcdn.com/image/fetch/$s_!x8Z8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff9eb5d41-6ace-40a7-8928-b2f32c05003e_613x1093.png)](https://substackcdn.com/image/fetch/$s_!x8Z8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff9eb5d41-6ace-40a7-8928-b2f32c05003e_613x1093.png)

Timothy Arcuri is trying to be clever here. Optics and AI semi-custom are both categorized as AI so he tried to ask about optics revenue growth and the optics baseline to force Marvell to give away info on AI semi-custom.

After some initial bullshit from Matt Murphy, Timmy Arcuri tried to push back and force a real answer.

Instead he got “I don’t have the spreadsheet in front of me”… 🤡

[![](https://substackcdn.com/image/fetch/$s_!diz9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbb4e71da-ae73-42ac-bd27-ad3e9a31bd4c_609x1137.png)](https://substackcdn.com/image/fetch/$s_!diz9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbb4e71da-ae73-42ac-bd27-ad3e9a31bd4c_609x1137.png)

Harsh Kumar attempts to get useful information about the mythical XPU attach revenue that is coming any day now.

He does not get a straight answer.

The tone in which he asked his question is telling.

Also… yea there is a lot of controversy. Alchip says they won your most important socket and you are too spinless to admit this. You knew the guidance was going to finally confirm this. Why are you still trying to hide this development? Stock is down 18% in one day because everybody knows! **YOU CANNOT HIDE THE IMPLICATIONS OF THE GUIDANCE NUMBERS.**

[![](https://substackcdn.com/image/fetch/$s_!qtSd!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F48939c0e-4dd4-48d9-a115-8f882d361ecb_616x741.png)](https://substackcdn.com/image/fetch/$s_!qtSd!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F48939c0e-4dd4-48d9-a115-8f882d361ecb_616x741.png)

Harlan is pissed. LOL

[![](https://substackcdn.com/image/fetch/$s_!lHWo!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd58043c0-0849-46b9-ab25-c67a982005b4_607x884.png)](https://substackcdn.com/image/fetch/$s_!lHWo!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd58043c0-0849-46b9-ab25-c67a982005b4_607x884.png)

Trainium 4 is being dual tracked by Amazon.

One version uses NVLink Fusion, the other version is UALink.

Astera Labs will make the UALink switch if Amazon choses that option. Nvidia (lol) makes Trainium 4 scale-up switch otherwise. **Marvell will not get this “XPU attach” scale-up switch socket.**

Bridge with Amazon appears to be burnt to a crisp.

[![](https://substackcdn.com/image/fetch/$s_!jmXP!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6ad4bee8-e050-411f-909d-cfa8e4748b69_581x1195.png)](https://substackcdn.com/image/fetch/$s_!jmXP!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6ad4bee8-e050-411f-909d-cfa8e4748b69_581x1195.png)

Alchip is making the main die for both Trainium 4 tracks.

[![](https://substackcdn.com/image/fetch/$s_!vUQr!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F933d1656-8f0b-4ccd-8470-79b5afdc3690_564x558.png)](https://substackcdn.com/image/fetch/$s_!vUQr!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F933d1656-8f0b-4ccd-8470-79b5afdc3690_564x558.png)

[![](https://substackcdn.com/image/fetch/$s_!nT-k!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F02bd7bec-d8c2-41dd-a808-97a9fe5f1216_582x439.png)](https://substackcdn.com/image/fetch/$s_!nT-k!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F02bd7bec-d8c2-41dd-a808-97a9fe5f1216_582x439.png)

Also, I know the two “emerging hyperscaler wins” Marvell claims. 

* * *

[![](https://substackcdn.com/image/fetch/$s_!i3JW!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd5945b84-3a13-4847-a50d-489f97900855_581x863.png)](https://substackcdn.com/image/fetch/$s_!i3JW!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd5945b84-3a13-4847-a50d-489f97900855_581x863.png)

I genuinely do not understand why Matt Murphy is still trying to obfuscate. Just say you lost Trn3 socket and pivot to Microsoft/Maia. 

[![](https://substackcdn.com/image/fetch/$s_!wVL7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Feb519b64-19ab-413a-9de2-e02c36eb4cc4_220x220.gif)](https://substackcdn.com/image/fetch/$s_!wVL7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Feb519b64-19ab-413a-9de2-e02c36eb4cc4_220x220.gif)

Marvell has some pockets of great engineering. Their 64G D2D PHY and dense SRAM are excellent. Marvell SerDes was good but has slipped meaningfully over the last 2 years. 

It’s honestly quite sad what is happening. Maybe an activist investor needs to jump in. I hear of rather extreme levels of attrition within Marvell engineering.

In the meantime, super fun trading instrument. Really enjoying day-trade shorting Marvell. It’s a shame Marvell employees legally cannot short their own stock and use the proceeds to buy Broadcom stock instead.

[![](https://substackcdn.com/image/fetch/$s_!9S60!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd04c77f9-a739-48fe-bcfa-54935e722988_626x1138.png)](https://substackcdn.com/image/fetch/$s_!9S60!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd04c77f9-a739-48fe-bcfa-54935e722988_626x1138.png)

[![](https://substackcdn.com/image/fetch/$s_!TPPY!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbf7a360e-380e-4f04-870a-8038b687214b_597x356.png)](https://substackcdn.com/image/fetch/$s_!TPPY!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbf7a360e-380e-4f04-870a-8038b687214b_597x356.png)

Is it legally possible for Marvell’s board to change the buyback authorization to buy [AVGO 0.00%↑](https://substack.com/discover/stocks/AVGO) shares instead of buying back [MRVL 0.00%↑](https://substack.com/discover/stocks/MRVL) shares? 

We have random companies becoming Bitcoin and Ethereum treasuries. **Why can’t Marvell become a Broadcom stock treasury?**

 _(can one of the hedge fund readers submit this proposal to the Marvell annual meeting vote lmao)_

### [3.b] d-Matrix

While listening to the d-Matrix presentation, two thoughts came to mind.

First, how is d-Matrix going to compete with upcoming HBM4 base die architectures?

<https://semianalysis.com/2025/08/12/scaling-the-memory-wall-the-rise-and-roadmap-of-hbm/>

Second, this looks like an SRAM machine (Cerebras, Groq). SRAM is possibly the worst scaling vector in semiconductors right now.

[![](https://substackcdn.com/image/fetch/$s_!9LFV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F80e662d4-28e1-4b83-8698-ae2af52a04a0_1837x1080.webp)](https://substackcdn.com/image/fetch/$s_!9LFV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F80e662d4-28e1-4b83-8698-ae2af52a04a0_1837x1080.webp)Old AMD slide from the Milan-X launch. Talking about why 3DVCACHE (hybrid bonded stacked SRAM) is good.

Let’s start with the microarchitecture.

[![](https://substackcdn.com/image/fetch/$s_!qNOo!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd0f908d4-9809-4232-8648-24f565df3d9f_1772x984.png)](https://substackcdn.com/image/fetch/$s_!qNOo!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd0f908d4-9809-4232-8648-24f565df3d9f_1772x984.png)

[![](https://substackcdn.com/image/fetch/$s_!ggDx!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd563d1bb-cc35-4984-9c6d-e93655f77989_1756x958.png)](https://substackcdn.com/image/fetch/$s_!ggDx!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd563d1bb-cc35-4984-9c6d-e93655f77989_1756x958.png)

Mentally, I consider “in memory compute” to mean “math inside a DRAM bank.

This is more like “in SRAM compute”. Effectively d-Matrix has designed custom SRAM cells that have compute woven inside. Ultra tight integration of compute and SRAM is more descriptive to what d-Matrix has done.

[![](https://substackcdn.com/image/fetch/$s_!AWye!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc4aa0a36-260b-4c2e-85d9-1f8914a127ba_1708x947.png)](https://substackcdn.com/image/fetch/$s_!AWye!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc4aa0a36-260b-4c2e-85d9-1f8914a127ba_1708x947.png)

VLIW == compiler is more complex

[![\[V\]ery \[L\]ong \[I\]ncoherent \[W\]riteup](https://substackcdn.com/image/fetch/$s_!lVhT!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1335e244-45bb-4add-a677-d9ab1ed74702_875x957.png)

#### [V]ery [L]ong [I]ncoherent [W]riteup

[Irrational Analysis](https://substack.com/profile/135313705-irrational-analysis)·February 24, 2024[Read full story](https://irrationalanalysis.substack.com/p/very-long-incoherent-writeup)](https://irrationalanalysis.substack.com/p/very-long-incoherent-writeup)

At least it is only 4-wide. 

[![](https://substackcdn.com/image/fetch/$s_!hIMF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb4eb9955-5cb9-418b-adae-0e79a507e39c_1699x951.png)](https://substackcdn.com/image/fetch/$s_!hIMF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb4eb9955-5cb9-418b-adae-0e79a507e39c_1699x951.png)

What d-Matrix refers to is how the MX standardized numerical formats alongside block FP enable near regular FP accuracy.

Pushed back on this and Sudeep shared a d-Matrix paper and a Microsoft Neurips paper to back up this claim.

<https://proceedings.neurips.cc/paper/2020/file/747e32ab0fea7fbd2ad9ec03daa3f840-Paper.pdf>

<https://arxiv.org/pdf/2210.05470>

[![](https://substackcdn.com/image/fetch/$s_!KMk3!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6761fee1-2170-4f26-b11c-a1e211451156_712x464.png)](https://substackcdn.com/image/fetch/$s_!KMk3!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6761fee1-2170-4f26-b11c-a1e211451156_712x464.png)

>  _“The Microsoft paper published at Neurips is also good independent validation of block floating point numerical accuracy._
> 
>  _MSFP12 is our [d-Matrix] 4 bit format. MSFP16 is our [d-Matrix] 8 bit format.”_
> 
> — Sudeep Bhoja, d-Matrix CTO and Co-Founder

* * *

So let’s talk about the roadmap because d-Matrix needs to compete with custom base die HBM4. 

The core argument d-Matrix was pushing is their in-development stacked/3D DRAM massively wins 

d-Matrix Claims:

  1. Their 3D DRAM will be 60% cheaper than HBM4 once the supply chain is ready.

  2. Their 3D DRAM uses 90% less energy for IO transport compared to HBM4.




Claim #1 is believable without much need for thinking. HBM yield is severely harmed by the compounding effect of stacking 12-16 layers. d-Matrix 3D DRAM roadmap only goes up to 4 layers because they are prioritizing energy efficiency and bandwidth over capacity.

[![](https://substackcdn.com/image/fetch/$s_!BAwX!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff613ce19-65a8-410e-a880-de90847e0ebf_600x480.jpeg)](https://substackcdn.com/image/fetch/$s_!BAwX!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff613ce19-65a8-410e-a880-de90847e0ebf_600x480.jpeg)HBM structure.

[![](https://substackcdn.com/image/fetch/$s_!6BEG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa2544901-7352-4db4-b6cc-0e30ef0e545d_1780x957.png)](https://substackcdn.com/image/fetch/$s_!6BEG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa2544901-7352-4db4-b6cc-0e30ef0e545d_1780x957.png)

Moving on to claim #2…

Sudeep showed me an old Nvidia ISSCC paper that directionally is similar to what d-Matrix is trying to do.

[![](https://substackcdn.com/image/fetch/$s_!ue2f!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8498496d-f3d6-46e5-9300-03428a26af06_1154x944.webp)](https://substackcdn.com/image/fetch/$s_!ue2f!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8498496d-f3d6-46e5-9300-03428a26af06_1154x944.webp)

Let’s compare the energy efficiency of HBM4 vs d-Matrix stacked DRAM.

[![](https://substackcdn.com/image/fetch/$s_!oIQ5!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc78c6716-5cb3-4a83-ad71-a3f34525f042_702x912.png)](https://substackcdn.com/image/fetch/$s_!oIQ5!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc78c6716-5cb3-4a83-ad71-a3f34525f042_702x912.png)

Traditional HBM4 will have 2.5 to 4 pJ/bit system-level efficiency. Cross-checked the numbers they gave me and it seems reasonable. 

[![](https://substackcdn.com/image/fetch/$s_!FH0f!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F579607c8-bf32-4d63-884d-3c18d6c64a56_384x632.png)](https://substackcdn.com/image/fetch/$s_!FH0f!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F579607c8-bf32-4d63-884d-3c18d6c64a56_384x632.png)

[![](https://substackcdn.com/image/fetch/$s_!DS7U!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F69ded80e-09af-4626-95aa-5024ad81cbae_1754x970.png)](https://substackcdn.com/image/fetch/$s_!DS7U!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F69ded80e-09af-4626-95aa-5024ad81cbae_1754x970.png)

So the energy efficiency claims in the Hot Chips slides are reasonable given how physically short the datapath is.

One rather obvious issue is the locality of memory. In a traditional HBM-style system, all compute cores can access all DRAM banks.

d-Matrix 3D DRAM cannot do this. Each DMIC core can only access the DRAM banks directly above it. This is a tradeoff between **compiler complexity** (compiler needs to schedule data movement) and **energy efficiency.**

* * *

Another question is how the supply-chain will adapt to d-Matrix needs. They need customization to the DRAM (LPDDR) die itself. d-Matrix refused to tell me which memory manufacturer is helping them but a quick look at their website suggests…

[![](https://substackcdn.com/image/fetch/$s_!oXE7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F14142382-235d-4c12-8ee9-00ed4052b70e_1308x296.png)](https://substackcdn.com/image/fetch/$s_!oXE7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F14142382-235d-4c12-8ee9-00ed4052b70e_1308x296.png)

Anyway, they have real test chips with this tech so the initial hurdle of convincing one of the big 3 DRAM players to help them has been overcome.

* * *

Nothing is going to convince me that small language models will be economically viable. Medium-sized language models… sure.

d-Matrix claims their 3D DRAM can achieve the following key metrics over normal HBM4:

  * 60% lower cost once the supply chain is ready.

  * 90% lower system-level energy consumption for data movement.

  * 2X the capacity per layer.

  * Insane bandwidth advantage of 100X.




I believe these claims are credible. **This is enough capacity to run medium-sized language models at incredible throughput and high batch sizes.**

Very exciting. It could actually work. Looking forward to seeing more progress from d-Matrix.

### [3.c] Huawei

The original presentation was going to talk about the Ascend AI accelerators. At the last minute, the slides were pulled and something completely different was presented.

Also, the Huawei guy apparently joined Q&A from his bed. Background blur was there but I legit think this dude was taking questions while chilling.

[![](https://substackcdn.com/image/fetch/$s_!h2G9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffd807609-bba6-431a-927a-47aa893de39d_1706x956.png)](https://substackcdn.com/image/fetch/$s_!h2G9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffd807609-bba6-431a-927a-47aa893de39d_1706x956.png)

Interesting. One proprietary standard to rule them all.

[![](https://substackcdn.com/image/fetch/$s_!UWxB!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3d7743a7-4395-4b50-bc6a-cb1d4773b2cc_1753x1043.png)](https://substackcdn.com/image/fetch/$s_!UWxB!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3d7743a7-4395-4b50-bc6a-cb1d4773b2cc_1753x1043.png)

Good explanation of the motivation behind what they are doing.

[![](https://substackcdn.com/image/fetch/$s_!34Kd!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7b610264-2f3a-4706-9ccc-e95a88be68a5_1700x1048.png)](https://substackcdn.com/image/fetch/$s_!34Kd!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7b610264-2f3a-4706-9ccc-e95a88be68a5_1700x1048.png)

Huawei is running 800G LPO using 7nm class process technology SerDes. Very impressive.

Western firms are just starting to get 800G LPO to work using much better 3nm class SerDes.

[![](https://substackcdn.com/image/fetch/$s_!LITt!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff65b8f4e-8c90-4dc7-9ded-a429f168315d_1657x980.png)](https://substackcdn.com/image/fetch/$s_!LITt!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff65b8f4e-8c90-4dc7-9ded-a429f168315d_1657x980.png)

Great explanation of LLR redundancy schemes.

### [3.d] Google TPU 6p/7 aka Ironwood

[![](https://substackcdn.com/image/fetch/$s_!EhOL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd624bc4c-af0c-4d24-81ae-56912e6d4242_1748x1057.png)](https://substackcdn.com/image/fetch/$s_!EhOL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd624bc4c-af0c-4d24-81ae-56912e6d4242_1748x1057.png)

6 connection points (+/- xyz) is important to remember.

4x4x4 cube is electrical only. OCS only hits when you connect multiple 444 cubes.

[![](https://substackcdn.com/image/fetch/$s_!JKlY!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffef9091f-2c6e-463f-8aba-58f2ed139cad_1755x933.png)](https://substackcdn.com/image/fetch/$s_!JKlY!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffef9091f-2c6e-463f-8aba-58f2ed139cad_1755x933.png)

The SparseCore is very interesting, primarily because of it’s location within the higher level block diagram.

[![](https://substackcdn.com/image/fetch/$s_!ffVX!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4f75cc1c-f2e5-4e39-9c32-2279a11ea7e2_1288x799.png)](https://substackcdn.com/image/fetch/$s_!ffVX!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4f75cc1c-f2e5-4e39-9c32-2279a11ea7e2_1288x799.png)

It’s on a separate node within the on-chip ring NoC. Allows for clever functional offload. “In network compute” happens on the main chip network, not the NIC or switch. This is because OCS is an ultra “dumb” switch with little to no computational flexibility.

Very interesting system design.

[![](https://substackcdn.com/image/fetch/$s_!sYQF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9a232cef-2fa3-4ced-b288-54140bd0b92d_1280x762.png)](https://substackcdn.com/image/fetch/$s_!sYQF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9a232cef-2fa3-4ced-b288-54140bd0b92d_1280x762.png)

The presenter verbally described the SDC mitigation strategy in a vague manner. Something about pre-job self-testing and even runtime based mathematical verification. 

Sounds like there is some dedicated hidden digital logic that monitors runtime floating-point math.

[![](https://substackcdn.com/image/fetch/$s_!NOyb!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7b5aa440-144b-4029-8570-3948d0bdf9b1_1310x733.png)](https://substackcdn.com/image/fetch/$s_!NOyb!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7b5aa440-144b-4029-8570-3948d0bdf9b1_1310x733.png)

The compute is VLIW based. Google is the only company in the world that has a good VLIW compiler. 

[![](https://substackcdn.com/image/fetch/$s_!qq5X!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F85680869-d9ad-497a-88f6-9a324266191f_1302x753.png)](https://substackcdn.com/image/fetch/$s_!qq5X!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F85680869-d9ad-497a-88f6-9a324266191f_1302x753.png)

6x8 = 48 lanes of 112G SerDes going across a wide variety of electrical channels. From KR reach PCB channels with multiple connection points to C2M channels to optical modules.

If you think the MediaTek jokers can make their 224G SerDes work at this scale… LOL.

[![](https://substackcdn.com/image/fetch/$s_!-o70!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd2c0ff2b-5139-4b26-9f32-0fb615fd9395_1290x829.png)](https://substackcdn.com/image/fetch/$s_!-o70!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd2c0ff2b-5139-4b26-9f32-0fb615fd9395_1290x829.png)

[![](https://substackcdn.com/image/fetch/$s_!te79!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7db3850d-52c1-424e-a321-12ffcc62224c_728x407.png)](https://substackcdn.com/image/fetch/$s_!te79!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7db3850d-52c1-424e-a321-12ffcc62224c_728x407.png)

You can see from the PCB that there are a wide variety of channel reaches. Designing one SerDes that can handle all possible channels is EXTREAMLY difficult. 

[![](https://substackcdn.com/image/fetch/$s_!j4BV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1cbc59bd-1c0c-49e7-b868-d48ba46675ca_226x249.png)](https://substackcdn.com/image/fetch/$s_!j4BV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1cbc59bd-1c0c-49e7-b868-d48ba46675ca_226x249.png)

[![](https://substackcdn.com/image/fetch/$s_!I5JK!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1bc0cf7a-f41e-4d3c-9ec2-977688825e03_1277x858.png)](https://substackcdn.com/image/fetch/$s_!I5JK!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1bc0cf7a-f41e-4d3c-9ec2-977688825e03_1277x858.png)

The nonstop rumors from Taiwan rumor mill regarding MediaTek taking TPU are still bullshit. Getting tired of explaining the same concepts over and over.

Maybe Google will make a prefill-style chip to copy Nvidia Rubin CPX

<https://semianalysis.com/2025/09/10/another-giant-leap-the-rubin-cpx-specialized-accelerator-rack/>

MediaTek could get their 200G working good enough to make a prefill-only chip using the following strategies.

  * Run the 200G SerDes in 100G mode. (brute force)

  * Tune the crap out of their 200G to make it work really well with Google’s specific TPUv8 PCB design.

    * Adjust fixed and floating FFE tap ratio.

    * Boost CTLE gain at Nyquist and accept the SerDes won’t function at short channel reaches.

    * Use SiTime chips to PPM sync entire compute blade.




Anyone who is worried about Broadcom losing Google TPU because of fucking MediaTek needs to chill.

I have like $20B+ worth of AVGO stock holders (various institutional investors combined) who keep asking me the same question over and over. Chill guys. Google is playing games because they know Hock has them locked in.

## [4] Rack-Scale Roundup

Half a day was dedicated to rack-scale stuff. Some interesting bits from several presentations. Going to lump them all into one section.

[![](https://substackcdn.com/image/fetch/$s_!q2dj!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe4d1d7c9-9a50-4940-86c0-e82f354f93b6_1769x1083.png)](https://substackcdn.com/image/fetch/$s_!q2dj!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe4d1d7c9-9a50-4940-86c0-e82f354f93b6_1769x1083.png)

[![](https://substackcdn.com/image/fetch/$s_!_qcF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F963f27dd-84e8-442f-8e39-78dc85218367_1728x991.png)](https://substackcdn.com/image/fetch/$s_!_qcF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F963f27dd-84e8-442f-8e39-78dc85218367_1728x991.png)

Remember the 4x4x4 block internal plumbing is all electrical and needs ultra-high end SerDes that can handle extremely short and extremely long channel reaches.

[![](https://substackcdn.com/image/fetch/$s_!UbTt!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1e9dc296-646b-4626-836d-6fbbde4dcac9_1548x1006.png)](https://substackcdn.com/image/fetch/$s_!UbTt!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1e9dc296-646b-4626-836d-6fbbde4dcac9_1548x1006.png)

[![](https://substackcdn.com/image/fetch/$s_!MUKN!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6be01264-8f00-4979-b116-27fb98c49f95_1681x1035.png)](https://substackcdn.com/image/fetch/$s_!MUKN!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6be01264-8f00-4979-b116-27fb98c49f95_1681x1035.png)

[![](https://substackcdn.com/image/fetch/$s_!ih-G!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7f69f9fd-6e71-4970-96d9-c0179788af37_1640x865.png)](https://substackcdn.com/image/fetch/$s_!ih-G!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7f69f9fd-6e71-4970-96d9-c0179788af37_1640x865.png)

Managing this many fiber cables in such a small space is apparently very difficult.

* * *

[![](https://substackcdn.com/image/fetch/$s_!18DI!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa1934ec2-3061-4f81-8cb6-50097e64c890_1758x969.png)](https://substackcdn.com/image/fetch/$s_!18DI!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa1934ec2-3061-4f81-8cb6-50097e64c890_1758x969.png)

All I could think about when seeing this slide is how fucked over Semtech was by ACC rack architecture changes. LOL

[![](https://substackcdn.com/image/fetch/$s_!CZ5o!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F55b02cb6-7bcf-4acc-9896-ff37bb0fb649_1720x960.png)](https://substackcdn.com/image/fetch/$s_!CZ5o!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F55b02cb6-7bcf-4acc-9896-ff37bb0fb649_1720x960.png)

Either these cross-rack cables are DAC or the volume of Catalina was way lower than what Semtech was hoping for.

[![](https://substackcdn.com/image/fetch/$s_!DbJi!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5dd8994e-5545-48ec-b3c5-438f4b19ccf2_1724x929.png)](https://substackcdn.com/image/fetch/$s_!DbJi!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5dd8994e-5545-48ec-b3c5-438f4b19ccf2_1724x929.png)

Meta has lots of workloads (particularly recommendation network inference) that thrives off CPU compute for embedding table math and higher DRAM to compute ratio from more LPDDR.

[![](https://substackcdn.com/image/fetch/$s_!TqE7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb75a8178-a882-44e9-bf19-02bfdd54b8a0_1736x963.png)](https://substackcdn.com/image/fetch/$s_!TqE7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb75a8178-a882-44e9-bf19-02bfdd54b8a0_1736x963.png)

[![](https://substackcdn.com/image/fetch/$s_!CymE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F907c61c4-80c2-4b33-939c-3d074e450f2c_1712x978.png)](https://substackcdn.com/image/fetch/$s_!CymE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F907c61c4-80c2-4b33-939c-3d074e450f2c_1712x978.png)

Those copper cables in the middle looks extraordinarily thick. Maybe the Skin effect is what fked Semtech. 

* * *

[![](https://substackcdn.com/image/fetch/$s_!aQIb!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbaa99999-1742-4049-bad6-1ee99033edf9_1724x1062.png)](https://substackcdn.com/image/fetch/$s_!aQIb!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbaa99999-1742-4049-bad6-1ee99033edf9_1724x1062.png)

These NVLink spine mechanical stabilizers are apparently very difficult to manufacture and required ultra specialized CNC machines.

* * *

[![](https://substackcdn.com/image/fetch/$s_!-joK!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9070afde-6440-4eca-b669-4cc92b250fd5_1706x1106.png)](https://substackcdn.com/image/fetch/$s_!-joK!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9070afde-6440-4eca-b669-4cc92b250fd5_1706x1106.png)

Ok… so your link budget analysis has so much variation that it is basically useless.

Also reflections reflections reflections. I hate it when novices focus on insertion loss and fail to mention channel complexity/reflections. 

[![](https://substackcdn.com/image/fetch/$s_!rHJa!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2a152788-9dd4-4d6f-83f6-127fcc03af49_1702x911.png)](https://substackcdn.com/image/fetch/$s_!rHJa!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2a152788-9dd4-4d6f-83f6-127fcc03af49_1702x911.png)

We gona need cheaper co-packaged optics that drop the Marvell DSPs and use redundant lasers in OIF ELSFP form factor.

* * *

[![](https://substackcdn.com/image/fetch/$s_!8sPV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F247670a2-ff09-449a-857f-2e5db641dd55_1759x988.png)](https://substackcdn.com/image/fetch/$s_!8sPV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F247670a2-ff09-449a-857f-2e5db641dd55_1759x988.png)

Whoever made this slide does not know what they talking about. All of the power numbers are way too high. For example, passive copper can easily hit 3.5 pJ/bit for long channels and 2.5 pJ/bit for short channels. 

Optical transceiver pJ/bit is very easy to calculate. 

## [5] Miscellaneous

Mostly CPU stuff that most people don’t care about. (I still care…)

### [5.a] Intel Clearwater Forrest

[![](https://substackcdn.com/image/fetch/$s_!nT1S!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F150d94c6-c191-43d2-a606-6d44a68679c3_1711x932.png)](https://substackcdn.com/image/fetch/$s_!nT1S!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F150d94c6-c191-43d2-a606-6d44a68679c3_1711x932.png)

[![](https://substackcdn.com/image/fetch/$s_!cp2d!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fce71902c-b4b1-4dd5-a2e4-165122925578_1751x940.png)](https://substackcdn.com/image/fetch/$s_!cp2d!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fce71902c-b4b1-4dd5-a2e4-165122925578_1751x940.png)

[![](https://substackcdn.com/image/fetch/$s_!LOhe!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F13b891fd-35a8-4f15-92f0-27ff0486f045_1718x965.png)](https://substackcdn.com/image/fetch/$s_!LOhe!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F13b891fd-35a8-4f15-92f0-27ff0486f045_1718x965.png)

[![](https://substackcdn.com/image/fetch/$s_!tARa!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3d94f0f9-07ce-443d-979b-56482de93869_1724x829.png)](https://substackcdn.com/image/fetch/$s_!tARa!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3d94f0f9-07ce-443d-979b-56482de93869_1724x829.png)

The Intel presenter repeatedly mentioned 18A and how it is real, this Clearwater Forest product is real, and will be shipping soon. They even underlined 18A repeatedly to hammer this home.

Someone in Q&A literally asked this dude if 18A is still on the roadmap. On the one hand, this is a rather rude question and people should not troll like this at Hot Chips.

On the other hand, this shit was hilarious. Look at the faces the Intel presenter made.

[![](https://substackcdn.com/image/fetch/$s_!n-1s!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F99bd0ee4-c03d-4907-a281-ab30a005eefc_309x1033.png)](https://substackcdn.com/image/fetch/$s_!n-1s!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F99bd0ee4-c03d-4907-a281-ab30a005eefc_309x1033.png)

This is the face of a man who is thinking _“what the fuck did you just ask me you little shit?”_ while trying VERY HARD to remain professional.

[![](https://substackcdn.com/image/fetch/$s_!cu59!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe0f61f83-18f1-41c7-a03f-ec84a073329b_1720x962.png)](https://substackcdn.com/image/fetch/$s_!cu59!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe0f61f83-18f1-41c7-a03f-ec84a073329b_1720x962.png)

[![](https://substackcdn.com/image/fetch/$s_!BGIW!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1762a6b5-ba24-41c5-9005-bc6be3056d87_1740x958.png)](https://substackcdn.com/image/fetch/$s_!BGIW!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1762a6b5-ba24-41c5-9005-bc6be3056d87_1740x958.png)

Much wider decode and OOO engine.

[![](https://substackcdn.com/image/fetch/$s_!37rv!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F02735c90-fe37-45c3-86d1-b28902287b28_1715x972.png)](https://substackcdn.com/image/fetch/$s_!37rv!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F02735c90-fe37-45c3-86d1-b28902287b28_1715x972.png)

Ok they just made everything bigger it seems.

[![](https://substackcdn.com/image/fetch/$s_!tt2u!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd8344306-7ef4-420c-9f19-661e34ac99d5_1726x904.png)](https://substackcdn.com/image/fetch/$s_!tt2u!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd8344306-7ef4-420c-9f19-661e34ac99d5_1726x904.png)

17% IPC uplift is nice but uh… that L2 latency looks a bit high?

[![](https://substackcdn.com/image/fetch/$s_!HEUd!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2fe31e43-2b61-43ef-99bb-63042c209ef1_1735x939.png)](https://substackcdn.com/image/fetch/$s_!HEUd!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2fe31e43-2b61-43ef-99bb-63042c209ef1_1735x939.png)

It was clarified in Q&A that standard (not MRDIMM) DDR5 8000 is natively supported. Nice!

### [5.b] Strange RISC-V CPUs

There were a few interesting/exotic RISC-V CPUs presented. Lets start of Andes/Condor.

[![](https://substackcdn.com/image/fetch/$s_!br-B!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0e791999-9cb1-463c-bf62-6e7a6754fa30_1747x986.png)](https://substackcdn.com/image/fetch/$s_!br-B!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0e791999-9cb1-463c-bf62-6e7a6754fa30_1747x986.png)

What if we took the pain and suffering of VLIW style compilers and used that to make a RISC-V CPU?

[![](https://substackcdn.com/image/fetch/$s_!XKgE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4669f0c2-3f89-4745-8582-44f3bee66eca_1729x976.png)](https://substackcdn.com/image/fetch/$s_!XKgE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4669f0c2-3f89-4745-8582-44f3bee66eca_1729x976.png)

A compiler efficiently scheduling branchy and dynamic CPU code. HMMMMM WHY DO I DOUBT THIS CLAIM???

[![](https://substackcdn.com/image/fetch/$s_!8nom!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe0cda13a-2734-46cb-babc-3c66c3cdea0b_1699x1023.png)](https://substackcdn.com/image/fetch/$s_!8nom!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe0cda13a-2734-46cb-babc-3c66c3cdea0b_1699x1023.png)

Well researched? More like “lots of others have tried and they all dead now.”

[![](https://substackcdn.com/image/fetch/$s_!Pzzp!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffedc0e7e-70f4-4a57-b592-fb78cf3c6ade_1700x974.png)](https://substackcdn.com/image/fetch/$s_!Pzzp!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffedc0e7e-70f4-4a57-b592-fb78cf3c6ade_1700x974.png)

The presenter tried to brush off 30% wasted instructions from dependency induced replays as “a reasonable impact”. LOL

* * *

Next we have PEZY. 

[![](https://substackcdn.com/image/fetch/$s_!YVBn!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F56b5c8af-0e1c-440d-9d65-b22ee8d1d822_1633x910.png)](https://substackcdn.com/image/fetch/$s_!YVBn!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F56b5c8af-0e1c-440d-9d65-b22ee8d1d822_1633x910.png)

Ok… this looks like a GPU but go on…

[![](https://substackcdn.com/image/fetch/$s_!4dHF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2847be9d-fa78-43d9-8ede-5ff2b4f89ae8_1635x879.png)](https://substackcdn.com/image/fetch/$s_!4dHF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2847be9d-fa78-43d9-8ede-5ff2b4f89ae8_1635x879.png)

No branch predictor or OOO engine.

[![](https://substackcdn.com/image/fetch/$s_!Ueat!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F334ede2f-0f18-4b2e-b5b9-34ecb5ba03bb_1653x923.png)](https://substackcdn.com/image/fetch/$s_!Ueat!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F334ede2f-0f18-4b2e-b5b9-34ecb5ba03bb_1653x923.png)

Interesting. Some internal NoC based compute.

[![](https://substackcdn.com/image/fetch/$s_!gToB!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc0c85af3-b7d9-455d-95ab-339bd09acb13_1673x916.png)](https://substackcdn.com/image/fetch/$s_!gToB!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc0c85af3-b7d9-455d-95ab-339bd09acb13_1673x916.png)

Well that is a very high area allocation to SRAM.

[![](https://substackcdn.com/image/fetch/$s_!CG0q!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F807b61dc-c9b6-428e-bf15-025e721d0284_1748x971.png)](https://substackcdn.com/image/fetch/$s_!CG0q!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F807b61dc-c9b6-428e-bf15-025e721d0284_1748x971.png)

[![](https://substackcdn.com/image/fetch/$s_!dA9D!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F13c59671-a813-4091-8dda-3478f685ca3f_1680x888.png)](https://substackcdn.com/image/fetch/$s_!dA9D!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F13c59671-a813-4091-8dda-3478f685ca3f_1680x888.png)

Overall an interesting architecture.

[![](https://substackcdn.com/image/fetch/$s_!iLhZ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff5519a71-71af-46a1-b710-46066e8de32d_1660x876.png)](https://substackcdn.com/image/fetch/$s_!iLhZ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff5519a71-71af-46a1-b710-46066e8de32d_1660x876.png)

Also they are developing their own HDL to compete with SystemVerilog. Great ambition guys. Best of luck.

### [5.c] Fully Homeomorphic Encryption RISC-V Accelerator

[![](https://substackcdn.com/image/fetch/$s_!9Mtm!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5e049d8c-9405-4a44-a975-8f49cfd07205_1754x1042.png)](https://substackcdn.com/image/fetch/$s_!9Mtm!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5e049d8c-9405-4a44-a975-8f49cfd07205_1754x1042.png)

This slide explains what FHE does pretty well. Encrypt data such that you can still run (some) math on it while encrypted without messing up decryption. Process data in a totally private manner.

[![](https://substackcdn.com/image/fetch/$s_!9In4!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe6db965e-9c51-402e-a822-9ded6de5aecd_1599x1004.png)](https://substackcdn.com/image/fetch/$s_!9In4!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe6db965e-9c51-402e-a822-9ded6de5aecd_1599x1004.png)

Each desired mathematical operation needs it’s own FHE strategy.

[![](https://substackcdn.com/image/fetch/$s_!UM21!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fda91513b-1c5d-4006-896a-0a0b95a58af2_1651x956.png)](https://substackcdn.com/image/fetch/$s_!UM21!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fda91513b-1c5d-4006-896a-0a0b95a58af2_1651x956.png)

[![](https://substackcdn.com/image/fetch/$s_!y20X!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fec0f8409-31a6-4937-b862-80fab46eab27_1675x894.png)](https://substackcdn.com/image/fetch/$s_!y20X!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fec0f8409-31a6-4937-b862-80fab46eab27_1675x894.png)

[![](https://substackcdn.com/image/fetch/$s_!f-hL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faf0efb70-7b0b-49ba-b2ba-5f71b9e0e4f7_1667x924.png)](https://substackcdn.com/image/fetch/$s_!f-hL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faf0efb70-7b0b-49ba-b2ba-5f71b9e0e4f7_1667x924.png)

Good overview of the objective for this Presto chip. One design that can run all the FHE strategies.

[![](https://substackcdn.com/image/fetch/$s_!qYk7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fefe9547b-e7bb-4c52-ab04-98b08c5a145d_1697x918.png)](https://substackcdn.com/image/fetch/$s_!qYk7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fefe9547b-e7bb-4c52-ab04-98b08c5a145d_1697x918.png)

Three blocks of custom instructions. Interesting that they have some custom load/store instructions. Seems to be for 128-bit operands?

[![](https://substackcdn.com/image/fetch/$s_!TV94!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9f2f06af-7814-45c2-bba8-c7ea744330ec_1633x892.png)](https://substackcdn.com/image/fetch/$s_!TV94!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9f2f06af-7814-45c2-bba8-c7ea744330ec_1633x892.png)

512-dim instructions ARE BACK BABY.

[![](https://substackcdn.com/image/fetch/$s_!R4dN!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F92ac1a66-2d28-4da2-9ce9-6150a83614be_1710x901.png)](https://substackcdn.com/image/fetch/$s_!R4dN!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F92ac1a66-2d28-4da2-9ce9-6150a83614be_1710x901.png)

[![](https://substackcdn.com/image/fetch/$s_!ShsD!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb225e907-d268-42b6-939e-916224c1b8c5_1692x826.png)](https://substackcdn.com/image/fetch/$s_!ShsD!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb225e907-d268-42b6-939e-916224c1b8c5_1692x826.png)

[![](https://substackcdn.com/image/fetch/$s_!g_0V!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F57a50f24-82e8-4c3a-9d95-ccfc88e0e18f_1679x909.png)](https://substackcdn.com/image/fetch/$s_!g_0V!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F57a50f24-82e8-4c3a-9d95-ccfc88e0e18f_1679x909.png)

[![](https://substackcdn.com/image/fetch/$s_!Bbk0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5d52374e-bc0a-4d05-9f69-571c9f844e89_1674x918.png)](https://substackcdn.com/image/fetch/$s_!Bbk0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5d52374e-bc0a-4d05-9f69-571c9f844e89_1674x918.png)

[![](https://substackcdn.com/image/fetch/$s_!agNS!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9180fbd5-6672-4dc4-8c05-eea31ba1f740_1656x900.png)](https://substackcdn.com/image/fetch/$s_!agNS!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9180fbd5-6672-4dc4-8c05-eea31ba1f740_1656x900.png)

I would have preferred benchmarks against a GPU. Say a weak Nvidia A10…

This is a highly parallel workload that probably competes with GPU acceleration in the real world?

### [5.d] IBM Power 11

[![](https://substackcdn.com/image/fetch/$s_!WyZV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faff1f7ba-bbcb-4b5d-b807-b8884fe928b4_1719x1008.png)](https://substackcdn.com/image/fetch/$s_!WyZV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faff1f7ba-bbcb-4b5d-b807-b8884fe928b4_1719x1008.png)

Pretty sure this is the only example of someone using Samsung Foundry advanced packaging.

[![](https://substackcdn.com/image/fetch/$s_!pmih!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F33205861-384b-40a0-bfcf-440d2e6cf33b_1757x1050.png)](https://substackcdn.com/image/fetch/$s_!pmih!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F33205861-384b-40a0-bfcf-440d2e6cf33b_1757x1050.png)

This is really cool. IBM has a universal memory interface that can attach to any kind of DRAM across multiple generations. It is SerDes (38.4 Gbps per lane) based and includes significant optimizations down to the CPU core uarch to mitigate latency issues. The presenter said the SerDes is synchronous with the DDR on the buffers so the pipeline is very long yet predictable. 

**Effectively, the latency penalty after all of these mitigations is only 6-8 nanoseconds.** This is an incredible result! Great job everyone who worked on this.

### [5.e] Weird 3D Printed Heatsinks

Ever wondered if it was possible to 3D print copper heatsinks?

Well… someone has done this. 

[![](https://substackcdn.com/image/fetch/$s_!SwjQ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F54d2706c-9d0a-4141-82ad-b906af86abcb_1871x1034.png)](https://substackcdn.com/image/fetch/$s_!SwjQ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F54d2706c-9d0a-4141-82ad-b906af86abcb_1871x1034.png)

[![](https://substackcdn.com/image/fetch/$s_!IQ9k!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb8c7032e-1a1f-4228-a2dc-3bf7c5adcf19_1502x831.png)](https://substackcdn.com/image/fetch/$s_!IQ9k!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb8c7032e-1a1f-4228-a2dc-3bf7c5adcf19_1502x831.png)

[![](https://substackcdn.com/image/fetch/$s_!Krso!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa664a1de-2e60-4cfd-9839-881e0ee77484_1504x842.png)](https://substackcdn.com/image/fetch/$s_!Krso!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa664a1de-2e60-4cfd-9839-881e0ee77484_1504x842.png)

This is super cool. Regular finned copper coldplates are limited to straight lines and this causes turbulence issues. Fabric8 has apparently developed a process that can create solid copper coldplates with arbitrary features.

[![](https://substackcdn.com/image/fetch/$s_!roIj!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1a0b7321-4bfe-43dc-84fd-7f9d6071ec5b_1508x829.png)](https://substackcdn.com/image/fetch/$s_!roIj!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1a0b7321-4bfe-43dc-84fd-7f9d6071ec5b_1508x829.png)

[![](https://substackcdn.com/image/fetch/$s_!gqna!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F44030982-7bff-4b9b-8505-7fcc65b0a250_1511x841.png)](https://substackcdn.com/image/fetch/$s_!gqna!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F44030982-7bff-4b9b-8505-7fcc65b0a250_1511x841.png)

[![](https://substackcdn.com/image/fetch/$s_!VtHH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2c1200b1-ba6e-494f-831f-b55dd349e475_1496x821.png)](https://substackcdn.com/image/fetch/$s_!VtHH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2c1200b1-ba6e-494f-831f-b55dd349e475_1496x821.png)

Incredible expansion in the design space for thermal solutions. 

[![](https://substackcdn.com/image/fetch/$s_!WSuw!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faf6dff6c-878f-4cfc-8eb2-b8732375fbc9_1495x825.png)](https://substackcdn.com/image/fetch/$s_!WSuw!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faf6dff6c-878f-4cfc-8eb2-b8732375fbc9_1495x825.png)

Two-phase immersion cooling is mostly dead. The fluids needed are ultra toxic “forever” chemicals that 3M has discontinued.

To say nothing of the maintenance nightmare that is immersion cooling.

Still interesting.

I doubt their claim of “cost competitiveness” with traditional coldplate manufacturing is legit. Still, I can see some people paying a premium to design turbulence-resistant DLC coldplates with extreme flexibility provided by ECAM.

## [6] Useless Keynotes

Last year, Trevor Cai (the OpenAI guy) gave an excellent keynote presentation. Very informative, educational, and technical. 

This year, we got two useless keynotes that were a complete waste of time.

I was going to pick apart these keynotes but both of the presenters seem like very nice people.

Subscribe for engineering-driven investment analysis.

Subscribe

Share with Alchip employees. Surely they will get a good laugh out of this.

[Share](https://irrationalanalysis.substack.com/p/hot-chips-2025-irrational-recap?utm_source=substack&utm_medium=email&utm_content=share&action=share)
