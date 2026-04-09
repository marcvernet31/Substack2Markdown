# A Background-Proof Guide on Co-Packaged Optics

## The future of high-speed datacenter communications.

**Apr 12, 2025**

**Likes:** 0

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Please check the [‘about’ page](https://irrationalanalysis.substack.com/about) for a list of active positions.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice, and readers should **always do their own research before investing in any security.**

  * Feel free to contact me via email at: _irrational_analysis@proton.me_




* * *

Welcome to a deep-dive on co-packaged optics.

Your background is irrelevant. Everyone will be able to learn something new, even the [pod monkeys. ](https://www.wsj.com/finance/investing/millennium-israel-englander-point72-steve-cohen-appaloosa-david-tepper-7561690b)

[![monkeys wearing suits trading stocks using many monitors](https://substackcdn.com/image/fetch/$s_!WPo9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc33b8ff9-a1f9-40aa-8bb2-4512c5531dea_1024x1024.jpeg)](https://substackcdn.com/image/fetch/$s_!WPo9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc33b8ff9-a1f9-40aa-8bb2-4512c5531dea_1024x1024.jpeg)

Some basic communication systems concepts will be hand-waived in the interest of time. I want to focus on optics specifically with this post.

Read this old one if you are interested.

The material for this post was developed from three primary sources:

  1. Incredible Texas A&M Professor Sam Palermo: <https://people.engr.tamu.edu/spalermo/ecen721.html>

  2. Broadband Circuits for Optical Fiber Communication 1st Edition

by [Eduard Säckinger](https://www.amazon.com/Eduard-S%C3%A4ckinger/e/B001HMKGZE/ref=dp_byline_cont_book_1)

    1. Back in college, I was poor and usually pirated books.

    2. Now, I regularly achieve losses of $20K or more in one day in one account. 🤡🤡🤡🤡🤡

    3. Makes it much easier to treat myself to expensive $100-$300 new copies of textbooks. 🤡

  3. A variety of public research papers I found while browsing Google Scholar.




[![Cyberpunk 2077's in game opinion on NDA's : r/cyberpunkgame](https://substackcdn.com/image/fetch/$s_!V5oJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd8026179-dde6-4707-b9a3-a24ab4c8963b_646x394.png)](https://substackcdn.com/image/fetch/$s_!V5oJ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd8026179-dde6-4707-b9a3-a24ab4c8963b_646x394.png)

There will be a section at the end discussing public companies who have either developed CPO solutions or are involved in the supply-chain.

[![](https://substackcdn.com/image/fetch/$s_!44i5!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb309b9ac-2183-4485-8cc6-863aa4f983f9_1309x1312.png)](https://substackcdn.com/image/fetch/$s_!44i5!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb309b9ac-2183-4485-8cc6-863aa4f983f9_1309x1312.png)

 _ **Sidenote:**_ _I listen to a single electronic music track for hours on end while writing these long posts._ _Track changes every few weeks._

 _Open this up on a new tab, right click, and enable looping on YouTube for the full experience._

[![](https://substackcdn.com/image/fetch/$s_!ZqWa!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F98ae7bba-d2e4-4fcd-8f2e-7f6871141183_567x412.png)](https://substackcdn.com/image/fetch/$s_!ZqWa!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F98ae7bba-d2e4-4fcd-8f2e-7f6871141183_567x412.png)

Let’s get started.

* * *

# Contents:

  1. The Channel Problem

    1. Electrical Channel Examples

    2. Optical Channels are Amazing

    3. Narrowband Carrier Waves: An Intuitive Approach

    4. Linearity and Differential Signaling 

  2. Light Sources (Lazer go pew pew pew)

  3. Photodetectors

  4. Modulators

    1. Direct Modulation (laser input current wiggles)

    2. External Modulation (constant laser output is wiggled later)

      1. Electroabsorption

      2. Mach-Zehnder (MZM)

      3. Micro-Ring Resonators (MRM)

  5. Two Tribes and a False Choice

  6. Electrical Periphery: TIA and all that

  7. Incorrect Obsession with Silicon “Beachfront/Shoreline”

  8. Photonic Process Nodes

  9. Walkthrough: Nvidia Quantum-X GTC 2025 Announcement

  10. Walkthrough: Broadcom Hot Chips 2024 Baily Presentation

  11. Public Market Investment Corner

    1. Transceiver Exposed Companies are Fucked

    2. oDSP Exposed Companies also Fucked (COUGH COUGH MARVELL)

    3. CPO Developers: Nvidia, Broadcom, and Marvell

    4. Laser Manufacturers: Lumentum and Coherent

    5. Outsourced Assembly: Fabrinet (is better than everyone else)

    6. Glass: Corning and Nittobo

    7. Fabs: TSMC War Against GloFo and Tower Semi




* * *

## [1] The Channel Problem

Every communication system has a channel that sits between the transmitter and the receiver.

[![](https://substackcdn.com/image/fetch/$s_!_v_3!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F68dfbc94-ba8a-4c91-ad4f-28b07f14d6cd_688x331.png)](https://substackcdn.com/image/fetch/$s_!_v_3!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F68dfbc94-ba8a-4c91-ad4f-28b07f14d6cd_688x331.png)

It could be air, copper, optical fiber, or a string between two tin cans.

[![](https://substackcdn.com/image/fetch/$s_!W8U5!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe4871e26-b938-423b-a443-37c747e39aa3_304x166.png)](https://substackcdn.com/image/fetch/$s_!W8U5!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe4871e26-b938-423b-a443-37c747e39aa3_304x166.png)

Math abstracts the attributes of a communication channel. The most important of which is frequency-selective fading.

[![](https://substackcdn.com/image/fetch/$s_!vdrw!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3f84376a-b79f-4de4-a25a-ec6217fef64b_1013x246.png)](https://substackcdn.com/image/fetch/$s_!vdrw!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3f84376a-b79f-4de4-a25a-ec6217fef64b_1013x246.png)

If you take a narrow enough slice of bandwidth, the channel response is “flat”, simply weakening the signal in a uniform manner.

 **Communication systems are designed around the channel.**

For example, wireless channels are nasty so all modern standards (4G/5G, WiFi) use OFDM.

[![Frequency selective fading in OFDM system. | Download Scientific Diagram](https://substackcdn.com/image/fetch/$s_!JkjG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F19889fb7-1f1e-4c57-9c87-407312982cb8_319x158.jpeg)](https://substackcdn.com/image/fetch/$s_!JkjG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F19889fb7-1f1e-4c57-9c87-407312982cb8_319x158.jpeg)

The channel (typically 20-100 MHz wide) is divided up into 12 KHz sub-segments.

### [1.a] Electrical Channel Examples

This is what a real, rather favorable electrical channel looks like.

[![](https://substackcdn.com/image/fetch/$s_!wCnY!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0ae92808-6dff-48db-bccd-119f7a47454a_867x579.png)](https://substackcdn.com/image/fetch/$s_!wCnY!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0ae92808-6dff-48db-bccd-119f7a47454a_867x579.png)

There is some loss (dB) at the Nyquist frequency which represents how “weak the signal becomes” as it passes through the channel.

But what many people miss is the frequency quality of the channel. As frequency goes up, the ripples and junk become much worse. This places enormous stress on the receiver, blowing up digital signal processing complexity, area, and power.

Here is another example:

[![](https://substackcdn.com/image/fetch/$s_!Bb5Y!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4d687b92-d416-4e50-bb0e-4577ddbcaac5_834x445.png)](https://substackcdn.com/image/fetch/$s_!Bb5Y!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4d687b92-d416-4e50-bb0e-4577ddbcaac5_834x445.png)

The blue channel consists of two very short, high-quality coax cables and a small PCB made of very high quality prepreg and core dielectric material.

The red channel is something more realistic. A regular, commercial QSFP-DD passive copper cable is added to the path alongside a SMA breakout board.

[![](https://substackcdn.com/image/fetch/$s_!xR8p!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F49eff291-5014-45f1-a540-4d3d5d28f477_480x320.jpeg)](https://substackcdn.com/image/fetch/$s_!xR8p!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F49eff291-5014-45f1-a540-4d3d5d28f477_480x320.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!sdhs!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff7f2a9dd-511c-4f34-90e1-1e0ad7fd614f_800x800.webp)](https://substackcdn.com/image/fetch/$s_!sdhs!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff7f2a9dd-511c-4f34-90e1-1e0ad7fd614f_800x800.webp)

As you can see, the red channel looks horrible. This is the fundamental problem with electrical high-speed links going forward.

 **Magic materials do not exist. 448G electrical SerDes is not going to work in any reasonable manner.**

[![](https://substackcdn.com/image/fetch/$s_!YM7O!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff9852b16-3bb1-4539-afb6-2ef42141b1c6_220x164.gif)](https://substackcdn.com/image/fetch/$s_!YM7O!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff9852b16-3bb1-4539-afb6-2ef42141b1c6_220x164.gif)

Co-packaged optics is the future.

### [1.b] Optical Channels are Amazing

[![](https://substackcdn.com/image/fetch/$s_!h_FY!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa47cfa84-3645-45da-b542-c950e3ceeed3_783x581.png)](https://substackcdn.com/image/fetch/$s_!h_FY!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa47cfa84-3645-45da-b542-c950e3ceeed3_783x581.png)

[![](https://substackcdn.com/image/fetch/$s_!85-X!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0dd6babc-72fd-46e6-b990-ddf3c5a9a130_777x584.png)](https://substackcdn.com/image/fetch/$s_!85-X!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0dd6babc-72fd-46e6-b990-ddf3c5a9a130_777x584.png)

[![](https://substackcdn.com/image/fetch/$s_!GVlQ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F315f827c-35ed-4bfa-8d50-0dab4ddeb56a_541x272.webp)](https://substackcdn.com/image/fetch/$s_!GVlQ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F315f827c-35ed-4bfa-8d50-0dab4ddeb56a_541x272.webp)Notice the Y-axis… **dB per KILLOMETER**

Note that the x-axis is in nanometer. Converting to Hz yields tens of terahertz of bandwidth!

[![](https://substackcdn.com/image/fetch/$s_!ITJr!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa8d1b902-15c4-462c-9fd6-a34ef9222717_756x595.png)](https://substackcdn.com/image/fetch/$s_!ITJr!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa8d1b902-15c4-462c-9fd6-a34ef9222717_756x595.png)

The “premium” spectrum is 11 THz wide lmao.

### [1.c] Narrowband Carrier Waves: An Intuitive Approach

“Narrowband” and “Broadband” are terms that become confusing because the definition depends on who you are talking to.

 **I consider any system with negligible frequency selective fading within the channel to be narrowband.**

[![](https://substackcdn.com/image/fetch/$s_!apqf!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F39796df3-f668-4deb-b4ac-1a93b7636965_533x304.jpeg)](https://substackcdn.com/image/fetch/$s_!apqf!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F39796df3-f668-4deb-b4ac-1a93b7636965_533x304.jpeg)

Traditionally, wireless is “narrowband” and electrical wireline is “broadband”.

Optics is the crazy world where you can have truly batshit insane quantities of bandwidth per carrier and still keep all the nice aspects of narrowband.

 **Each lambda (aka wavelength aka color) of light is a narrowband carrier.**

[![](https://substackcdn.com/image/fetch/$s_!38fU!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1780b61b-79b4-4ad9-aaf1-7bc139390138_200x200.gif)](https://substackcdn.com/image/fetch/$s_!38fU!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1780b61b-79b4-4ad9-aaf1-7bc139390138_200x200.gif)

It took a while for me to realize this and my mind is still regularly blown lol.

[![](https://substackcdn.com/image/fetch/$s_!vDAb!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd94c9455-e55b-4104-bf90-dc8ff4b409d2_220x165.gif)](https://substackcdn.com/image/fetch/$s_!vDAb!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd94c9455-e55b-4104-bf90-dc8ff4b409d2_220x165.gif)

### [1.d] Linearity and Differential Signaling 

The vast majority of modern electrical SerDes uses differential signaling.

 _*Die-2-die interfaces like UCIe are singled ended._

[![](https://substackcdn.com/image/fetch/$s_!bpbr!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1027e999-21c7-4334-a635-093650964137_1024x489.png)](https://substackcdn.com/image/fetch/$s_!bpbr!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1027e999-21c7-4334-a635-093650964137_1024x489.png)

This technique doubles the number of wires per link but has several crucial benefits.

  * Doubles swing. (peak to peak voltage)

  * Noise rejection.

  *  **Improved linearity.**




 **Linearity is critical and it explains why the optics people are so afraid of PAM4 signaling.**

I could bore you with a bunch of math and physics but here are some pictures that make the point quick and easy.

 **Here is a differential output. (D1A)**

[![](https://substackcdn.com/image/fetch/$s_!Y0oD!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff01114c6-480f-4c1b-98a9-26b64e1179f8_4000x2270.png)](https://substackcdn.com/image/fetch/$s_!Y0oD!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff01114c6-480f-4c1b-98a9-26b64e1179f8_4000x2270.png)

This is nice looking. Three highly linear eyes within the two PAM4 symbols.

Remember that PAM4 encodes two bits of data per symbol (word).

[![](https://substackcdn.com/image/fetch/$s_!Orgf!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7dd83ecb-8adb-4cbc-ac4b-3e6ba2895b91_755x343.png)](https://substackcdn.com/image/fetch/$s_!Orgf!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7dd83ecb-8adb-4cbc-ac4b-3e6ba2895b91_755x343.png)

Suppose one of the three eyes was smaller than the other two. That would lead to correlated errors.

Correlated (burst) errors destroy most forward-error-correction schemes. FEC math is designed around randomly distributed (uncorrelated) errors.

Let’s look at the **EXACT SAME SIGNAL but single-ended.**

[![](https://substackcdn.com/image/fetch/$s_!XnhW!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F54a5bc5a-fca8-4107-9a10-90f28d2c799c_865x628.png)](https://substackcdn.com/image/fetch/$s_!XnhW!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F54a5bc5a-fca8-4107-9a10-90f28d2c799c_865x628.png)

 **As you can see, the single-ended output is dogshit.**

Differential signaling is a wonderful tool that the optics world does not have. Optical carriers are very limited and matching the response (impedance?) of optical resonators is too difficult.

## [2] Light Sources

[![](https://substackcdn.com/image/fetch/$s_!aKrt!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc6e1b9a7-3468-4d70-9a38-0c2200d33a77_1908x1456.png)](https://substackcdn.com/image/fetch/$s_!aKrt!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc6e1b9a7-3468-4d70-9a38-0c2200d33a77_1908x1456.png)

Silicon is terrible for building lasers. The material of choice is either Gallium-Arsenide or Indium-Phosphide. 

Vikram Sekar covered this topic very well.

[![](https://substackcdn.com/image/fetch/$s_!9JlA!,w_56,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa409d69d-ca10-4bfe-a1fc-f8d291690566_185x185.png)Vik's NewsletterWhy We Can't Build Lasers on SiliconSilicon technology has dominated for decades for its low cost and ability to scale, but it has its Achilles heel: you can’t build lasers on silicon…Read morea year ago · 26 likes · 6 comments · Vikram Sekar](https://www.viksnewsletter.com/p/why-we-cant-build-lasers-on-silicon?utm_source=substack&utm_campaign=post_embed&utm_medium=web)

There are a wide variety of laser types. Keep in mind that each of these emits a single wavelength of light. One carrier wave.

[![](https://substackcdn.com/image/fetch/$s_!Zz6m!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fec34f2b6-8263-45c3-a1b4-811cc5d8a34d_1903x1420.png)](https://substackcdn.com/image/fetch/$s_!Zz6m!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fec34f2b6-8263-45c3-a1b4-811cc5d8a34d_1903x1420.png)

For generating multiple wavelengths of light, there are three broad categories of solutions.

  1. Laser Arrays

    1. Put many lasers of different wavelengths on a single chip.

    2. Alternatively, combine an array of lasers using an external waveguide.

    3.  **Terrible reliability and huge power draw.**

  2. Quantum Dot

    1. Use specialty process tech.

    2.  **Terrible yield.**

  3. Kerr Comb

    1. Use nonlinear phenomenon to split light into multiple wavelengths.

    2.  **Terrible energy conversion efficiency.**




Generating multiple wavelengths of light is a major challenge.

## [3] Photodetectors

Photodetectors convert light into electrical signals.

[![](https://substackcdn.com/image/fetch/$s_!VSFT!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa441db50-c72b-4e0f-9896-55c889793595_1951x1450.png)](https://substackcdn.com/image/fetch/$s_!VSFT!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa441db50-c72b-4e0f-9896-55c889793595_1951x1450.png)

[![](https://substackcdn.com/image/fetch/$s_!zN79!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F421ce8d4-7384-4494-9556-4861a8b456cb_1932x1453.png)](https://substackcdn.com/image/fetch/$s_!zN79!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F421ce8d4-7384-4494-9556-4861a8b456cb_1932x1453.png)

A lot of this stuff is materials science and physics related so I want to avoid writing about it.

What matters from a communications systems perspective is the optical to electrical (OE) conversion efficiency and noise performance.

[![](https://substackcdn.com/image/fetch/$s_!j4jH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F20f02ad6-23a3-43b3-b08f-86f879a36e71_1933x1450.png)](https://substackcdn.com/image/fetch/$s_!j4jH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F20f02ad6-23a3-43b3-b08f-86f879a36e71_1933x1450.png)

It is easy to juice receiver electrical output with stronger light. However, that requires very large power boosts on the transmitter.

The key point is… 

**Laser noise performance and linearity at high power is the limiting factor, not the photodetector.**

## [4] Modulators

Think of modulation as “encoding binary data onto an analog carrier signal”.

[![](https://substackcdn.com/image/fetch/$s_!LyfK!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5c9463bf-6f8a-4e87-890a-207c4d03ba95_659x601.webp)](https://substackcdn.com/image/fetch/$s_!LyfK!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5c9463bf-6f8a-4e87-890a-207c4d03ba95_659x601.webp)

There are several types but co-packaged optics tends to use amplitude shift based modulation.

### [4.a] Direct Modulation 

Direct modulation occurs when the power source to the laser acts as the modulation mechanism.

[![](https://substackcdn.com/image/fetch/$s_!AGOE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9d47d9fa-3c75-4db1-9c7b-30492be247bc_598x297.webp)](https://substackcdn.com/image/fetch/$s_!AGOE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9d47d9fa-3c75-4db1-9c7b-30492be247bc_598x297.webp)

  * Pros:

    * Cheap.

    * Easy to design and implement.

  * Cons:

    * Severely bandwidth limited.

    * Horrible reliability.




[![](https://substackcdn.com/image/fetch/$s_!kmYE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe794e417-32dd-48ae-bfff-63c0f16a370f_1729x1255.png)](https://substackcdn.com/image/fetch/$s_!kmYE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe794e417-32dd-48ae-bfff-63c0f16a370f_1729x1255.png)

### [4.b] External Modulation 

External modulation uses a silicon-photonics device to modulate a continuous-wave external laser.

[![](https://substackcdn.com/image/fetch/$s_!clCo!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff6cea8f1-bce8-45e9-8127-63894221311d_627x323.webp)](https://substackcdn.com/image/fetch/$s_!clCo!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff6cea8f1-bce8-45e9-8127-63894221311d_627x323.webp)

  * Pros:

    * Can support multiple wavelengths in a single PIC.

    * Bandwidth not limited by laser.

  * Cons:

    * Optical insertion loss.

    * Modulator tuning and stability.

    * Yield issues from fiber attach.




#### [4.b.i] Electroabsorption (EAM)

Electroabsorption modulators look like this.

[![](https://substackcdn.com/image/fetch/$s_!31R9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F70f045d0-f539-4139-9892-a02a0e1de8f3_778x560.jpeg)](https://substackcdn.com/image/fetch/$s_!31R9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F70f045d0-f539-4139-9892-a02a0e1de8f3_778x560.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!N3u1!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F910e100a-306c-4778-9bd5-be0aab1e7cbb_400x277.webp)](https://substackcdn.com/image/fetch/$s_!N3u1!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F910e100a-306c-4778-9bd5-be0aab1e7cbb_400x277.webp)

These are chunky devices traditionally used in telecom applications where space is not an issue. The reason is reliability.

[![](https://substackcdn.com/image/fetch/$s_!BoSC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F21b5e580-dd83-4e81-bc22-61183400d765_1924x1464.png)](https://substackcdn.com/image/fetch/$s_!BoSC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F21b5e580-dd83-4e81-bc22-61183400d765_1924x1464.png)

[![](https://substackcdn.com/image/fetch/$s_!H3u7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbb7695a6-2c57-4e1d-ba52-c2310993c528_1900x1426.png)](https://substackcdn.com/image/fetch/$s_!H3u7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbb7695a6-2c57-4e1d-ba52-c2310993c528_1900x1426.png)

Switching voltage from 1.5V to 4V is not a good thing.

Modern process nodes cannot deal with such high voltages.

[![](https://substackcdn.com/image/fetch/$s_!nZSd!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1abb3fd7-6c13-4ee1-82cc-21bcee42047c_1855x1236.png)](https://substackcdn.com/image/fetch/$s_!nZSd!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1abb3fd7-6c13-4ee1-82cc-21bcee42047c_1855x1236.png)

This tech is not viable for CPO or datacom in general. The modulation is too weak and the reliability is horrible.

#### [4.b.ii] Mach-Zehnder (MZM)

MZM use phase shifting to destructively interfere a signal to a logical zero.

[![](https://substackcdn.com/image/fetch/$s_!Dn-r!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1d6d7112-2354-46d8-a678-feaa59cc1338_1924x1438.png)](https://substackcdn.com/image/fetch/$s_!Dn-r!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1d6d7112-2354-46d8-a678-feaa59cc1338_1924x1438.png)

These devices work very well but have two major flaws:

  1. Take up a lot of space.

  2. Meaningful insertion loss.




[![](https://substackcdn.com/image/fetch/$s_!hSeK!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F212871fa-f866-44be-b3ca-272f694f4fee_1911x1437.png)](https://substackcdn.com/image/fetch/$s_!hSeK!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F212871fa-f866-44be-b3ca-272f694f4fee_1911x1437.png)

MZM loss in a normal topology is not an issue. However, a DWDM topology with many wavelengths cannot easily chain MZMs in a row. 

In other words, a chain of 8+ MZMs on the same waveguide will induce way too much optical insertion loss.

#### [4.b.iii] Micro-Ring Resonators (MRM)

MRMs are special because they enable massively scalable systems on a single fiber.

[![](https://substackcdn.com/image/fetch/$s_!phes!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7f82c4f2-6184-41c6-8807-d0d6352c14e3_1921x1462.png)](https://substackcdn.com/image/fetch/$s_!phes!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7f82c4f2-6184-41c6-8807-d0d6352c14e3_1921x1462.png)

Each of the rings modulates a single wavelength of light. Insertion loss is minimal. You can chain these devices very aggressively.

Intuitively, you can think of a MRM as an optical notch filter.

[![](https://substackcdn.com/image/fetch/$s_!VMD9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdfcd6a5d-3b42-4a5d-a39f-358db9be736d_1948x1306.png)](https://substackcdn.com/image/fetch/$s_!VMD9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdfcd6a5d-3b42-4a5d-a39f-358db9be736d_1948x1306.png)

And it is helpful to directly compare MRM with MZM.

[![](https://substackcdn.com/image/fetch/$s_!WB0I!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb25bcbcc-9336-49d6-824e-cc12d78eeb22_1776x1395.png)](https://substackcdn.com/image/fetch/$s_!WB0I!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb25bcbcc-9336-49d6-824e-cc12d78eeb22_1776x1395.png)

Wavelength sensitivity == thermal stability

So lets talk about the circular elephant in the room.

[![a circular elephant in a room. the word "stability" is overlayed](https://substackcdn.com/image/fetch/$s_!psb_!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4c784b8f-6b67-441e-8afd-eed5572566f5_1024x1024.jpeg)](https://substackcdn.com/image/fetch/$s_!psb_!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4c784b8f-6b67-441e-8afd-eed5572566f5_1024x1024.jpeg)

Micro-rings are very sensitive and need to be controlled with tiny heaters.

[![](https://substackcdn.com/image/fetch/$s_!LzER!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3e07e7f2-939c-48ba-a7cc-538f9ce02736_768x520.png)](https://substackcdn.com/image/fetch/$s_!LzER!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3e07e7f2-939c-48ba-a7cc-538f9ce02736_768x520.png)

Those of you who work in the semiconductor industry might be thinking…

 _“Wow… controlling sensitive devices with heaters sounds very difficult.”_

You are right. This shit is a nightmare.

[![](https://substackcdn.com/image/fetch/$s_!bOcb!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F835a7800-5c1e-4592-b9c6-832804c9218c_1903x1342.png)](https://substackcdn.com/image/fetch/$s_!bOcb!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F835a7800-5c1e-4592-b9c6-832804c9218c_1903x1342.png)

If the temperature is not just right, the modulation strength (aka extinction ratio… aka “how different a logical 0 is from logical 1” goes WAY DOWN.

[![](https://substackcdn.com/image/fetch/$s_!fIX5!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5ce11498-7987-4604-a421-2a78fb28814b_1893x1422.png)](https://substackcdn.com/image/fetch/$s_!fIX5!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5ce11498-7987-4604-a421-2a78fb28814b_1893x1422.png)

MRMs are incredible relative to MZM in every way EXCEPT for stability.

Solve the stability problem and you win.

## [5] Two Tribes and a False Choice

The optics world is divided into two tribes.

Clan Micro-Ring and Clan Mach-Zehnder each tell the outside world the other tribe are morons.

 _Mach-Zehnder modulators are too large and have significant insertion loss, Clan Micro-Ring screeches._

[![](https://substackcdn.com/image/fetch/$s_!sHKv!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd2df215a-9fad-42c5-b139-dd1a93122f12_727x469.png)](https://substackcdn.com/image/fetch/$s_!sHKv!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd2df215a-9fad-42c5-b139-dd1a93122f12_727x469.png)

 _Micro-Rings are too thermally unstable, shouts Clan Mach-Zehnder._

[![](https://substackcdn.com/image/fetch/$s_!90Jl!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa3b43e45-1763-43f7-8648-0e6901743c6e_712x463.png)](https://substackcdn.com/image/fetch/$s_!90Jl!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa3b43e45-1763-43f7-8648-0e6901743c6e_712x463.png)

This is the false choice presented to investors and prospective employees.

Don’t fall for it. Dig deeper.

It’s based on a technology called micro-ring resonator modulator. (MRM)

Now the reason we decided to invest in MRM is so that we could prepare ourselves using MRM’s incredible density… better density and power compared to Mach-Zehnder which is used for telecommunications.. when you um uh drive from one datacenter to another… or even in the transceivers we use… we use Mach-Zehnder because the density requirement is not very high… **until now.**

-Mr. Leather Jacket, GTC 2025

Both technologies are viable for CPO. The engineering challenges are very different, which is why each tribe so aggressively shills their choice. Once a company makes a choice on modulator, they are basically committed.

Rings are really damn unstable. Thermals are a huge problem.

Notice something about Nvidia CPO?

[![](https://substackcdn.com/image/fetch/$s_!Eclv!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdea0bcfd-e0bb-441f-baf7-4b68491592c2_1696x994.png)](https://substackcdn.com/image/fetch/$s_!Eclv!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdea0bcfd-e0bb-441f-baf7-4b68491592c2_1696x994.png)

The switch chip itself is liquid cooled. Photonics IC (aka PIC aka photonic engine) is far away, surrounded by a block of aluminum. This chunky heatsink is there to absorb and slow down thermal variation induced by the switch chip.

[![](https://substackcdn.com/image/fetch/$s_!a70R!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9759c557-9e70-46de-bb7a-cd0f373f92f7_1074x499.png)](https://substackcdn.com/image/fetch/$s_!a70R!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9759c557-9e70-46de-bb7a-cd0f373f92f7_1074x499.png)

Mach-Zehnder is thermally stable but now you have to make a make a lot of changes to the package design. 

[ https://en.wikipedia.org/wiki/False_dilemma](https://en.wikipedia.org/wiki/False_dilemma)

[![](https://substackcdn.com/image/fetch/$s_!h8H8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F22cd2ba9-78d8-4e7f-b67d-3698d01f703f_1681x1068.png)](https://substackcdn.com/image/fetch/$s_!h8H8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F22cd2ba9-78d8-4e7f-b67d-3698d01f703f_1681x1068.png)

[![](https://substackcdn.com/image/fetch/$s_!40Fq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7214cb3e-de58-4614-9e46-31f1cfad2ebc_721x1099.png)](https://substackcdn.com/image/fetch/$s_!40Fq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7214cb3e-de58-4614-9e46-31f1cfad2ebc_721x1099.png)

## [6] Electrical Periphery: TIA and all that

I often see sell-side research notes discuss TIA (transimpedance amplifier) as if this thing is some kind of discrete optics-specific component.

TIA is a basic circuit that has many applications.

[![](https://substackcdn.com/image/fetch/$s_!5ww7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F77f3829e-5a6f-437c-b2bd-fd4c14a7c470_275x183.png)](https://substackcdn.com/image/fetch/$s_!5ww7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F77f3829e-5a6f-437c-b2bd-fd4c14a7c470_275x183.png)

Electrical SerDes often have multiple TIAs as a part of their CTLEs.

[![](https://substackcdn.com/image/fetch/$s_!ZTdB!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F68cf272d-65e7-4e74-86e7-105c96bc6bfb_1948x1435.png)](https://substackcdn.com/image/fetch/$s_!ZTdB!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F68cf272d-65e7-4e74-86e7-105c96bc6bfb_1948x1435.png)

[![](https://substackcdn.com/image/fetch/$s_!QjxM!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F353456bb-376d-4ba0-a99a-93779a259c18_1902x1447.png)](https://substackcdn.com/image/fetch/$s_!QjxM!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F353456bb-376d-4ba0-a99a-93779a259c18_1902x1447.png)

Would you look at that! Basically every high-speed system has multiple TIA integrated on die. It’s almost as if TIA is a basic circuit and not some kind of magic optics-only discrete component.

* * *

In general, optical systems need a series of electrical amplifiers to deal with low electrical output from the photodetectors/photodiodes. 

The amplifier chain tends to follow a similar structure across designs. For example, a TIA followed by a main amplifier that likely has automatic gain control (AGC).

Managing noise across the amplification chain is important. Integration helps with mitigating the effects of parasitics.

## [7] Incorrect Obsession with Silicon “Beachfront/Shoreline”

I see many people (engineers and analysts) obsess over beachfront and shoreline. 

_We are limited by bandwidth per silicon/die millimeter, they screech._

 **This take is extremely wrong.**

Go ahead and pack together SerDes lanes on silicon. Your system will have dogshit performance because of crosstalk at the package level.

Here is a snip from a TSMC paper on integrating UCIe on CoWoS-R.

[![](https://substackcdn.com/image/fetch/$s_!trZK!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7f4e81e9-c6b0-4735-bf11-67a6f3181790_949x1225.png)](https://substackcdn.com/image/fetch/$s_!trZK!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7f4e81e9-c6b0-4735-bf11-67a6f3181790_949x1225.png)

Crosstalk at the package kills performance.

Package cost (many high-speed signal layers) kills gross margins.

At 200G speeds, most of the link margin is eaten just from the package.

Why, you might ask?

It’s because of the skin effect.

[![](https://substackcdn.com/image/fetch/$s_!WTCP!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2dde99b1-ac7a-44a5-9a6c-477f800fb8c6_491x468.webp)](https://substackcdn.com/image/fetch/$s_!WTCP!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2dde99b1-ac7a-44a5-9a6c-477f800fb8c6_491x468.webp)

Also the fact that most packaging technologies cannot build proper ground shields.

[![](https://substackcdn.com/image/fetch/$s_!u17J!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F91d3b13c-259e-4f7e-9e97-bc7d82fd082b_639x463.webp)](https://substackcdn.com/image/fetch/$s_!u17J!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F91d3b13c-259e-4f7e-9e97-bc7d82fd082b_639x463.webp)

Ideally, you want ground to uniformly surround the signal wire. 

This is not possible on most packaging tech.

As a workaround, package and PCB designers use tricks.

[![](https://substackcdn.com/image/fetch/$s_!YHKS!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F95ba96de-2dfb-4971-ae3b-cfaed7ddee9a_1217x701.png)](https://substackcdn.com/image/fetch/$s_!YHKS!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F95ba96de-2dfb-4971-ae3b-cfaed7ddee9a_1217x701.png)

See all those dots next to the traces? Those are vertical VIAs that connect to ground planes.

It’s a ghetto way of building a partial coax ground shield. 

Two planes with many vertical pillars connecting them together.

 **Anyone who claims that silicon beachfront/shoreline is the I/O limit does not know what they are talking about.**

 ****Package crosstalk is the limit.****

## [8] Photonic Process Nodes

Photonics nodes tend to be around 45nm to 65nm class.

This is because optical structures (modulators, waveguides, photodiodes) tend to be large. Scaling sucks. It’s like analog scaling but so much worse.

Global Foundries has a 22nm-class photonic node called 22FDX.

[![](https://substackcdn.com/image/fetch/$s_!1xuT!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1d82b372-032d-4779-a64b-70f80377065c_1296x826.png)](https://substackcdn.com/image/fetch/$s_!1xuT!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1d82b372-032d-4779-a64b-70f80377065c_1296x826.png)

It was launched in 2015 and still nobody fucking wants to use it.

It’s too expensive.

Photonic process nodes also have terrible PDK relative to logic nodes. I have had several “wait they don’t provide you with this info” conversations.

[![](https://substackcdn.com/image/fetch/$s_!IWtA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F86facfc2-f005-4bd2-b996-4c4c50da426e_787x1404.png)](https://substackcdn.com/image/fetch/$s_!IWtA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F86facfc2-f005-4bd2-b996-4c4c50da426e_787x1404.png)

## [9] Walkthrough: Nvidia Quantum-X GTC 2025 Announcement

Previously wrote a low-quality news post:

Now that I have had time to properly explain the technical background, let’s go over this again. 

[![](https://substackcdn.com/image/fetch/$s_!3wrJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffdea3057-c751-418f-998f-19e1cde4fb1f_2338x1303.png)](https://substackcdn.com/image/fetch/$s_!3wrJ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffdea3057-c751-418f-998f-19e1cde4fb1f_2338x1303.png)

[![](https://substackcdn.com/image/fetch/$s_!WEBP!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbd9c071e-4205-41d0-bd9c-1bdc81e0db75_1312x1054.png)](https://substackcdn.com/image/fetch/$s_!WEBP!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbd9c071e-4205-41d0-bd9c-1bdc81e0db75_1312x1054.png)

Liquid cooling of the switch chips.

[![](https://substackcdn.com/image/fetch/$s_!bBCo!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fedaa17d3-9a8c-45d0-822b-c21d0faeedf4_1528x1180.png)](https://substackcdn.com/image/fetch/$s_!bBCo!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fedaa17d3-9a8c-45d0-822b-c21d0faeedf4_1528x1180.png)

Chunky aluminum heat shields to protect the ring modulators on the photonic ICs.

[![](https://substackcdn.com/image/fetch/$s_!hRAL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F465124fe-c299-446a-9aa5-089123b852c1_1693x1132.png)](https://substackcdn.com/image/fetch/$s_!hRAL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F465124fe-c299-446a-9aa5-089123b852c1_1693x1132.png)

[![](https://substackcdn.com/image/fetch/$s_!UM8U!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3df64250-fd35-4417-bb5c-2e6efdd610ca_1830x934.png)](https://substackcdn.com/image/fetch/$s_!UM8U!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3df64250-fd35-4417-bb5c-2e6efdd610ca_1830x934.png)

They are directly driving the rings at 200G PAM4. This is interesting because the frequency response of MRMs is not good. Nvidia likely had to use agressive pre-distortion to get this to work.

[![](https://substackcdn.com/image/fetch/$s_!BSeQ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8f3de9ca-472f-4218-b6ba-58779930f880_2089x1138.png)](https://substackcdn.com/image/fetch/$s_!BSeQ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8f3de9ca-472f-4218-b6ba-58779930f880_2089x1138.png)

TSMC N6 is for the EIC. The PIC is likely TSMC 65nm based on some papers I found.

[![](https://substackcdn.com/image/fetch/$s_!6IZt!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5b8e99bf-736c-4c1c-9240-b9dccfc11c60_2080x1096.png)](https://substackcdn.com/image/fetch/$s_!6IZt!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5b8e99bf-736c-4c1c-9240-b9dccfc11c60_2080x1096.png)

[![](https://substackcdn.com/image/fetch/$s_!YKn6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc647d2c4-8170-4f48-abdb-62ec3a40795b_1783x1126.png)](https://substackcdn.com/image/fetch/$s_!YKn6!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc647d2c4-8170-4f48-abdb-62ec3a40795b_1783x1126.png)

It’s a laser array. You think this shit is reliable? LOL

Having 1152 fibers in your system is not a good thing. Nvidia is limited by the number of wavelengths from the light source. A 16-lambda laser could cut fiber count in half-ish.

## [10] Walkthrough: Broadcom Hot Chips 2024 Baily Presentation

I previously covered Broadcom’s CPO presentation at Hot Chips 2024 here:

Understand the tech much better now so lets try again.

[![](https://substackcdn.com/image/fetch/$s_!NcSC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8f1da650-0b6d-44fe-b9eb-f534f1ec04ee_2365x1285.png)](https://substackcdn.com/image/fetch/$s_!NcSC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8f1da650-0b6d-44fe-b9eb-f534f1ec04ee_2365x1285.png)

[![](https://substackcdn.com/image/fetch/$s_!Rapt!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Febe7ab3d-3d63-4fe9-aca1-41a1b955da07_2337x1288.png)](https://substackcdn.com/image/fetch/$s_!Rapt!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Febe7ab3d-3d63-4fe9-aca1-41a1b955da07_2337x1288.png)

Structurally, Broadcom’s solution is similar to Nvidia’s.

[![](https://substackcdn.com/image/fetch/$s_!DOVF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F15c9724c-f56c-4412-98ca-eac88b6acddb_2377x1297.png)](https://substackcdn.com/image/fetch/$s_!DOVF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F15c9724c-f56c-4412-98ca-eac88b6acddb_2377x1297.png)

[![](https://substackcdn.com/image/fetch/$s_!ZopC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fde1284e2-51e3-4d8f-929f-8b3f72347562_2361x1300.png)](https://substackcdn.com/image/fetch/$s_!ZopC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fde1284e2-51e3-4d8f-929f-8b3f72347562_2361x1300.png)

[![](https://substackcdn.com/image/fetch/$s_!oska!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F89b660b7-76d6-493a-a650-6a1cb1be2225_2365x1302.png)](https://substackcdn.com/image/fetch/$s_!oska!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F89b660b7-76d6-493a-a650-6a1cb1be2225_2365x1302.png)

Unlike Nvidia, Broadcom did not use COUPE (TSMC hybrid bonding). Instead, they used a cheaper RDL-based packaging tech. I expect them to move to COUPE for next generation.

[![](https://substackcdn.com/image/fetch/$s_!ArGo!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa3834e72-143d-45d6-ab35-a51322801bd9_2362x1296.png)](https://substackcdn.com/image/fetch/$s_!ArGo!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa3834e72-143d-45d6-ab35-a51322801bd9_2362x1296.png)

TDECQ of 1.07 dB is kickass. 

[![](https://substackcdn.com/image/fetch/$s_!QKzr!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb241d29b-220f-40ac-a170-549ee59b1885_2368x1293.png)](https://substackcdn.com/image/fetch/$s_!QKzr!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb241d29b-220f-40ac-a170-549ee59b1885_2368x1293.png)

No errors past RS-FEC symbol 5, with further optimization likely achieved by now.

Unfortunately, the presentation had very little information on the PIC itselft.

I suspect Broadcom used MZM. If they were using rings, they would have bragged about it.

## [11] Public Market Investment Corner

This is not meant to be an exhaustive overview of all companies involved with CPO. Only companies I am aware of and interested in covering are included.

### [11.a] Transceiver Exposed Companies are Fucked

Any company that has significant revenue exposure to optical transceivers is fucked. The entire point of CPO is to remove the transceivers…

[![](https://substackcdn.com/image/fetch/$s_!-wqM!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb65d5fe1-62c1-43a1-b0f9-0e6208e3c5ee_480x415.png)](https://substackcdn.com/image/fetch/$s_!-wqM!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb65d5fe1-62c1-43a1-b0f9-0e6208e3c5ee_480x415.png)

### [11.b] oDSP Exposed Companies also Fucked (COUGH COUGH MARVELL)

A huge portion of Marvell’s revenue is optical DSPs from their Inphi acquisition.

[![](https://substackcdn.com/image/fetch/$s_!A7uF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F85392542-76aa-4069-8780-f792ece26a71_1174x585.png)](https://substackcdn.com/image/fetch/$s_!A7uF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F85392542-76aa-4069-8780-f792ece26a71_1174x585.png)

THE ENTIRE POINT OF CPO IS TO GET RID OF THIS PART.

<https://www.marvell.com/products/pam-dsp.html>

[![](https://substackcdn.com/image/fetch/$s_!RnUR!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcb2dc79a-fd59-4990-88e6-d36cbf75b6ba_889x310.png)](https://substackcdn.com/image/fetch/$s_!RnUR!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcb2dc79a-fd59-4990-88e6-d36cbf75b6ba_889x310.png)

My gut feeling is this business revenue peaks in 2025 and declines by 50-70% by 2030.

### [11.c] CPO Developers: Nvidia, Broadcom, and Marvell

Nvidia and Broadcom both have excellent CPO solutions.

Marvell’s solution is dogshit. 

I went to the [MRVL 0.00%↑](https://substack.com/discover/stocks/MRVL) booth at OFC and gently asked some questions about their vaporware CPO mock-up. Knew all of the answers already. Just wanted to pretend to be an idiot and get the marketing dude to dig his own grave by confirming my priors.

They don’t have anything. 

[![](https://substackcdn.com/image/fetch/$s_!Mar0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F76104bd8-08ca-435a-8744-aea2d97e771e_1717x1222.png)](https://substackcdn.com/image/fetch/$s_!Mar0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F76104bd8-08ca-435a-8744-aea2d97e771e_1717x1222.png)_Co-packaged optics losers playing poker. (original artwork)_

I call their bluff. 

Marvell had profound “loser energy” at their OFC booth.

[![](https://substackcdn.com/image/fetch/$s_!Lfnw!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb0980a90-7982-473a-95ab-461a07a5b7fc_220x189.gif)](https://substackcdn.com/image/fetch/$s_!Lfnw!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb0980a90-7982-473a-95ab-461a07a5b7fc_220x189.gif)

Attractive funding short in semis.

### [11.d] Laser Manufacturers: Lumentum and Coherent

Both of these companies make a variety of lasers. They both also have sizable transceiver businesses.

Just because Mr. Leather Jacket showed their logos at GTC does not mean these tickers are good investments.

[![](https://substackcdn.com/image/fetch/$s_!4v_X!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F81c6fcba-d5cb-49c2-99ff-04f544b81a04_1813x1024.png)](https://substackcdn.com/image/fetch/$s_!4v_X!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F81c6fcba-d5cb-49c2-99ff-04f544b81a04_1813x1024.png)

### [11.e] Outsourced Assembly: Fabrinet (is better than everyone else)

I have covered Fabrinet multiple times. Go check out old posts.

They are exposed to transceivers, but are uniquely positioned to gain overall share with CPO.

Co-packaged optics involves a lot of sensitive IP. This is not the kind of shit you want to share with Eoptolink or Innolight…

[![](https://substackcdn.com/image/fetch/$s_!8hYX!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa5bd3e6c-5af3-428f-93de-4db8e22b2368_250x250.jpeg)](https://substackcdn.com/image/fetch/$s_!8hYX!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa5bd3e6c-5af3-428f-93de-4db8e22b2368_250x250.jpeg)

Fabrinet is a trusted manufacturing partner within the industry. They literally segregate cleanroom space and employees for each customer.

### [11.f] Glass: Corning and Nittobo

You may be familiar with Corning from the “Gorilla Glass” product inside basically every smartphone.

They have a huge optical communications fiber depeartment.

Nittobo is a Japanese company that makes ultra-low loss glass fiber. Given the shitshow that is going on right now, I am seriously considering buying some foreign stocks just to get exposure to “anything other than USD”.

### [11.g] Fabs: TSMC War Against GloFo and Tower Semi

Traditionally, Global Foundries and Tower Semiconductor are the Fabs that have good photonic process nodes.

TSMC has a photonic node and it sucks. This is not my opinion. It is the opinion of MANY people across MANY companies who I have spoken with.

Mr. Leather Jacket shilling TSMC photonics node is a publicity stunt. 

The problem is, COUPE (TSMC tech for hybrid bonding PIC and EIC) and TSMC advanced packaging (CoWoS-L) are fucking amazing.

TSMC has a policy of refusing to advanced-package chips from other fabs. 

This policy is “encouraging” many companies to ditch Tower/GloFo and use TSMC for their PIC instead.

[![](https://substackcdn.com/image/fetch/$s_!RXGv!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1f7d2c65-8f07-4a0d-89bc-0f8f6aab0649_1159x1138.png)](https://substackcdn.com/image/fetch/$s_!RXGv!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1f7d2c65-8f07-4a0d-89bc-0f8f6aab0649_1159x1138.png)

COUPE has incredible return loss. Also basically zero insertion loss.

[![](https://substackcdn.com/image/fetch/$s_!40ET!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4fde31e5-2785-4a33-8818-648325f7f566_1021x664.png)](https://substackcdn.com/image/fetch/$s_!40ET!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4fde31e5-2785-4a33-8818-648325f7f566_1021x664.png)

Ultra clean power supply. Basically no ripple.

[![](https://substackcdn.com/image/fetch/$s_!zzIj!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F11cb72e5-8600-4a06-b2b7-1797f8b46b6c_1000x736.png)](https://substackcdn.com/image/fetch/$s_!zzIj!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F11cb72e5-8600-4a06-b2b7-1797f8b46b6c_1000x736.png)

CoWoS-L has incredible insertion loss. Less than 2 dB at 53 GHz. This is nothing. A normal package easily hits 8 dB insertion loss under the same conditions.

CPO using COUPE and CoWoS-L can easily achieve less than 3 dB of insertion loss with exceptional crosstalk isolation.

[TSM 0.00%↑](https://substack.com/discover/stocks/TSM) photonics process node sucks but COUPE and CoWoS-L creates an incredible moat. [GFS 0.00%↑](https://substack.com/discover/stocks/GFS) and [TSEM 0.00%↑](https://substack.com/discover/stocks/TSEM) shareholders beware.

[![TSMC's New Chairman Affirms Hopes of AI-Fueled 2024 Recovery](https://substackcdn.com/image/fetch/$s_!xQPv!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F52586b4c-74c5-4fe3-90ef-7234a9b99a19_768x512.jpeg)](https://substackcdn.com/image/fetch/$s_!xQPv!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F52586b4c-74c5-4fe3-90ef-7234a9b99a19_768x512.jpeg)

Subscribe for engineering-driven investment analysis.

Subscribe

Share with Marvell employees. I heard from a hedge fund friend that management asked employees to accept bonus in the form of extra RSUs at ~$120/share price. 🤣

[Share](https://irrationalanalysis.substack.com/p/a-background-proof-guide-on-co-packaged?utm_source=substack&utm_medium=email&utm_content=share&action=share)
