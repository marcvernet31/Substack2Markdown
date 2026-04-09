# [V]ery [L]ong [I]ncoherent [W]riteup

## Historical context on Groq.

**Feb 24, 2024**

**Likes:** 0

# IMPORTANT

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Please check the [‘about’ page](https://irrationalanalysis.substack.com/about) for a list of active positions.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice and readers should **always do their own research before investing in any security.**

* * *




You are probably here to read about Groq. Please read this post in-order and refrain from skipping directly to the Groq section. Intuition is built through an understanding of history and is one of the most useful skills to develop.

# Contents:

  1. What is VLIW?

  2. Origins

  3. Selected (non-Groq) Examples

    1. Intel Itanium (IA-64)

    2. Movidius/Intel (Meteor Lake NPU)

    3. Xilinx/AMD (XDNA)

    4. Qualcomm Hexagon

    5. Google TPU

    6. Texas Instruments VelociTI

  4. High-level Attributes and Comparisons

  5. VLIW Product Cycle

  6. Groq

  7. The Dog and ~~Pony~~ Llama Show

    1. PPAP

    2. Attrition

  8. Conclusion




* * *

### [1] What is VLIW?

Very-Long Instruction-Word is an exotic style of computer architecture that is drastically different from CPUs and GPUs.

For more information about how CPUs and GPUs work at a high-level, see this post:

[![A Guide on Computer Architecture](https://substackcdn.com/image/fetch/$s_!4cPo!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F20df94e9-a115-4209-a526-6f4cf1578298_2662x3415.jpeg)

#### A Guide on Computer Architecture

[Daud's Scout](https://substack.com/profile/135313705-dauds-scout)·February 4, 2024[Read full story](https://irrationalanalysis.substack.com/p/a-guide-on-computer-architecture)](https://irrationalanalysis.substack.com/p/a-guide-on-computer-architecture)

For details on the leading CPU instruction sets (x86, ARM, RISC-V), see this post:

[![Instruction Sets For Investors](https://substackcdn.com/image/youtube/w_728,c_limit/QMiubC6LdTA)

#### Instruction Sets For Investors

[Daud's Scout](https://substack.com/profile/135313705-dauds-scout)·October 7, 2023[Read full story](https://irrationalanalysis.substack.com/p/instruction-sets-for-investors)](https://irrationalanalysis.substack.com/p/instruction-sets-for-investors)

VLIW is interesting because it enables hardware that is simple, elegant, efficient, and low latency. The drawback is incredible, crushing burden/expectations placed upon the compiler team, often requiring end-users to **hand write assembly code.**

For decades, VLIW has excelled in niche markets such as low-power DSP and embedded microcontrollers. With the rise of AI, there has been a VLIW renascence. I will get to that in section [3].

But first, how does VLIW work at a high-level?

[![](https://substackcdn.com/image/fetch/$s_!LLqj!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F30b58215-8453-474e-a040-bd80f93b50bf_1072x463.jpeg)](https://substackcdn.com/image/fetch/$s_!LLqj!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F30b58215-8453-474e-a040-bd80f93b50bf_1072x463.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!_CQz!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe3805803-bea0-46aa-ad62-4cc5666eed6f_848x292.jpeg)](https://substackcdn.com/image/fetch/$s_!_CQz!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe3805803-bea0-46aa-ad62-4cc5666eed6f_848x292.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!rPhb!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdc4ed1a7-2c5b-4555-a5a1-237bc46a0100_960x690.jpeg)](https://substackcdn.com/image/fetch/$s_!rPhb!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdc4ed1a7-2c5b-4555-a5a1-237bc46a0100_960x690.jpeg)

CPUs and GPUs must dedicate significant resources (chip area, power burn) in order to schedule work (instructions) in an efficient manner. These transistors are always on, always burning power, and increase the final cost of the chip.

VLIW architectures essentially remove all these transistors and place enormous responsibility upon the compiler. 

The compiler must group instructions together into a “bundle” while making sure they are not dependent on one another. The bundle maps to the architecture in an often heterogeneous manner. For example, an arithmetic operation can only go into slot #1 or #3 while a load instruction can only go in slot #5. 

### [2] Origins

[![](https://substackcdn.com/image/fetch/$s_!iL2c!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6d78ce0c-a83f-400e-9341-77e45954b690_2086x1103.png)](https://substackcdn.com/image/fetch/$s_!iL2c!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6d78ce0c-a83f-400e-9341-77e45954b690_2086x1103.png)Intel/Movidius (Meteor Lake NPU), Qualcomm Hexagon, and AMD/Xilinx XDNA are all VLIW (compiler-dependent) like Groq and marketed as AI architectures.

VLIW is not new. In fact, it has a rich history starting in the early 1980’s. The first commercial VLIW processors were created by Multiflow, a startup founded by Josh Fisher, and released in 1987. 

Over a span of 36-years, many engineering teams across countless public and private companies have tried to make VLIW work with mixed success. This architecture is extremely unbalanced and leads to extreme results, for better or for worse.

### [3] Selected (non-Groq) Examples

Let’s take a look at some of the most important examples throughout this 36-year history.

#### [3.a] Intel Itanium (IA-64)

[![](https://substackcdn.com/image/fetch/$s_!kMV1!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8c2b54ea-dfb6-4440-a1f7-1c68792bec8f_1209x773.png)](https://substackcdn.com/image/fetch/$s_!kMV1!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8c2b54ea-dfb6-4440-a1f7-1c68792bec8f_1209x773.png)

[![](https://substackcdn.com/image/fetch/$s_!HlR1!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff56fc6d9-2318-4179-9bb0-3083fb90523a_1298x898.png)](https://substackcdn.com/image/fetch/$s_!HlR1!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff56fc6d9-2318-4179-9bb0-3083fb90523a_1298x898.png)

Itanium was Intel’s effort to enter the 64-bit era. They believed that it was impossible to extend x86 (32-bit) to 64-bit and had a strong desire to snuff out other x86 ISA licensees like AMD. And so, Itanium was born. A completely new, radically different architecture. 

Itanium is technically not VLIW. Computer nerds consider Itanium to be something “different” called EPIC. I am not going to waste time going over the nuances of a dead, one-off architecture. Itanium is the only EPIC architecture ever commercialized and it has very similar strengths/weaknesses when compared to “pure” VLIW. Close enough.

Why did Itanium die? 

  1. The compiler was bad and never got better. 

  2. AMD (Jim Keller) extended x86 to 64-bit with AMD64 aka x86-64, delivering a much better alternative with full backwards compatibility.




Fun fact, the lead architect of Itanium was Pat Gelsinger, current CEO of Intel.

[![](https://substackcdn.com/image/fetch/$s_!eui6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F902f48a7-445e-41de-90f9-32980693aa59_3150x2962.webp)](https://substackcdn.com/image/fetch/$s_!eui6!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F902f48a7-445e-41de-90f9-32980693aa59_3150x2962.webp)

He looks so happy in this photo.

[![](https://substackcdn.com/image/fetch/$s_!3qGP!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F040f50fe-b380-4058-8f7e-3c1b14124f8a_678x381.jpeg)](https://substackcdn.com/image/fetch/$s_!3qGP!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F040f50fe-b380-4058-8f7e-3c1b14124f8a_678x381.jpeg)Jim Keller remembering that time he flipped the table on Intel by out-innovating the creators of x86 on their own ISA.

Because of the joint venture between Intel and HP, Itanium lived on in a zombie state until 2021. It was a mess. [HP even sued Oracle for $3B because Oracle stopped porting their software to IA-64. ](https://www.nextplatform.com/2021/12/01/the-ghost-of-itanium-and-hpc-give-hpe-long-sought-profits/)

#### [3.b] Movidius/Intel (Meteor Lake NPU)

In 2016, intel acquired a startup called [Movidius](https://techcrunch.com/2016/09/05/intel-buys-computer-vision-startup-movidius-as-it-looks-to-build-up-its-realsense-platform/) that focused on computer vision. Their focus was on ultra-low power (< 1 watt) visual tracking. 

[![](https://substackcdn.com/image/fetch/$s_!FpmU!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe60f70e5-d7e1-49f0-b6ac-e0a4588448fb_1170x659.jpeg)](https://substackcdn.com/image/fetch/$s_!FpmU!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe60f70e5-d7e1-49f0-b6ac-e0a4588448fb_1170x659.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!_Hu1!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F326f4bf8-4fa4-4589-b48b-7ff949283aa1_1170x659.jpeg)](https://substackcdn.com/image/fetch/$s_!_Hu1!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F326f4bf8-4fa4-4589-b48b-7ff949283aa1_1170x659.jpeg)

The NPU in Intel’s most recent client product (Meteor Lake // Core Ultra) is from the Movidus team. And surprise… the **control** is handled by **VLIW DSPs**. This is the beginning of a pattern. #forshadowing

#### [3.c] Xilinx/AMD (XDNA)

AMD acquired Xilinx in 2022 so let’s start with Xilinx first as there is some re-branding going on.

[![](https://substackcdn.com/image/fetch/$s_!4dOE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe11e0186-4d43-48e7-83f0-039b71dfabab_1387x758.jpeg)](https://substackcdn.com/image/fetch/$s_!4dOE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe11e0186-4d43-48e7-83f0-039b71dfabab_1387x758.jpeg)

Xilinx is (er… was) an FPGA company. The best FPGA company IMO. At a high-level, FPGAs allow users to write hardware code (Verilog, VHDL) to test chip prototypes and rapidly iterate. Instead of waiting months for a chip to get taped-out, fabricated, and brought up, you can re-program and FPGA in typically 90 seconds or less. This makes FPGAs super useful in certain markets that want to iterate hardware and willing to pay a significant area/cost penalty for flexibility and “adaptability”. 

[![](https://substackcdn.com/image/fetch/$s_!xlfb!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0678f127-1838-413c-93a0-f4b9465c2dfe_512x265.png)](https://substackcdn.com/image/fetch/$s_!xlfb!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0678f127-1838-413c-93a0-f4b9465c2dfe_512x265.png)

The “adaptable” hardware (red block) is really a giant set of look-up tables, flip-flops, and multiplexers. Maximum flexibility for terrible efficiency. 

This is why Xilinx (and other FPGA vendors) add fixed-function “hard” IPs to their products. One of the most popular engines (green block) is for digital signal processing, **DSP.**

But if you look at newer Xilinx block diagrams, there are some new blocks.

[![](https://substackcdn.com/image/fetch/$s_!HHRG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F30edc1b0-aee4-4dbe-9016-6abd21910962_1797x1330.png)](https://substackcdn.com/image/fetch/$s_!HHRG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F30edc1b0-aee4-4dbe-9016-6abd21910962_1797x1330.png)

[![](https://substackcdn.com/image/fetch/$s_!eL0B!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb5718b69-1172-4f8f-9e28-c8dfee1c5873_959x864.webp)](https://substackcdn.com/image/fetch/$s_!eL0B!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb5718b69-1172-4f8f-9e28-c8dfee1c5873_959x864.webp)

Look! There is a shiny new green block right above the **DSP** engine. A new… AI engine.

[![](https://substackcdn.com/image/fetch/$s_!ubV3!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8dcdf0f0-209b-46ac-99cb-3f83bf8f3b04_670x461.png)](https://substackcdn.com/image/fetch/$s_!ubV3!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8dcdf0f0-209b-46ac-99cb-3f83bf8f3b04_670x461.png)

And guess what… it is **VLIW.**

The delta between “AI” and “DSP” is some minor changes in the ISA. Some DSP-specific instructions (beamforming, LDPC) are removed, support for low-precision INT4 and BF16 added, and some changes in memory structure.

[![](https://substackcdn.com/image/fetch/$s_!WEA1!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbff0003e-16d3-490f-9d93-28d961dfc6f4_921x663.png)](https://substackcdn.com/image/fetch/$s_!WEA1!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbff0003e-16d3-490f-9d93-28d961dfc6f4_921x663.png)I edited out the weird “AIE vs AIE-ML” naming scheme for clarity. 

AMD has since rebranded this **VLIW** IP from Xilinx as “XDNA” and “Ryzen AI”. Another **DSP VLIW** that has been expanded/evolved into an AI engine.

[![](https://substackcdn.com/image/fetch/$s_!2p7D!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbc9567b4-77e5-4a78-b99d-b72ca52def4c_540x405.jpeg)](https://substackcdn.com/image/fetch/$s_!2p7D!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbc9567b4-77e5-4a78-b99d-b72ca52def4c_540x405.jpeg)

#### [3.d] Qualcomm Hexagon

[![](https://substackcdn.com/image/fetch/$s_!OQbi!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F97c956e9-f2df-469f-9c9e-989922c1c379_923x616.png)](https://substackcdn.com/image/fetch/$s_!OQbi!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F97c956e9-f2df-469f-9c9e-989922c1c379_923x616.png)

[![](https://substackcdn.com/image/fetch/$s_!eWL8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F100ab694-46f9-4745-8a53-891974550058_750x563.jpeg)](https://substackcdn.com/image/fetch/$s_!eWL8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F100ab694-46f9-4745-8a53-891974550058_750x563.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!nI3W!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F942ec46d-53c6-4f48-9326-8820b67a37d4_676x474.png)](https://substackcdn.com/image/fetch/$s_!nI3W!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F942ec46d-53c6-4f48-9326-8820b67a37d4_676x474.png)

[![](https://substackcdn.com/image/fetch/$s_!cRoD!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3d104ef0-ee1f-413f-a48f-aba81506b612_634x394.png)](https://substackcdn.com/image/fetch/$s_!cRoD!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3d104ef0-ee1f-413f-a48f-aba81506b612_634x394.png)

What a surprise. Another **DSP** engine that uses **VLIW** for **scalar control**.

I wonder if they maybe added a matrix extension to this DSP and re-branded it as an NPU/NSP/AI engine.

[![](https://substackcdn.com/image/fetch/$s_!ie32!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F110af491-5ff4-4507-9184-07880f180e21_2308x1112.png)](https://substackcdn.com/image/fetch/$s_!ie32!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F110af491-5ff4-4507-9184-07880f180e21_2308x1112.png)

[![](https://substackcdn.com/image/fetch/$s_!sJl5!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd3c5d345-692e-4882-9941-691a7093edc8_2290x1054.png)](https://substackcdn.com/image/fetch/$s_!sJl5!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd3c5d345-692e-4882-9941-691a7093edc8_2290x1054.png)

[![](https://substackcdn.com/image/fetch/$s_!Ut6g!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1deb4742-6ed1-4e68-bdb1-6eea30a3e2c0_1354x784.jpeg)](https://substackcdn.com/image/fetch/$s_!Ut6g!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1deb4742-6ed1-4e68-bdb1-6eea30a3e2c0_1354x784.jpeg)

For an excellent deep-dive, check out this [Chips and Cheese post.](https://chipsandcheese.com/2023/10/04/qualcomms-hexagon-dsp-and-now-npu/)

#### [3.e] Google TPU

[![](https://substackcdn.com/image/fetch/$s_!HXG5!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd1f5299d-d323-425c-82b6-05a935d1f315_2970x1700.jpeg)](https://substackcdn.com/image/fetch/$s_!HXG5!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd1f5299d-d323-425c-82b6-05a935d1f315_2970x1700.jpeg)

8-wide VLIW for scalar unit and control. Groq founder is ex-TPU team.

[![](https://substackcdn.com/image/fetch/$s_!HwSb!,w_56,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2F0150776c-9bf2-4bea-a9c2-41b24b7a0f15_1280x1280.png)SemiAnalysisGoogle AI Infrastructure Supremacy: Systems Matter More Than MicroarchitectureThe dawn of the AI era is here, and it is crucial to understand that the cost structure of AI-driven software deviates considerably from traditional software. Chip microarchitecture and system architecture play a vital role in the development and scalability of these innovative new forms of software. The hardware infrastructure on which AI software runs has a notably larger impact on Capex and Opex, and subsequently the gross margins, in contrast to earlier generations of software, where developer costs were relatively larger. Consequently, it is even more crucial to devote considerable attention to optimizing your AI infrastructure to be able to deploy AI software. Firms that have an advantage in infrastructure will also have an advantage in the ability to deploy and scale applications with AI…Read more3 years ago · 96 likes · 32 comments · Dylan Patel, George Cozma, and Gerald Wong](https://www.semianalysis.com/p/google-ai-infrastructure-supremacy?utm_source=substack&utm_campaign=post_embed&utm_medium=web)

>  **A 322b Very Long Instruction Word (VLIW) Scalar Computation Unit** is included in the TPU v4. In VLIW architectures, the instructions are grouped together into a single, long instruction word, which is then dispatched to the processor for execution. These grouped instructions, also known as **bundles** , are explicitly defined by the **compiler during program compilation.** The VLIW bundle comprises up to 2 scalar instructions, 2 vector ALU instructions, 1 vector load and 1 vector store instruction, and 2 slots for transferring data to and from the MXUs.

#### [3.f] Texas Instruments VelociTI

[![](https://substackcdn.com/image/fetch/$s_!3fae!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff008806e-76cd-46ff-8345-a85ab39d1d4c_864x442.png)](https://substackcdn.com/image/fetch/$s_!3fae!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff008806e-76cd-46ff-8345-a85ab39d1d4c_864x442.png)

5ns latency on an 8-wide **VLIW** for **DSP** markets.

### [4] High-level Attributes and Comparisons

[![](https://substackcdn.com/image/fetch/$s_!4b5U!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faa9cf1f8-cd48-4097-af8c-8d18179a1bde_740x178.png)](https://substackcdn.com/image/fetch/$s_!4b5U!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faa9cf1f8-cd48-4097-af8c-8d18179a1bde_740x178.png)One of these is not like the other.

VLIW architectures have the following attributes:

  * Excellent area efficiency. 

  * Extremely low latency.

  * Enables low-power (< 1 watt) designs.

  * Frees up significant power budget for other blocks. (matrix unit)

  * Historical success in DSP markets.

  *  **A nightmarish compiler problem that effectively forces expert end-users to hand-write assembly code in a soul-crushing manner.**




My formal education is on digital signal processing. This market needs low-latency and low power and tends to have intrinsically parallel workloads. Because of the severe constrains, the end-users of DSP-world are willing to hand-code assembly.

 **VLIW compilers are notoriously useless.** So bad that most folks view the compiler output as a starting point for the required, labor-intensive hand-optimization process. 

Here are some made up numbers that are directionally correct. 

_*I know the real averages of a certain widely deployed VLIW architecture but don’t want to violate NDA. Feel free to ask engineers you know who have worked with VLIW for additional color._

  * VLIW architecture has 8-wide bundles.

  * Compiler outputs code with average bundle occupancy of ~2. 

    * 25% utilization

    * Basically useless. Comically inefficient.

  *  **Highly experienced assembly programmers who are experts (5+ years) with that particular architecture spend weeks to months optimizing the code.**

    * Boost average occupancy to ~4. (50% utilization)

    * Maybe ~6 (75%) if some unrelated workloads can be woven in.




### [5] VLIW Product Cycle

Throughout the past 36-years of computer history, there have been many VLIW architectures. I only covered a small subset in section [3] but there are dozens more out there for the curious. Most of them are dead because of the typical product lifecycle for this extremely unbalanced architecture.

[![](https://substackcdn.com/image/fetch/$s_!lVhT!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1335e244-45bb-4add-a677-d9ab1ed74702_875x957.png)](https://substackcdn.com/image/fetch/$s_!lVhT!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1335e244-45bb-4add-a677-d9ab1ed74702_875x957.png)

There is always a massive disconnect between the hardware and compiler/software teams for VLIW projects. Hardware and systems folks are very proud of their work. They calculate the theoretical maximum throughput. They compare perf/watt against CPUs and GPUs. They present idealistic, rosy numbers to upper management and investors.

Inevitably, the compiler team fails. It’s not their fault. The expectations are unreasonable. Technical challenge is immense.

 **Over the last 36-years, Google is the only company that has made a good compiler for their ***8-wide*** VLIW core.**

We know the compiler is good because Google keeps putting out impressive results like Gemini 1.5 with the 10-million token context window.

However, traction amongst third parties for Google’s excellent TPU has been almost non-existent. [According to The Information](https://www.theinformation.com/articles/googles-cloud-unit-gains-key-ai-chip-team-to-compete-with-microsoft?rc=2zxinj), Google reorged the TPU team into Google Cloud back in April 2023 to get more traction for renting in-house TPUs to 3rd party customers.

 **This re-org cannot fix the VLIW compiler problem. Internal super-expert assembly programmers can get great performance out of TPUs but 3rd parties cannot. They would rather rent Nvidia GPUs.**

* * *

All hope is not lost for VLIW (outside of Google). Intel, AMD, and Qualcomm are all aggressively working on improving their compilers for small neural networks to enable on-device (smartphone/laptop/PC) use. There’s not much outside of cherry-picked demos but… they are trying really hard. Maybe with the launch of Windows 11 this year we can get some proper, 3rd party benchmarks.

Before moving on to Groq, I want to re-emphasize the following points.

  * Creating a high-performance VLIW compiler is extraordinarily difficult. 

  * The vast majority of VLIW architectures use 4-8 wide bundles.

  * Google TPU is the only success story but with important caveats.

    *  **TPU uses 8-wide while Groq uses 144-wide.**

    * 3rd-party traction for TPU has been very poor.




### [6] Groq

Groq has tried their hardest to avoid saying “VLIW”. Their marketing material basically shows all of the wonderful benefits of VLIW while hand-waving the compiler problem.

If you scrolled down directly to this section… shame!

[![](https://substackcdn.com/image/fetch/$s_!BoKG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb162973b-83d2-4b4d-944a-ec28bd65863a_270x278.gif)](https://substackcdn.com/image/fetch/$s_!BoKG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb162973b-83d2-4b4d-944a-ec28bd65863a_270x278.gif)

 **Scroll back up and read this post from the beginning like you were supposed to.**

\\(!!˚☐˚)/

\\(!!˚☐˚)/

\\(!!˚☐˚)/

\\(!!˚☐˚)/

[![](https://substackcdn.com/image/fetch/$s_!Mxiw!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7e5f2510-9903-4000-8ef9-3cd7d8459d51_469x751.png)](https://substackcdn.com/image/fetch/$s_!Mxiw!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7e5f2510-9903-4000-8ef9-3cd7d8459d51_469x751.png)

The whitepaper describes 144-VLIW without saying the damn acronym once in any of the 14 pages. There are plenty of other architectures out there that are similar in their “tradeoff” that pushes scheduling complexities onto the compiler. 

Let’s take a look at a late-2022 presentation by the **Chief Architect** of Groq.

[![](https://substackcdn.com/image/fetch/$s_!3vtH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F244b8be5-b58f-432e-9f61-d3752d0244f0_2013x859.png)](https://substackcdn.com/image/fetch/$s_!3vtH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F244b8be5-b58f-432e-9f61-d3752d0244f0_2013x859.png)

[![](https://substackcdn.com/image/fetch/$s_!3MjI!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2075ce98-5f62-46a2-beba-def42703af88_1986x1111.png)](https://substackcdn.com/image/fetch/$s_!3MjI!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2075ce98-5f62-46a2-beba-def42703af88_1986x1111.png)

There is one slide that admits the quiet part out loud. The one thing all the other papers, presentations, interviews, and marketing docs avoid.

 **This is a 144-wide VLIW architecture.**

Given how interesting and informative this presentation is, **I wonder where Dennis Abts, Chief Architect, is working now.**

[![](https://substackcdn.com/image/fetch/$s_!2E9C!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd0d63ed5-a045-49ab-b8e7-c334fa744aa1_713x395.png)](https://substackcdn.com/image/fetch/$s_!2E9C!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd0d63ed5-a045-49ab-b8e7-c334fa744aa1_713x395.png)

Oh.

He realized the compiler was never going to work, joined Nvidia in October 2022, and became filthy rich with RSUs that have rocketed in value? Oops.

* * *

Here is recent, hard evidence that the Groq compiler is just like all the other (non-Google) VLIW compilers. From their own marketing doc:

[![](https://substackcdn.com/image/fetch/$s_!gz07!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4196a402-5632-4587-91ba-690391f05712_1014x425.png)](https://substackcdn.com/image/fetch/$s_!gz07!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4196a402-5632-4587-91ba-690391f05712_1014x425.png)

Take a moment to carefully read this snippet and form your own opinion/understanding.

[![](https://substackcdn.com/image/fetch/$s_!xKXq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcdd7027b-b1c3-4981-b96f-780750fc22ab_509x404.png)](https://substackcdn.com/image/fetch/$s_!xKXq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcdd7027b-b1c3-4981-b96f-780750fc22ab_509x404.png)

They do not specify what “today” means so I extrapolated via linear fit. 

I believe the following are reasonable assumptions:

  * The Groq team achieved optimal performance of Llama-2 70B approximately 48 days after the model was released.

  * They have not acheived meaningfully better results since then, otherwise the marketing document would have been updated.

  * All the compiler, software, and systems engineers spent 100% of their time crunching to get this one model working, because they have no customers and nothing else to do.




What conclusions can we make based on this first-party information Groq so helpfully provided?

  1. It took the entire team of foremost experts of Groq architecture 5 days just to get the compiler to spit something out that functions.

  2. The 144-wide VLIW compiler completely failed at its job, delivering 1/30th (3.3%) of the optimal performance for that particular model.

  3. The super-expert team spent approximately 43 days hand-writing assembly code to optimize performance and improve average VLIW bundle occupancy.




This is standard VLIW stuff.

This is what happens when you try to compile AI models to 144-wide VLIW.

 **This time is not different.**

The compiler is practically useless. (not the compiler team’s fault)

They don’t have anything.

### [7] The Dog and ~~Pony~~ Llama Show

[![](https://substackcdn.com/image/fetch/$s_!-BGA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F278eceab-014e-4c9e-a517-c91198a36e17_1200x627.png)](https://substackcdn.com/image/fetch/$s_!-BGA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F278eceab-014e-4c9e-a517-c91198a36e17_1200x627.png)

Groq is very proud that their team was able to optimize one model by hand-writing complex assembly code over approximately 48 days.

[![](https://substackcdn.com/image/fetch/$s_!1att!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa17a6588-9f60-4dd4-a338-fc2b22170c37_800x926.jpeg)](https://substackcdn.com/image/fetch/$s_!1att!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa17a6588-9f60-4dd4-a338-fc2b22170c37_800x926.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!ODlg!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc84b2144-35d8-4a5a-ab53-2bf9b56dff37_4032x2268.jpeg)](https://substackcdn.com/image/fetch/$s_!ODlg!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc84b2144-35d8-4a5a-ab53-2bf9b56dff37_4032x2268.jpeg)

They even rented a real Llama to parade at conferences. 

Now you understand what VLIW is and how much effort it took for Groq employees (expert 1st-parties) to achieve this Llama-2 70B demo.

Do you think 3rd-party customers are going to get anything useful out of the compiler? Think they are willing to hand-code complex assembly for an exotic architecture?

 **This time is not different.**

The compiler is practically useless. (not the compiler team’s fault)

They don’t have anything. 

> " **Dog and pony show** " is a [colloquial](https://en.wikipedia.org/wiki/Colloquialism) term which has come to mean a highly promoted, often over-staged performance, presentation, or event designed to sway or convince opinion for political, or less often, commercial ends. Typically, the term is used in a [pejorative](https://en.wikipedia.org/wiki/Pejorative) sense to connote disdain, [jocular](https://en.wikipedia.org/wiki/Jocular) lack of appreciation, or distrust of the message being presented or the efforts undertaken to present it.[[1]](https://en.wikipedia.org/wiki/Dog_and_pony_show#cite_note-1)

Replace the pony with a llama and you have Groq.

#### [7.A] PPAP

In the semiconductor industry there is an acronym: PPA

  * [P]ower

    * How much energy the chip uses.

  * [P]erformance

    * How fast the chip is.

    * Can be measured my clock speed, IPC, FLOPS, or TOPS depending on the target market.

  * [A]rea

    * How big the chip is, and thus how expensive it is to manufacture.

    * Transistor count does not directly translate into area because some structures take up more area (SRAM, analog) than others (high-frequency logic).




But there is a fourth dimension that nobody really talks about, the third “P”.

 **[P]ain and suffering 3rd-party developers must subject themselves to utilize the chip effectively.**

VLIW is incredibly low-power because all the power-hungry (always-on) transistors for scheduling, speculative execution, and dependency checking logic are omitted.

VLIW has incredible ** **theoretical**** performance numbers, assuming the average bundle occupancy is high. 

VLIW utilizes very low chip area because again, all those pesky scheduling transistors are gone… replaced by a magical compiler that does not function outside of Google’s intranet.

Chips are balanced across PPA for various markets. VLIW hardware architects can claim they get the best of all worlds, if only the compiler team can deliver the impossible. 

This is why I prefer PPAP over PPA. 

#### [7.b] Attrition

Attrition is natural across every organization. But when high-ranking people leave, it is almost always a very bad sign. 

[![](https://substackcdn.com/image/fetch/$s_!Xs6M!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc0ff58fc-d654-4d7b-8985-276f9730a440_713x395.png)](https://substackcdn.com/image/fetch/$s_!Xs6M!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc0ff58fc-d654-4d7b-8985-276f9730a440_713x395.png)

Since finding out that the Chief Architect, the guy who presented at Hot Chips, noped out, I just had to… utilize LinkedIn search to dig deeper.

[![](https://substackcdn.com/image/fetch/$s_!yQzk!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3d69147b-f889-48f5-8b36-a93901213d08_757x747.png)](https://substackcdn.com/image/fetch/$s_!yQzk!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3d69147b-f889-48f5-8b36-a93901213d08_757x747.png)

A lot of high-ranks (Director and above) seem to have left Groq for greener pastures. Perhaps they know something that the show Llama does not?

Interestingly, there seems to be an AI chip startup called Positron AI that is basically all ex-Groq. Maybe the venture capitalists considering funding Groq should take a look at [positron.ai](https://www.positron.ai/).

### [8] Conclusion

“History does not repeat itself but it does rhyme.” — Mark Twain

VLIW architectures have a 36-year long, colorful history.

If you read this post from the beginning, you now have an understanding of this history and what to search for.

Feel free to dig deeper via Google, ChatGPT, Gemmini, or even Bing. The internet is a big, wonderful place full of information. Plenty to make up your own mind on if a 144-wide VLIW architecture is viable.

[![](https://substackcdn.com/image/fetch/$s_!R9Z9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F33ac7705-5a40-445a-8c0c-ec1d7360974e_527x265.png)](https://substackcdn.com/image/fetch/$s_!R9Z9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F33ac7705-5a40-445a-8c0c-ec1d7360974e_527x265.png)

You know my opinion.

If you enjoyed this content, please consider subscribing.

Subscribe

Already subscribed? Thanks! Please consider sharing. 

[Share](https://irrationalanalysis.substack.com/p/very-long-incoherent-writeup?utm_source=substack&utm_medium=email&utm_content=share&action=share)
