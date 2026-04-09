# A Background-Proof Guide on Process Development Kits

## A practical approach.

**Jan 24, 2025**

**Likes:** 0

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Please check the [‘about’ page](https://irrationalanalysis.substack.com/about) for a list of active positions.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice, and readers should **always do their own research before investing in any security.**

  * Feel free to contact me via email at: _irrational_analysis@proton.me_




* * *

Process Development Kits (PDKs) are perhaps the most poorly understood sub-section of semiconductors. It’s mostly because of all the secrecy. 

Documents and data associated with PDKs are the most NDA-ed stuff out there. Very aggressive watermarking. 

Today I want to help all of you understand what is actually in a PDK and why it matters. Lots of practical issues depend on these top-secret documents, statistical models, and library files.

My first public post is a high-level guide on the entire semiconductor lifecycle with a fake chip design walked through from start to finish.

[![A Guide on Semiconductor Development ](https://substackcdn.com/image/fetch/$s_!gQ75!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2cc1731f-66e6-480b-af49-c0267681bffa_1365x986.png)

#### A Guide on Semiconductor Development 

[Irrational Analysis](https://substack.com/profile/135313705-irrational-analysis)·September 2, 2023[Read full story](https://irrationalanalysis.substack.com/p/a-guide-on-semiconductor-development)](https://irrationalanalysis.substack.com/p/a-guide-on-semiconductor-development)

Consider this a deep-dive into specific parts of semiconductor development. 

Four textbooks were used to develop the material. 

  * CMOS VLSI Design: A Circuits and Systems Perspective by Weste and Harris

  * Foundations of Analog and Digital Electronic Circuits by Agarwal and Lang

  * Principles of CMOS VLSI Design: A Systems Perspective by Weste and Eshaghian

  * Semiconductor Device Fundamentals by Pierret




For a full list of recommended books and resources, please refer here:

[![Recommended Books and Resources](https://substackcdn.com/image/fetch/$s_!G3HW!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2d79efd8-cff8-4c42-b450-d27a82357068_1024x1024.jpeg)

#### Recommended Books and Resources

[Irrational Analysis](https://substack.com/profile/135313705-irrational-analysis)·November 4, 2024[Read full story](https://irrationalanalysis.substack.com/p/recommended-books-and-resources)](https://irrationalanalysis.substack.com/p/recommended-books-and-resources)

* * *

I have written this material with the goal that ****anyone**** can understand and learn something new. **No pre-requisites and no dumbing-down either.** If you only understand 20% of this post, that is still a huge win IMO.

[![a semiconductor fab on fire](https://substackcdn.com/image/fetch/$s_!wHKp!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3fee8348-0707-4292-890a-fc2ecdb472d3_1024x1024.jpeg)](https://substackcdn.com/image/fetch/$s_!wHKp!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3fee8348-0707-4292-890a-fc2ecdb472d3_1024x1024.jpeg)

Let’s get started.

# Contents:

  1. What is in a PDK?

  2. Basic Theory

  3. Ideal Basic Devices

    1. Resistor, Capacitor, Inductor

    2. MOSFET (Popular Transistor)

  4. Stackup

  5. Design Rules

  6. Practical Issues

    1. Device Parasitics

    2. Wire Network Parasitics

    3. Electromagnetic Coupling

    4. Process Variation

    5. Temperature Sensitivity

    6. Voltage Uniformity

    7. Electromigration

    8. Leakage and Noise

    9. Detailed Example: Capacitors

  7. Design-Technology Co-Optimization (DTCO)

  8. Derivative Nodes

  9. Library Managment

  10. Simulations: **Garbage In? Garbage Out!**

  11. Bump-Out (Packaging)

  12. Overview of the three leading-edge logic foundries.




* * *

## [1] What is in a PDK?

A Process Development Kit (PDK) consists of three primary categories of materials.

  1. Standard Cell Libraires

    1. Transistors

    2. Resistor, Inductor, Capacitor (RLC)

    3. Higher Level Blocks

    4. …

  2. Models for the process, voltage, and temperature (PVT) sensitivity of devices.

    1. Gain behavior

    2. Noise

    3. Parasitics

    4. …

  3. Thousands of slides and pages of documentation that provide guidelines on how to place cells, improve yield, mitigate parasitics, and so on.




Standard cells are like building blocks. 

[![](https://substackcdn.com/image/fetch/$s_!NASA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb1842eee-0d4e-4e96-9e90-8dba48f67f4d_668x558.jpeg)](https://substackcdn.com/image/fetch/$s_!NASA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb1842eee-0d4e-4e96-9e90-8dba48f67f4d_668x558.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!u2FD!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7dc3fbb1-df0c-4c6d-bdb4-4b7220828306_1400x1010.jpeg)](https://substackcdn.com/image/fetch/$s_!u2FD!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7dc3fbb1-df0c-4c6d-bdb4-4b7220828306_1400x1010.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!9b-q!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4e18941c-644a-4348-93f3-1688d04852bc_378x417.png)](https://substackcdn.com/image/fetch/$s_!9b-q!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4e18941c-644a-4348-93f3-1688d04852bc_378x417.png)

[![](https://substackcdn.com/image/fetch/$s_!Zy3P!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3719cccb-bddb-4e16-9893-67f9ea0ce68e_1200x675.webp)](https://substackcdn.com/image/fetch/$s_!Zy3P!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3719cccb-bddb-4e16-9893-67f9ea0ce68e_1200x675.webp)

[![](https://substackcdn.com/image/fetch/$s_!MCNG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2b00b820-f965-44c2-8d49-828f42b332ff_1200x675.jpeg)](https://substackcdn.com/image/fetch/$s_!MCNG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2b00b820-f965-44c2-8d49-828f42b332ff_1200x675.jpeg)

## [2] Basic Theory

Digital signals do not exist in the real world. They are simply a very powerful abstraction.

[![](https://substackcdn.com/image/fetch/$s_!sjZk!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3d5b23e8-9df6-48c4-8cb8-7052eac8af9f_526x1045.png)](https://substackcdn.com/image/fetch/$s_!sjZk!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3d5b23e8-9df6-48c4-8cb8-7052eac8af9f_526x1045.png)

Analog problems need to be accounted for. For example, the rise/fall time of a transistor (switching element).

[![](https://substackcdn.com/image/fetch/$s_!7qKk!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa40e0d95-6582-4b8c-abbb-832d7338b871_1052x680.png)](https://substackcdn.com/image/fetch/$s_!7qKk!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa40e0d95-6582-4b8c-abbb-832d7338b871_1052x680.png)

Failure to do so results in bit errors, breaking the digital abstraction. 

* * *

Chips are 3-dimentional structures. “Stick Diagrams” are a useful tool for visualizing what is going on.

[![](https://substackcdn.com/image/fetch/$s_!E2qu!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F27c844e1-2acf-446d-b4fa-42eeaa7c3f6f_1598x731.png)](https://substackcdn.com/image/fetch/$s_!E2qu!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F27c844e1-2acf-446d-b4fa-42eeaa7c3f6f_1598x731.png)

[![](https://substackcdn.com/image/fetch/$s_!SOMV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F25ba2c49-1a53-484b-9967-bbc8e15daad1_1447x982.png)](https://substackcdn.com/image/fetch/$s_!SOMV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F25ba2c49-1a53-484b-9967-bbc8e15daad1_1447x982.png)

[![](https://substackcdn.com/image/fetch/$s_!y9tY!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F83e287eb-f6fe-4e47-8790-227c29955345_1524x980.png)](https://substackcdn.com/image/fetch/$s_!y9tY!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F83e287eb-f6fe-4e47-8790-227c29955345_1524x980.png)

[![](https://substackcdn.com/image/fetch/$s_!rusH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5d2f14c6-1237-46be-871e-c5df18385e85_616x653.png)](https://substackcdn.com/image/fetch/$s_!rusH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5d2f14c6-1237-46be-871e-c5df18385e85_616x653.png)

Think of these as top-down views of a structure.

PDKs have libraries full of variants of the same structure. Each version of the structure offers different tradeoffs.

For example, here are eight (8) versions of the same basic inverter.

[![](https://substackcdn.com/image/fetch/$s_!OoIC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff00c12bd-469b-4060-a274-a0de497d6fe5_930x931.png)](https://substackcdn.com/image/fetch/$s_!OoIC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff00c12bd-469b-4060-a274-a0de497d6fe5_930x931.png)

[![](https://substackcdn.com/image/fetch/$s_!povZ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4e513352-beef-4ed1-8301-8545145dbee7_565x779.png)](https://substackcdn.com/image/fetch/$s_!povZ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4e513352-beef-4ed1-8301-8545145dbee7_565x779.png)

Logic Foundries and design companies do not make up many versions of the same standard cell for fun. Various performance, area, and power characteristics drive the creation of so many “redundant” cells. (its not redundant)

* * *

Finally, the dynamic (frequency) response of a circuit is what really matters in most scenarios. To understand frequency response, we need to go beyond simple resistive models (V = IR). We need impedance.

[![](https://substackcdn.com/image/fetch/$s_!xlwk!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1c4c28bb-2b7c-4239-b30d-5dc92f9c64d1_550x270.png)](https://substackcdn.com/image/fetch/$s_!xlwk!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1c4c28bb-2b7c-4239-b30d-5dc92f9c64d1_550x270.png)

Impedance is a circuits resistance to an AC (sinusoidal) input. This will hopefully make more sense shortly.

## [3] Ideal Basic Devices

Note that everything in this section is ideal. **Real devices do not behave like this!**

### [3.a] Resistor, Capacitor, Inductor

Resistors are obvious. They simply create a voltage drop.

Capacitors and inductors are energy-storage elements. 

Capacitors (aka caps) are typically built with two parallel plates.

Inductors (aka chokes aka coils) are typically built with wire wounded in a circular manner.

Let’s look at the basic time-domain response of these energy storage elements.

[![](https://substackcdn.com/image/fetch/$s_!SL_I!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3ab47dfb-8ef7-450c-8826-cd6bb771380b_1102x847.png)](https://substackcdn.com/image/fetch/$s_!SL_I!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3ab47dfb-8ef7-450c-8826-cd6bb771380b_1102x847.png)A basic RC circuit smoothing out a step response of an ideal current source.

[![](https://substackcdn.com/image/fetch/$s_!BIM4!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F25192eb5-bfb5-4603-99c1-71499118721a_1460x1140.png)](https://substackcdn.com/image/fetch/$s_!BIM4!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F25192eb5-bfb5-4603-99c1-71499118721a_1460x1140.png)

[![](https://substackcdn.com/image/fetch/$s_!j5qG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4b68f32b-3ea5-450f-a9d7-63bf9ff47f90_1423x1164.png)](https://substackcdn.com/image/fetch/$s_!j5qG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4b68f32b-3ea5-450f-a9d7-63bf9ff47f90_1423x1164.png)Series RC circuit response to an ideal voltage source step.

[![](https://substackcdn.com/image/fetch/$s_!a0O9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe9f8f683-d8ae-40f9-8642-d88fc1bb650b_1451x940.png)](https://substackcdn.com/image/fetch/$s_!a0O9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe9f8f683-d8ae-40f9-8642-d88fc1bb650b_1451x940.png)Response to an ideal square wave. Note that the digital abstraction (0/1) is strained at larger RC values.

Similar analysis for inductors…

[![](https://substackcdn.com/image/fetch/$s_!KEH0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fec2fa343-c763-4e23-a4c5-1395f3f127b1_1372x986.png)](https://substackcdn.com/image/fetch/$s_!KEH0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fec2fa343-c763-4e23-a4c5-1395f3f127b1_1372x986.png)

[![](https://substackcdn.com/image/fetch/$s_!TOPq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd1ffea5e-7e21-425e-81ea-ef458790cc20_1545x655.png)](https://substackcdn.com/image/fetch/$s_!TOPq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd1ffea5e-7e21-425e-81ea-ef458790cc20_1545x655.png)

Time-domain responses are of limited use. What we really need for proper analysis is the frequency response. In other words, the response of a circuit to a sinusoidal input of arbitrary frequency. **Impedance.**

[![](https://substackcdn.com/image/fetch/$s_!wf28!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5568a12e-bfcd-4e2c-87b1-8f5a57b50bea_1540x813.png)](https://substackcdn.com/image/fetch/$s_!wf28!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5568a12e-bfcd-4e2c-87b1-8f5a57b50bea_1540x813.png)

[![](https://substackcdn.com/image/fetch/$s_!XGbV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa733fbfd-6ea8-4402-ba9a-5d23ad08a6b5_1497x979.png)](https://substackcdn.com/image/fetch/$s_!XGbV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa733fbfd-6ea8-4402-ba9a-5d23ad08a6b5_1497x979.png) Log-log plot for the AGI cultists.

### [3.b] MOSFET (Popular Transistor)

There are multiple types of transistors. The Metal-Oxide-Semiconductor Field-Effect-Transistor is the most popular and important flavor. 

[![](https://substackcdn.com/image/fetch/$s_!EFwg!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa42b6238-0d9f-4d3f-ac25-7df9e6dab1d9_1704x844.png)](https://substackcdn.com/image/fetch/$s_!EFwg!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa42b6238-0d9f-4d3f-ac25-7df9e6dab1d9_1704x844.png)

[![](https://substackcdn.com/image/fetch/$s_!hjKd!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff79e32ff-a47f-4511-b3d9-b3b9e709eacc_874x1018.png)](https://substackcdn.com/image/fetch/$s_!hjKd!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff79e32ff-a47f-4511-b3d9-b3b9e709eacc_874x1018.png)

The physics and complexities of material science are a topic for another day. 

All you really need to know for this post is that **transistors are voltage controlled switches.**

[![](https://substackcdn.com/image/fetch/$s_!V7jq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5c398d4e-4f5e-4a69-bbf6-4d46dd293daf_1644x902.png)](https://substackcdn.com/image/fetch/$s_!V7jq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5c398d4e-4f5e-4a69-bbf6-4d46dd293daf_1644x902.png)

And the math of an ideal MOSFET looks like this.

[![](https://substackcdn.com/image/fetch/$s_!HSx4!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F517182d5-2a66-448b-99f5-68aa97c67daa_1644x891.png)](https://substackcdn.com/image/fetch/$s_!HSx4!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F517182d5-2a66-448b-99f5-68aa97c67daa_1644x891.png)

There is a separate curve for gate-source (“control”) voltage.

As the voltage across the switch (drain-source) increases, the current across the switch also increases… up to a saturation point.

[![](https://substackcdn.com/image/fetch/$s_!aynY!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F674783ae-836c-47db-bb07-cc36437dd5ba_726x678.png)](https://substackcdn.com/image/fetch/$s_!aynY!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F674783ae-836c-47db-bb07-cc36437dd5ba_726x678.png)

Ideal MOSFETs are modeled with three regions. The math is a piecewise function.

[![](https://substackcdn.com/image/fetch/$s_!n9GS!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7382339c-9f23-4fa5-81d8-b0555043a121_568x588.jpeg)](https://substackcdn.com/image/fetch/$s_!n9GS!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7382339c-9f23-4fa5-81d8-b0555043a121_568x588.jpeg)

## [4] Stackup

[![](https://substackcdn.com/image/fetch/$s_!tNV2!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5c887ed8-d232-4fa7-b9b0-9e04f2bda37e_375x558.png)](https://substackcdn.com/image/fetch/$s_!tNV2!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5c887ed8-d232-4fa7-b9b0-9e04f2bda37e_375x558.png)

Every process node has multiple “stackup” options. How many layers (and of what thickness) are available for designers and automated tools to use.

In general, the transistors are at the bottom and the wires are above. This is over-simplified. Various analog components can be on many different layers.

[![](https://substackcdn.com/image/fetch/$s_!LzXi!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5e490122-a116-4090-9813-53371ccc3523_601x659.png)](https://substackcdn.com/image/fetch/$s_!LzXi!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5e490122-a116-4090-9813-53371ccc3523_601x659.png)

[![](https://substackcdn.com/image/fetch/$s_!0wsj!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6d950b08-9a43-42ad-9892-89c1f22298df_577x450.png)](https://substackcdn.com/image/fetch/$s_!0wsj!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6d950b08-9a43-42ad-9892-89c1f22298df_577x450.png)

[![](https://substackcdn.com/image/fetch/$s_!_CwD!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc5f29adc-fef5-42fe-b52b-0e563967e19b_950x449.webp)](https://substackcdn.com/image/fetch/$s_!_CwD!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc5f29adc-fef5-42fe-b52b-0e563967e19b_950x449.webp)

Backside-Power Delivery is a major change that has the transistors in the middle.

[![](https://substackcdn.com/image/fetch/$s_!i2OE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0db944d5-6773-4acf-a7bf-2937503bc6b0_862x575.png)](https://substackcdn.com/image/fetch/$s_!i2OE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0db944d5-6773-4acf-a7bf-2937503bc6b0_862x575.png)20A scrapped because 18A is going so well!

## [5] Design Rules

Design rules are physical constraints.

[![](https://substackcdn.com/image/fetch/$s_!BLOd!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F069a5d35-95c9-421d-8698-dd3dbdae364e_4000x3000.jpeg)](https://substackcdn.com/image/fetch/$s_!BLOd!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F069a5d35-95c9-421d-8698-dd3dbdae364e_4000x3000.jpeg)

The above rules are for a basic planar process node. FinFet (~22/14nm-class through ~3nm-class) is far more complicated. Gate-All-Around (GAA) is even more complex.

Automates tools perform Design Rule Checking (DRC). It is rumored that the last time Intel tried to be a logic foundry (~2015-2018) failed because the Altera people were in charge of making design rules for external customers.

[![](https://substackcdn.com/image/fetch/$s_!6DhX!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd18709c4-1c20-4ee1-bf66-9303619f99be_772x433.png)](https://substackcdn.com/image/fetch/$s_!6DhX!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd18709c4-1c20-4ee1-bf66-9303619f99be_772x433.png)

## [6] Practical Issues

Section [3] went over **ideal devices.** Real devices have lots of unwanted attributes that cause interesting problems. 

For example, clock speed and voltage of the final product are both decided after samples come back from the logic foundry.

[![](https://substackcdn.com/image/fetch/$s_!c4gf!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F30605782-ba3f-4f07-87e9-7eecdb90806d_829x1065.png)](https://substackcdn.com/image/fetch/$s_!c4gf!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F30605782-ba3f-4f07-87e9-7eecdb90806d_829x1065.png)

 **Always remember… clock speed and voltage (by extension power/TDP) are economic choices.**

### [6.a] Device Parasitics

Real devices have many parasitic (unwanted) properties. Let’s look at this basic inductor model.

[![](https://substackcdn.com/image/fetch/$s_!pP-F!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa49d459e-0a9c-4ce4-ab79-f3a8e7eff1c7_816x1273.png)](https://substackcdn.com/image/fetch/$s_!pP-F!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa49d459e-0a9c-4ce4-ab79-f3a8e7eff1c7_816x1273.png)

 **Accurate and detailed modeling of parasitic behaviors for each standard cell in a PDK is critical to enabling successful design efforts.**

[![](https://substackcdn.com/image/fetch/$s_!ULtV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc4c14472-50e3-4e03-9cf5-b29b86f51b26_1566x931.png)](https://substackcdn.com/image/fetch/$s_!ULtV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc4c14472-50e3-4e03-9cf5-b29b86f51b26_1566x931.png)

[![](https://substackcdn.com/image/fetch/$s_!YCfZ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2e0e6442-994e-4cf4-9a4b-56dbabc54370_590x828.png)](https://substackcdn.com/image/fetch/$s_!YCfZ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2e0e6442-994e-4cf4-9a4b-56dbabc54370_590x828.png)

[![](https://substackcdn.com/image/fetch/$s_!cLZG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F12701db0-20f0-44fc-a415-3d07436eca36_933x672.png)](https://substackcdn.com/image/fetch/$s_!cLZG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F12701db0-20f0-44fc-a415-3d07436eca36_933x672.png)

[![](https://substackcdn.com/image/fetch/$s_!0pKC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0fbf07a0-7892-4501-9323-42ded72b0c30_834x1076.png)](https://substackcdn.com/image/fetch/$s_!0pKC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0fbf07a0-7892-4501-9323-42ded72b0c30_834x1076.png)

A basic inverter chain and it’s time-domain response accounting for basic parasitic properties.

[![](https://substackcdn.com/image/fetch/$s_!Rz2V!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F01af5b04-276e-49c8-8c48-9712b0995caa_1555x520.png)](https://substackcdn.com/image/fetch/$s_!Rz2V!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F01af5b04-276e-49c8-8c48-9712b0995caa_1555x520.png)

[![](https://substackcdn.com/image/fetch/$s_!2gxv!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdbdec9bc-b9fd-4acc-8934-71e5d29b14dc_1545x631.png)](https://substackcdn.com/image/fetch/$s_!2gxv!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdbdec9bc-b9fd-4acc-8934-71e5d29b14dc_1545x631.png)

A more complex model of cascaded inverter parasitics…

[![](https://substackcdn.com/image/fetch/$s_!iOdb!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F20249eb6-0252-4f80-82a2-d8eec53d6887_792x415.png)](https://substackcdn.com/image/fetch/$s_!iOdb!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F20249eb6-0252-4f80-82a2-d8eec53d6887_792x415.png)

[![](https://substackcdn.com/image/fetch/$s_!FdEn!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F08a81b6f-9307-4615-bce8-a53d6937c504_275x318.png)](https://substackcdn.com/image/fetch/$s_!FdEn!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F08a81b6f-9307-4615-bce8-a53d6937c504_275x318.png)

[![](https://substackcdn.com/image/fetch/$s_!Pnbq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbc397a6c-d1d2-4119-8931-83bc08c24ecf_879x374.png)](https://substackcdn.com/image/fetch/$s_!Pnbq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbc397a6c-d1d2-4119-8931-83bc08c24ecf_879x374.png)

* * *

Even something as simple as a capacitor has parasitic that dramatically change it’s behavior relative to the ideal model. At high frequencies, capacitors behave like inductors (the opposite)!

[![](https://substackcdn.com/image/fetch/$s_!BGKJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F03264127-429b-4092-867b-928fab98c51e_1625x1120.png)](https://substackcdn.com/image/fetch/$s_!BGKJ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F03264127-429b-4092-867b-928fab98c51e_1625x1120.png)An ideal capacitor would follow along the red line. Ideal capacitors do not exist in the real world.

Note the units. Parasitic inductance is three orders of magnitude smaller than the capacitance. Small parasitic properties lead to big problems.

### [6.b] Wire Network Parasitics

Wires have parasitic properties too. It’s a big problem.

[![](https://substackcdn.com/image/fetch/$s_!N0wm!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F976f0c37-944b-4d95-aaa5-2c7f22dc3905_688x867.png)](https://substackcdn.com/image/fetch/$s_!N0wm!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F976f0c37-944b-4d95-aaa5-2c7f22dc3905_688x867.png)Capacitive parasitic properties of a wire and pair of wires with respect to a ground plane.

[![](https://substackcdn.com/image/fetch/$s_!HwKv!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4fdbdc98-eb90-4a52-bdc0-c2ac279d3783_1444x623.png)](https://substackcdn.com/image/fetch/$s_!HwKv!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4fdbdc98-eb90-4a52-bdc0-c2ac279d3783_1444x623.png)

[![](https://substackcdn.com/image/fetch/$s_!Zz6l!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F90826d08-aadb-4c59-ba6b-54540b29e59e_1556x508.png)](https://substackcdn.com/image/fetch/$s_!Zz6l!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F90826d08-aadb-4c59-ba6b-54540b29e59e_1556x508.png)

[![](https://substackcdn.com/image/fetch/$s_!2uSZ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcde3d0ab-25c7-46b8-816b-a61d7ca3806f_700x927.png)](https://substackcdn.com/image/fetch/$s_!2uSZ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcde3d0ab-25c7-46b8-816b-a61d7ca3806f_700x927.png)

[![](https://substackcdn.com/image/fetch/$s_!OUDV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6a24d5b8-23aa-41e9-b272-786c12b7102d_1307x1273.png)](https://substackcdn.com/image/fetch/$s_!OUDV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6a24d5b8-23aa-41e9-b272-786c12b7102d_1307x1273.png)

### [6.c] Electromagnetic Coupling

An antenna is just a piece of metal. Wires can inadvertently become antennas.

[![](https://substackcdn.com/image/fetch/$s_!pdul!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F63812b73-1b38-40f4-8793-39e7fe9f556f_1446x638.png)](https://substackcdn.com/image/fetch/$s_!pdul!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F63812b73-1b38-40f4-8793-39e7fe9f556f_1446x638.png)

[![](https://substackcdn.com/image/fetch/$s_!LkFY!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F82b41dcb-005d-4f5e-8b8f-23321e2242e4_1359x786.png)](https://substackcdn.com/image/fetch/$s_!LkFY!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F82b41dcb-005d-4f5e-8b8f-23321e2242e4_1359x786.png)What do PCIe, Ethernet, Infiniband, DDR5, and HBM all have in common? Mutal coupling problems in silicon, package, and PCB design.

Here is a great figure on what electromagnetic coupling looks like in time-domain.

[![](https://substackcdn.com/image/fetch/$s_!NpEf!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0a769b64-b2f7-42c0-a30f-0c1c31944b0a_1454x970.png)](https://substackcdn.com/image/fetch/$s_!NpEf!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0a769b64-b2f7-42c0-a30f-0c1c31944b0a_1454x970.png)

### [6.d] Process Variation

Process nodes have intrinsic variation. 

[![](https://substackcdn.com/image/fetch/$s_!OFDd!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8e0f372d-d581-416b-ab33-aed87a61021e_975x383.png)](https://substackcdn.com/image/fetch/$s_!OFDd!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8e0f372d-d581-416b-ab33-aed87a61021e_975x383.png)

[![](https://substackcdn.com/image/fetch/$s_!1jou!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1cfd94b2-bcb8-4783-b8cb-b656e9a0d042_1532x1209.png)](https://substackcdn.com/image/fetch/$s_!1jou!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1cfd94b2-bcb8-4783-b8cb-b656e9a0d042_1532x1209.png)

The industry standard method for determining parametric yield (how many chips are meet performance specifications) is by using process corners.

[![](https://substackcdn.com/image/fetch/$s_!y2SR!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F77f406b5-9f7b-41a1-8db2-52091fbcbb7a_728x796.png)](https://substackcdn.com/image/fetch/$s_!y2SR!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F77f406b5-9f7b-41a1-8db2-52091fbcbb7a_728x796.png)

Designers simulate against specific process corners. Testing and tuning is done on special batches of chips (samples) that have the process corner known a-priori.

Logic Foundries run a special shuttle (batch of wafers) through the process slowly to intentionally make slow (SS), fast (FF), typical (TT), and skewed (FS/SF) parts. Specific sections of the 300mm wafer are intentionally over/under doped.

Real production wafers move thought the process steps too quickly to know which chips are what corner. 

**It is the logic foundries responsibility to provide accurate numbers that characterize the process corners of the node.**

[![](https://substackcdn.com/image/fetch/$s_!L2Os!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe1e19fac-2d0e-40d6-94b8-2e31a5b0be7d_921x988.png)](https://substackcdn.com/image/fetch/$s_!L2Os!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe1e19fac-2d0e-40d6-94b8-2e31a5b0be7d_921x988.png)

Some examples of how process variation effects various basic circuits.

[![](https://substackcdn.com/image/fetch/$s_!oO5g!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F68fadf2f-f75c-4729-ab46-0f51ae7d16a5_829x715.png)](https://substackcdn.com/image/fetch/$s_!oO5g!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F68fadf2f-f75c-4729-ab46-0f51ae7d16a5_829x715.png)

[![](https://substackcdn.com/image/fetch/$s_!zlXD!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe4e18829-73a7-45b5-bb84-33bdf502fd99_684x943.png)](https://substackcdn.com/image/fetch/$s_!zlXD!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe4e18829-73a7-45b5-bb84-33bdf502fd99_684x943.png)

### [6.e] Temperature Sensitivity

[![](https://substackcdn.com/image/fetch/$s_!0UVu!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb222af7b-4a5e-45ec-9ecf-a743ad2a1558_1203x1061.png)](https://substackcdn.com/image/fetch/$s_!0UVu!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb222af7b-4a5e-45ec-9ecf-a743ad2a1558_1203x1061.png)

Every device has a temperature response. Higher-level circuits such as amplifiers will have more pronounced sensitivity to temperature.

### [6.f] Voltage Uniformity

Distributing power evenly to tens of billions of transistors is… challenging.

An important standard concept is the power grid.

[![](https://substackcdn.com/image/fetch/$s_!fDot!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc22304a6-2771-4cd4-8e7e-a667dc3d8c68_1385x1256.png)](https://substackcdn.com/image/fetch/$s_!fDot!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc22304a6-2771-4cd4-8e7e-a667dc3d8c68_1385x1256.png)

A chip will have many power and ground input bumps. Internally, these bumps get shorted into a grid.

[![](https://substackcdn.com/image/fetch/$s_!nFiT!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5c6b0ef1-68d7-4051-8543-086cd5fbebe3_870x840.png)](https://substackcdn.com/image/fetch/$s_!nFiT!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5c6b0ef1-68d7-4051-8543-086cd5fbebe3_870x840.png)

There will always be variation. It must be carefully managed. If one sub-block of a SoC does not get enough voltage, you have a problem. The only easy way to fix is to boost input voltage to everything connected to the same supply rail.

 _(designs often have internal tuning registers to boost particular sub-circuits)_

Additionally, the input DC power supply is never true DC. There is always some noise and voltage ripple.

[![](https://substackcdn.com/image/fetch/$s_!9TzL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F24d4ffc4-3580-49f7-9057-9ea3e8d7e0ec_1333x974.png)](https://substackcdn.com/image/fetch/$s_!9TzL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F24d4ffc4-3580-49f7-9057-9ea3e8d7e0ec_1333x974.png)

Circuits must be designed to handle supply noise.

### [6.g] Electromigration

Electromigration is how semiconductors degrade over time. Higher voltage and higher temperature accelerate the process.

[![](https://substackcdn.com/image/fetch/$s_!P_91!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6a314f27-4af5-4f86-b1f5-29323725e6c2_967x854.png)](https://substackcdn.com/image/fetch/$s_!P_91!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6a314f27-4af5-4f86-b1f5-29323725e6c2_967x854.png)

Intuitively, electromigration leads to the following types of example failures:

  * Transistor stuck in on or off state.

  * Capacitor degraded. (can’t hold enough charge)

  * Wire thinning leading to signal integrity issues.




All those Intel 13th and 14th generation failures you may have heard about on the news are electromigration failures. Industry standard is to design and test chips such that they survive 10 years in normal operation.

Intel 13th and 14th generation (Raptor Lake) chips survive for 6-12 months. The excuses Intel has publicly stated like “oh we messed up microcode” and there is “unintended excessive voltage” are bullshit.

There exists a standardized test that is grunted to catch these kind of problems. It takes ~2 months and costs < $50K per design. 

<https://en.wikipedia.org/wiki/High-temperature_operating_life>

**Intel Products skipping HTOL testing (to save less than $100K in NRE) is their own fault. There is no excuse for such incompetence.**

### [6.h] Leakage and Noise

Transistors are never truly off. There will always be some leakage. (unwanted power draw)

This leakage also acts as noise for the rest of the circuit.

All devices have intrinsic noise which must be modeled by the logic foundry in the PDK.

<https://en.wikipedia.org/wiki/Johnson%E2%80%93Nyquist_noise>

[![](https://substackcdn.com/image/fetch/$s_!T2NA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8545bc18-62ab-4bbf-86d0-9ffa9d199aa1_635x456.png)](https://substackcdn.com/image/fetch/$s_!T2NA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8545bc18-62ab-4bbf-86d0-9ffa9d199aa1_635x456.png)

Thermal noise is typically gaussian.

[![](https://substackcdn.com/image/fetch/$s_!ESSe!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7df61fb7-c394-455c-8f38-3cdc5776b574_271x233.png)](https://substackcdn.com/image/fetch/$s_!ESSe!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7df61fb7-c394-455c-8f38-3cdc5776b574_271x233.png)

### [6.i] Detailed Example: Capacitors

To bring all of the practical issues together, I found this delightful blog post from Ansys.

<https://www.ansys.com/blog/difference-between-mom-mim-mos-capacitor>

As an exercise to the reader, please click on the link and try to read/understand for yourself. 

[![](https://substackcdn.com/image/fetch/$s_!2jmX!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd1c2e38c-4bce-470e-b874-b88706531aa9_680x923.png)](https://substackcdn.com/image/fetch/$s_!2jmX!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd1c2e38c-4bce-470e-b874-b88706531aa9_680x923.png)

For the lazy, there are three main ways of building a capacitor. 

There are tradeoffs.

## [7] Design-Technology Co-Optimization (DTCO)

[![](https://substackcdn.com/image/fetch/$s_!xe2b!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb9416659-d717-45ef-a257-4d0826813d34_1372x634.png)](https://substackcdn.com/image/fetch/$s_!xe2b!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb9416659-d717-45ef-a257-4d0826813d34_1372x634.png)

Nvidia talks about how their chips are built on a TSMC “4N” process node. This is not a typo.

Large companies like Nvidia and AMD engage in “design-technology co-optimization”. Essentially, they ask the logic foundry (TSMC) for customizations.

Examples of possible customizations:

  * Alternative metal stackup. (typically, more/fewer layers)

  * Custom cells. 

  * Relaxed design rules.

  * Shifts in process to skew or move corners.




[![](https://substackcdn.com/image/fetch/$s_!KGSR!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2ac31cd4-e11a-4b4a-a42b-68d3bbfbdba3_628x329.webp)](https://substackcdn.com/image/fetch/$s_!KGSR!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2ac31cd4-e11a-4b4a-a42b-68d3bbfbdba3_628x329.webp)

[![](https://substackcdn.com/image/fetch/$s_!zdWT!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcf9162ab-9d9e-4b9f-82bd-4855b275ec59_2698x1454.png)](https://substackcdn.com/image/fetch/$s_!zdWT!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcf9162ab-9d9e-4b9f-82bd-4855b275ec59_2698x1454.png)

## [8] Derivative Nodes

If you look at TSMC financial statements, there are some nodes missing.

[![](https://substackcdn.com/image/fetch/$s_!CKNk!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0853c22d-df90-41da-9b8e-0a07bdca2ada_1514x818.png)](https://substackcdn.com/image/fetch/$s_!CKNk!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0853c22d-df90-41da-9b8e-0a07bdca2ada_1514x818.png)

Where are N6 and N4?

Logic Foundry process node names are mostly marketing nonsense these days. The “nanometer” designation is detached from reality. 

The “4 nanometer” node is not 20% smaller or better than the “5 nanometer” node. Derivative nodes like TSMC N7P, N6, N5P, N4, and N4P are minor updates to the parent node.

[![](https://substackcdn.com/image/fetch/$s_!AJE3!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8f86dc7a-37d4-4320-a337-b86798edc2ae_1000x470.jpeg)](https://substackcdn.com/image/fetch/$s_!AJE3!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8f86dc7a-37d4-4320-a337-b86798edc2ae_1000x470.jpeg)Original TSMC N3 (N3B) failed. The N3 we know today is N3E, a completely different node. **In other words, N3B and N3E are not derivative nodes.** However, N3P and N3X are both derivative nodes of N3E.

Three common tactics:

  1. A low-single-digit lithography mask shrink.

  2. Updated (better characteristics) standard cells in the PDK.

  3. Relaxed design rules.




Intel’s roadmap also includes several derivative nodes.

[![](https://substackcdn.com/image/fetch/$s_!Av26!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8cffac9c-beb7-4270-9c45-562cb66698f8_3245x1864.png)](https://substackcdn.com/image/fetch/$s_!Av26!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8cffac9c-beb7-4270-9c45-562cb66698f8_3245x1864.png)

Intel 3 is a derivative of Intel 4.

 **Intel 18A is a derivative of Intel 20A. This is very important and will be explained in-depth later.**

As an aside, the public power/performance/area improvements publicly disclosed by logic foundries tend to be optimistic. Real designs do not get such significant improvements.

## [9] Library Managment

Given the complexity of modern semiconductors, it is critical for logic foundries and design companies to manage IP (intellectual property) libraries.

Examples of IP in this context:

  * Standard low-level device cells.

    * Transistor libraries, RLC devices, via geometries, …

    * Can be from the foundry (PDK) or custom made (DTCO).

  * Low-level circuits.

    * PLL, SRAM, accumulator, DAC/ADC, ALU sub-units

  * High-level blocks.

    * Network on Chip (NoC) nodes

    * Branch Predictor

    * SerDes

    * Memory Controller

    * ALU/FPU core

    * CPU/GPU/XPU/ASIC Core

    * …




Typically, teams are structured in a “divide and contour” organization. It is common for individual teams to have no idea what the other groups are working on. 

For very large projects, a centralized organization (let’s call them the SoC team) is responsible for taking IP block deliveries from all other groups and stitching them together into a target product.

How the centralized team interacts with other departments depends on company culture.

Some companies have back-and-forth between central team and sub-unit teams.

Sometimes the sub-unit teams deliver blocks at a hard deadline and do not really interact much with the centralized team, outside of occasional consultation.

Sometimes the overall team is so small that distinct separation within a discipline is unnecessary. For example, a unified digital team, a separate analog team (that also handles large portions of physical design), and a mask/layout team. 

Regardless of the chosen structure, all teams must carefully organize IP libraries for future designs and ports to other process nodes. **The semiconductor industry relies heavily on re-use of work.**

In general, work can be re-used to an extent so long as nothing drastic changes.

Transistor geometry changes (planar —> FinFet —> Gate-all-Around) and innovations like backside power delivery are examples of _“oh we have to re-do everything…”_ technologies.

[![](https://substackcdn.com/image/fetch/$s_!fF31!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F10cb0c58-46e1-4398-8577-a1ede35c0ce2_936x270.webp)](https://substackcdn.com/image/fetch/$s_!fF31!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F10cb0c58-46e1-4398-8577-a1ede35c0ce2_936x270.webp)

 **Derivative nodes are very nice because they give great return on investment.**

A modest amount of R&D effort translates into pretty good improvements. 

It’s asymmetric.

## [10] Simulations: Garbage In? Garbage Out!

A very over-simplified view of a Process Development Kit is that it’s just a bunch of numbers.

These numbers act as inputs into EDA simulations.

[![](https://substackcdn.com/image/fetch/$s_!9P-Y!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcc9ffd57-42e2-4123-ab3c-6b62f41c1e2e_963x928.png)](https://substackcdn.com/image/fetch/$s_!9P-Y!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcc9ffd57-42e2-4123-ab3c-6b62f41c1e2e_963x928.png)

If the numbers are garbage, then the simulator will output garbage.

[![](https://substackcdn.com/image/fetch/$s_!54H6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7d9270fc-601f-4c09-816d-27dbe94707a1_1448x901.png)](https://substackcdn.com/image/fetch/$s_!54H6!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7d9270fc-601f-4c09-816d-27dbe94707a1_1448x901.png)

[![](https://substackcdn.com/image/fetch/$s_!34t8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F279ad9f7-a7b0-493b-984e-ed00af482fc7_1456x890.png)](https://substackcdn.com/image/fetch/$s_!34t8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F279ad9f7-a7b0-493b-984e-ed00af482fc7_1456x890.png)I love it when AI inserts random shit that no human would add. It’s charming.

Theoretically, how can a PDK be garbage?

  * The numbers are lies. (intentionally wrong)

  * The numbers have very high variation.

  * Some numbers are missing, and **entire categories of devices are modeled as ideal.**

    * 🤡🤡🤡🤡🤡

    * 🙈🙈🙈🙈🙈

    * 🙊🙊🙊🙊🙊




Certain companies think that hiding information under aggressive NDA will protect them from catastrophic failure. 

[![](https://substackcdn.com/image/fetch/$s_!l_Dn!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2b33b68b-4720-481a-8701-a2e275551785_396x300.jpeg)](https://substackcdn.com/image/fetch/$s_!l_Dn!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2b33b68b-4720-481a-8701-a2e275551785_396x300.jpeg)

## [11] Bump-Out (Packaging)

[![](https://substackcdn.com/image/fetch/$s_!xtgc!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd4fd31f7-8e94-4887-851e-74f7524da279_1024x361.webp)](https://substackcdn.com/image/fetch/$s_!xtgc!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd4fd31f7-8e94-4887-851e-74f7524da279_1024x361.webp)

Regardless of the intended packaging, from complex CoWoS-L to basic ABF substrate, every chip needs a bump-out. Rules and specifications on where power, ground, and signal pads are.

[![](https://substackcdn.com/image/fetch/$s_!eacV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcbcfbd9d-f66b-41c1-996e-2c4def49752b_224x224.jpeg)](https://substackcdn.com/image/fetch/$s_!eacV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcbcfbd9d-f66b-41c1-996e-2c4def49752b_224x224.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!y6DL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F63db58dc-8d65-4b5b-ad06-3f09237243af_1902x690.jpeg)](https://substackcdn.com/image/fetch/$s_!y6DL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F63db58dc-8d65-4b5b-ad06-3f09237243af_1902x690.jpeg)

This is more difficult that it might initially seem. 

  * Power and ground need to be evenly distributed across the chip.

  * Signal wires need to be surrounded by ground to maintain signal integrity.

  * If too many power bumps are near each other, there will be a hot-spot.

    * Chip could overheat.

    * Warpage of the package and silicon (not same thermal coefficient) can result in the chip de-soldering itself.




Nvidia has had two run-in with bump-out related failures.

  1. A long time ago, Nvidia made a laptop GPU that failed due to hot-spots.

    1. To this day, Apple holds a grudge against Nvidia because of this fiasco.

    2. Nvidia was sued and paid very low compensation to laptop OEMs.

  2. Blackwell was delayed due to some bump-related issue.

    1. Issue was due to aggressive timeline and adoption of CoWoS-L on Nvidia’s first chiplet design.

    2. The upper 6 metal layers of the Blackwell logic die needed to be re-worked to re-arrange the micro-bumps.




Because bump-out is standard PDK information, companies are almost always allowed to…

  * Design their own package.

  * Choose which company (usually 3rd party) manufactures the package.

  * Choose which company (usually 3rd party) does the packaging. (places dice on package)




This is how the industry normally operates.

[![](https://substackcdn.com/image/fetch/$s_!XfgT!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4739fe73-0655-47a9-9e60-466ea9214cf7_450x453.jpeg)](https://substackcdn.com/image/fetch/$s_!XfgT!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4739fe73-0655-47a9-9e60-466ea9214cf7_450x453.jpeg)

It’s almost as if insisting on non-standard workflows will lead to inefficiency, unnecessary risk, and future disasters.

[![](https://substackcdn.com/image/fetch/$s_!18gy!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fecd93d23-f31a-48d4-b7c7-1392088d4a5e_1151x616.jpeg)](https://substackcdn.com/image/fetch/$s_!18gy!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fecd93d23-f31a-48d4-b7c7-1392088d4a5e_1151x616.jpeg)

## [12] Overview of the three leading-edge logic foundries.

[![](https://substackcdn.com/image/fetch/$s_!J3vx!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F90ea2ad7-cd5b-4a75-bd7a-4faf7757e5c4_471x1110.png)](https://substackcdn.com/image/fetch/$s_!J3vx!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F90ea2ad7-cd5b-4a75-bd7a-4faf7757e5c4_471x1110.png)

Here is an updated positions list so you know my biases.

I own a lot of TSMC shares at the time of writing.

 **Am I still going to own these shares ten years from now? Absolutely not.**

 **Am I still going to own these shares two years from now? Almost certainly.**

[![](https://substackcdn.com/image/fetch/$s_!O6az!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe60083b5-03a0-49da-b59d-d287d273ddca_1473x911.png)](https://substackcdn.com/image/fetch/$s_!O6az!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe60083b5-03a0-49da-b59d-d287d273ddca_1473x911.png)

TSMC stock trades at a very low Price/Earnings multiple. This is the market pricing in the risk of an involuntary merger with SMIC.

* * *

Samsung Foundry is such a disaster, I don’t want to bother writing about them. 

There is no hope.

[![](https://substackcdn.com/image/fetch/$s_!C6qi!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5b92c718-947a-41d8-8aa6-9a9368e409cb_415x416.png)](https://substackcdn.com/image/fetch/$s_!C6qi!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5b92c718-947a-41d8-8aa6-9a9368e409cb_415x416.png)

Spend 15 minutes Google searching “Samsung yield”. Plenty of material is online from the past 7 years.

* * *

Intel is where I have to engage in some NDA-mandated memes.

I cannot write about many topics. However, public statements from Intel and public rumors are fair game. Nothing prevents me from talking about the news and chiming in with funny pictures.

[![Brief Intel 18A Yield Note](https://substackcdn.com/image/fetch/$s_!BNsT!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc91733fc-6539-4fa9-8c33-39345cb0bcff_736x482.jpeg)

#### Brief Intel 18A Yield Note

[Irrational Analysis](https://substack.com/profile/135313705-irrational-analysis)·December 8, 2024[Read full story](https://irrationalanalysis.substack.com/p/brief-intel-18a-yield-note)](https://irrationalanalysis.substack.com/p/brief-intel-18a-yield-note)

Please go check out my (1 month old) note on 18A and the rumored 10% yields of Intel Products Panther Lake CPU chiplet/tile, built on Intel 18A. 

_At the time, I did not have enough spare cycles to write up a detailed explanation of PDKs. This post is what I wish I could have written back then._ :)

[![](https://substackcdn.com/image/fetch/$s_!YnG0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0744c2f3-19ae-40f0-83cf-34a696bfcfd9_1151x577.png)](https://substackcdn.com/image/fetch/$s_!YnG0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0744c2f3-19ae-40f0-83cf-34a696bfcfd9_1151x577.png)If something is falling off a cliff and accelerating to terminal velocity, that counts as momentum… right? <https://www.intel.com/content/www/us/en/newsroom/opinion/continued-momentum-intel-18a.html>

[![](https://substackcdn.com/image/fetch/$s_!mPVC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0dff659d-f996-4c3e-a99c-0745c1edbcd8_884x304.png)](https://substackcdn.com/image/fetch/$s_!mPVC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0dff659d-f996-4c3e-a99c-0745c1edbcd8_884x304.png)I WONDER WHY INTEL PROCLAIMED EVERYTHING IS FINE AND 18A D0 IS SO GOOD THAT 20A IS CANCLED ON **THE SAME DAY** INCREDIBLY DAMAGING NEWS WAS PUBLISHED BY REUTERS. <https://www.reuters.com/technology/intel-manufacturing-business-suffers-setback-broadcom-tests-disappoint-sources-2024-09-04/>

I find it immensely entertaining that the name of the Intel executive who had to put out a press release in response to Reuters reporting has the last name of “Sell”.

An Intel VP literally named “Sell” told you all you need to know. 🤣

There are two key factual claims Mr. Sell wrote on September 4th, 2024:

  1. 20A is canceled and this is actually good news!

  2. 18A, a derivative node, is yielding well with a defect density (D0) of < 0.4.




[![](https://substackcdn.com/image/fetch/$s_!2KEd!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffba5cbbc-fdaf-42d0-95de-fc6da18cdd91_813x838.png)](https://substackcdn.com/image/fetch/$s_!2KEd!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffba5cbbc-fdaf-42d0-95de-fc6da18cdd91_813x838.png)

Executive officers (VP and above) of publicly traded companies cannot intentionally lie in public statements to investors. 

[![](https://substackcdn.com/image/fetch/$s_!qJ-S!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3ec5d6e6-d6aa-4df2-b8d7-417aa434dbe4_981x497.png)](https://substackcdn.com/image/fetch/$s_!qJ-S!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3ec5d6e6-d6aa-4df2-b8d7-417aa434dbe4_981x497.png)To be clear, the investors suing Gelsinger and Zinsner are retarded clowns. They don’t deserve a penny. Do some due diligence next time, idiots. <https://news.bloomberglaw.com/litigation/intel-officers-ex-ceo-sued-over-market-dip-after-reorganization>

**Therefore, we have to assume that the 0.4 D0 claim is true. Presumably, Mr. Sell does not want to get sued. This is exactly the kind of claim that can EASILY be proven true/false in the discovery process.**

This does not mean 18A (derivative node) is going well! Cancelation of 20A (parent node) strongly indicates that the entire node family is busted.

The following three statements can all be simultaneously true. 

  1. 18A D0 is < 0.4

  2. Parametric yield on the entire 20A/18A node family is really bad.

  3.  **Rumor that Panther Lake CPU tile/chiplet on 18A has 10% overall yield.**




 **These statements are not mutually exclusive.**

 **Rumor is plausible in this case.**

 **It really can be this bad.**

 **I keep seeing technical peers in denial.**

 **This rumor is decisively within the realm of possibility.**

[![](https://substackcdn.com/image/fetch/$s_!XhzV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff2e7c7ab-3974-41dd-b223-9b70baf1e667_762x130.png)](https://substackcdn.com/image/fetch/$s_!XhzV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff2e7c7ab-3974-41dd-b223-9b70baf1e667_762x130.png)[Please read my older post to understand where these numbers are coming from.](https://irrationalanalysis.substack.com/p/brief-intel-18a-yield-note)

[![](https://substackcdn.com/image/fetch/$s_!zmpy!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe96e6422-37bb-49a2-8e47-027f2cbdc07d_854x964.png)](https://substackcdn.com/image/fetch/$s_!zmpy!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe96e6422-37bb-49a2-8e47-027f2cbdc07d_854x964.png)

Subscribe for engineering-driven investment analysis.

Subscribe

Share?

[Share](https://irrationalanalysis.substack.com/p/a-background-proof-guide-on-process?utm_source=substack&utm_medium=email&utm_content=share&action=share)

Regarding the rumors that some combination of Elon Musk, GloFo, Broadcom, Qualcomm, and Broadcom is trying to buy parts of intel… I have no fucking idea.

We really are on the spiciest timeline.

[![the spiciest timeline, cyberpunk](https://substackcdn.com/image/fetch/$s_!IskJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5026e4fe-ecdf-4a31-89a2-f387f0961acf_1024x1024.jpeg)](https://substackcdn.com/image/fetch/$s_!IskJ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5026e4fe-ecdf-4a31-89a2-f387f0961acf_1024x1024.jpeg)
