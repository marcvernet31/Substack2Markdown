# Practical Optical Communication Systems

## An intuitive approach.

**Nov 07, 2025**

**Likes:** 0

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice, and readers should **always do their own research before investing in any security.**

  * Feel free to contact me via email at: _irrational_analysis@proton.me_




* * *

The quality and reach of a communication system is typically determined by the channel.

  * How wide is the channel? (bandwidth)

  * How flat is the channel?

    * Frequency selective fading.

    * Return loss (reflections).

    * ISI




Imagine you stumble upon a [cursed monkey paw](https://en.wikipedia.org/wiki/The_Monkey%27s_Paw) and wish for a channel that has 10’s of terahertz worth of spectrally flat channel bandwidth where insertion loss is measured in tenths of a dB per kilometer and reflections are almost non-existent.

[![](https://substackcdn.com/image/fetch/$s_!JGwQ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F651c833a-549c-47bb-ad23-48a73fd321a4_270x466.png)](https://substackcdn.com/image/fetch/$s_!JGwQ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F651c833a-549c-47bb-ad23-48a73fd321a4_270x466.png)

The cursed monkey paw grants your wish, with hellish consequences.

Welcome to optical communication systems, where everything (except the channel) is a satanic nightmare and it’s a miracle any of this shit works at all.

[![a cursed monkey paw holding fibber cable](https://substackcdn.com/image/fetch/$s_!eLH6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4a982079-03f5-462c-a693-3f30cfbf9c40_1024x1024.webp)](https://substackcdn.com/image/fetch/$s_!eLH6!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4a982079-03f5-462c-a693-3f30cfbf9c40_1024x1024.webp)

* * *

For a detailed primer on communication systems, see this old post.

[![A Background-Proof Guide on Communication Systems](https://substackcdn.com/image/fetch/$s_!Ys6o!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd54998c3-a315-4dc4-8e5c-9150e8f53631_640x360.jpeg)

#### A Background-Proof Guide on Communication Systems

[Irrational Analysis](https://substack.com/profile/135313705-irrational-analysis)·December 2, 2024[Read full story](https://irrationalanalysis.substack.com/p/a-background-proof-guide-on-communication)](https://irrationalanalysis.substack.com/p/a-background-proof-guide-on-communication)

For an intro into co-packaged optics, see this old post.

[![A Background-Proof Guide on Co-Packaged Optics](https://substackcdn.com/image/fetch/$s_!44i5!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb309b9ac-2183-4485-8cc6-863aa4f983f9_1309x1312.png)

#### A Background-Proof Guide on Co-Packaged Optics

[Irrational Analysis](https://substack.com/profile/135313705-irrational-analysis)·April 12, 2025[Read full story](https://irrationalanalysis.substack.com/p/a-background-proof-guide-on-co-packaged)](https://irrationalanalysis.substack.com/p/a-background-proof-guide-on-co-packaged)

For a brief primer on the current 1.6T tranceiver ecosystem, see this old post.

[![Tower Semi, Fabrinet, and the Incredible Nvidia 1.6T Transceiver Ramp](https://substackcdn.com/image/fetch/$s_!WW5o!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F94e15b19-f2e1-494c-9862-45d6e0930f54_848x528.png)

#### Tower Semi, Fabrinet, and the Incredible Nvidia 1.6T Transceiver Ramp

[Irrational Analysis](https://substack.com/profile/135313705-irrational-analysis)·August 22, 2025[Read full story](https://irrationalanalysis.substack.com/p/tower-semi-fabrinet-and-the-incredible)](https://irrationalanalysis.substack.com/p/tower-semi-fabrinet-and-the-incredible)

Today I will focus on the **practical** side of things. A lot of theory is going to get handwaved in the interest of time. Go read above old posts for theory.

* * *

# Contents:

  1. Tuning

    1. Electronics/Analog

    2. Electronics/Digital

    3. Photonics: Monkey Paw Says “Fuck You”

  2. Periodicity and Filters

  3. Modulation

    1. The Driver Problem

    2. The TIA Problem

    3. Pointless Arguments and Modulator Tier List

  4. Reliability

    1. Standard Logic/Electronics Reliability: 1K Hour HTOL + ESD

    2. GR-468: Another Hell From The Monkey Paw

  5. Electronics Integration

    1. GloFo “Fusion” Node

    2. TSMC COUPE

  6. Simulation, PDK, and Test Equipment Time Machine

  7. Public Market Investment Corner




## [1] Tuning

All complex systems need tuning mechanisms to optimize performance and yield.

Let’s compare electronics and photonics using some simple examples.

### [1.a] Electronics/Analog

Here is an example of a tunable electrical amplifier inside a high-speed SerDes.

[![](https://substackcdn.com/image/fetch/$s_!xHYN!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc7cc0b19-04e4-495d-93cb-0a887a75f1b9_1243x708.png)](https://substackcdn.com/image/fetch/$s_!xHYN!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc7cc0b19-04e4-495d-93cb-0a887a75f1b9_1243x708.png)

[![](https://substackcdn.com/image/fetch/$s_!mQGf!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2a5ffc17-73d1-4ec4-8a67-01b3d58c0df3_1253x703.png)](https://substackcdn.com/image/fetch/$s_!mQGf!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2a5ffc17-73d1-4ec4-8a67-01b3d58c0df3_1253x703.png)

It is very important to have these tuning options because every electrical channel will be different. Two identical cables/connectors/PCB can easily have meaningfully different channel response and thus need different CTLE settings. This is a common thing.

Let’s take a more granular look at a generic analog circuit.

[![](https://substackcdn.com/image/fetch/$s_!VEsO!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa3bba3b3-cea1-41a1-b22c-c64aae563a55_846x658.png)](https://substackcdn.com/image/fetch/$s_!VEsO!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa3bba3b3-cea1-41a1-b22c-c64aae563a55_846x658.png)

This simple amplifier consists of five transistors.

Four transistors (M_1-M_4) are the amplifier itself.

One transistor (M_b) is for tuning the gain aka bias adjust aka common mode adjust aka “how strong amplifier is”.

Real designs typically need MUCH MORE tuning circuitry. Here are some examples of tuning options I would like to have for this one circuit.

  * Granular (8-bit) Vdd adjustment.

  * At least 3 transistors to adjust bias instead of just one.

  * A varactor and potentiometer to adjust output impedance to match load.

  * Tunable decap for VDD.

  * Separate common mode adjustment for both NMOS and PMOS.




The nice thing about electronics is there are many options for adding such tuning circuitry. This means that yield can be high and performance can be tuned across many temperatures and channel/operating conditions.

### [1.b] Electronics/Digital

Digital electronics are also highly tunable. Inside a modern chip, there can be thousands of sub-circuits with independently tunable clock-speeds. 

[![](https://substackcdn.com/image/fetch/$s_!ubJi!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3b689ce9-0880-4180-8d81-de3ee166f642_455x377.jpeg)](https://substackcdn.com/image/fetch/$s_!ubJi!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3b689ce9-0880-4180-8d81-de3ee166f642_455x377.jpeg)

Designers also include “chicken bits” that allow post-silicon validation to disable specific features.

Each sub-system in a digital logic IP block is highly configurable. This is a good thing.

### [1.c] Photonics: Monkey Paw Says “Fuck You”

All photonic structures are tuned with tiny heaters.

[![](https://substackcdn.com/image/fetch/$s_!hQC2!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6d2a9fa9-32ff-468b-8df8-21cffa34ad3e_225x225.jpeg)](https://substackcdn.com/image/fetch/$s_!hQC2!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6d2a9fa9-32ff-468b-8df8-21cffa34ad3e_225x225.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!Z2Lv!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F46932e3f-0952-47f5-9a79-56f97d9fdd58_681x443.png)](https://substackcdn.com/image/fetch/$s_!Z2Lv!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F46932e3f-0952-47f5-9a79-56f97d9fdd58_681x443.png)

[![](https://substackcdn.com/image/fetch/$s_!-B_P!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd1f6f4b3-bed1-4a3f-b39e-514091da3be5_767x515.png)](https://substackcdn.com/image/fetch/$s_!-B_P!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd1f6f4b3-bed1-4a3f-b39e-514091da3be5_767x515.png)A traditional EML chip that has a DFB laser and EAM modulator on the same InP substrate. A TEC (thermoelectric-cooler) is placed on top the entire chip to control both.

[![](https://substackcdn.com/image/fetch/$s_!SvJi!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4bfef77d-64ee-4951-b2f8-9f4e2175b560_643x230.png)](https://substackcdn.com/image/fetch/$s_!SvJi!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4bfef77d-64ee-4951-b2f8-9f4e2175b560_643x230.png)

Those of you with electronics background understand how fucked up this is.

For everyone else, let me express how painful this is in the form of gif.

[![](https://substackcdn.com/image/fetch/$s_!owwX!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa2c66921-8b21-49f1-acf6-91261b8be289_498x209.gif)](https://substackcdn.com/image/fetch/$s_!owwX!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa2c66921-8b21-49f1-acf6-91261b8be289_498x209.gif)Visual approximation of me realizing what tuning options I have to work with.

Almost zero granularity or programmability. Struggling to find words to express how obnoxious this tuning issue in photonics is.

Quick detour is necessary.

[![](https://substackcdn.com/image/fetch/$s_!b-m-!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6b7c1cd1-337b-47d6-a659-dde7851b6862_488x464.png)](https://substackcdn.com/image/fetch/$s_!b-m-!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6b7c1cd1-337b-47d6-a659-dde7851b6862_488x464.png)

<https://en.wikipedia.org/wiki/Proportional%E2%80%93integral%E2%80%93derivative_controller>

[![](https://substackcdn.com/image/fetch/$s_!3PxV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa10ba1c9-09bd-4e25-bcb2-b85a70865cae_2880x1025.png)](https://substackcdn.com/image/fetch/$s_!3PxV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa10ba1c9-09bd-4e25-bcb2-b85a70865cae_2880x1025.png)

Within engineering, there is a field called control theory.

A very popular (fundamental) control loop is called PID.

The system has a feedback mechanism to measure error.

Then the error, integral of the error, and derivative of the error are computed with a scaling factor for each.

Closed-loop PID control of parameters is a useful tool.

Directionally, electronic systems have maybe 5-10% of parameters under closed-loop PID control.

 **In photonics, almost everything is PID controlled.**

 **THIS IS NOT A GOOD THING.**

 **THIS IS FUCKING PAINFUL.**

Each PID control loop needs precise tuning of the coefficients. Debugging one of these things is very painful.

Within electronics, people often find that hardcoding values and disabling a PID controller leads to better results. In photonics, you can’t disable the PID loops because those fucking tiny heaters are unstable.

(this applies to all photonic structures… even MZIs in many situations need PID control)

The best part is, all the structures on a photonic chip dump thermal noise into each other. Adjusting the PID control of one structure regularly fucks up control of other structures. Standard debugging tactics like “lets turn off parts of the chip to isolate issue” don’t work.

## [2] Periodicity and Filters

Filters are an important tool for building communication systems.

Need a way to get rid of unwanted junk.

Here are some examples of filters found within traditional electronic systems.

[![](https://substackcdn.com/image/fetch/$s_!9ipi!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fad71405c-0243-4221-9a36-b2d9ac7f2a56_1051x1065.png)](https://substackcdn.com/image/fetch/$s_!9ipi!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fad71405c-0243-4221-9a36-b2d9ac7f2a56_1051x1065.png)

[![](https://substackcdn.com/image/fetch/$s_!z_79!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fec8f7c14-260c-4a24-8d16-863648efbac7_450x450.gif)](https://substackcdn.com/image/fetch/$s_!z_79!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fec8f7c14-260c-4a24-8d16-863648efbac7_450x450.gif)

[![](https://substackcdn.com/image/fetch/$s_!Thi7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F54874df4-a025-499f-a1f3-0b2475bf073f_1065x874.png)](https://substackcdn.com/image/fetch/$s_!Thi7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F54874df4-a025-499f-a1f3-0b2475bf073f_1065x874.png)

[![](https://substackcdn.com/image/fetch/$s_!vJsm!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe9c8a6e4-f7e0-415e-9ab8-ac0ab21fdf34_881x701.png)](https://substackcdn.com/image/fetch/$s_!vJsm!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe9c8a6e4-f7e0-415e-9ab8-ac0ab21fdf34_881x701.png)

[![](https://substackcdn.com/image/fetch/$s_!6i-J!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd9aaf507-21d9-4080-ab6b-58deb11ff158_1200x450.png)](https://substackcdn.com/image/fetch/$s_!6i-J!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd9aaf507-21d9-4080-ab6b-58deb11ff158_1200x450.png)

[![](https://substackcdn.com/image/fetch/$s_!RYY3!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3e186bc1-6e88-4ecb-af57-87849a9bc094_989x893.png)](https://substackcdn.com/image/fetch/$s_!RYY3!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3e186bc1-6e88-4ecb-af57-87849a9bc094_989x893.png)

[![](https://substackcdn.com/image/fetch/$s_!t_XD!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd12a7111-bc30-4c35-ae66-829d49ffcf8d_614x839.jpeg)](https://substackcdn.com/image/fetch/$s_!t_XD!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd12a7111-bc30-4c35-ae66-829d49ffcf8d_614x839.jpeg)

All of these analog and digital filters (within electronics world) have similar attributes:

  * Flat in the passband (good)

  * Sharp rejection of stopband (good)

  * Minimal weird spikes in the stopband (good)

    * Spikes in stopband still have over 30 dB rejection.

    * Not periodic.

    * Can design filter so spike is in less-problematic part of stopband.




 **Photonic filters are the opposite.** (complete dogshit… hilariously bad)

[![](https://substackcdn.com/image/fetch/$s_!xt0s!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F59769d53-18ac-4e8b-9969-dfe3ef83b9d2_885x646.png)](https://substackcdn.com/image/fetch/$s_!xt0s!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F59769d53-18ac-4e8b-9969-dfe3ef83b9d2_885x646.png)Ring filter response.

[![](https://substackcdn.com/image/fetch/$s_!cn2c!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7deecca0-6662-40f0-a8f1-c1fbc2cba0ce_574x480.png)](https://substackcdn.com/image/fetch/$s_!cn2c!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7deecca0-6662-40f0-a8f1-c1fbc2cba0ce_574x480.png)MZI filter response.

[![](https://substackcdn.com/image/fetch/$s_!KGl9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb9b6c375-8d7b-47eb-8f02-a4744a9bb473_316x242.gif)](https://substackcdn.com/image/fetch/$s_!KGl9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb9b6c375-8d7b-47eb-8f02-a4744a9bb473_316x242.gif)Another MZI filter response.

Not only are the filter responses dogshit (trash insertion loss, trash rejection ratio, trash passband flatness), they are also fucking periodic.

This is mind-blowingly annoying. 

**NOTHING IN ELECTRONICS IS PERFECTLY PERIODIC LIKE THIS PHOTONICS SHIT.**

## [3] Modulation

Modulation (in this context) is the process of making an electrical signal wiggle light.

[![](https://substackcdn.com/image/fetch/$s_!u0rV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd1cbf307-b853-426e-af3e-1d1b405015fc_852x359.png)](https://substackcdn.com/image/fetch/$s_!u0rV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd1cbf307-b853-426e-af3e-1d1b405015fc_852x359.png)

[![](https://substackcdn.com/image/fetch/$s_!WW5o!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F94e15b19-f2e1-494c-9862-45d6e0930f54_848x528.png)](https://substackcdn.com/image/fetch/$s_!WW5o!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F94e15b19-f2e1-494c-9862-45d6e0930f54_848x528.png)

[![](https://substackcdn.com/image/fetch/$s_!y63O!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7b1c487d-4d04-4ac8-8104-c7c13a7ac6da_840x486.png)](https://substackcdn.com/image/fetch/$s_!y63O!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7b1c487d-4d04-4ac8-8104-c7c13a7ac6da_840x486.png)

### [3.a] The Driver Problem

In general, optical modulators require high voltage swing (2+ Volt) and are usually singled-ended, commonly denoted by Vpp which stands for voltage-peak-peak.

[![](https://substackcdn.com/image/fetch/$s_!M3Tz!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2912db56-cf8d-4e9c-bc0a-7c0b7964911d_796x279.png)](https://substackcdn.com/image/fetch/$s_!M3Tz!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2912db56-cf8d-4e9c-bc0a-7c0b7964911d_796x279.png)

[![](https://substackcdn.com/image/fetch/$s_!GihC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9d8b17fe-e885-46aa-9441-359679859352_775x203.png)](https://substackcdn.com/image/fetch/$s_!GihC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9d8b17fe-e885-46aa-9441-359679859352_775x203.png)

All high-speed electrical SerDes are differential. Ignore this for now. Go read old posts if you want to understand why differential signaling exists.

Anyway, as an example, Ethernet SerDes is limited to 1200 mV Vpp.

[![](https://substackcdn.com/image/fetch/$s_!DQgo!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0a8fc3b1-9f64-4eb4-a69f-c0a6993be0df_782x514.png)](https://substackcdn.com/image/fetch/$s_!DQgo!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0a8fc3b1-9f64-4eb4-a69f-c0a6993be0df_782x514.png)

High-speed SerDes has swing of around 400-1100 mV and is optimized for 600-800 mV operation.

Die-to-die SerDes (UCIe, NVLink D2D, Broadcom MAX, Marvell D2D, Elyian) operate around 400 mV with an absolute theoretical maximum in the 800 mV ballpark.

So if you try the drive an optical modulator with an Ethernet SerDes directly, your system wont work at all.

Certain companies like to argue about how their modulators require lower voltage swing but fundamentally, all optical modulators need an external driver (amplifier/booster) to function. 

(all optical modulators suck)

Having an external driver in your system is not a good thing. It is a necessary evil.

  * More noise.

  * More power and cost.

  * Packaging/integration challenges.

  * Interoperability issues.

    * This is one of the reasons why LPO transceivers have taken so long to finally ramp.




### [3.b] The TIA Problem

Once light makes it to the receiver of an optical communication system, it needs to be converted back into electricity using a photodiode (PD).

You know bout LEDs right? You looking at LEDs right now reading this.

LED convert electricity into light.

PD does the opposite. Simple. 

The problem with PDs is the efficiency is… shit.

Electrical signal coming out of the PD is super weak and needs to be amplified with a transimpedance amplifier (TIA).

TIA is ****not**** an optics-specific component.

There are two basic amplifiers.

One is called TIA.

The other is called Gm.

You can chain these building blocks to create more complex amplifiers.

[![](https://substackcdn.com/image/fetch/$s_!ECHl!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbac15b45-6022-4e88-b7ec-331686dc44ff_663x651.png)](https://substackcdn.com/image/fetch/$s_!ECHl!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbac15b45-6022-4e88-b7ec-331686dc44ff_663x651.png)

You can put TIAs on the SerDes chip too. This is a common strategy. Problem is, you need a VERY POWRFULL TIA to boost the shitty signal coming out of PDs. 

Very Powerful means…

  * Poor power efficiency.

  * Adds lots of noise.

  * Expensive.

  * Packaging/integration challenges.




Having a discrete TIA in your system is not a good thing. It is another necessary evil.

### [3.c] Pointless Arguments and Modulator Tier List

The photonics industry is full of people making the following argument:

“My modulation tech is better than yours. Your modulation tech will never work.”

Within traditional transceivers, there are four options.

  1. VCSEL

  2. EML (InP monolithic EAM)

  3. SiPho MZI

  4. SiPho DR (single wavelength) Ring

    1. My old post on this assumed CWDM 4 wavelength.

    2. Old post wrong. It’s single-wavelength DR rings.

    3. Conclusions still same.

    4. I don’t edit old posts. Public record of mistakes and wrong calls is good thing.




Option #1 does not work for 200G per lane (1.6T transceiver) modulation. Reliability bad. Certain companies are coping that they gona get 200G VSCEL to work.

Nvidia is using option #4 for their 1.6T transceivers. They save power because the optical insertion loss of ring modulators is much lower than MZI or EAM.

But frankly, there is no reason to argue on option #2 vs #3 vs #4.

 **This is a business, not a philosophical debate.**

Ship as many units as possible at the highest gross margin as possible using whichever of the three viable options you want. There are tradeoffs. That’s the point of engineering.

* * *

For co-packaged optics, there are different options.

  1. VCSEL

  2. SiPho DR MZI

  3. SiPho DR (single-wavelength) ring

  4. SiPho CWDM (4 wavelength) ring bus

  5. SiPho DWDM (8+ wavelength) ring bus

  6. SiPho (Germanium) EAM

  7. Micro-LED




Let’s set aside #7 for now. 

(will shit on micro-LED later)

Honestly, all options 1-6 are theoretically viable.

I find it very irritating when people shill their modulator technology and make questionable arguments.

[![](https://substackcdn.com/image/fetch/$s_!A0RY!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff43c5cd5-298a-4da8-af1d-44c94f6f0b57_779x405.png)](https://substackcdn.com/image/fetch/$s_!A0RY!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff43c5cd5-298a-4da8-af1d-44c94f6f0b57_779x405.png)

Here is my personal opinion in tier form.

[![](https://substackcdn.com/image/fetch/$s_!vQCE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0d479827-2f0c-4811-b357-db480093d003_576x465.png)](https://substackcdn.com/image/fetch/$s_!vQCE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0d479827-2f0c-4811-b357-db480093d003_576x465.png)

In 2026, Nvidia is going to ship at least 10K units of CPO switches using DR rings running at 200G PAM4. (number is much higher…)

* * *

 ***Note:** _There is a reason why Nvidia is not using WDM in their initial CPO product. Many rings packed closely together lead to **MASSIVE** thermal crosstalk issues. Nvidia has not solved DWDM ring bus stability yet and they are the clear leaders. Something to think about._

_THERMAL STABILITY WITH ONE TRING ACTIVE != THERMAL STABILITY WITH ALL RINGS ACTIVE AND DUMPING NOISE INTO EACH OTHER_

 _THERMAL STABILITY WITH SLOW TEMPERATURE RAMP (DEGREES C PER SEC) DOES NOT PROVIDE USEFUL INFORMATION OR PROOF OF STABILITY._

* * *

Also in 2026, Broadcom is going to ship at least 10K units of Tomahawk 6 CPO switches using 200G PAM4 modulated MZI. (number is much higher…)

I feel like a reasonable definition of success for a CPO system is to meet all of the following requirements:

  1. Ship at least 10K units in one year.

  2. Achieve gross margins of at least 20%.

    1. If your margins suck, that means yield and thus technology suck.

    2. Are you a business or a science project?

    3. If your margins are worse than Chinese transceivers then you might have a problem.

  3. Pass GR-468, a reliability pre-requisite for people to buy your product.

    1. More on this in next section.




As far as I can tell, Nvidia and Broadcom are the only two companies who will meet these success requirements in 2026.

What if Nvidia and Broadcom wipe everyone else out? It’s a real possibility lol.

* * *

Now let’s talk about micro-LED.

In order to reduce the chance of a new cease-and-desist letter getting added to my collection, I will limit discussion to a specific paper published by Microsoft.

Do not extrapolate my commentary on the Micro[soft] LED paper with any other company that might work on something similar.

<https://www.microsoft.com/en-us/research/wp-content/uploads/2025/08/benyahya25mosaic.pdf>

[![](https://substackcdn.com/image/fetch/$s_!eBFm!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F36a84ed2-f5a6-4077-899c-85275b4a1c78_687x339.png)](https://substackcdn.com/image/fetch/$s_!eBFm!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F36a84ed2-f5a6-4077-899c-85275b4a1c78_687x339.png)

[![](https://substackcdn.com/image/fetch/$s_!NZc7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4a320592-59cd-48f5-854f-f207c93c170d_691x101.png)](https://substackcdn.com/image/fetch/$s_!NZc7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4a320592-59cd-48f5-854f-f207c93c170d_691x101.png)

I happen to have a pirated copy of IEEE 8021.3ck-2022. Also happen to be very familiar with this specification.

The citation in this Microsoft paper that pre-FEC BER needs to be 2e-4 or lower is technically correct. 

[![](https://substackcdn.com/image/fetch/$s_!bkbR!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffda4e3b0-1468-402b-9bec-128422df1b10_996x1291.png)](https://substackcdn.com/image/fetch/$s_!bkbR!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffda4e3b0-1468-402b-9bec-128422df1b10_996x1291.png)Open standard my ass. PUBLISH CRITICAL DOCUMENTS PUBLICLY FOR FREE YOU HYPOCRITES.

Within industry, this 2e-4 spec has been widely ridiculed for years. Its complete bullshit.

Real systems need at least 1e-7 pre-FEC BER MINIMUM TO BARELY PASS FEC TESTING.

A target of 1e-9 under adversarial conditions (HTHV+PSRR+JTOL+ITOL+PPM) is what people actually want. Clean operating conditions should hit 1e-11 or lower.

 **Every hyperscaler went to IEEE/Ethernet committee and complained that this 2e-4 spec is bullshit.**

 **This is why 200G standard (IEEE 802.3dj) made all compliance testing require **post-FEC data at 2e-13**.**

[![](https://substackcdn.com/image/fetch/$s_!Be5k!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3b19672f-7640-4991-8315-99656107b6df_727x338.png)](https://substackcdn.com/image/fetch/$s_!Be5k!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3b19672f-7640-4991-8315-99656107b6df_727x338.png)

[![](https://substackcdn.com/image/fetch/$s_!94K1!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F892b6518-c1cd-4b1e-aded-5e5df2fbe110_690x460.png)](https://substackcdn.com/image/fetch/$s_!94K1!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F892b6518-c1cd-4b1e-aded-5e5df2fbe110_690x460.png)

**2e-4 pre-FEC BER target is bullshit. Everyone in industry knows this. ****Ethernet changed spec to 2e-13 post-FEC for a reason!******

 **Showing data with only 25/100 channels is a huge red flag. Micro-LED solutions encounter massive electrical crosstalk issues. Turning off 75% of the channels massively distorts performance into an unreasonably favorable state.**

[![](https://substackcdn.com/image/fetch/$s_!E3Qk!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faac8d3e9-5f16-47c4-8ea5-4a0d0f9f7aea_734x928.png)](https://substackcdn.com/image/fetch/$s_!E3Qk!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faac8d3e9-5f16-47c4-8ea5-4a0d0f9f7aea_734x928.png)

1e-7 is frankly a generous threshold. I am being nice. Should draw the line at 1e-9.

The amount of power and digital area that needs to be allocated to FEC just to get this cheezed low-crosstalk (only 25/100 channels active) demo is truly hilarious. 

There is no indication at what temperature these (bad) BER numbers were measured at. Another huge red flag.

## [4] Reliability

I briefly touched on optical reliability in my recent OCP 2025

[![OCP Global Summit 2025: Irrational Recap](https://substackcdn.com/image/fetch/$s_!4Hlz!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc8d1aa2e-fe4e-48e7-87db-103321636868_536x831.png)

#### OCP Global Summit 2025: Irrational Recap

[Irrational Analysis](https://substack.com/profile/135313705-irrational-analysis)·October 24, 2025[Read full story](https://irrationalanalysis.substack.com/p/ocp-global-summit-2025-irrational)](https://irrationalanalysis.substack.com/p/ocp-global-summit-2025-irrational)

[![](https://substackcdn.com/image/fetch/$s_!zBo9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F166a4bdb-4a1f-47b5-b613-74e751c3c0c6_841x905.png)](https://substackcdn.com/image/fetch/$s_!zBo9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F166a4bdb-4a1f-47b5-b613-74e751c3c0c6_841x905.png)[OCP Global Summit 2025: Irrational Recap](https://irrationalanalysis.substack.com/p/ocp-global-summit-2025-irrational)

[![](https://substackcdn.com/image/fetch/$s_!DQLV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F955f6037-4813-44fe-837e-b7bce2531b45_732x357.png)](https://substackcdn.com/image/fetch/$s_!DQLV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F955f6037-4813-44fe-837e-b7bce2531b45_732x357.png)[OCP Global Summit 2025: Irrational Recap](https://irrationalanalysis.substack.com/p/ocp-global-summit-2025-irrational)

Some more details here. I think it is helpful to compare electronics and photonics again.

### [4.a] Standard Logic/Electronics Reliability: 1K Hour HTOL + ESD

Reliability of logic chips (electronics) is generally simple.

Here is the whole process with some typical numbers:

  1. Measure performance of a set of devices (typically 80-160 packaged dice) at room temperature and nominal voltage.

  2. Place all devices into an oven.

  3. Set the devices to run at +20% above nominal voltage on all power rails.

  4. Configure the oven temperature such that all device internal temperature monitor diodes read 125C or higher.

  5. Run all devices continuously for 48 hours, monitoring performance and current draw on all power rails.

  6. Remove devices from oven, measure at room temp, nominal voltage.

  7. Repeat steps 2-6 again at 168, 500, and 1000 hours.




This test is called “high-temperature operating life”, AKA HTOL.

<https://en.wikipedia.org/wiki/High-temperature_operating_life>

Broadly, the goal is to check a design for electromigration issues.

[![](https://substackcdn.com/image/fetch/$s_!jESa!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffc7aa97f-5687-4e30-8616-9d38253f8064_955x297.webp)](https://substackcdn.com/image/fetch/$s_!jESa!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffc7aa97f-5687-4e30-8616-9d38253f8064_955x297.webp)

[![](https://substackcdn.com/image/fetch/$s_!2-5f!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcb63353d-238b-475e-887d-e7dedf4ac919_780x247.png)](https://substackcdn.com/image/fetch/$s_!2-5f!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcb63353d-238b-475e-887d-e7dedf4ac919_780x247.png)

HTOL takes 1000 hours, which translates to about 43 days theoretically.

In practice, shit goes wrong. It takes more like 3 months realistically.

Modern EDA software (Synopsys, Cadence, Ansys) is generally quite good at simulating electromigration, commonly referred to as “EM” by designers.

If a design fails HTOL, someone fucked up and is probably going to get fired.

If a design passes HTOL, it is theoretically reliable up to 10 years of nominal operation. The numbers change on a case by case basis. For example, a particular chip might need to HTOL at (135C, +25% voltage) instead of (125C +20% voltage) to meet this industry-standard 10 year reliability criteria. I am just giving the common numbers.

* * *

The next major category to reliability testing for electronics is ESD, electro-static discharge.

Procedure for this is very simple.

  1. Measure the performance of a lot of devices (10-20 packaged dice) at NTNV.

  2. Use a special machine to “zap” certain bumps of each device at increasingly higher voltage.

    1. Not all bumps need to be checked for ESD.

    2. Only bumps sensitive to ESD such as high-speed signal, IO, or memory.

    3. VDD and ground bumps generally safe in most cases. 

  3. Measure the peak current of each zap.

  4. Measure the performance of each device after zap.

  5. Use a scatterplot to find where the design failed. (max tolerable current)




<https://www.electronicdesign.com/technologies/power/article/21799383/whats-the-difference-between-hbm-cdm-and-mm-test>

Above link is a good resource for more details. I plan on writing about reliability testing in more detail next year. For now… backlog of more interesting topics.

* * *

Broadly speaking, HTOL and ESD are the main reliability gates for electronics. Of course, automotive and military-grade parts need more reliability testing. But… the standard reliability testing is not that bad.

### [4.b] GR-468: Another Hell From The Monkey Paw

It’s so much worse. Legit order of magnitude more painful.

Investors, say the “GR-468” keyword to anyone who claims their optical product is ready for mass production. They either gona shit themselves or show you the data.

 **GR-468 is a hard requirement set by all major customers. This is not some “legacy” spec that can be ignored or handwaved. It is a satanic nightmare that must get done.**

No GR-468 == you die

[![](https://substackcdn.com/image/fetch/$s_!XfnC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdcd1d785-bc90-4a30-b9d2-69dfb2f727b0_588x388.png)](https://substackcdn.com/image/fetch/$s_!XfnC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdcd1d785-bc90-4a30-b9d2-69dfb2f727b0_588x388.png)

[![](https://substackcdn.com/image/fetch/$s_!JDD_!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6887936d-4bd3-4e0c-8143-a2addc63f65c_642x361.png)](https://substackcdn.com/image/fetch/$s_!JDD_!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6887936d-4bd3-4e0c-8143-a2addc63f65c_642x361.png)

[![](https://substackcdn.com/image/fetch/$s_!LYNO!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F84b2e070-1432-4f48-826d-f4281786af8e_690x609.png)](https://substackcdn.com/image/fetch/$s_!LYNO!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F84b2e070-1432-4f48-826d-f4281786af8e_690x609.png)

[![](https://substackcdn.com/image/fetch/$s_!Hla_!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc869996f-e7d0-4435-a681-596dd36d5bf0_641x308.png)](https://substackcdn.com/image/fetch/$s_!Hla_!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc869996f-e7d0-4435-a681-596dd36d5bf0_641x308.png)5000 hours. 5x electronics HTOL.

[![](https://substackcdn.com/image/fetch/$s_!5OeZ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F43e882b8-96ea-4cff-b0d0-cc3d77ff9c70_686x820.png)](https://substackcdn.com/image/fetch/$s_!5OeZ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F43e882b8-96ea-4cff-b0d0-cc3d77ff9c70_686x820.png)

[![](https://substackcdn.com/image/fetch/$s_!kgKq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8e95cd7a-17a9-4093-ada0-d045ce9a8ec8_639x537.png)](https://substackcdn.com/image/fetch/$s_!kgKq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8e95cd7a-17a9-4093-ada0-d045ce9a8ec8_639x537.png)

[![](https://substackcdn.com/image/fetch/$s_!nyH5!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3da636e4-59cf-442e-92bc-29b8f17f4b33_629x456.png)](https://substackcdn.com/image/fetch/$s_!nyH5!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3da636e4-59cf-442e-92bc-29b8f17f4b33_629x456.png)

[![](https://substackcdn.com/image/fetch/$s_!fENn!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fde4bd112-4dd2-42d7-925c-6a55d2ed099c_696x692.png)](https://substackcdn.com/image/fetch/$s_!fENn!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fde4bd112-4dd2-42d7-925c-6a55d2ed099c_696x692.png)

[![](https://substackcdn.com/image/fetch/$s_!4CcG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd830bb4d-de20-456f-a8d7-e1fdd103e684_725x812.png)](https://substackcdn.com/image/fetch/$s_!4CcG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd830bb4d-de20-456f-a8d7-e1fdd103e684_725x812.png)

[![](https://substackcdn.com/image/fetch/$s_!hxDV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb300d665-09f4-4270-9afd-95439db89ca6_689x837.png)](https://substackcdn.com/image/fetch/$s_!hxDV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb300d665-09f4-4270-9afd-95439db89ca6_689x837.png)Ring, MZI, EAM, whatever… all of them need to pass these tests. Minimum 5K hour HTOL.

[![](https://substackcdn.com/image/fetch/$s_!lUpD!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7158ffe1-ce34-443e-8d6f-cfe8ee9cb367_1280x720.jpeg)](https://substackcdn.com/image/fetch/$s_!lUpD!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7158ffe1-ce34-443e-8d6f-cfe8ee9cb367_1280x720.jpeg)

## [5] Electronics Integration

One of the major challenges that has plagued optics-land for decades is integrating the electronics. 

Ideally, you would want all of those drivers, TIAs, and photonics integrated into a single chip. Lower cost, better power efficiency, lower noise, higher performance.

The normal approach is to just have flip-chip packaging for the PIC, EIC, and (if applicable) discrete components.

[![](https://substackcdn.com/image/fetch/$s_!HIfz!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F256c75cd-acb5-48eb-9b05-519182b5339e_824x449.png)](https://substackcdn.com/image/fetch/$s_!HIfz!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F256c75cd-acb5-48eb-9b05-519182b5339e_824x449.png)

Here are the two novel approaches. 

### [5.a] GloFo “Fusion” Node

Global Foundries [GFS 0.00%↑](https://substack.com/discover/stocks/GFS) has a special process node that I like to call the “Fusion” node.

Their public marketing is unfortunately confusing. 

<https://gf.com/technology-platforms/silicon-photonics/>

[![](https://substackcdn.com/image/fetch/$s_!Wz14!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fae0e1bae-7e02-47f8-8c14-e7d4d12265c0_1290x751.png)](https://substackcdn.com/image/fetch/$s_!Wz14!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fae0e1bae-7e02-47f8-8c14-e7d4d12265c0_1290x751.png)

<https://gf.com/blog/next-gen-gf-fotonix-redefining-flexibility-bandwidth-upgrades-full-turnkey-support/>

[![](https://substackcdn.com/image/fetch/$s_!xrIo!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd86cfe10-bfa4-423f-b1f9-8ca2ceb94586_1138x425.png)](https://substackcdn.com/image/fetch/$s_!xrIo!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd86cfe10-bfa4-423f-b1f9-8ca2ceb94586_1138x425.png)

They use the “Photonix” branding for completely different process nodes.

Set aside the photonics-only nodes. Nothing I am about to write pertains to those nodes.

When GloFo talks about ”monolithic electo-optical” or “integrated photonics + RF CMOS” they are talking about what I call “the Fusion node”.

* * *

GloFo Fusion node is unique within industry. I am not aware of anyone else who has tried this.

They basically take a photonic process node and an 45nm-class electronic process node and smash them together.

This means that the “Fusion” node has a crazy layer count. When I first heard about how many layers this thing has and the cycle time, I burst out laughing.

Cycle time is worse than 3nm logic. It’s hilarious.

* * *

Now you have to understand that I talk to many people across dayjobs and though this hobby. On every topic, there is always a distribution of opinion.

Except on GloFo Fusion node.

I have had conversations with 40+ engineers across 7+ companies and the GloFo Fusion node is universally derided. **Not one person had a nice thing to say about GloFo fusion.**

Some common themes….

  * 45nm-class electronics not good enough for most applications, especially CPO.

  * 45nm-class GloFo electronics much worse than TSMC N45.

  * Massive electrical crosstalk issues.

  * Massive thermal crosstalk issues.

  * Reliability concerns due to warpage from having so many layers in the process.

  * Painful cycle time which delays R&D efforts.

  * Way too expensive.

  * Poor yield.




Optics industry went through a phase where this GloFo Fusion node was viewed as the “least-worst” option.

Until TSMC released COUPE.

### [5.b] TSMC COUPE

COUPE is TSMC’s answer to the “electronics integration” problem.

It’s amazing. Go read old posts for detailed coverage on why. 

[![](https://substackcdn.com/image/fetch/$s_!ZQ6k!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0c447057-1c5a-452b-9e6d-2e3bfd63a228_727x1195.png)](https://substackcdn.com/image/fetch/$s_!ZQ6k!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0c447057-1c5a-452b-9e6d-2e3bfd63a228_727x1195.png)[My backlog is good. Plz read old stuff. ](https://irrationalanalysis.substack.com/p/a-background-proof-guide-on-co-packaged)

Problem is cost. Hybrid bonding makes this solution very expensive.

TSMC has marketed COUPE for both traditional transceivers and CPO.

[![](https://substackcdn.com/image/fetch/$s_!-3hn!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5afa6407-4d88-4310-a126-075d7c1132dc_508x713.png)](https://substackcdn.com/image/fetch/$s_!-3hn!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5afa6407-4d88-4310-a126-075d7c1132dc_508x713.png)

Need to put my foot down here and say COUPE will NEVER BE VIABLE FOR TRANCEIVERS. Too expensive and frankly overkill.

## [6] Simulation, PDK, and Test Equipment Time Machine

All of this is so much worse than electronics. Feels like going back 15-20 years. Remarkable the optics/photonics industry has functioned all of this time with such crap tooling.

## [7] Public Market Investment Corner

Too lazy to update my long-only account manual spreadsheet. Sold all my Verizon, bought more Keysight with the proceeds. Goto old posts to find long-only holdings.

Here is trading account.

[![](https://substackcdn.com/image/fetch/$s_!6fxK!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F351bb0e9-acfa-4940-8f24-992a51df69e7_812x1368.webp)](https://substackcdn.com/image/fetch/$s_!6fxK!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F351bb0e9-acfa-4940-8f24-992a51df69e7_812x1368.webp)

[![](https://substackcdn.com/image/fetch/$s_!J__1!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F32c83d57-f55d-443a-9b9d-f0b3c0d42dd5_1229x1264.webp)](https://substackcdn.com/image/fetch/$s_!J__1!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F32c83d57-f55d-443a-9b9d-f0b3c0d42dd5_1229x1264.webp)

[![](https://substackcdn.com/image/fetch/$s_!RPXj!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fba846c7a-3732-4c23-8726-029ea345749b_755x1264.webp)](https://substackcdn.com/image/fetch/$s_!RPXj!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fba846c7a-3732-4c23-8726-029ea345749b_755x1264.webp)

[![](https://substackcdn.com/image/fetch/$s_!S7zd!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F76bf9896-55c1-4f5d-8653-d320f38ec4d5_926x1264.webp)](https://substackcdn.com/image/fetch/$s_!S7zd!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F76bf9896-55c1-4f5d-8653-d320f38ec4d5_926x1264.webp)

[![](https://substackcdn.com/image/fetch/$s_!djhL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8f506b58-8f88-4ebc-9075-a19e874b896c_1081x1264.webp)](https://substackcdn.com/image/fetch/$s_!djhL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8f506b58-8f88-4ebc-9075-a19e874b896c_1081x1264.webp)

Note: My average price for [LITE 0.00%↑](https://substack.com/discover/stocks/LITE) shares was $154 but I paper handed and sold half the position before buying back in after-hours while listening to the call.

[![](https://substackcdn.com/image/fetch/$s_!Oa-D!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc7f297b7-23b6-4ae5-b2d2-2d6215197afd_1440x2644.jpeg)](https://substackcdn.com/image/fetch/$s_!Oa-D!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc7f297b7-23b6-4ae5-b2d2-2d6215197afd_1440x2644.jpeg)

Ends up not mattering in terms of non-tax performance but it makes my taxes this year suck slightly more. I still need to pre-pay like $250K in taxes before EOY lol.

Anyway, here is brief opinion of several names in table form. Some earnings call analysis afterwards.

[![](https://substackcdn.com/image/fetch/$s_!_eo_!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7788b9e5-5c18-468e-82ca-a1e38111e5fa_1093x901.png)](https://substackcdn.com/image/fetch/$s_!_eo_!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7788b9e5-5c18-468e-82ca-a1e38111e5fa_1093x901.png)

Lumentum and Coherent earnings calls were super interesting. 

Let’s start with Lumentum.

[![](https://substackcdn.com/image/fetch/$s_!py8s!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5bd8a08d-c983-482b-a0c1-980b9665157d_798x292.png)](https://substackcdn.com/image/fetch/$s_!py8s!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5bd8a08d-c983-482b-a0c1-980b9665157d_798x292.png)

They were sold out, added 40% more capacity by migrating for 3in to 4in InP wafers, and are sold out again lol. Hyper-omega bullish.

[![](https://substackcdn.com/image/fetch/$s_!9k3i!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F29f52361-2e9f-46da-bf41-b6b225a99703_797x347.png)](https://substackcdn.com/image/fetch/$s_!9k3i!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F29f52361-2e9f-46da-bf41-b6b225a99703_797x347.png)

I like the Lumentum CEO. He seems to actually know what he is talking about.

[![](https://substackcdn.com/image/fetch/$s_!iQc2!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F54dcf1ab-a214-4259-8fe4-e0820dfd1b4c_361x219.gif)](https://substackcdn.com/image/fetch/$s_!iQc2!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F54dcf1ab-a214-4259-8fe4-e0820dfd1b4c_361x219.gif)

Linewidth of a laser is typically defined as the frequency span of the 3dB cutoff. 

1 MHz is considered to be good linewidth. For long-reach telecom applications, you want much more narrow. 

<https://www.lumentum.com/en/products/ultra-narrow-linewidth-micro-integrable-tunable-laser-assembly-mitla>

[![](https://substackcdn.com/image/fetch/$s_!8OV4!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6cf1fc2e-ded6-4f12-a922-977e478eab78_607x256.png)](https://substackcdn.com/image/fetch/$s_!8OV4!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6cf1fc2e-ded6-4f12-a922-977e478eab78_607x256.png)

[![](https://substackcdn.com/image/fetch/$s_!Lg70!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F45b93417-b09a-4ecd-901e-89dc7eb5384b_807x312.png)](https://substackcdn.com/image/fetch/$s_!Lg70!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F45b93417-b09a-4ecd-901e-89dc7eb5384b_807x312.png)

CW lasers have traditionally been 20-40 mW.

70 mW is a nice jump and they are ramping to 100 mW. Very nice.

[![](https://substackcdn.com/image/fetch/$s_!pTxq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc938d573-5b9a-4a74-9fbf-07f0737ca87f_823x263.png)](https://substackcdn.com/image/fetch/$s_!pTxq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc938d573-5b9a-4a74-9fbf-07f0737ca87f_823x263.png)

Pipe-cleaning for Nvidia CPO ramp H2 2026.

[![](https://substackcdn.com/image/fetch/$s_!7U4p!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F815a8c90-cadb-4b4f-b224-1450a6648fd0_825x522.png)](https://substackcdn.com/image/fetch/$s_!7U4p!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F815a8c90-cadb-4b4f-b224-1450a6648fd0_825x522.png)

[![](https://substackcdn.com/image/fetch/$s_!3Jz7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1e36580c-775c-42bb-a953-7a8279bada3b_802x240.png)](https://substackcdn.com/image/fetch/$s_!3Jz7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1e36580c-775c-42bb-a953-7a8279bada3b_802x240.png)

[![](https://substackcdn.com/image/fetch/$s_!hP9B!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F357cbf2c-2d3e-4952-b38f-8374613fca0e_790x285.png)](https://substackcdn.com/image/fetch/$s_!hP9B!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F357cbf2c-2d3e-4952-b38f-8374613fca0e_790x285.png)

[![](https://substackcdn.com/image/fetch/$s_!hOKs!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fafc00c91-96c6-4efe-bc2f-885190cc0640_820x317.png)](https://substackcdn.com/image/fetch/$s_!hOKs!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fafc00c91-96c6-4efe-bc2f-885190cc0640_820x317.png)

ultra-high power laser = 250-350 mW class

Nvidia CPO ramp is bigger now. 

Lumentum also appears to hint that they are talking to Broadcom for CPO ELSFP which is uh… surprising. 

* * *

Coherent call now.

[![](https://substackcdn.com/image/fetch/$s_!qQpY!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4bcf6c76-3f1a-4be1-9571-aa69ac65d40b_991x259.png)](https://substackcdn.com/image/fetch/$s_!qQpY!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4bcf6c76-3f1a-4be1-9571-aa69ac65d40b_991x259.png)

VCSEL is not going to work at 200G per lane. Reliability issues. I don’t understand why Coherent keeps coping and bringing this up.

[![](https://substackcdn.com/image/fetch/$s_!6cL4!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F716450d1-6d00-427c-a7a4-3f2ef0f53e5b_994x289.png)](https://substackcdn.com/image/fetch/$s_!6cL4!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F716450d1-6d00-427c-a7a4-3f2ef0f53e5b_994x289.png)

This claim that 6in InP yields are higher than 3in is frankly shocking. I am not sure how this is possible. Like its legit unbelievable.

Yield is usually defined as a percentage of good dice.

Maybe Coherent CEO is cheezing this by re-defining yield as number of dice at ISO cost. 

[![](https://substackcdn.com/image/fetch/$s_!OwwJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F700aab19-b475-4bf0-a4d4-c7c9b33b370d_609x425.png)](https://substackcdn.com/image/fetch/$s_!OwwJ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F700aab19-b475-4bf0-a4d4-c7c9b33b370d_609x425.png)

There is also the question of how they define yield in terms of quality.

If yield is “sellable EML” and only a small number of EML can work at 200G speeds while vast majority only work at 100G speeds, that would be good to know lol.

Coherent buys a lot of EML from Lumentum. There is a reason for this. (quality…)

[![](https://substackcdn.com/image/fetch/$s_!pMze!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdde8e30e-f214-4689-8a79-8d10f296b5b8_992x318.png)](https://substackcdn.com/image/fetch/$s_!pMze!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdde8e30e-f214-4689-8a79-8d10f296b5b8_992x318.png)

Bro if your 6in yield is so amazing and you doubling capacity why u buying **MORE** EML from Lumentum lol.

[![](https://substackcdn.com/image/fetch/$s_!aO6E!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbc10c166-af58-4adc-b10e-48f57f6e3848_993x324.png)](https://substackcdn.com/image/fetch/$s_!aO6E!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbc10c166-af58-4adc-b10e-48f57f6e3848_993x324.png)

Coherent is around 2-years behind on ultra-high-power CW lasers.

Lumentum is clear leader. 

**Finance friends, go ask Coherent CEO how far they are with GR-468 of these 400 mW lasers. Then go ask Lumentum CEO the same question.**

My email is public at the top of every post. Send me what they say plz.

[![](https://substackcdn.com/image/fetch/$s_!Ovd8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcb13191a-d396-4ece-abe8-0c6bf24c8318_1007x322.png)](https://substackcdn.com/image/fetch/$s_!Ovd8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcb13191a-d396-4ece-abe8-0c6bf24c8318_1007x322.png)

Coherent OCS tech has massive optical insertion loss. It’s like 3 dB lol.

[![](https://substackcdn.com/image/fetch/$s_!ntfC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F15f8ecab-db84-4634-921e-ed6d966a9752_1007x273.png)](https://substackcdn.com/image/fetch/$s_!ntfC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F15f8ecab-db84-4634-921e-ed6d966a9752_1007x273.png)

Liquid-crystal OCS is indeed way better reliability than MEMS OCS.

But what the hell u talking about with superior performance? Bro I have seen the insertion loss of public demo. It’s not good.

[![](https://substackcdn.com/image/fetch/$s_!s0VO!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F57f6c2de-0de9-4471-86f1-081af7f5c191_1030x539.png)](https://substackcdn.com/image/fetch/$s_!s0VO!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F57f6c2de-0de9-4471-86f1-081af7f5c191_1030x539.png)

Well… manufacturing PD is much easier than manufacturing lasers.

Sounds like some of the finance-crowd have picked up on something and there is trash talk behind the scenes.

[![](https://substackcdn.com/image/fetch/$s_!-Qck!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbf1c8461-13f8-4f55-81a9-109a3c2fe5ff_980x251.png)](https://substackcdn.com/image/fetch/$s_!-Qck!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbf1c8461-13f8-4f55-81a9-109a3c2fe5ff_980x251.png)

If cost is half then what is gross margin improvement?

Cost + Yield —> Gross Margin

The more Coherent execs talk about 6in InP amazing yield the more suspicious I get.

Messa smell bullshit.

[![](https://substackcdn.com/image/fetch/$s_!veKS!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0e4acc88-42ab-49c9-814d-01de8194bd1e_1023x438.png)](https://substackcdn.com/image/fetch/$s_!veKS!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0e4acc88-42ab-49c9-814d-01de8194bd1e_1023x438.png)

VCSEL IS NOT RELIABLE AT 200G PER LANE. SHOW GR-468 DATA. BROADCOM IS WORLD-LEADER IN VCSEL AND THEY STOPPED AT 100G/lane.

[![](https://substackcdn.com/image/fetch/$s_!T1lH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa65732fb-b0ea-444f-b4cb-2f501b3fc9b6_1591x1141.png)](https://substackcdn.com/image/fetch/$s_!T1lH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa65732fb-b0ea-444f-b4cb-2f501b3fc9b6_1591x1141.png)

Subscribe for engineering-driven investment analysis.

Subscribe

Share?

[Share](https://irrationalanalysis.substack.com/p/practical-optical-communication-systems?utm_source=substack&utm_medium=email&utm_content=share&action=share)
