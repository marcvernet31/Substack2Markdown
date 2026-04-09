# The Astera Labs Extinction Event

## There is no moat.

**Mar 10, 2024**

**Likes:** 0

# IMPORTANT:

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Please check the [‘about’ page](https://irrationalanalysis.substack.com/about) for a list of active positions.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice and readers should **always do their own research before investing in any security.**




* * *

Hello wonderful subscribers. Astera Labs is a connectivity company that is trying to go public on the AI wave. Recently, Broadcom made [an announcement](https://www.servethehome.com/broadcom-fires-a-shot-at-astera-labs-and-more-with-new-pcie-and-cxl-retimers/) that I view as nothing less than apocalyptic for Astera Labs.

This is an interesting short opportunity. 

# Contents:

  1. What does Astera Labs do?

  2. Technical Background

    1. SerDes

    2. PCB Stackup

    3. Signal Integrity

    4. Loss, Reflections, and DFE

    5. Jitter, CDR Bandwidth, and Adaptation

  3. Broadcom’s Killing Blow

  4. There is no moat.




* * *

### [1] What does Astera Labs do?

[![](https://substackcdn.com/image/fetch/$s_!DGUU!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8321c3cb-b692-4c32-ad77-7fc96d0d8648_1270x820.png)](https://substackcdn.com/image/fetch/$s_!DGUU!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8321c3cb-b692-4c32-ad77-7fc96d0d8648_1270x820.png)

They make small “extender” chips which are often referred to as retimers. 

[![](https://substackcdn.com/image/fetch/$s_!2oHq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F11bbbddb-2579-4c91-8a5d-cecacd58fb17_925x953.png)](https://substackcdn.com/image/fetch/$s_!2oHq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F11bbbddb-2579-4c91-8a5d-cecacd58fb17_925x953.png)

These retimers enable new design topologies via extended reach and also lower costs by enabling cheaper PCB materials.

[![](https://substackcdn.com/image/fetch/$s_!4VnQ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F999db6d2-74c9-475d-b85e-f90c45bf0542_784x164.png)](https://substackcdn.com/image/fetch/$s_!4VnQ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F999db6d2-74c9-475d-b85e-f90c45bf0542_784x164.png)

[![](https://substackcdn.com/image/fetch/$s_!A8oK!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff23af181-1fa6-4b1b-aa77-01f4a6c0b94e_851x393.png)](https://substackcdn.com/image/fetch/$s_!A8oK!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff23af181-1fa6-4b1b-aa77-01f4a6c0b94e_851x393.png)

[![](https://substackcdn.com/image/fetch/$s_!kGIX!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9de4deb8-981a-47f0-bad2-edacf23e53d1_858x1124.png)](https://substackcdn.com/image/fetch/$s_!kGIX!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9de4deb8-981a-47f0-bad2-edacf23e53d1_858x1124.png)

Astera Labs S-1 filing and public marketing really loves to highlight their COSMS software management system. “Software-Defined” gets thrown in over and over again to dupe dumb investors. This is not a SaaS business. **There is no competitive moat.**

### [2] Technical Background

To understand the antihalation Broadcom has wrought upon Astera Labs, you must first understand some technical terms. 

#### [2.a] SerDes

SerDes is shorthand for “serializer-deserializer”. USB, HDMI, Ethernet and PCIe are all examples of SerDes. Each protocol has it’s own electrical specification alongside upper-layer operations. For example, CXL has the exact same electrical specification as PCIe. This means CXL is really just an upper layer protocol built on top of the PCIe physical layer.

Currently, there are two main types of SerDes, NRZ and PAM4.

[![](https://substackcdn.com/image/fetch/$s_!Q8sf!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe10ef0ba-8db3-4431-aac2-ba2fbac97720_755x343.png)](https://substackcdn.com/image/fetch/$s_!Q8sf!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe10ef0ba-8db3-4431-aac2-ba2fbac97720_755x343.png)

NRZ sends one bit per symbol. 

PAM4 sends two bits. 00, 01, 10, or 11, depending on the voltage.

PCIe 5 and older uses NRZ while PCIe 6 uses PAM4.

Ethernet made the jump from NRZ to PAM4 around the 100GbE module to 400GbE module generation.

[![](https://substackcdn.com/image/fetch/$s_!nSwI!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdb6e88e1-3775-4390-8ba6-d6c4944d49c7_2048x966.webp)](https://substackcdn.com/image/fetch/$s_!nSwI!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdb6e88e1-3775-4390-8ba6-d6c4944d49c7_2048x966.webp)

There was some talk that 224G electrical (for 1.6TbE modal) Ethernet SerDes would need to use PAM6 but the standards body (IEEE) decided to stay on PAM4.

A tradeoff exists between modulation order and system bandwidth.

#### [2.b] PCB Stackup

[![](https://substackcdn.com/image/fetch/$s_!jAkF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6677cdfe-b7c6-4ed6-877b-f1400c31e7d9_1448x1032.jpeg)](https://substackcdn.com/image/fetch/$s_!jAkF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6677cdfe-b7c6-4ed6-877b-f1400c31e7d9_1448x1032.jpeg)

Printed circuit boards (PCBs) are manufactured much like semiconductors except there is no metal deposition. Each “core” consists of a dielectric sandwiched between two solid copper layers. Photomask, lithography, and etch are all applied. Then a “prepreg” layer is added on top before continuing. 

The Prepreg can be the same material as the core dielectric or something thicker/thinner/cheaper. Depends on the design.

It is standard industry practice to have all high-speed SerDes (PCIe, Ethernet) on the same layer of a PCB. Expensive materials used on that layer only.

Modern high-end PCBs can have 12-20 metal layers.

#### [2.c] Signal Integrity

[![](https://substackcdn.com/image/fetch/$s_!luq5!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6d5cb865-392f-4e91-ab34-82777da28c8b_1280x720.jpeg)](https://substackcdn.com/image/fetch/$s_!luq5!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6d5cb865-392f-4e91-ab34-82777da28c8b_1280x720.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!O1ya!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6031e4e0-60b1-491e-80cd-c733ba846a60_768x383.png)](https://substackcdn.com/image/fetch/$s_!O1ya!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6031e4e0-60b1-491e-80cd-c733ba846a60_768x383.png)

[![](https://substackcdn.com/image/fetch/$s_!PErD!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fccb68c1b-4512-4f14-be15-3c9214efea12_1002x519.jpeg)](https://substackcdn.com/image/fetch/$s_!PErD!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fccb68c1b-4512-4f14-be15-3c9214efea12_1002x519.jpeg)Notice how a lot of traces have wiggles to intentionally lengthen the run.

[![](https://substackcdn.com/image/fetch/$s_!MY06!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Febe963f6-d5d5-42d1-9e7f-a26a3b0c2152_320x217.jpeg)](https://substackcdn.com/image/fetch/$s_!MY06!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Febe963f6-d5d5-42d1-9e7f-a26a3b0c2152_320x217.jpeg)

Signal integrity is a very important aspect of board design. Often, there are dedicated engineers who only handle signal integrity, nothing else. Differential traces need precise impedance matching. Load capacitance and impedance of devices need to be modeled. Traces can easily interfere with one another, ruining a design if simulations are not checked properly.

Additionally, the skin effect makes everything much more difficult for high-speed (PCIe, Ethernet) signals. Most of the energy ends up going on the surface of each trace. This means most of the copper metal is not accomplishing much other than providing structural rigidity.

#### [2.d] Loss, Reflections, CTLE, and DFE

Marketing materials for SerDes often quote loss tolerance. A lot more goes into the quality of a SerDes than just loss.

Each type of material induces some amount of loss, measured in (dB). PCB, cables, connectors, and so on. 

[![](https://substackcdn.com/image/fetch/$s_!Xmzv!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F50368929-6615-43dd-830d-bbe882e6c0c2_650x400.jpeg)](https://substackcdn.com/image/fetch/$s_!Xmzv!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F50368929-6615-43dd-830d-bbe882e6c0c2_650x400.jpeg)

Insertion loss is really a measurement across frequency. The numbers that get quoted are loss at Nyquist. Faster SerDes use more bandwidth and thus have a higher Nyquist frequency.

The smoothness of a channel is important. Bad materials/cables/connectors can cause unnecessary reflections.

[![](https://substackcdn.com/image/fetch/$s_!mygE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F98139761-7ebd-4e77-8ad7-e21efbb06f54_1004x606.jpeg)](https://substackcdn.com/image/fetch/$s_!mygE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F98139761-7ebd-4e77-8ad7-e21efbb06f54_1004x606.jpeg)

Every time an electrical signal moves to a new medium, some of the energy is reflected backwards. Reflections cause problems for the receiver which must be corrected by some form of equalization/filtering.

Because PCIe spec cares a lot about latency, they do not use digital filtering aka post-ADC FFE. Ethernet places a strong emphasis on digital FIR filtering.

[![](https://substackcdn.com/image/fetch/$s_!0FrJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc62dcdaf-ed4a-4641-bfc8-742a31bba527_1766x1268.png)](https://substackcdn.com/image/fetch/$s_!0FrJ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc62dcdaf-ed4a-4641-bfc8-742a31bba527_1766x1268.png)

CTLEs are analog circuits that adjust the gain and shape of the incoming signal. Very powerful but very painful to tune, calibrate, and maintain in mission mode.

For example, suppose a link is established when the silicon is at 60C. As the chip warms up to say 110C, the CTLE response changes dramatically, requiring live tuning by firmware.

[![](https://substackcdn.com/image/fetch/$s_!jlAT!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd3b97588-3b49-437a-8fac-f5376bde15d1_1358x916.png)](https://substackcdn.com/image/fetch/$s_!jlAT!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd3b97588-3b49-437a-8fac-f5376bde15d1_1358x916.png)

[![](https://substackcdn.com/image/fetch/$s_!vDs6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F63e8d378-8c35-44d8-84e0-bda32994d5ad_1362x985.png)](https://substackcdn.com/image/fetch/$s_!vDs6!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F63e8d378-8c35-44d8-84e0-bda32994d5ad_1362x985.png)

DFE’s are a type of non-linear analog filter. Not quite like a digital IIR filter because of the conditional blocks. 

Often, SerDes include extra DFE coefficients for resilience. A higher-quality SerDes (such as Broadcom’s) can turn off some of the DFE coefficients because there is less junk for the receiver to clean up. This saves a lot of power.

#### [2.e] Jitter, Adaptation, and CDR Bandwidth

[![](https://substackcdn.com/image/fetch/$s_!o1yq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F05e3016a-9680-48da-b1d7-13635c7d6691_610x523.gif)](https://substackcdn.com/image/fetch/$s_!o1yq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F05e3016a-9680-48da-b1d7-13635c7d6691_610x523.gif)

Jitter is an industry term for time-domain noise. There are many types and sources of jitter but I want to keep this simple.

The problem with jitter is when it changes after the link is already up. Suppose you have a PCIe link between a CPU and a GPU. All is well until a neighboring PCIe storage device is hot-plugged in and starts dumping sinusoidal noise into neighboring lanes.

[![](https://substackcdn.com/image/fetch/$s_!g3bK!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8979be4a-6e81-4765-88df-465ea2a463b3_522x788.png)](https://substackcdn.com/image/fetch/$s_!g3bK!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8979be4a-6e81-4765-88df-465ea2a463b3_522x788.png)

SerDes include various adjustable circuits to alter the jitter rejection profile of a particular lane. How the firmware handles these situations in mission mode is very important. CDR design and tuning is a subject on it’s own.

### [3] Broadcom’s Killing Blow

Amusingly, Broadcom decided to make some [major product announcements](https://www.servethehome.com/broadcom-fires-a-shot-at-astera-labs-and-more-with-new-pcie-and-cxl-retimers/) right as Astera Labs is trying to IPO.

[![](https://substackcdn.com/image/fetch/$s_!mjai!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5b7de304-a764-4840-80c9-1ee3a588fa6f_1200x675.jpeg)](https://substackcdn.com/image/fetch/$s_!mjai!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5b7de304-a764-4840-80c9-1ee3a588fa6f_1200x675.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!ZYvE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F273c1d3d-311d-4c18-a494-9c30df5b225c_696x392.jpeg)](https://substackcdn.com/image/fetch/$s_!ZYvE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F273c1d3d-311d-4c18-a494-9c30df5b225c_696x392.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!RCaH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5cf619f8-4840-491f-be44-d4e5a168515a_951x519.png)](https://substackcdn.com/image/fetch/$s_!RCaH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5cf619f8-4840-491f-be44-d4e5a168515a_951x519.png)

I have made some minor modifications to the official Broadcom marketing slide. It is not fair for them to state Astera’s solution is > 32 dB because most references to loss within datasheets is > 36 dB. Seems like a cherry-pick. 

Regardless, they should be terrified.

Broadcom has:

  * 2/3 the power draw at Gen5 and stills wins on Gen6/PAM4 power!

    * This is plausible because of full process node advantage.

    * Also better SerDes quality enabling fewer DFE taps.

  * Drop-in PCIe Gen6 compatibility.

  * 4-9 dB of guarantied extra reach. MASSIVE!

  * Better software ecosystem.

  * Industry-leading interoperability.




### [4] There is no moat.

Astera Labs loves to hype up their COSMOS software as a major differentiator and moat. It is not either of those things.

Having an upper layer software stack to collect telemetry on CTLE settings, CDR bandwidth, DFE configuration, temperature, … and so on is normal. Broadcom’s diagnostic stack does all these things and more. 

Broadcom is the leader in PCIe network switches and NICs. Their monitoring software is industry leading.

Astera is way behind on power.

Has no PCIe 6 product.

Is way behind on link budget (loss) margin.

Is way behind on interoperability.

 **There is no competitive moat for Astera Labs because Broadcom has all the moats.**

Astera Labs has until late summer 2024 to put out a new product and try to compete in the low-end. Otherwise, everyone is going to design them out, switch to Broadcom’s retimers, and save a huge amount of money on CapEx (cheaper PCB designs, cheaper cables, cheaper connectors) and OpEx (power burn, stability/downtime),

[![](https://substackcdn.com/image/fetch/$s_!guSL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcaa3d94d-7b1e-4f45-ac8d-ea5f6d78b8c6_889x677.png)](https://substackcdn.com/image/fetch/$s_!guSL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcaa3d94d-7b1e-4f45-ac8d-ea5f6d78b8c6_889x677.png)

If you enjoyed this content, please consider subscribing.

Subscribe

Already subscribed? Thanks! Please consider sharing.

[Share](https://irrationalanalysis.substack.com/p/the-astera-labs-extinction-event?utm_source=substack&utm_medium=email&utm_content=share&action=share)
