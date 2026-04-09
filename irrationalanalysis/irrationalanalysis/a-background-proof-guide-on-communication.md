# A Background-Proof Guide on Communication Systems

## Optics, 5G, Wi-Fi, Ethernet, PCIe... all the same.

**Dec 02, 2024**

**Likes:** 0

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Please check the [‘about’ page](https://irrationalanalysis.substack.com/about) for a list of active positions.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice, and readers should **always do their own research before investing in any security.**

  * Feel free to contact me via email at: _irrational_analysis@proton.me_




* * *

This post is inspired by the excellent SemiAnalysis article on the coming role of optical networks in distributed AI training.

 _Note: I have some very strong opinions on what multi-datacenter training means. There are some deeper themes…_

[![](https://substackcdn.com/image/fetch/$s_!HwSb!,w_56,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2F0150776c-9bf2-4bea-a9c2-41b24b7a0f15_1280x1280.png) SemiAnalysisMulti-Datacenter Training: OpenAI's Ambitious Plan To Beat Google's InfrastructureBuildouts of AI infrastructure are insatiable due to the continued improvements from fueling the scaling laws. The leading frontier AI model training clusters have scaled to 100,000 GPUs this year, with 300,000+ GPUs clusters in the works for 2025. Given many physical constraints including construction timelines, permitting, regulations, and…Read more2 years ago · 95 likes · 11 comments · Dylan Patel, Daniel Nishball, and Jeremie Eliahou Ontiveros](https://www.semianalysis.com/p/multi-datacenter-training-openais?utm_source=substack&utm_campaign=post_embed&utm_medium=web)

My goal is to teach all of you (regardless of your background) how communication systems work in a first-principals manner. 

[![A Background-Proof Guide on AI](https://substackcdn.com/image/fetch/$s_!aZG5!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4fd51c7a-67d1-4cf2-825e-97be0e1fb16c_4000x2570.png)

#### A Background-Proof Guide on AI

[Daud's Scout](https://substack.com/profile/135313705-dauds-scout)·August 17, 2024[Read full story](https://irrationalanalysis.substack.com/p/a-background-proof-guide-on-ai)](https://irrationalanalysis.substack.com/p/a-background-proof-guide-on-ai)

“Background-Proof” means the following:

  * I assume the reader has zero relevant education or experience.

  * Concepts are explained in-depth. (avoid “dumbing-down”) 

  * Many readers will only understand a small subset of this post, say 20%.

    *  **This is perfectly fine!**

    * As long as you learn something new and build a little intuition, I am happy and consider this outcome a win.




If you **intuitively understand** some key concepts, every communication system will make sense. From 800Gbps electrical Ethernet to Wi-Fi to long-haul optical networks. 

It’s all the same.

[![](https://substackcdn.com/image/fetch/$s_!Ys6o!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd54998c3-a315-4dc4-8e5c-9150e8f53631_640x360.jpeg)](https://substackcdn.com/image/fetch/$s_!Ys6o!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd54998c3-a315-4dc4-8e5c-9150e8f53631_640x360.jpeg)

 _Note: Your feedback is very important to me. Please leave a comment or privately email me at irrational_analysis@proton.me_

# Contents:

  1. The real world is analog.

    1. Connecting computers to the real world: ADC and DAC

    2. Fourier Transforms: Time Domain vs Frequency Domain

    3. The Nyquist-Shannon Sampling Theorem

    4. SNR, Bandwidth, and the Shannon-Hartley Capacity Theorem 

    5. Impulse Response, Frequency Response, and Transfer Functions

    6. Impedance and Buffer Circuits

  2. Noise

    1. Common Sources

    2. Synchronous vs Asynchronous 

  3. Propagation Mediums

    1. Insertion Loss, Return Loss, and Reflections

    2. Calculation and Measurment

    3. Design Choices

  4. Digital tricks to out-smart errors.

    1. Forward Error Correction (FEC) Basics

    2. Example: Reed-Solomon 

    3. Reference Signals and Channel Sounding

  5. Modulation 

    1. NRZ, PAM, QAM, and all that.

    2. Sending complex numbers… (mixers)

    3. Public Enemy #1: Phase Noise

    4. Public Enemy #2: Non-Linearity

  6. Basic Filter Theory and Terminology

  7. Channel Equalization

    1. FIR/FFE

    2. IIR

    3. DFE

    4. CTLE

  8. Statistical Estimation Theory

    1. Basics

    2. LMS

    3. MLSD

  9. PLL and CDR

  10. Advanced Tactics

    1. MIMO

    2. Beamforming

    3. Multiple Carriers (Multiplexing)

  11. Practical Walkthrough

    1. 800Gbps Electrical Ethernet (IEEE 802.3ck)

    2. 5G (3GPP Release 15)

    3. Long-Haul Optics (Open ZR+)

  12. Bringing balance to your system.

  13. The Optics Section

    1. Short Reach: DSP, LRO, and LPO

    2. Long Reach: ZR, ZR+, and DWDM

    3. TIA, Drivers, and Optical Modulators

    4. PIC: Electrical —> Things Before Diode —> Diode

  14. Investment Time! 

    1. Core Ideas

      1. Broadcom 

      2. Marvell

      3. Fabrinet

      4. Ciena

      5. Keysight

      6. SiTime

      7. Lumen

      8. Tower Semi and Global Foundries

    2. Secondary Ideas

      1. Maxlinear

      2. Applied Optoelectronics

      3. MediaTek

      4. Lumentum

      5. Nittobo

      6. Innolight/Eoptolink

      7. Coherent

      8. Cogent Communications

    3. Niche

      1. Cisco/Arista Warning

      2. Astera Labs (┛◉Д◉)┛彡┻━┻

      3. Aeluma

      4. Credo (LRO YOLO)

  15. Existential/Philosophical Nonsense

    1.  **The Deeper Meaning of Multi-Datacenter Training Clusters**

    2. AGI Cultist Rocketship

    3. Corporations are people…

    4. The future is bright.




* * *

## [1] The real world is analog.

Take a moment to consider the difference in how your biological system (eyes + brain) process light relative to your smartphone imaging system (CMOS image sensor + ISP).

[![](https://substackcdn.com/image/fetch/$s_!zsYs!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffb13a90c-c5b5-4120-bdcd-024a25d94855_737x386.png)](https://substackcdn.com/image/fetch/$s_!zsYs!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffb13a90c-c5b5-4120-bdcd-024a25d94855_737x386.png)

Both systems need an array of sensors to capture light in the form of the three primary colors. 

What happens to the sensed data is where things get interesting.

Brains are analog computers. They process data using continuous electrical signals.

Nearly every modern computer is digital. All the data processing is done using discrete, binary values. 

[![](https://substackcdn.com/image/fetch/$s_!a1pR!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F375c8ad5-82e7-4f4c-8c90-4622e050292d_530x458.jpeg)](https://substackcdn.com/image/fetch/$s_!a1pR!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F375c8ad5-82e7-4f4c-8c90-4622e050292d_530x458.jpeg)

Of course, these billions of digital logic transistors are not really binary. It’s still analog but constructed in such a way that the analog world is largely abstracted out. 

Every digital logic chip has a voltage vs frequency response.

[![](https://substackcdn.com/image/fetch/$s_!YH0n!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F84cb25cc-4e22-438d-8d49-f46630dc0f1a_1500x844.jpeg)](https://substackcdn.com/image/fetch/$s_!YH0n!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F84cb25cc-4e22-438d-8d49-f46630dc0f1a_1500x844.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!IH_r!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F020a8045-b529-496f-819c-75b5bf9b3c42_1313x664.png)](https://substackcdn.com/image/fetch/$s_!IH_r!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F020a8045-b529-496f-819c-75b5bf9b3c42_1313x664.png)

More voltage causes the transistors to switch faster, enabling a higher clock speed of the logic circuit. There are diminishing returns because the process technology the chip design is built upon has intrinsic limits to transistor rise/fall time.

Instability in a digital circuit is a sign that the analog world has re-asserted it’s presence. Bits are flipped because the transistors cannot physically switch fast enough. Internal analog voltages are no longer correctly classified, breaking the binary abstraction.

* * *

Processing data in the analog domain is extraordinarily difficult. The modern world runs on digital computers for good reason.

Unfortunately, the real world is still analog. Our computers need to interact with wires, antennas, image sensors, microphones, touchscreens, and keyboard+mouse.

Understanding how this interaction works is key to understanding communication systems, amongst other topics.

Let’s get started.

### [1.a] Connecting computers to the real world: ADC and DAC

We need a way to convert digital (binary) data into an analog signal. This is called a DAC and here is a simple circuit design.

[![](https://substackcdn.com/image/fetch/$s_!6Ova!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbd56b1c4-46f7-4375-9f00-ffdc3e9fc9c1_935x602.webp)](https://substackcdn.com/image/fetch/$s_!6Ova!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbd56b1c4-46f7-4375-9f00-ffdc3e9fc9c1_935x602.webp)

Three binary signals get combined into one analog output.

For example, 0b000 ties Vout to ground.

0b001 only activates the least-significant bit (LSB) which has the most resistance between it and Vout. Thus, the LSB raises the voltage less than the other two bits.

[![](https://substackcdn.com/image/fetch/$s_!xH0A!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd3fa2072-c38e-4a0c-a3ca-954546f90377_600x510.jpeg)](https://substackcdn.com/image/fetch/$s_!xH0A!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd3fa2072-c38e-4a0c-a3ca-954546f90377_600x510.jpeg)

Non-linearity is a serious issue. Tactics such as differential signaling and interleaving help. It is also common to calibrate DAC bits with a bias voltage.

[![](https://substackcdn.com/image/fetch/$s_!M3a6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9f0eea9f-91b5-43af-8ff2-64ecdf4c13b1_1600x1198.png)](https://substackcdn.com/image/fetch/$s_!M3a6!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9f0eea9f-91b5-43af-8ff2-64ecdf4c13b1_1600x1198.png)

Eventually, transmitted analog signals need to be converted back to digital within the receiver, using an ADC.

The most common type of ADC is the [SAR-ADC.](https://en.wikipedia.org/wiki/Successive-approximation_ADC)

The Wikipedia page is really good. Just click the link and go read that.

For the lazy, I am copying over an excellent GIF and schematic.

[![](https://substackcdn.com/image/fetch/$s_!OK4M!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3450a0e1-ca54-49c2-837a-4b84e9851308_1218x962.gif)](https://substackcdn.com/image/fetch/$s_!OK4M!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3450a0e1-ca54-49c2-837a-4b84e9851308_1218x962.gif)Wikipedia is great.

[![](https://substackcdn.com/image/fetch/$s_!gVWK!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fedd2603e-7d52-459e-be6f-9410b28b87fd_1078x864.png)](https://substackcdn.com/image/fetch/$s_!gVWK!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fedd2603e-7d52-459e-be6f-9410b28b87fd_1078x864.png)

Notice how SAR-ADCs have a DAC inside, alongside a non-trivial amount of high-speed digital logic.

[![](https://substackcdn.com/image/fetch/$s_!bgBG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F853753dd-577e-4959-8fdc-bbc37893548c_1237x658.png)](https://substackcdn.com/image/fetch/$s_!bgBG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F853753dd-577e-4959-8fdc-bbc37893548c_1237x658.png)Interleaves are your friend but need to be calibrated.

[![](https://substackcdn.com/image/fetch/$s_!x3S8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4445920c-ef48-4efa-b85d-8d38fa68c220_678x203.jpeg)](https://substackcdn.com/image/fetch/$s_!x3S8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4445920c-ef48-4efa-b85d-8d38fa68c220_678x203.jpeg)Example of an interleaved DAC. Each of the four mini-DACs is fed the same reference clock but with slight phase offsets. Thus, the transistors in the design only need to run at 1/4th speed.

 **Key Points: DAC/ADC**

  * Non-linearity is a problem that needs significant design effort to mitigate.

  * For high-speed systems, interleaving is a requirement, alongside accurate phase calibration of said interleaves.

  * Highly sensitive to process node, temperature, and reference voltage. (PVT) 




### [1.b] Fourier Transforms: Time Domain vs Frequency Domain

This 3blue1brown video is incredible. Go watch it.

In a nutshell, the Fourier transform allows us to represent any arbitrary time-domain signal as a weighted sum of sinusoids. 

[![](https://substackcdn.com/image/fetch/$s_!cVxm!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffa21a206-575c-4883-bd03-7db8c6eaf402_1232x688.png)](https://substackcdn.com/image/fetch/$s_!cVxm!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffa21a206-575c-4883-bd03-7db8c6eaf402_1232x688.png)

Take this square wave built with three sinusoids of varying frequency.

[![](https://substackcdn.com/image/fetch/$s_!8Guo!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1554ce3f-a38c-4dd2-83fd-1bcfc0c03e8b_4010x2189.png)](https://substackcdn.com/image/fetch/$s_!8Guo!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1554ce3f-a38c-4dd2-83fd-1bcfc0c03e8b_4010x2189.png)

The more sinusoids you have, the better the representation.

Any continuous or sampled time-domain signal can be transformed into **frequency domain using a simple change-of-basis called the Fourier Transform.**

This is an incredibly powerful tool. Many tasks are easier to accomplish in frequency domain.

[![](https://substackcdn.com/image/fetch/$s_!tO5U!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F16b0675d-c29d-4c83-a601-2a75bb2e86b8_2615x3191.jpeg)](https://substackcdn.com/image/fetch/$s_!tO5U!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F16b0675d-c29d-4c83-a601-2a75bb2e86b8_2615x3191.jpeg)

Imagine if these three signals were on top of each other, constructively and destructively interfering. You could not separate them out in time-domain.

The Fourier transform would be the same.

 **Key Points: Fourier Transform**

  * Incredibly powerful tool.

  * Fast algorithms (FFT) enable real-time Fourier analysis of high-speed signals.

  * Everything has a frequency domain transform. Images have 2-D transforms. It’s just linear algebra. Highly extendable.

  * Go watch the 3blue1brown video.




### [1.c] The Nyquist-Shannon Sampling Theorem

So we now know how to convert from digital to analog, and vice versa… but how often should the system sample data?

 _Another way to think about this: How many Fourier Transform coefficients do we need for perfect (or good enough) re-construction._

[![](https://substackcdn.com/image/fetch/$s_!eW3g!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8ea31668-5724-43a5-8ed4-7413a2fd8c03_600x433.jpeg)](https://substackcdn.com/image/fetch/$s_!eW3g!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8ea31668-5724-43a5-8ed4-7413a2fd8c03_600x433.jpeg)

Too much sampling leads to waste. Excessive die size and power consumption.

Too little sampling results in information loss.

Intuitively, there must be some sweet spot where there is no wasted sampling, and the continuous-time (analog) signal can be perfectly reconstructed from the sampled signal.

This limit exists and is called the [Nyquist-Shannon Sampling Theorem.](https://en.wikipedia.org/wiki/Nyquist_rate)

Suppose you have some arbitrary bandlimited signal.

[![](https://substackcdn.com/image/fetch/$s_!pRN9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F669da54e-a697-416a-854a-e894eb61777b_2560x1306.png)](https://substackcdn.com/image/fetch/$s_!pRN9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F669da54e-a697-416a-854a-e894eb61777b_2560x1306.png)

Where the frequencies greater than B are either not present or you don’t care about them.

[![](https://substackcdn.com/image/fetch/$s_!VHUQ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F735934ce-713d-4d62-98ae-ad32e5c7d91e_2880x1372.png)](https://substackcdn.com/image/fetch/$s_!VHUQ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F735934ce-713d-4d62-98ae-ad32e5c7d91e_2880x1372.png)

If you sample at twice the highest frequency of interest, then the original signal can be perfectly re-constructed. Thus, there is no risk of information loss from going back and forth between time and frequency domain.

In practice, the **Nyquist frequency** (half of sampling rate) is very important. Most of the energy will be concentrated at or near the Nyquist Frequency.

[![](https://substackcdn.com/image/fetch/$s_!C6t5!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffc9335da-e721-4d53-bd95-9993c7a4e45f_1254x690.png)](https://substackcdn.com/image/fetch/$s_!C6t5!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffc9335da-e721-4d53-bd95-9993c7a4e45f_1254x690.png)

More on materials and design considerations in section [3.a].

 **Key Points: Sampling Theorem**

  * System bandwidth is directly linked to the minimum required sampling rate.

  * Undersampling results in aliasing, irrecoverable loss/distortion of information.

  * In practice, most systems over-sample (to varying levels) to improve performance.




### [1.d] SNR, Bandwidth, and the Shannon-Hartley Capacity Theorem

Signal to noise ratio (SNR) is one of two key metrics in a communication system.

[![](https://substackcdn.com/image/fetch/$s_!TalT!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc81943d8-585c-4fcc-bbb8-5eee3d34c233_494x278.jpeg)](https://substackcdn.com/image/fetch/$s_!TalT!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc81943d8-585c-4fcc-bbb8-5eee3d34c233_494x278.jpeg)

Once again, the frequency domain is our friend.

[![](https://substackcdn.com/image/fetch/$s_!tkcL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff7ce781c-0c9e-4e65-b5c9-253e3c50ef44_476x318.png)](https://substackcdn.com/image/fetch/$s_!tkcL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff7ce781c-0c9e-4e65-b5c9-253e3c50ef44_476x318.png)

[![](https://substackcdn.com/image/fetch/$s_!2FEn!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F78f8a122-882f-4726-bb6f-914441c9fb90_1024x576.jpeg)](https://substackcdn.com/image/fetch/$s_!2FEn!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F78f8a122-882f-4726-bb6f-914441c9fb90_1024x576.jpeg)

Every system has intrinsic noise, often referred to as the noise floor. More on that in section [2.a]. 

Interference is also noise from the perspective of a receiver. 

[![](https://substackcdn.com/image/fetch/$s_!_6CH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffc89057d-2574-4024-b8d4-6163c59e9d89_1280x720.jpeg)](https://substackcdn.com/image/fetch/$s_!_6CH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffc89057d-2574-4024-b8d4-6163c59e9d89_1280x720.jpeg)

SINR includes the power of noise sources that act as jammers. Sometimes, SNR and SINR are used interchangeably. People write SNR even though interference is implicitly included in the calculation. 

* * *

The second key metric of a communication system is the bandwidth. The mathematical concept was already covered in section [1.c] so let’s look at some practical examples.

[![](https://substackcdn.com/image/fetch/$s_!WrYL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F873200d2-4c3a-4ba1-838d-6ecdb088cdf9_1024x768.webp)](https://substackcdn.com/image/fetch/$s_!WrYL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F873200d2-4c3a-4ba1-838d-6ecdb088cdf9_1024x768.webp)

Wi-Fi operates in unlicensed spectrum. This means that anyone can operate in these frequency bands up to a certain power level, typically 100 mW (20dBm) but up to 1 W (30dBm) in some regions.

Your router scans all the bands and tries to select one with low noise. Every other router nearby acts as a jammer. 

[![](https://substackcdn.com/image/fetch/$s_!DEy6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb9ebe4d7-3f2b-4d5c-bcf0-c9b12bae1f55_654x414.png)](https://substackcdn.com/image/fetch/$s_!DEy6!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb9ebe4d7-3f2b-4d5c-bcf0-c9b12bae1f55_654x414.png)My router automatically picked channel #44 based on a scan of nearby spectral activity.

[![](https://substackcdn.com/image/fetch/$s_!SH56!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F98eefafb-7a5e-4eb7-b0f4-16e628b77e00_989x570.png)](https://substackcdn.com/image/fetch/$s_!SH56!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F98eefafb-7a5e-4eb7-b0f4-16e628b77e00_989x570.png)

Cellular networks operate on licensed spectrum. Government agencies auction spectrum to individual companies for specific uses. 

[![](https://substackcdn.com/image/fetch/$s_!8RtV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F77474c76-7d89-41ec-9719-90f7b7ae6d98_1200x768.jpeg)](https://substackcdn.com/image/fetch/$s_!8RtV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F77474c76-7d89-41ec-9719-90f7b7ae6d98_1200x768.jpeg)

Some of these bands sell for billions of dollars. Bandwidth (spectrum) is a precious resource.

[![](https://substackcdn.com/image/fetch/$s_!vekx!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F22836215-011f-42e6-9bcf-6a7b8fe60d27_1157x819.png)](https://substackcdn.com/image/fetch/$s_!vekx!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F22836215-011f-42e6-9bcf-6a7b8fe60d27_1157x819.png)

Typically, wireless frequency bands are 100 MHz wide or less due to frequency selective fading and channel coherence concerns.

mmWave 5G is a rare expectation, sometimes operated at 400 MHz wide slices.

Wireline communications (PCIe, Ethernet, NVLink, Infinity Fabric, USB, …) don’t have to worry about spectrum allocation. These systems have multiple GHz worth of bandwidth. More on this in section [3.a].

* * *

These two key attributes (SNR, bandwidth) determine the theoretical information capacity of any arbitrary communication system.

[![](https://substackcdn.com/image/fetch/$s_!PPIO!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb7e78cd7-36a9-4261-b9c5-58dac088d0db_460x309.png)](https://substackcdn.com/image/fetch/$s_!PPIO!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb7e78cd7-36a9-4261-b9c5-58dac088d0db_460x309.png)

Channel capacity is a theoretical limit. 

Physics says you can’t go faster than the speed of light.

The Shannon-Hartley Capacity theorem says you cannot transmit more information than “C”.

 _ **Note:** Don’t think too hard about the units. This is just a theoretical limit. The key takeaway is more bandwidth is (usually) better than more SNR. Drives system design._

In practice, real communication systems are not this efficient. 

**Notice that SNR scales channel capacity logarithmically while bandwidth offers linear scaling.**

Bandwidth is precious. 

* * *

One final topic is on narrow-band vs wide-band systems. Often, these terms are used incorrectly outside of technical forums.

[![](https://substackcdn.com/image/fetch/$s_!dAs-!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Feca00448-9cb4-4811-9aa0-8831beda97b0_1200x630.avif)](https://substackcdn.com/image/fetch/$s_!dAs-!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Feca00448-9cb4-4811-9aa0-8831beda97b0_1200x630.avif)

How narrow does the frequency band need to be?

The answer depends on the propagation medium the system is expected to operate in.

All materials (copper, optical fiber, air, …) have a frequency response.

Here is some arbitrary example propagation medium.

[![](https://substackcdn.com/image/fetch/$s_!nSy6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F00ee04dc-6e67-41eb-a4dd-68522763b294_276x182.jpeg)](https://substackcdn.com/image/fetch/$s_!nSy6!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F00ee04dc-6e67-41eb-a4dd-68522763b294_276x182.jpeg)

If the system uses a narrow chunk of bandwidth where the loss is relatively flat, say the frequencies between 10 GHz and 11 GHz, then it is narrowband. Using a wider bandwidth where frequency-selective fading is significant results in the system being classified as broadband and requiring different engineering considerations.

[![](https://substackcdn.com/image/fetch/$s_!WFXJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F380aba5d-e995-4122-b922-6f4908848c85_1013x246.png)](https://substackcdn.com/image/fetch/$s_!WFXJ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F380aba5d-e995-4122-b922-6f4908848c85_1013x246.png)

How narrow is narrow enough depends heavily on the physical materials. Optical “narrowband” is much wider than RF “narrowband”.

 **Key Points: Shannon-Hartley Capacity Theorem**

  * Information capacity has a hard limit determined by bandwidth and SNR.

  * Bandwidth is precious because it scales capacity linearly.

  * “Narrowband” means that channel coherence is maintained. In other words, frequency-selective fading is negligible. Narrowband/Broadband is frequently mis-classified!




### [1.e] Impulse Response, Frequency Response, and Transfer Functions

In order to mathematically model real systems (circuits, communication channels) we need some additional tools.

The first tool is an impulse response, the response of a system to a sharp stimulus.

[![](https://substackcdn.com/image/fetch/$s_!hwQy!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff426b3b0-17c6-4a59-a565-b8ab57dac9a9_630x424.webp)](https://substackcdn.com/image/fetch/$s_!hwQy!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff426b3b0-17c6-4a59-a565-b8ab57dac9a9_630x424.webp)

[![](https://substackcdn.com/image/fetch/$s_!kkWo!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F79b85f5e-19a7-4efb-9898-79b1eceb8363_601x500.png)](https://substackcdn.com/image/fetch/$s_!kkWo!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F79b85f5e-19a7-4efb-9898-79b1eceb8363_601x500.png)

[![](https://substackcdn.com/image/fetch/$s_!Qf1e!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4255057a-3e04-4b49-861b-b72e46518e9c_2052x1270.png)](https://substackcdn.com/image/fetch/$s_!Qf1e!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4255057a-3e04-4b49-861b-b72e46518e9c_2052x1270.png)

Imagine a perfect, instantaneous voltage spike. Or a single digital sample of unitary magnitude. The frequency response of the system is labeled as H(z), H(jw), or H(s) depending on the context (discrete, continuous). A lowercase ‘h’ is used for the time domain representation of the same impulse response.

[![](https://substackcdn.com/image/fetch/$s_!vCgn!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0f29fecf-2385-4c30-9f7f-454dc9731782_2942x2145.png)](https://substackcdn.com/image/fetch/$s_!vCgn!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0f29fecf-2385-4c30-9f7f-454dc9731782_2942x2145.png)

A step response is similar. Input is a unit step function. Zero to one indefinitely.

Channel Impulse Responses are very useful. They typically look something like this.

[![](https://substackcdn.com/image/fetch/$s_!RKen!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0c8647a9-c113-431d-9397-12f7f0813071_407x261.png)](https://substackcdn.com/image/fetch/$s_!RKen!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0c8647a9-c113-431d-9397-12f7f0813071_407x261.png)

The main spike is a scaled and shifted copy of the transmitted signal. The spikes that follow are reflections, also known as inter-symbol interference. 

Broadly speaking, the receiver’s primary objective to is estimate the channel and equalize it. Goal is to use math to “flatten” the channel impulse response into a single, strong, thin spike. This corrects channel distortions.

[![](https://substackcdn.com/image/fetch/$s_!Taew!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F14072991-9637-45c1-bcf1-e7574bea3505_749x377.png)](https://substackcdn.com/image/fetch/$s_!Taew!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F14072991-9637-45c1-bcf1-e7574bea3505_749x377.png)

* * *

The frequency response of a system element is very helpful because it can be cascaded with other elements. This is called transfer function analysis.

[![](https://substackcdn.com/image/fetch/$s_!EQ6-!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb153a5a8-404b-4f07-aa44-bca85ffc31c6_335x151.png)](https://substackcdn.com/image/fetch/$s_!EQ6-!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb153a5a8-404b-4f07-aa44-bca85ffc31c6_335x151.png)

This math enables lots of fun things. More on that in section [6].

 **Key Points: Impulse Response and Transfer Functions**

  * Circuits and systems are abstracted into transfer functions using math. 

  * Transfer functions are easy to cascade and analyze.

  * In the context of a communication system, the idea impulse response is a single scaled and shifted [Dirac delta function.](https://en.wikipedia.org/wiki/Dirac_delta_function) Everything else is reflections/noise/junk that needs to be equalized.




### [1.f] Impedance and Buffer Circuits

Impedance is important for high-frequency communication systems.

[![](https://substackcdn.com/image/fetch/$s_!iCYY!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc4afc914-14b6-4e27-ab7d-479ab1f4bb9b_450x261.avif)](https://substackcdn.com/image/fetch/$s_!iCYY!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc4afc914-14b6-4e27-ab7d-479ab1f4bb9b_450x261.avif)

[![](https://substackcdn.com/image/fetch/$s_!FXks!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8e2b506e-db23-491d-ac0d-94199d1d469b_550x270.png)](https://substackcdn.com/image/fetch/$s_!FXks!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8e2b506e-db23-491d-ac0d-94199d1d469b_550x270.png)

In many instances, it is desirable to have a buffer circuit in between two loads.

[![](https://substackcdn.com/image/fetch/$s_!LizU!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F18a3fcc4-6a68-4539-805d-d06438e750b4_725x493.png)](https://substackcdn.com/image/fetch/$s_!LizU!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F18a3fcc4-6a68-4539-805d-d06438e750b4_725x493.png)

An [ideal buffer](https://en.wikipedia.org/wiki/Buffer_amplifier) would have unitary gain, a flat frequency response, infinite/zero input impedance, and zero/infinite output impedance.

It’s an impedance converter. Prevents the circuits on each end from interacting with one another via parasitic properties.

[Here is a great explanation](http://www.learningaboutelectronics.com/Articles/Voltage-follower) on voltage follower buffers and why they are needed.

 **Key Points: Buffer Circuits**

  * Take up area and consume non-trivial power.

  * Used to isolate circuits.

  * One end is very high impedance, other end is very low impedance. 




## [2] Noise

You have heard about “noise floor” and “signal to noise ratio” but these may feel like abstract concepts. Where does noise come from? What factors affect the noise floor of a system?

### [2.a] Common Sources

Thermal noise is intrinsic and broadly defined. Semiconductor PDKs have models for the intrinsic (thermal) noise of every device (transistor, standard cell, wire, capacitor, …) in the process node.

[![](https://substackcdn.com/image/fetch/$s_!Y5Ho!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F67e99087-44e1-46db-b4b7-d252eb96a111_320x240.webp)](https://substackcdn.com/image/fetch/$s_!Y5Ho!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F67e99087-44e1-46db-b4b7-d252eb96a111_320x240.webp)

Clock time domain noise (jitter) originates from the reference clock (Quartz, SiTime).

[![](https://substackcdn.com/image/fetch/$s_!oaGe!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F42c317b1-b305-4392-8f15-c1b8add02c9a_600x350.avif)](https://substackcdn.com/image/fetch/$s_!oaGe!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F42c317b1-b305-4392-8f15-c1b8add02c9a_600x350.avif)

Ultra-low noise selenium and rubidium clock sources are used in laboratory environments.

Background noise can come from many sources such as:

  * Outer Space

  * Your microwave

    * Runs at 2.4 GHz, interfering with old Wi-Fi. 

    * Some radiation does leak. (it’s safe, relax Karen)

  * Other devices on the same frequency.

  * DC power supply noise.

  * Neighboring circuits within a chip that are improperly grounded. 

  * Electromagnetic coupling between PCB layers.




[![](https://substackcdn.com/image/fetch/$s_!Nz1E!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F09c60c52-5632-4ddf-a946-3fe6b77614bc_760x537.webp)](https://substackcdn.com/image/fetch/$s_!Nz1E!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F09c60c52-5632-4ddf-a946-3fe6b77614bc_760x537.webp)The FCC takes safety very seriously. You are safe as long as you don’t engage in moronic behavior. If you see a fence with one of these signs, don’t climb it. Don’t climb cell towers. Do you want to get barbequed? The signs exist for a reason.

[![](https://substackcdn.com/image/fetch/$s_!qbge!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fff49defb-e7c6-4d34-a803-934b066ac117_701x328.png)](https://substackcdn.com/image/fetch/$s_!qbge!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fff49defb-e7c6-4d34-a803-934b066ac117_701x328.png)

[![](https://substackcdn.com/image/fetch/$s_!yUow!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc6585e74-67ce-4313-bede-cc81cf2f4baa_501x375.png)](https://substackcdn.com/image/fetch/$s_!yUow!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc6585e74-67ce-4313-bede-cc81cf2f4baa_501x375.png)DC voltage is not flat. There is always some ripple. Minimizing power supply noise is more difficult for higher voltage and high current applications.

### [2.b] Synchronous vs Asynchronous

One important distinction I want you to be aware of is that there are two categories of noise.

 **Synchronous** noise is periodic and matched with the clock of a circuit. This type of noise can be mitigated with careful matching of circuit elements. If a particular voltage is 10 mV off, that is ok because all important nodes in the design see the same error simultaneously.

 **Asynchronous** noise is the opposite. Some async noise is random. Often, the two ends of a communication system do not share a common reference clock. Thus, each end will dump async noise in the form of PPM.

[![](https://substackcdn.com/image/fetch/$s_!vIdF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb88295bf-f6d9-4884-90ac-bf03f7058e89_1002x888.png)](https://substackcdn.com/image/fetch/$s_!vIdF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb88295bf-f6d9-4884-90ac-bf03f7058e89_1002x888.png)<https://www.sitime.com/ppm-hz-calculator>

A lot of energy is stored in the clock frequency, so some standards such as PCIe require spread-spectrum clocking.

[![](https://substackcdn.com/image/fetch/$s_!MIvg!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F030a8792-9e5d-47e4-9011-0c4e109d68b8_756x534.png)](https://substackcdn.com/image/fetch/$s_!MIvg!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F030a8792-9e5d-47e4-9011-0c4e109d68b8_756x534.png)

Performance is sacrificed in exchange for lower EM leakage radiation.

For short-reach communication systems, sharing a clock (known as clock forwarding) eliminates the vast majority of async noise. Automatic 0 PPM. UCIe and NVLink-C2C are both clock-forwarded architectures.

[![](https://substackcdn.com/image/fetch/$s_!N65k!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1ced41ca-6a12-4b1d-aaad-659f09f6b0af_850x345.webp)](https://substackcdn.com/image/fetch/$s_!N65k!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1ced41ca-6a12-4b1d-aaad-659f09f6b0af_850x345.webp)Example of UCIe, a clock-forwarded SerDes. Notice how there is only one global PLL (reference clock… will explain in section [9]).

[![](https://substackcdn.com/image/fetch/$s_!LPvT!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9fbc13d3-f91c-42c8-948e-430b5669db76_595x453.webp)](https://substackcdn.com/image/fetch/$s_!LPvT!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9fbc13d3-f91c-42c8-948e-430b5669db76_595x453.webp)A regular SerDes architecture. Notice how there are two reference clocks. They will have a frequency offset, inducing PPM and async noise.

 **Key Points: Noise**

  * Noise is inevitable, just like death and taxes.

  * Synchronous noise (with respect to a reference clock) is easier to mitigate than asynchronous noise such as PPM.

  * Chip-to-Chip technology such as UCIe and NVLink-C2C use clock-forwarding, a special architecture that eliminates PPM.




## [3] Propagation Mediums

[![](https://substackcdn.com/image/fetch/$s_!3Us6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F94c15823-1422-4bb5-9b5f-37212e809424_410x173.jpeg)](https://substackcdn.com/image/fetch/$s_!3Us6!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F94c15823-1422-4bb5-9b5f-37212e809424_410x173.jpeg)

Every communication system has a channel. Could be an optical fiber, a copper cable, air (line of sight), air+trees+wall (non-line of sight), … whatever.

Math abstracts all this away. 

### [3.a] Insertion Loss, Return Loss, and Reflections

Insertion loss is the measure of how weak your signal gets. Typically, this number is represented in dB and associated with the Nyquist frequency (broadband) or carrier frequency (narrowband).

[![](https://substackcdn.com/image/fetch/$s_!a6Tj!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F41248aac-1d25-4f2f-b489-ca3e5f9c0ea8_600x450.png)](https://substackcdn.com/image/fetch/$s_!a6Tj!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F41248aac-1d25-4f2f-b489-ca3e5f9c0ea8_600x450.png)

For broadband communications, the linearity of a channel frequency response is very important. Bumps cause problems (reflections).

[![](https://substackcdn.com/image/fetch/$s_!QlYV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdc0cf093-172b-40a8-86f5-e518f2262263_650x400.jpeg)](https://substackcdn.com/image/fetch/$s_!QlYV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdc0cf093-172b-40a8-86f5-e518f2262263_650x400.jpeg)

This is a very important concept. Bandwidth of wireline communication systems is limited by material science. If the frequency is too high, the frequency response becomes shit. Receiver equalizer gets overloaded.

[![](https://substackcdn.com/image/fetch/$s_!Gppl!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F87c52d34-3f6f-4ba0-8bc2-bc255f1fa45d_1600x1258.jpeg)](https://substackcdn.com/image/fetch/$s_!Gppl!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F87c52d34-3f6f-4ba0-8bc2-bc255f1fa45d_1600x1258.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!nqD_!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8bf504ca-eac2-4819-97d4-d82863170474_700x525.png)](https://substackcdn.com/image/fetch/$s_!nqD_!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8bf504ca-eac2-4819-97d4-d82863170474_700x525.png)

[![](https://substackcdn.com/image/fetch/$s_!SSex!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F431463f6-46c1-4f7b-a0d5-4e843b7331e5_878x840.png)](https://substackcdn.com/image/fetch/$s_!SSex!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F431463f6-46c1-4f7b-a0d5-4e843b7331e5_878x840.png)

[![](https://substackcdn.com/image/fetch/$s_!fdcZ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcd00a4bc-bdf1-4741-9035-a88787c15af5_858x542.png)](https://substackcdn.com/image/fetch/$s_!fdcZ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcd00a4bc-bdf1-4741-9035-a88787c15af5_858x542.png)Large reflection at 30 GHz. Likely due to connector geometry.

Return loss measures how the signal “bounces”. 

[![](https://substackcdn.com/image/fetch/$s_!Txdb!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F93979ffb-d53b-44a0-be25-97a8ed603779_573x410.png)](https://substackcdn.com/image/fetch/$s_!Txdb!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F93979ffb-d53b-44a0-be25-97a8ed603779_573x410.png)

[![](https://substackcdn.com/image/fetch/$s_!4hCs!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb4472295-378c-4d07-b0b1-aca50101c4c2_1280x720.jpeg)](https://substackcdn.com/image/fetch/$s_!4hCs!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb4472295-378c-4d07-b0b1-aca50101c4c2_1280x720.jpeg)

Insertion loss (S12) and Return loss (S11) are both scattering parameters, more commonly known as S-Parameters.

[This Analog Devices blog](https://www.analog.com/en/resources/analog-dialogue/raqs/raq-issue-202.html) is a good overview for beginners.

 **Key Points: Loss and Reflections**

  * Insertion loss (S12) at Nyquist frequency is the primary driver in how much reach a communication system has.

  * For wireline systems, the linearity (smoothness) of S12 is important. 

  * Notches and ripple in S-parameters indicate reflections. (bad)

  * Package, PCB, and connector materials are a non-trivial limitation that drives important design decisions such ad baud rate and modulation scheme.




### [3.b] Calculation and Measurment

So how do you measure S-parameters?

There are two primary instruments.

Time-Domain Reflectometers (TDR) send out pulses and measure reflections.

[![](https://substackcdn.com/image/fetch/$s_!48v-!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F52ab3804-bd46-4741-bc39-a565098d8881_845x417.jpeg)](https://substackcdn.com/image/fetch/$s_!48v-!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F52ab3804-bd46-4741-bc39-a565098d8881_845x417.jpeg)

Vector Network Analyzers (VNA) send out frequency-domain pulses (precise sinusoids) to characterize S-Parameters. 

[![](https://substackcdn.com/image/fetch/$s_!VgJR!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc1015c84-3c60-430c-857b-c006adcc6382_1600x900.png)](https://substackcdn.com/image/fetch/$s_!VgJR!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc1015c84-3c60-430c-857b-c006adcc6382_1600x900.png)

Both instruments have their pros and cons. VNA’s are precise but extremely expensive.

Simulating a design is difficult. Every material has its own dielectric constant (DK) and dissipation factor (DF).

[![](https://substackcdn.com/image/fetch/$s_!KI_G!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4f367c59-9425-47f6-a48b-c77dc62b3c00_1013x1255.png)](https://substackcdn.com/image/fetch/$s_!KI_G!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4f367c59-9425-47f6-a48b-c77dc62b3c00_1013x1255.png)

Due to the Skin effect, the thickness of wires drastically change insertion loss. Trace shape and neighboring structures induce parasitic capacitance and inductance, sometimes referred to as electromagnetic coupling.

[![](https://substackcdn.com/image/fetch/$s_!d88d!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5ece00b7-bec0-4986-a74d-06f088c68902_710x404.gif)](https://substackcdn.com/image/fetch/$s_!d88d!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5ece00b7-bec0-4986-a74d-06f088c68902_710x404.gif)

[![](https://substackcdn.com/image/fetch/$s_!1dAP!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F87d616c7-fed7-415f-8d9e-3dc0a2836660_491x468.webp)](https://substackcdn.com/image/fetch/$s_!1dAP!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F87d616c7-fed7-415f-8d9e-3dc0a2836660_491x468.webp)

[![](https://substackcdn.com/image/fetch/$s_!6jsg!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6e5f6699-50a4-49ac-b2da-985b47242117_480x295.webp)](https://substackcdn.com/image/fetch/$s_!6jsg!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6e5f6699-50a4-49ac-b2da-985b47242117_480x295.webp)

To estimate insertion loss of a wired communication system, you need detailed simulations. **Cable length mostly meaningless.** Each component (cable, connectors, package, PCB) has its own insertion loss and S-parameters. 

Obviously, longer cable probably has more loss. You can’t guess how much by looking at pictures! Loss is measured in dB, not meters.

Guessing wireless channel loss is doable though.

Air at sea level has a well characterized loss. [The Friis equation is a fairly reliable tool ](https://www.pasternack.com/t-calculator-friis.aspx)for estimating wireless channel loss (pathloss).

[![](https://substackcdn.com/image/fetch/$s_!iurc!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F915377eb-7981-4928-9a48-6021bb8c46e1_525x316.png)](https://substackcdn.com/image/fetch/$s_!iurc!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F915377eb-7981-4928-9a48-6021bb8c46e1_525x316.png)

[![](https://substackcdn.com/image/fetch/$s_!FHBe!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffd24033d-4014-4d6d-b7ea-411932422d38_784x847.png)](https://substackcdn.com/image/fetch/$s_!FHBe!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffd24033d-4014-4d6d-b7ea-411932422d38_784x847.png)Mid-Band 5G at N78 (3.5 GHz)

[![](https://substackcdn.com/image/fetch/$s_!4FM_!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fabc40565-6c7d-4287-87c4-ad0552c31ca2_774x836.png)](https://substackcdn.com/image/fetch/$s_!4FM_!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fabc40565-6c7d-4287-87c4-ad0552c31ca2_774x836.png)mmWave 5G at N258 (26 GHz)

As you can see, mmWave is 17 dB lower than mid-band 5G. This is a lot for those who lack context.

It gets worse. Friis pathloss estimations assume line-of-sight. 

mmWave is easily absorbed by… everything. Walls, your hand, trees….

 **Key Points: Pathloss Measurment and Estimation**

  * Wireline systems are measured in dB, not length!

    * You cannot reasonably estimate a cable’s insertion loss from length alone. Skin effect (wire gauge) and connector loss are huge variables.

    * High-end systems (GB200) have very complex advanced package and PCB designs. Package loss is huge.

  * Pathloss of wireless channels with line-of-sight can be reasonably estimated with the Friis equation.

  * mmWave is a commercial failure. Now you understand why. 




### [3.c] Design Choices

In general, cables tend to have lower loss than PCB materials. 

The linearity of component S-parameters is an important consideration in how much bandwidth (baud rate) the system can handle. 

**You cannot blindly increase transmit power.** Amplifiers have non-linearity issues at higher power levels.

[![](https://substackcdn.com/image/fetch/$s_!8mES!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4f284fff-0ebf-4c2f-b288-a11b23004eda_981x538.png)](https://substackcdn.com/image/fetch/$s_!8mES!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4f284fff-0ebf-4c2f-b288-a11b23004eda_981x538.png)

Noise from the source circuit and the amplifier itself both scale as you increase transmit power.

Suppose you have a system with 10 dB of gain on each end, Tx and Rx.

A second system with 25 dB of gain on Tx and 0 dB on Rx is not intrinsically better. Depending on many factors, it is probably worse in terms of cost, power efficiency, and performance due to noise figure.

Specifications such as Ethernet and PCIe have limits on transmit power for compatibility and interoperability reasons. Proprietary specs such as NVLink can in theory do whatever they want, but juicing power is not a silver bullet.

In wireless, regulations prevent higher transmit power. Most large cell sites are limited to 45-65 dBm, depending on the frequency band. 

dBm means dB with respect to a milliwatt. So a mmWave 5G macro cell at 65 dBm outputs 3000 watts. 

## [4] Digital tricks to out-smart errors.

Errors are inevitable. There needs to be some digital mechanism to automatically detect and correct errors.

### [4.a] Forward Error Correction (FEC) Basics

In a nutshell, FEC algorithms use data redundancy, codewords, and parity checks to detect and correct errors.

A simple (terribly inefficient and fragile) FEC algorithm would be to send three copies of the data and choose the most common result for each bit.

[![](https://substackcdn.com/image/fetch/$s_!x1SX!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1ef7f6a0-47fe-41d1-9cfd-789ccb45c064_279x262.png)](https://substackcdn.com/image/fetch/$s_!x1SX!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1ef7f6a0-47fe-41d1-9cfd-789ccb45c064_279x262.png)

This method triples payload data and still does not provide robustness. Errors are often correlated, which is why most FEC algorithms scramble data and organize it into blocks.

### [4.b] Example: Reed-Solomon 

A popular FEC algorithm is [Reed-Solomon.](https://en.wikipedia.org/wiki/Reed%E2%80%93Solomon_error_correction)

[![](https://substackcdn.com/image/fetch/$s_!4I3j!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa5d8759d-da4f-4b58-ad37-d8db838fecaa_325x537.png)](https://substackcdn.com/image/fetch/$s_!4I3j!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa5d8759d-da4f-4b58-ad37-d8db838fecaa_325x537.png)

[![](https://substackcdn.com/image/fetch/$s_!g5_j!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5afa24db-8fb6-45cf-8373-45aa3ed9346a_629x269.png)](https://substackcdn.com/image/fetch/$s_!g5_j!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5afa24db-8fb6-45cf-8373-45aa3ed9346a_629x269.png)

RS-FEC has interesting math behind it. If you want to dive into polynomial coefficient codewords and other details, [check out this excellent Github blog thing.](https://tomverbeure.github.io/2022/08/07/Reed-Solomon.html)

[Cisco also has a great writeup.](https://www.cisco.com/c/en/us/products/collateral/interfaces-modules/transceiver-modules/implementation-optics-wp.html)

Currently, the most popular wireline FEC is RS (544, 514) which uses 30 parity symbols (00, 10, 01, 11 are the four possibilities of a PAM4 symbol) to form a 544-symbol codeword (data block). The algorithm on the receiver can correct up to 15 errors within the same block. 

Therefore, if the physical communication system has less than 15 errors in each block, the upper layer software will not see any errors. No dropped packets. No need to re-transmit.

“Heavier” FEC schemes offer improved error detection and correction at the cost of one or more of the following:

  * More parity bits/symbols —> reduced coderate (efficiency)

  * More digital processing, inducing latency.

  * More die area and power consumption.




RS (544, 514) is a good balance at the moment. Certain companies choose to run lighter, out-of-spec (custom) FEC schemes to save power and reduce latency. 

### [4.c] Reference Signals and Channel Sounding

Estimating your channel in critical for bringing up the communication link. Channel estimation is a huge topic. Only going over the basics here.

One obvious tactic is to estimate the channel at a lower datarate. But what to send? Perhaps an impulse response?

The reference signal needs to have a very sharp [autocorrelation](https://en.wikipedia.org/wiki/Autocorrelation) to estimate phase delay accurately.

This most popular reference signal is the [Zadoff-Chu sequence.](https://en.wikipedia.org/wiki/Zadoff%E2%80%93Chu_sequence)

[![](https://substackcdn.com/image/fetch/$s_!ybAq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1ed114e6-2652-49c8-a1da-cd6d69d7058b_1589x845.png)](https://substackcdn.com/image/fetch/$s_!ybAq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1ed114e6-2652-49c8-a1da-cd6d69d7058b_1589x845.png)Time domain plot of a Zadoff-Chu sequence.

[![](https://substackcdn.com/image/fetch/$s_!zI-w!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb6859301-f5e6-4da4-8789-44d6a58cf5ff_850x400.png)](https://substackcdn.com/image/fetch/$s_!zI-w!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb6859301-f5e6-4da4-8789-44d6a58cf5ff_850x400.png)The power spectral density is another way of intuitively understanding with Zadoff-Chu is good for channel sounding.

[![](https://substackcdn.com/image/fetch/$s_!38sx!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6979a8b2-67aa-4621-bc56-7cd30276ddb7_685x569.png)](https://substackcdn.com/image/fetch/$s_!38sx!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6979a8b2-67aa-4621-bc56-7cd30276ddb7_685x569.png)Very un-correlated with itself. Perfect for channel sounding.

[![](https://substackcdn.com/image/fetch/$s_!zoth!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4965a092-021c-4836-a7b2-db71b59fced0_2709x2164.jpeg)](https://substackcdn.com/image/fetch/$s_!zoth!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4965a092-021c-4836-a7b2-db71b59fced0_2709x2164.jpeg)ZC = Zadoff-Chu. Black line is ideal. Other lines are various channel sounding methods under comparison.

## [5] Modulation 

Modulation is a topic that a lot of people get confused over. 

It is the mapping of binary bits to physical (analog) symbols.

### [5.a] NRZ, PAM, QAM, and all that.

Let’s start with the easiest modulation scheme, NRZ.

[![](https://substackcdn.com/image/fetch/$s_!Hkt3!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4932bb36-1591-42b7-b5cf-012ace02e4fc_210x100.png)](https://substackcdn.com/image/fetch/$s_!Hkt3!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4932bb36-1591-42b7-b5cf-012ace02e4fc_210x100.png)

There are two voltages. One representing ‘0’ and the other representing ‘1’.

PAM<X> extends this to X voltage levels.

[![](https://substackcdn.com/image/fetch/$s_!IYkS!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2ffda866-e48b-46b3-b5b3-be1a148aaf35_1430x626.png)](https://substackcdn.com/image/fetch/$s_!IYkS!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2ffda866-e48b-46b3-b5b3-be1a148aaf35_1430x626.png)

[![](https://substackcdn.com/image/fetch/$s_!_Um1!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F38e43c72-7640-4c35-b404-4e786889f173_600x312.png)](https://substackcdn.com/image/fetch/$s_!_Um1!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F38e43c72-7640-4c35-b404-4e786889f173_600x312.png)[Gray coding](https://en.wikipedia.org/wiki/Gray_code) is just a re-shuffling of binary such that neighboring values only involve one bit flip. 

We can go further. What if it is possible to transmit complex numbers?

 _Don’t question this for now. It is explained in the next section._

[![](https://substackcdn.com/image/fetch/$s_!F1Bp!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffc04023d-b18a-47f4-a855-cf6a40859e1a_230x219.png)](https://substackcdn.com/image/fetch/$s_!F1Bp!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffc04023d-b18a-47f4-a855-cf6a40859e1a_230x219.png)

Now we have two dimensions to play with.

[![](https://substackcdn.com/image/fetch/$s_!UCqg!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6a85ea87-56eb-4a38-9cd6-a123ecf7c4e0_290x200.gif)](https://substackcdn.com/image/fetch/$s_!UCqg!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6a85ea87-56eb-4a38-9cd6-a123ecf7c4e0_290x200.gif)

Four binary bits can be transmitted per symbol in QAM16.

Quadrature amplitude modulation is popular in wireless systems, often extending to 256 symbols (8 bits per symbol).

[![](https://substackcdn.com/image/fetch/$s_!ikrO!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5727e028-c3d8-4752-a04a-70b22347b99e_772x403.png)](https://substackcdn.com/image/fetch/$s_!ikrO!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5727e028-c3d8-4752-a04a-70b22347b99e_772x403.png)

### [5.b] Sending complex numbers… (mixers)

To transmit a complex number, you need accurate 90-degree phase shifters on each end of the system. 

[![](https://substackcdn.com/image/fetch/$s_!mJ0N!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb772c3c3-aee9-4dc9-b6f3-e9959578fc2d_750x544.png)](https://substackcdn.com/image/fetch/$s_!mJ0N!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb772c3c3-aee9-4dc9-b6f3-e9959578fc2d_750x544.png)Polar form of a complex number.

Interleaving real and imaginary magnitude of each data symbol such that every other sample experiences a 90-degree phase shift allows for the transition of complex numbers. 

[![](https://substackcdn.com/image/fetch/$s_!FEfZ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fec6fb36a-55d9-41a1-b857-5a852c5d6ee4_1017x498.png)](https://substackcdn.com/image/fetch/$s_!FEfZ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fec6fb36a-55d9-41a1-b857-5a852c5d6ee4_1017x498.png)Local oscillator means quartz crystal or SiTime.

A 90-degree phase shifter is used with a mixer to create a complex (IQ) signal. 

Mixers are also used to move signals from baseband (0 Hz) up to the carrier frequency.

[![](https://substackcdn.com/image/fetch/$s_!Utom!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F16b58ceb-cb7e-4053-9758-9d3490e4b0fc_600x299.avif)](https://substackcdn.com/image/fetch/$s_!Utom!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F16b58ceb-cb7e-4053-9758-9d3490e4b0fc_600x299.avif)<https://www.digikey.nl/nl/articles/the-basics-of-mixers>

### [5.c] Public Enemy #1: Phase Noise

Phase noise is a huge problem. QAM modulation schemes are very sensitive to this.

[![](https://substackcdn.com/image/fetch/$s_!NIcY!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5beeca2b-67a5-4f93-9244-3153f56d7346_568x550.gif)](https://substackcdn.com/image/fetch/$s_!NIcY!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5beeca2b-67a5-4f93-9244-3153f56d7346_568x550.gif)

[![](https://substackcdn.com/image/fetch/$s_!qGOW!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff7c248be-cbff-4559-9f04-16a110a25261_685x722.png)](https://substackcdn.com/image/fetch/$s_!qGOW!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff7c248be-cbff-4559-9f04-16a110a25261_685x722.png)Optical laser phase noise turning a useable constellation into a worthless doughnut.

### [5.d] Public Enemy #2: Non-Linearity

System linearity is critical for enabling all the DSP tools in the receiver to work as well as possible. 

[![](https://substackcdn.com/image/fetch/$s_!YxZq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb5d4903d-e3eb-42bd-8954-03b1d409e86e_1119x471.png)](https://substackcdn.com/image/fetch/$s_!YxZq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb5d4903d-e3eb-42bd-8954-03b1d409e86e_1119x471.png)

Here is an intuitive reason why linearity is important.

In a highly linear system, the probability of symbol errors is uniform.

A ‘3’ misinterpreted as a ‘2’ has the same probability as a ‘1’ being misinterpreted as a ‘2’.

Nonlinearity means more correlation in errors. Correlated errors (burst errors) are extremely harmful to system performance. The likelihood of too many errors in a single FEC symbol becomes high.

## [6] Basic Filter Theory and Terminology

Filters are basically transfer functions that we intentionally add to a system to improve performance.

[![](https://substackcdn.com/image/fetch/$s_!yWSt!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd7197b71-946c-4e76-8cbe-0357dc8aa5a9_3594x1854.jpeg)](https://substackcdn.com/image/fetch/$s_!yWSt!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd7197b71-946c-4e76-8cbe-0357dc8aa5a9_3594x1854.jpeg)

There are three regions.

  1. Pass band (signal goes through and is optionally amplified)

  2. Transition band

  3. Stopband (signal attenuated by some target value)




[![](https://substackcdn.com/image/fetch/$s_!TBs9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc1c6c637-1724-4256-97d3-349915038a54_600x826.png)](https://substackcdn.com/image/fetch/$s_!TBs9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc1c6c637-1724-4256-97d3-349915038a54_600x826.png)Example of a digital FIR filter. 

There are several important metrics that are commonly used.

[![](https://substackcdn.com/image/fetch/$s_!3YaF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9148cc6f-564d-49c0-a67e-05f61bad60ca_780x476.gif)](https://substackcdn.com/image/fetch/$s_!3YaF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9148cc6f-564d-49c0-a67e-05f61bad60ca_780x476.gif)

3 dB bandwidth determines how wide the passband is.

[![](https://substackcdn.com/image/fetch/$s_!SU5D!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc6270dca-c4f1-4679-a5d8-693b92b99b77_502x296.png)](https://substackcdn.com/image/fetch/$s_!SU5D!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc6270dca-c4f1-4679-a5d8-693b92b99b77_502x296.png)

The passband and stopband will each have their own ripple. Passband ripple means non-linearity. Stopband ripple means that some aggressor bands may be less effectively attenuated.

[![](https://substackcdn.com/image/fetch/$s_!HZ8t!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8aee4d31-0f9c-4359-b6bc-17317ba09345_424x360.png)](https://substackcdn.com/image/fetch/$s_!HZ8t!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8aee4d31-0f9c-4359-b6bc-17317ba09345_424x360.png)Datasheet of an analog filter. Notice the asymmetric rejection bands. 10 dB delta!

## [7] Channel Equalization

There are several ways of equalizing a channel. Most (basically all) systems use a combination of these methods. Each has its own performance, cost, power, reliability, and area considerations.

### [7.a] FIR/FFE

Finite Impulse Response (FIR) filters have two special properties. First, the impulse response is… finite which means convergence is (almost) guaranteed.

[![](https://substackcdn.com/image/fetch/$s_!IVuO!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F811f261f-eded-4cf2-8abb-091bb3156869_432x117.png)](https://substackcdn.com/image/fetch/$s_!IVuO!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F811f261f-eded-4cf2-8abb-091bb3156869_432x117.png)

In other words, fewer stability issues compared to an IIR filter.

Secondly, filters is the ability to (easily) achieve linear phase.

 _(very important. explained in next section.)_

FIR filters have the following drawbacks:

  * Need many memory taps to achieve design objectives.

  * Significant delay/latency.

  * High area cost.

  * High power cost.




### [7.b] IIR

Infinite Impulse Response (IIR) filters look like this.

[![](https://substackcdn.com/image/fetch/$s_!ZuNT!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc3a7269c-c8ea-46f5-a04e-db27233f4450_580x302.png)](https://substackcdn.com/image/fetch/$s_!ZuNT!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc3a7269c-c8ea-46f5-a04e-db27233f4450_580x302.png)

There are feedback paths, which cause the impulse response to be… infinite.

[![](https://substackcdn.com/image/fetch/$s_!04Xn!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0df92357-d04c-4e49-9b19-b8342142dffc_1339x615.jpeg)](https://substackcdn.com/image/fetch/$s_!04Xn!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0df92357-d04c-4e49-9b19-b8342142dffc_1339x615.jpeg)

IIR filters are more likely to be unstable. It takes more design work to deal with this problem.

The critical issues with IIR filters is non-linear phase. Here is a great example of what that means.

Suppose you have an IIR filter with the following transfer function and pole-zero plot.

[![](https://substackcdn.com/image/fetch/$s_!C_Ep!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd1c12a8d-7a92-45aa-a56e-94a40ac1a6de_2773x1536.jpeg)](https://substackcdn.com/image/fetch/$s_!C_Ep!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd1c12a8d-7a92-45aa-a56e-94a40ac1a6de_2773x1536.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!76Pp!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe72f42d3-6642-43f2-ab4f-ef45c2f23dfb_2943x2036.jpeg)](https://substackcdn.com/image/fetch/$s_!76Pp!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe72f42d3-6642-43f2-ab4f-ef45c2f23dfb_2943x2036.jpeg)

Let’s have an input time series consisting of three sequential sinusoids.

[![](https://substackcdn.com/image/fetch/$s_!S1uX!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fde52dc7f-9d61-477f-8734-b9bac661958a_2878x821.jpeg)](https://substackcdn.com/image/fetch/$s_!S1uX!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fde52dc7f-9d61-477f-8734-b9bac661958a_2878x821.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!ANkO!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe968a42a-e26a-4588-aa62-80da05671a44_2384x3029.jpeg)](https://substackcdn.com/image/fetch/$s_!ANkO!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe968a42a-e26a-4588-aa62-80da05671a44_2384x3029.jpeg)

The magnitude and group delay (derived from phase response) of the example IIR filter looks like this:

[![](https://substackcdn.com/image/fetch/$s_!Sml1!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff1009fc7-3b6d-427b-9d7e-bf18c1e37928_2514x2827.jpeg)](https://substackcdn.com/image/fetch/$s_!Sml1!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff1009fc7-3b6d-427b-9d7e-bf18c1e37928_2514x2827.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!Qk0N!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa59a4f3d-faf6-4fdb-a1aa-518d86809b1e_3000x1757.jpeg)](https://substackcdn.com/image/fetch/$s_!Qk0N!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa59a4f3d-faf6-4fdb-a1aa-518d86809b1e_3000x1757.jpeg)Note that these two windowed sinusoids reversed order in the output. The IIR filter did not just attenuate. It “altered” time.

Non-linear phase causes different frequency components to experience different delays. Some applications don’t care about linear phase, but most applications do. IIR filters must be carefully designed to mitigate this issue. Cascading unitary gain IIR filters to correct prior phase shifts is one tactic.

 **Excluding the two major issues of non-linear phase and stability,** IIR filters are objectively better than FIR filters in every way.

  * Cheaper.

  * More power efficient.

  * Sharper frequency response.

  * More passband gain and rejection band attenuation with far fewer memory taps.




[![](https://substackcdn.com/image/fetch/$s_!bxTI!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc23eb941-f9b5-4396-a570-47c4256fd569_333x231.jpeg)](https://substackcdn.com/image/fetch/$s_!bxTI!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc23eb941-f9b5-4396-a570-47c4256fd569_333x231.jpeg)A 5th order IIR filter clearly outperforming an 30th order (6x memory requirement!) in magnitude response. 

### [7.c] DFE

On the surface, Decision Feedback Equalizers (DFE) may look like digital IIR filters.

[![](https://substackcdn.com/image/fetch/$s_!lbgM!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fecea4ccd-fb6a-4a43-8c45-027ae7c374e1_738x459.png)](https://substackcdn.com/image/fetch/$s_!lbgM!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fecea4ccd-fb6a-4a43-8c45-027ae7c374e1_738x459.png)

This is not correct. DFE filters use a slicer that make a hard decision on what value the input should be quantized to. IIR filters do not do this!

DFE filters are non-linear but quite powerful at eliminating reflections, AKA post-cursors.

[![](https://substackcdn.com/image/fetch/$s_!hk7t!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6b87ff3f-e0e0-4e6e-ae03-ec981051e108_1642x1245.png)](https://substackcdn.com/image/fetch/$s_!hk7t!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6b87ff3f-e0e0-4e6e-ae03-ec981051e108_1642x1245.png)

[![](https://substackcdn.com/image/fetch/$s_!6Pwt!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F18599117-a47c-4e01-88da-6732c87c3205_1626x1186.png)](https://substackcdn.com/image/fetch/$s_!6Pwt!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F18599117-a47c-4e01-88da-6732c87c3205_1626x1186.png)

A major weakness of DFE filters is the timing challenges in high-speed systems.

The benefit relative to a (much larger tap) FIR filter is that DFE taps do not amplify noise.

### [7.e] CTLE

Continuous-Time Linear Equalization filters are broadband analog filters.

[![](https://substackcdn.com/image/fetch/$s_!PShI!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb73100a2-ca03-42c0-b90a-256cf1b548f9_854x641.png)](https://substackcdn.com/image/fetch/$s_!PShI!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb73100a2-ca03-42c0-b90a-256cf1b548f9_854x641.png)

CTLE offers large gain at Nyquist leading to excellent performance, if and only if tuned properly. Designing a 50 GHz wide broadband filter that works across PVT is difficult. Tuning the filter once silicon hits lab is a time-consuming process.

High-speed (224G) designs often have multiple CTLE stages and tuning mechanisms. 

[![](https://substackcdn.com/image/fetch/$s_!PM2G!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffe0cd3aa-9b05-489e-95f7-45f9aeca8728_1252x694.png)](https://substackcdn.com/image/fetch/$s_!PM2G!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffe0cd3aa-9b05-489e-95f7-45f9aeca8728_1252x694.png)

[![](https://substackcdn.com/image/fetch/$s_!cx40!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdb44d0d4-1b04-46bb-b336-fa507cd5cc00_1243x711.png)](https://substackcdn.com/image/fetch/$s_!cx40!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdb44d0d4-1b04-46bb-b336-fa507cd5cc00_1243x711.png)

Variable capacitance, inductance, and resistance banks can program the CTLE.

[![](https://substackcdn.com/image/fetch/$s_!f4fH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1ae6d157-8291-48ba-8125-894bbcdada0f_850x244.png)](https://substackcdn.com/image/fetch/$s_!f4fH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1ae6d157-8291-48ba-8125-894bbcdada0f_850x244.png)Example programmable capacitance bank.

## [8] Statistical Estimation Theory

Suppose you already have an equalization filter calculated based on a channel estimate. Re-estimating the channel is expensive. What if you could adapt the filter using a feedback system based on error rate?

### [8.a] Basics

[![](https://substackcdn.com/image/fetch/$s_!V2Pf!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F69ca9fa0-819c-4123-afbb-c59045df6dca_407x206.png)](https://substackcdn.com/image/fetch/$s_!V2Pf!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F69ca9fa0-819c-4123-afbb-c59045df6dca_407x206.png)

Recall that forward-error-correction (FEC) schemes allow the system to know how many errors are in a block and where they are located, to an extent. Thus, the desired signal d(k) can be usually estimated well. 

In scenarios which the error rate is high, FEC will be unable to reconstruct the desired signal, and the error signal blows up. The typical response to this is for a higher layer (MAC, PCS/PMA) to ratchet down code-rate, adding more parity bits to the payload. FEC is not the only layer of parity checking. More can be enabled on an as-needed basis.

There are two important families of adaptation algorithms:

  1. Least-Mean Squares (LMS)

    1. Fast, cheap, and simple.

    2. Does not require matrix inversion or correlation functions.

    3. The standard which all other algos are compared against.

  2. Maximum Likelihood Sequence Detection

    1. Uses statistical properties of the sequence to predict the most likely sequence.

    2. Has many variants such as Viterbi, DSFE, and Soft-Output MLSD.




The simplest way of comparing these two is that LMS assumes each symbol is a gaussian while MLSD estimates each symbol’s probability distribution.

[![](https://substackcdn.com/image/fetch/$s_!Ntjh!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd458dcc4-f4b8-43fc-8f1f-e65a207b8d95_4000x2593.jpeg)](https://substackcdn.com/image/fetch/$s_!Ntjh!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd458dcc4-f4b8-43fc-8f1f-e65a207b8d95_4000x2593.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!qlNU!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fac116d21-4d3b-4f40-8098-e671cefef324_2534x2593.jpeg)](https://substackcdn.com/image/fetch/$s_!qlNU!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fac116d21-4d3b-4f40-8098-e671cefef324_2534x2593.jpeg)

### [8.b] LMS

[![](https://substackcdn.com/image/fetch/$s_!gAoE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbd32fcd0-e0af-414d-bf42-62ae1f935b8b_2958x2377.jpeg)](https://substackcdn.com/image/fetch/$s_!gAoE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbd32fcd0-e0af-414d-bf42-62ae1f935b8b_2958x2377.jpeg)

Notice how simple the computational load is.

Vector multiply, subtraction, and complex conjugate. 

### [8.c] MLSD

[Viterbi is the most common form of MLSD](https://en.wikipedia.org/wiki/Viterbi_algorithm).

[![](https://substackcdn.com/image/fetch/$s_!z8nR!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0f514e9e-05f7-4acc-8b79-975ea0801459_1262x875.png)](https://substackcdn.com/image/fetch/$s_!z8nR!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0f514e9e-05f7-4acc-8b79-975ea0801459_1262x875.png)

It can be visualized with a Trellis diagram.

Here is a 50-minute lecture that explains this better than I ever could.

Note that a full implementation of Viterbi is quite expensive in terms of power.

There are tricks to reduce the computational load.

[![](https://substackcdn.com/image/fetch/$s_!5z5C!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb608b51b-6d45-48fe-9167-d279e21acf43_1259x701.png)](https://substackcdn.com/image/fetch/$s_!5z5C!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb608b51b-6d45-48fe-9167-d279e21acf43_1259x701.png)

## [9] PLL and CDR

A phased-locked loop is a simple circuit that tracks an input frequency.

[![](https://substackcdn.com/image/fetch/$s_!Db1W!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F01f070c6-3436-428a-93bb-0a10e86db7f9_2880x1703.png)](https://substackcdn.com/image/fetch/$s_!Db1W!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F01f070c6-3436-428a-93bb-0a10e86db7f9_2880x1703.png)

It consists of three major components:

  1. [A phase detector (PD)](https://en.wikipedia.org/wiki/Phase_detector)

  2. A low-pass filter to remove high-frequency noise.

  3. A voltage-controlled oscillator. (VCO)




A feedback divider can be added to enable programmable output frequencies.

[![](https://substackcdn.com/image/fetch/$s_!ssbW!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa0e067c2-4aff-4831-918a-365d95e09904_938x370.png)](https://substackcdn.com/image/fetch/$s_!ssbW!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa0e067c2-4aff-4831-918a-365d95e09904_938x370.png)

The primary purpose of a PLL is to clean up noise coming from the external reference clock (Quartz, SiTime). All other clocks are derived from the global PLL (GPLL).

[![](https://substackcdn.com/image/fetch/$s_!aVmP!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fde3b0c83-456b-4e59-8fd8-1071ea17ee0f_414x293.gif)](https://substackcdn.com/image/fetch/$s_!aVmP!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fde3b0c83-456b-4e59-8fd8-1071ea17ee0f_414x293.gif)

SerDes embed the clock into the data stream.

[![](https://substackcdn.com/image/fetch/$s_!f8Fg!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1c4313f1-b878-4cfb-8aa7-072ba175014d_1894x817.png)](https://substackcdn.com/image/fetch/$s_!f8Fg!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1c4313f1-b878-4cfb-8aa7-072ba175014d_1894x817.png)

 **Most modern CDRs are PLL based.** This leads to confusion sometimes.

[![](https://substackcdn.com/image/fetch/$s_!QMf5!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc4139f62-1dd9-4159-b0d2-c681c8f2c758_1920x1456.png)](https://substackcdn.com/image/fetch/$s_!QMf5!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc4139f62-1dd9-4159-b0d2-c681c8f2c758_1920x1456.png)

The CDR usually is a PLL, with some modifications. From the perspective of the CDR, the input is a clock with noise in the form of data.

[![](https://substackcdn.com/image/fetch/$s_!B-Yo!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fec4536f1-6e99-499c-972d-53284502a2ac_1893x1426.png)](https://substackcdn.com/image/fetch/$s_!B-Yo!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fec4536f1-6e99-499c-972d-53284502a2ac_1893x1426.png)

Oversimplified, a CDR is a special PLL with a high-performance phase-detector circuit to compensate for missing clock edges.

[![](https://substackcdn.com/image/fetch/$s_!xMVH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb43f4241-04bf-44e3-b903-8bc6afe23032_1927x703.png)](https://substackcdn.com/image/fetch/$s_!xMVH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb43f4241-04bf-44e3-b903-8bc6afe23032_1927x703.png)

I have screenshotted many excellent slides from Professor Sam Palermo of Texas A&M university. If you are interested in learning more, check out his course website:

<https://people.engr.tamu.edu/spalermo/ecen720.html>

[![](https://substackcdn.com/image/fetch/$s_!Rx_S!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8c8dd707-9089-41dd-b932-bd52052d8de0_298x448.jpeg)](https://substackcdn.com/image/fetch/$s_!Rx_S!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8c8dd707-9089-41dd-b932-bd52052d8de0_298x448.jpeg)

## [10] Advanced Tactics

There exist certain advanced (expensive) tactics to boost communication system performance and capacity. These methods are generally cost bound.

### [10.a] MIMO

Reflections are usually considered to be undesired interference…

[![](https://substackcdn.com/image/fetch/$s_!Jy8n!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F25d16fbb-e365-4b5e-9b59-32586b96da66_850x531.png)](https://substackcdn.com/image/fetch/$s_!Jy8n!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F25d16fbb-e365-4b5e-9b59-32586b96da66_850x531.png)Example of the multipath effect.

…but what if it was possible to encode different data streams to each signal path? 

It is possible, at the cost of system complexity.

[![](https://substackcdn.com/image/fetch/$s_!0-WR!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb348443a-503c-41f8-8035-a3fe573616cb_753x487.webp)](https://substackcdn.com/image/fetch/$s_!0-WR!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb348443a-503c-41f8-8035-a3fe573616cb_753x487.webp)

Suppose you have a system where each side has four independent antennas. This system will have a 4x4 [spatial correlation matrix.](https://en.wikipedia.org/wiki/Spatial_correlation_%28wireless%29)

The rank of this matrix determines how many independent data streams can be encoded onto the multipath channel. Eigenvalue strength indicates how reliable the path is.

[![](https://substackcdn.com/image/fetch/$s_!vYk-!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1aba7d60-6fb7-465b-8fb1-89ce17e07c6e_579x451.webp)](https://substackcdn.com/image/fetch/$s_!vYk-!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1aba7d60-6fb7-465b-8fb1-89ce17e07c6e_579x451.webp)

[![](https://substackcdn.com/image/fetch/$s_!VK4N!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F784ff262-0dc5-41ff-9985-51d3dfcef9f4_281x180.jpeg)](https://substackcdn.com/image/fetch/$s_!VK4N!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F784ff262-0dc5-41ff-9985-51d3dfcef9f4_281x180.jpeg)

It is very common for the primary reflection from the ground to be strong enough to achieve rank2 MIMO operation.

### [10.b] Beamforming (Phased Arrays)

Suppose you have an array of evenly spaced antennas, each of which has independently controllable phase.

[![](https://substackcdn.com/image/fetch/$s_!J-OU!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F266ee38e-9d9b-49cf-8f3d-fe7cb5a03a6c_759x515.png)](https://substackcdn.com/image/fetch/$s_!J-OU!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F266ee38e-9d9b-49cf-8f3d-fe7cb5a03a6c_759x515.png)

The antennas could be place in arbitrary locations within 3D space but that makes things difficult. 

Usually, antennas are evenly spaced in a line (Uniform Linear Array) or a 2-D grid (Rectangular array). Circular arrays might sound nice but the math for those involve Bessel function calculus. A nightmare to work with.

 **Sidenote:** _The most epic phased array I have ever seen is the SpaceX Starlink dish. They actually used a non-rectangular array geometry!_

[![](https://substackcdn.com/image/fetch/$s_!A1mt!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4708e05a-7780-4137-aaf9-cb81649722ff_2155x1862.webp)](https://substackcdn.com/image/fetch/$s_!A1mt!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4708e05a-7780-4137-aaf9-cb81649722ff_2155x1862.webp) Uniform Linear Array diagram. 

[![](https://substackcdn.com/image/fetch/$s_!6r4K!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F218d74fa-dd73-416d-806c-449d6364c3d8_744x667.png)](https://substackcdn.com/image/fetch/$s_!6r4K!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F218d74fa-dd73-416d-806c-449d6364c3d8_744x667.png)Sample ULA beampatterns. More elements means sharper beams.

[![](https://substackcdn.com/image/fetch/$s_!Bpw4!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1e65952f-6461-4fab-862d-805f64515514_746x1112.png)](https://substackcdn.com/image/fetch/$s_!Bpw4!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1e65952f-6461-4fab-862d-805f64515514_746x1112.png)Example rectangular array beampattern.

[![](https://substackcdn.com/image/fetch/$s_!t7RZ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F672d7e75-a190-4d24-a0f6-27737d617a7b_900x457.png)](https://substackcdn.com/image/fetch/$s_!t7RZ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F672d7e75-a190-4d24-a0f6-27737d617a7b_900x457.png)

Intuitively, each digitally steerable (in terms of phase) array element is a FIR filter tap. Phased arrays filter in spatial frequency. 

Due to extraordinary costs (CapEx and electricity), phased arrays have largely been limited to military applications.

  * Each digitally steerable array element needs its own high-speed ADC and DAC.

  * Hybrid solutions with analog phase shifters exist, sacrificing performance and resolution in favor of reducing cost. Difficult to calibrate.

  * A lot of compute is needed to process all this data in baseband.




[![](https://substackcdn.com/image/fetch/$s_!yNFi!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2574c176-d360-4fe2-8493-88ba831c4dbd_619x316.jpeg)](https://substackcdn.com/image/fetch/$s_!yNFi!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2574c176-d360-4fe2-8493-88ba831c4dbd_619x316.jpeg)[United States military radar phased array from 1962.](https://www.darpa.mil/about-us/timeline/phased-arrays)

One of the major differences between 4G/LTE and 5G is the extent in which phased arrays are used. 4G/LTE is limited to 8 array elements while large 5G macro cells can reach 64 elements. Larger phased arrays offer more beamforming gain (translates to better SNR) and sharper beams (attenuates aggressor signals from other basestations, phones, noise sources).

### [10.c] Multiple Carriers (Multiplexing)

Multiplexing (also known as carrier aggregation) is a method of combining multiple communication channels in the same system. 

This method is common in wireless and optical communications as they are both narrowband.

[![](https://substackcdn.com/image/fetch/$s_!aZB0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3100198a-031a-40e2-a568-9f3478de1f8d_1024x562.png)](https://substackcdn.com/image/fetch/$s_!aZB0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3100198a-031a-40e2-a568-9f3478de1f8d_1024x562.png)

[![](https://substackcdn.com/image/fetch/$s_!QMdi!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fffc84533-a591-4a3c-b30e-dd9ed09d1e4d_512x290.png)](https://substackcdn.com/image/fetch/$s_!QMdi!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fffc84533-a591-4a3c-b30e-dd9ed09d1e4d_512x290.png)

[![](https://substackcdn.com/image/fetch/$s_!91QA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd621a718-21dd-4b0d-91f3-24474aebcea5_512x512.webp)](https://substackcdn.com/image/fetch/$s_!91QA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd621a718-21dd-4b0d-91f3-24474aebcea5_512x512.webp)

Multiplexing adds significant cost on the analog/RF/optical front-end. High-speed muxes and the necessary analog filters must be carefully designed to ensure neighboring carriers do not interfere with one another.

This cost issue is why Wi-Fi has avoided supporting carrier aggregation for a long time. Wi-Fi 7 is introduces this feature. This is why your home Wi-Fi (almost certainly not v7) has separate 2.4 GHz and 5 GHz networks. 

## [11] Practical Walkthrough

Let’s go over a practical walkthrough of several communication standards to get a high-level understanding of design tradeoffs. **Intuition is key!**

### [11.a] 400/800Gbps Electrical Ethernet (IEEE 802.3ck)

400GBps Ethernet is built using four lanes of 106Gbps PAM4 SerDes.

[![](https://substackcdn.com/image/fetch/$s_!amW1!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F47561eef-6f96-46bb-a766-8d9e84a2d3b5_2368x1161.png)](https://substackcdn.com/image/fetch/$s_!amW1!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F47561eef-6f96-46bb-a766-8d9e84a2d3b5_2368x1161.png)

The physical module is called “Attachment Unit Interface” or AUI.

There are many specifications for various physical connectors.

[![](https://substackcdn.com/image/fetch/$s_!n16G!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F13708b40-12f9-43ef-a50f-cf75110032bc_2274x1224.png)](https://substackcdn.com/image/fetch/$s_!n16G!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F13708b40-12f9-43ef-a50f-cf75110032bc_2274x1224.png)

800 GbE is built using 8 lanes with a fatter connector.

Electrical specifications are where things get interesting.

[![](https://substackcdn.com/image/fetch/$s_!we5Z!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F42b1a880-6cd3-4ba6-b0bf-5cbb0ec7a94c_1147x933.png)](https://substackcdn.com/image/fetch/$s_!we5Z!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F42b1a880-6cd3-4ba6-b0bf-5cbb0ec7a94c_1147x933.png)

As you can see, maximum voltage (differential pk-pk voltage) is 1200 mV. There is also a minimum diff pk-pk voltage that typically falls around 400 mV. The actual number varies based on the package design and is associated with R_peak and V_f.

RLM is a linearity measurement. (1 means perfect linearity)

[![](https://substackcdn.com/image/fetch/$s_!Bm4R!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F179caba2-6af4-414c-8b8d-feeb65f811c7_2349x1177.png)](https://substackcdn.com/image/fetch/$s_!Bm4R!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F179caba2-6af4-414c-8b8d-feeb65f811c7_2349x1177.png)

Transmitter jitter limits are also defined. This is time-domain noise.

[![](https://substackcdn.com/image/fetch/$s_!jXlW!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9f7adbed-61ee-4ac6-a0fd-5adc9209142d_410x180.gif)](https://substackcdn.com/image/fetch/$s_!jXlW!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9f7adbed-61ee-4ac6-a0fd-5adc9209142d_410x180.gif)

For the receiver, the compliance requirements are simpler to understand.

[![](https://substackcdn.com/image/fetch/$s_!r2Ig!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F59e09dd3-eb98-4c80-a3e4-006f02be4ef2_2359x1332.png)](https://substackcdn.com/image/fetch/$s_!r2Ig!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F59e09dd3-eb98-4c80-a3e4-006f02be4ef2_2359x1332.png)

Receivers must tolerate sinusoidal jitter (pure tone noise) at specified frequencies and magnitudes. This is called JTOL.

Interference tolerance (ITOL) is also required. Think of ITOL as broadband random noise. (full spectrum, not a pure sinusoidal tone)

PCIe differs from Ethernet is several ways:

  * Requires spread-spectrum clocking.

  * Much stricter JTOL.

  * Lower (better/stricter) required pre-FEC bit-error-rate.

  * Strict latency requirements.

  * Rigid reach specification. (no sub-specs)




[![](https://substackcdn.com/image/fetch/$s_!yewy!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4d9340d4-81c6-4a68-a1d3-fa4e29566ea9_1280x525.jpeg)](https://substackcdn.com/image/fetch/$s_!yewy!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4d9340d4-81c6-4a68-a1d3-fa4e29566ea9_1280x525.jpeg)There are many flavors of Ethernet and Optical (Common Electrical Interface) specifications for a variety of applications. PCIe spec is much more rigid.

### [11.b] 5G (3GPP Release 15)

5G has a very high error tolerance compared to wireline systems. Block-level error under 5% is considered good enough.

[![](https://substackcdn.com/image/fetch/$s_!DBFl!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1a2342b4-eddc-44d9-a7fe-3d49c6f35895_838x1153.png)](https://substackcdn.com/image/fetch/$s_!DBFl!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1a2342b4-eddc-44d9-a7fe-3d49c6f35895_838x1153.png)

Basestations are constantly re-scheduling your Modulation Coding Scheme (MCS) based on channel conditions. This happens on the order of tens of milliseconds. You could go from QAM256 (8 bit per symbol) all the way to QAM4 (2 bit per symbol). Data density (code rate) also dynamically adjusts.

[![](https://substackcdn.com/image/fetch/$s_!ud1t!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fab47e3da-5316-4987-8df4-22301e2155ae_1870x884.webp)](https://substackcdn.com/image/fetch/$s_!ud1t!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fab47e3da-5316-4987-8df4-22301e2155ae_1870x884.webp)

Nearly all modern wireless systems use Orthogonal Frequency-Division Multiplexing (OFDM). This method places thin orthogonal sub-carriers within a frequency band to mitigate frequency-selective fading. 

[![](https://substackcdn.com/image/fetch/$s_!vCP9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F06fad779-4ffc-4284-b870-550fa1b060b9_507x191.jpeg)](https://substackcdn.com/image/fetch/$s_!vCP9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F06fad779-4ffc-4284-b870-550fa1b060b9_507x191.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!3gAR!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa7654fa5-ae65-4d89-be7e-91f6b5645ea8_319x158.jpeg)](https://substackcdn.com/image/fetch/$s_!3gAR!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa7654fa5-ae65-4d89-be7e-91f6b5645ea8_319x158.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!gyUS!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5582dd2f-7780-47c5-961f-6801fdab1f29_564x284.jpeg)](https://substackcdn.com/image/fetch/$s_!gyUS!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5582dd2f-7780-47c5-961f-6801fdab1f29_564x284.jpeg)

Bad sub-carriers are simply un-allocated by the scheduler.

One major drawback of OFDM is that the signal must be digitally pre-constructed (burns power) and tends to generate high peak-to-average-power ratio (PAPR) time-domain signals.

[![](https://substackcdn.com/image/fetch/$s_!hFrU!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5ea1d478-9a0b-4a23-85dd-cc991641e7ca_534x408.png)](https://substackcdn.com/image/fetch/$s_!hFrU!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5ea1d478-9a0b-4a23-85dd-cc991641e7ca_534x408.png)

High PAPR signals place strain on RF components, blowing up cost. Advances in RFFE technology allowed OFDM to become more prominent starting with 4G/LTE. Prior to that, CDMA, SC-FDMA, and TDMA.

[![](https://substackcdn.com/image/fetch/$s_!Xvka!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1a68502c-c1be-4d80-838b-0a7bfaff6945_329x153.png)](https://substackcdn.com/image/fetch/$s_!Xvka!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1a68502c-c1be-4d80-838b-0a7bfaff6945_329x153.png)

### [11.c] Long-Haul Optics (Open ZR+)

Open ZR+ is a long-haul optical specification. Think about the optical lines that go across buildings instead of within a building.

[![](https://substackcdn.com/image/fetch/$s_!N6kx!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa7088fa6-0391-4ed8-bea8-db18fe536969_1020x1104.png)](https://substackcdn.com/image/fetch/$s_!N6kx!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa7088fa6-0391-4ed8-bea8-db18fe536969_1020x1104.png)

Very sensitive to PPM. Power also needs to be tightly controlled across temperatures.

[![](https://substackcdn.com/image/fetch/$s_!a3zL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa3f4a2a3-069c-476a-868c-cc89a19bcc2f_258x195.jpeg)](https://substackcdn.com/image/fetch/$s_!a3zL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa3f4a2a3-069c-476a-868c-cc89a19bcc2f_258x195.jpeg)

Long-haul optical lasers are so sensitive, they often use piezoelectric heaters/coolers to keep the diode temperature within a tight tolerance.

[![](https://substackcdn.com/image/fetch/$s_!KuL6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdd5175f4-59c9-4382-847f-7f5fc68a6240_996x718.png)](https://substackcdn.com/image/fetch/$s_!KuL6!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdd5175f4-59c9-4382-847f-7f5fc68a6240_996x718.png)

Pre-FEC BER is very high. This means Open ZR+ prefers to use a very heavy FEC and is tolerant of the latency penalty.

## [12] Bringing balance to your system.

Every communication system specification exists for a reason. There must be balance in the context of design objectives and market conditions.

 **Transmit power** is limited by interference concerns, amplifier non-linearity, noise figure of low-level devices, an expected operating temperature.

 **Bandwidth** is limited by regulations (channel coherence too) in wireless, and material quality (PCB, connectors, package, cable, backplane) in wireline.

 **Modulation method (PAM vs QAM) and order** is linked to phase noise and SNR requirements.

 **Pre-FEC target bit-error-rate** **and FEC scheme** are decided based on latency requirements, re-transmit tolerance, and digital logic power targets. 

[![](https://substackcdn.com/image/fetch/$s_!JMwk!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F60f1ce54-adee-4e95-a595-e20c9fc7c87f_1180x238.png)](https://substackcdn.com/image/fetch/$s_!JMwk!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F60f1ce54-adee-4e95-a595-e20c9fc7c87f_1180x238.png)

## [13] The Optics Section

Optical systems have some extra vocabulary that I found to be confusing. Some terms like TIA are ambiguous, especially in non-technical contexts. TIA is a fairly simple circuit that many sell-side financial notes treat as some kind of optical-only component.

The last section of this chapter, [13.d], has a mental model I hope you find useful.

### [13.a] Short Reach: DSP, LRO, and LPO

[![](https://substackcdn.com/image/fetch/$s_!tNG0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe1614c97-9bed-4811-a127-1bed4c3f14c3_2812x1521.png)](https://substackcdn.com/image/fetch/$s_!tNG0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe1614c97-9bed-4811-a127-1bed4c3f14c3_2812x1521.png)

oDSP means Optical Digital Signal Processor. Intuitively, it is a SerDes converter.

The **host-side** SerDes is a normal electrical SerDes.

The **line-side SerDes** is a special electrical SerDes designed to **drive sensitive** optical circuits. It is still an electrical SerDes! Optics stuff has not started yet.

oDSP chips are expensive and consume a lot of power. Somewhere in the neighborhood on ~10-15W per module.

LRO and LPO are methods of removing the oDSP, partially or completely.

[![](https://substackcdn.com/image/fetch/$s_!zXdw!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F460c4e92-50b4-4f43-aa09-b29b2f987142_1536x839.jpeg)](https://substackcdn.com/image/fetch/$s_!zXdw!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F460c4e92-50b4-4f43-aa09-b29b2f987142_1536x839.jpeg)

In LRO, there is still a chip re-timing the transmit waveform. Thus, transmit optics get a clean signal as an input. 

LPO removes the oDSP entirely, attempting to drive and receive directly from the photonics IC (PIC). LPO is also sometimes referred to as direct linear drive. Nvidia is rumored to use this in Rubin rack-scale systems.

[![](https://substackcdn.com/image/fetch/$s_!mE1A!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8dff4862-c694-4151-b733-a9d9515c3d05_1030x1200.png)](https://substackcdn.com/image/fetch/$s_!mE1A!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8dff4862-c694-4151-b733-a9d9515c3d05_1030x1200.png)Marvell makes a lot of money from oDSP. LPO is terrifying for them.

### [13.b] Long Reach: ZR, ZR+, and DWDM

[![](https://substackcdn.com/image/fetch/$s_!A-w6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F846538ef-d2f2-4b6f-a903-4263d503a0bd_778x337.jpeg)](https://substackcdn.com/image/fetch/$s_!A-w6!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F846538ef-d2f2-4b6f-a903-4263d503a0bd_778x337.jpeg)

ZR is an old long-haul optical standard that can only reach 80-120 kilometers.

ZR+ is an enhanced version. More modulation options are available, and the power limits are raised.

[![](https://substackcdn.com/image/fetch/$s_!750j!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F47fc6ca8-af11-43fa-9bf9-ad97c87457cb_1252x308.png)](https://substackcdn.com/image/fetch/$s_!750j!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F47fc6ca8-af11-43fa-9bf9-ad97c87457cb_1252x308.png)

Modulation order and SNR requirements are directly linked.

[![](https://substackcdn.com/image/fetch/$s_!GW5z!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F11a97a2f-d25a-4ece-af21-5a354046c3bf_734x514.png)](https://substackcdn.com/image/fetch/$s_!GW5z!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F11a97a2f-d25a-4ece-af21-5a354046c3bf_734x514.png)

More optical carriers mean more data transmission on the same fiber.

[![](https://substackcdn.com/image/fetch/$s_!KsQ3!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F25cbe62c-4c14-480c-8038-30bb227984f1_999x649.png)](https://substackcdn.com/image/fetch/$s_!KsQ3!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F25cbe62c-4c14-480c-8038-30bb227984f1_999x649.png)

Fiber-optic cables have a frequency response that looks like this:

[![](https://substackcdn.com/image/fetch/$s_!rqwt!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F776456e7-e9c5-4f05-9ce2-60810128d7d4_541x272.webp)](https://substackcdn.com/image/fetch/$s_!rqwt!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F776456e7-e9c5-4f05-9ce2-60810128d7d4_541x272.webp)

Plotted against wavelength, not frequency. Easy enough to convert. These bands can be sliced up such that the narrowband assumption holds. (negligible frequency selective fading)

[Optical bandwidth is nuts. ](https://edgeoptic.com/kb_article/dwdm-channel-chart/) 100 GHz and maintaining narrowband model. LOL

[![](https://substackcdn.com/image/fetch/$s_!o9vB!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9a5a8580-d7d4-475b-8f04-25015febedfa_1258x607.png)](https://substackcdn.com/image/fetch/$s_!o9vB!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9a5a8580-d7d4-475b-8f04-25015febedfa_1258x607.png)No guard bands required. LAMO

DWDM requires high-precision optical components, lasers in particular. Expensive gear.

### [13.c] TIA, Drivers, and Optical Modulators

TIA stands for [Transimpedance amplifier. ](https://en.wikipedia.org/wiki/Transimpedance_amplifier)

[![](https://substackcdn.com/image/fetch/$s_!aklJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffad6e2a7-8fc0-46e5-a644-284fa2facf61_275x183.png)](https://substackcdn.com/image/fetch/$s_!aklJ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffad6e2a7-8fc0-46e5-a644-284fa2facf61_275x183.png)

It’s just an amplifier that isolates each end and carefully mitigates parasitics. For example, photodiodes have parasitic capacitance that need to be mitigated. TIA’s are common circuits, not some special optical system component. 

Optical systems need highly linear gain and noise compensation. This is why TIAs are so popular.

Some good resources:

<https://www.ti.com/document-viewer/lit/html/SSZTBC4>

<https://ultimateelectronicsbook.com/op-amp-transimpedance-amplifier/>

<https://en.wikipedia.org/wiki/Transimpedance_amplifier>

* * *

Optical drivers are actually quite simple. It took me forever to find a good diagram to explain this well…

[![](https://substackcdn.com/image/fetch/$s_!CV1Q!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F640bd747-0312-4a6e-9f07-69d3285ed1f2_2142x714.png)](https://substackcdn.com/image/fetch/$s_!CV1Q!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F640bd747-0312-4a6e-9f07-69d3285ed1f2_2142x714.png)

Allow me to simplify….

[![](https://substackcdn.com/image/fetch/$s_!GNJB!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F64d982a6-a465-47b9-89b7-2497c0f6b741_1786x838.png)](https://substackcdn.com/image/fetch/$s_!GNJB!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F64d982a6-a465-47b9-89b7-2497c0f6b741_1786x838.png)

* * *

Optical modulation is the tricky part. In a nutshell, the photodiode light output needs to be precisely polarized. Lacking performance will result in symbols interfering with one another. Phase stability is also critical as these systems use QAM modulation.

Remember, phase noise is public enemy #1!

[![](https://substackcdn.com/image/fetch/$s_!gtaE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbef19b8f-0282-4dfe-bfd1-84136674545e_460x312.jpeg)](https://substackcdn.com/image/fetch/$s_!gtaE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbef19b8f-0282-4dfe-bfd1-84136674545e_460x312.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!fsbF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9fc6219f-e02e-41be-8df4-2bd6ac98edd3_600x257.gif)](https://substackcdn.com/image/fetch/$s_!fsbF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9fc6219f-e02e-41be-8df4-2bd6ac98edd3_600x257.gif)

[![](https://substackcdn.com/image/fetch/$s_!JrYu!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F64d0a0fe-cd94-47ae-9d8b-c30ec8531a32_489x298.jpeg)](https://substackcdn.com/image/fetch/$s_!JrYu!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F64d0a0fe-cd94-47ae-9d8b-c30ec8531a32_489x298.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!-blE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe708c28b-6d95-4334-b868-a1a628d399ee_489x368.jpeg)](https://substackcdn.com/image/fetch/$s_!-blE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe708c28b-6d95-4334-b868-a1a628d399ee_489x368.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!gNOg!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F24f26d8f-f8f8-4a4b-b42a-d8e7d60e0907_685x625.png)](https://substackcdn.com/image/fetch/$s_!gNOg!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F24f26d8f-f8f8-4a4b-b42a-d8e7d60e0907_685x625.png)

### [13.d] PIC: Electrical —> Things Before Diode —> Diode

Optics is a new subject for me. I found the following mental model to be helpful for my own understanding.

 **On the transmit side:**

  1. Normal electrical SerDes goes from device (ASIC, NIC, Switch) to an oDSP chip.

  2. The oDSP chip re-times the signal and outputs a special, ultra-short-reach, calibrated electrical SerDes.

  3. A special driver chip (photonic IC [PIC] built on a special process node) takes in this special SerDes, converts it to common mode (single-ended signal), and powers a very sensitive laser. 

  4. The laser outputs light that then passes through a variety of polarizers, lenses, and optical modulators.

    1. These optical components are precise and temperature sensitive.

    2. Use of exotic crystals and materials. 




**On the receive side:**

  1. Optical front-end de-modulation.

  2. A photodiode converts the light into an electrical signal.

  3. A TIA (large die area to ensure excellent linearity) amplifies the signal.

  4. The oDSP converts this calibrated/tuned electrical SerDes into regular standards-based electrical SerDes.

  5. Host chip (ASIC, NIC, Switch) receives the signal.




## [14] Investment Time! 

I am hyper-bullish optics. The latest generation of high-speed SerDes (224G) is the last generation that can function with active electrical cables.

Loss at Nyquist is too high. Even the most expensive materials are barely good enough. Bump-pitch itself is becoming a major limitation.

[![](https://substackcdn.com/image/fetch/$s_!lS1Y!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1a3bc5fb-3043-4f2f-aeab-fb9034cc3fad_2292x1306.png)](https://substackcdn.com/image/fetch/$s_!lS1Y!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1a3bc5fb-3043-4f2f-aeab-fb9034cc3fad_2292x1306.png)

[![](https://substackcdn.com/image/fetch/$s_!ZZPn!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9f2fa770-9fde-442d-affd-b659a1b7a883_2274x1309.png)](https://substackcdn.com/image/fetch/$s_!ZZPn!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9f2fa770-9fde-442d-affd-b659a1b7a883_2274x1309.png)

[![](https://substackcdn.com/image/fetch/$s_!SR9V!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2ce5b5df-9798-4c8e-9417-5663947d45f0_2323x1294.png)](https://substackcdn.com/image/fetch/$s_!SR9V!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2ce5b5df-9798-4c8e-9417-5663947d45f0_2323x1294.png)

[![](https://substackcdn.com/image/fetch/$s_!nKXG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff724819b-9b25-4f2b-9645-6a4d8708116e_2304x1291.png)](https://substackcdn.com/image/fetch/$s_!nKXG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff724819b-9b25-4f2b-9645-6a4d8708116e_2304x1291.png)

[![](https://substackcdn.com/image/fetch/$s_!bT6E!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb684f70f-6514-4571-b643-84f4f746be03_2326x1290.png)](https://substackcdn.com/image/fetch/$s_!bT6E!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb684f70f-6514-4571-b643-84f4f746be03_2326x1290.png)

There was some debate on if 224G should be at PAM4 (with a doubling of the bandwidth) or PAM6 (only 50% more bandwidth gen-on-gen). It ended up that material science and clever design advances allowed for PAM4 to continue use.

QAM modulation is not really viable for broadband wireline systems due to phase noise (jitter) constraints. 448G cannot be PAM4. The reflections beyond 70-80GHz are too nasty.

Right now, IEEE is debating between PAM6 and PAM8. My guess is PAM8 will be necessary, but we shall see.

Remember, a higher Nyquist frequency means more insertion loss.

Higher modulation order means higher SNR requirements to meet the same pre-FEC bit-error-rate.

448G reach is going to be dramatically worse than 224G. Active electrical cables won’t be enough for most applications.

Optics is the future. Co-packaged optics in particular.

At the time of writing, I hold the following positions.

[![](https://substackcdn.com/image/fetch/$s_!yVCG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F21496e76-3d87-4e2b-81bd-00673f5cb5f7_447x1038.png)](https://substackcdn.com/image/fetch/$s_!yVCG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F21496e76-3d87-4e2b-81bd-00673f5cb5f7_447x1038.png)

The following securities will be discussed. I am going to give you a brief overview of each so that you can **DO YOUR OWN RESEARCH.**

[![](https://substackcdn.com/image/fetch/$s_!zJn5!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa9f41bb6-1c3a-4c25-8534-24b787ddd622_744x453.png)](https://substackcdn.com/image/fetch/$s_!zJn5!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa9f41bb6-1c3a-4c25-8534-24b787ddd622_744x453.png)**Note:** _Some stocks are listed as a “maybe” because I have not made up my mind yet._

I take ethics very seriously. You know what I own, average price, weight, and my future plans (within reason). Maximum transparency is my self-imposed compliance policy.

I do not make any money from this Substack, consulting/expert calls, sponsorships, or other financial conflicts of interest. This is my hobby. How I choose to invest **my own money.**

[![](https://substackcdn.com/image/fetch/$s_!-jzr!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb3ae319c-8578-4e7e-acee-dea108d71fef_1551x1161.png)](https://substackcdn.com/image/fetch/$s_!-jzr!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb3ae319c-8578-4e7e-acee-dea108d71fef_1551x1161.png)

I have a (very fun) dayjob in industry and take great care to keep it separate from what goes on here. Making money on the side is an automatic firing offence. I’m probably going to get fired anyway if/when <employer> finds out… but want to have a chance at talking my way out of the situation.

 **You know my biases. Go make up your own mind.**

### [14.a] Core Ideas

Core ideas are stocks that I find genuinely interesting.

#### [14.a.1] Broadcom

Broadcom covered their incredible co-packaged optics solution in detail at Hot Chips 2024.

[![Hot Chips 2024: Irrational Recap](https://substackcdn.com/image/fetch/$s_!HPuv!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe1c7faec-bb00-4052-a4e4-0be3f604b0d1_1024x1024.jpeg)

#### Hot Chips 2024: Irrational Recap

[Irrational Analysis](https://substack.com/profile/135313705-irrational-analysis)·September 2, 2024[Read full story](https://irrationalanalysis.substack.com/p/hot-chips-2024-irrational-recap)](https://irrationalanalysis.substack.com/p/hot-chips-2024-irrational-recap)

The most based marketing guy I ever seen. Maximum confidence. Excellent understanding of technical material.

[![](https://substackcdn.com/image/fetch/$s_!fmDx!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb46f865f-e30d-4460-9321-1d7ff1fd092c_1411x901.png)](https://substackcdn.com/image/fetch/$s_!fmDx!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb46f865f-e30d-4460-9321-1d7ff1fd092c_1411x901.png)

They showed a real system with all ports populated and active. This is to induce maximum synchronous noise. 

[![](https://substackcdn.com/image/fetch/$s_!LGLT!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4fff03ad-c7e5-4398-b5d7-10d911e3dbe5_2202x1167.png)](https://substackcdn.com/image/fetch/$s_!LGLT!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4fff03ad-c7e5-4398-b5d7-10d911e3dbe5_2202x1167.png)

TDECQ is a measure of eye linearity.

[![](https://substackcdn.com/image/fetch/$s_!bss3!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1bd394d6-8fa2-4efb-98f0-85ae924b9014_1035x463.jpeg)](https://substackcdn.com/image/fetch/$s_!bss3!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1bd394d6-8fa2-4efb-98f0-85ae924b9014_1035x463.jpeg)

These results are pretty good! Not good enough for commercialization, but not far off from that milestone either.

Recall that the goal of forward-error correction (FEC) is to achieve error-free operation.

[![](https://substackcdn.com/image/fetch/$s_!tGwN!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F362fc7cb-807f-421d-8d40-2802db058c1a_2517x1390.png)](https://substackcdn.com/image/fetch/$s_!tGwN!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F362fc7cb-807f-421d-8d40-2802db058c1a_2517x1390.png)

They show all the ports using a production quality sample. This is not some hack-ed demo unit built with non-standard (uneconomical) methods.

Broadcom even shows raw FEC symbol data.

[![](https://substackcdn.com/image/fetch/$s_!luIJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc74f01bd-3000-45f8-aed1-83e278f7d26d_2524x1372.png)](https://substackcdn.com/image/fetch/$s_!luIJ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc74f01bd-3000-45f8-aed1-83e278f7d26d_2524x1372.png)Note: These results are without PPM. Minimal async noise. A real system will have PPM induced from each attached device with its own refclk.

 **Nobody else shares this information publicly.**

Customers can easily run a lighter FEC and still achieve error-free operation. Higher effective bitrate and lower latency.

[![](https://substackcdn.com/image/fetch/$s_!H0k3!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7d9d33b6-ae2b-49b1-a137-9151d2fa950e_766x960.png)](https://substackcdn.com/image/fetch/$s_!H0k3!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7d9d33b6-ae2b-49b1-a137-9151d2fa950e_766x960.png)Visual approximation of Manish Mehta.

I believe [AVGO 0.00%↑](https://substack.com/discover/stocks/AVGO) will ramp CPO switches in H2 2025. Q1 2026 at the latest. They are already enabling CPO TPUs for Google.

#### [14.a.2] Marvell

[MRVL 0.00%↑](https://substack.com/discover/stocks/MRVL) is a terrible long-term investment. **LPO (direct linear drive) and CPO are going to severely harm their oDSP business.**

Honestly, Marvell is just an inferior version of Broadcom. 

But… the Amazon Trainium 2 ramp is nuts. Great swing-trade opportunity.

[Amazon is forcing Anthropic to use Trainium 2.](https://www.anthropic.com/news/anthropic-amazon-trainium) This is round-tripped revenue as far as I am concerned. If the chip was good, Amazon would not need to use financial coercion to gain customers.

[![](https://substackcdn.com/image/fetch/$s_!4-0x!,w_1456,c_limit,f_auto,q_auto:good,fl_lossy/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8386ca5a-2cf0-48c5-b9d5-897aa3040bb6_640x640.gif)](https://substackcdn.com/image/fetch/$s_!4-0x!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8386ca5a-2cf0-48c5-b9d5-897aa3040bb6_640x640.gif)Visual approximation of Amazon force-feeding Trainum 2 to Anthropic. **Talk about GPU poor!**

#### [14.a.3] Fabrinet

[FN 0.00%↑](https://substack.com/discover/stocks/FN) is an outsourced manufacturer of optics. They are good at what they do. Low cost (cost plus model) manufacturing that protects customer IP. Dedicated staff and segregated cleanroom space.

Think of this company as the TSMC of optical integration, but with much worse margins.

I have traded in and out of this stock multiple times. The issue is sentiment swings the stock easily. Fabrinet has 100% share of Nvidia 1st-party optical modules. As Nvidia qualifies other vendors modules, people panic and stock tanks. 

[![](https://substackcdn.com/image/fetch/$s_!JbEu!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2f4ebef1-b8d4-40e2-b589-01b4edbd366c_1035x924.png)](https://substackcdn.com/image/fetch/$s_!JbEu!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2f4ebef1-b8d4-40e2-b589-01b4edbd366c_1035x924.png)

Long-term, I like this company. CPO is going to drive a ton of business to them. The less sophisticated competitors will not be able to keep up and maintain the level of quality/precision required for CPU.

For now, pods and hedge funds are trading the crap out of this ticker based on Nvidia supply chain whispers. Tread lightly. 

Also, most of their manufacturing capacity is in Thailand. Big advantage if Trump follows through on anti-China tariffs.

[![](https://substackcdn.com/image/fetch/$s_!codB!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe89c84c3-95df-4fd1-b38c-9cabd12c4970_1768x1314.png)](https://substackcdn.com/image/fetch/$s_!codB!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe89c84c3-95df-4fd1-b38c-9cabd12c4970_1768x1314.png)

 _(I have made a nice profit on each FN trade but not the maximum profit)_

#### [14.a.4] Ciena

[CIEN 0.00%↑](https://substack.com/discover/stocks/CIEN) is a pure-play for long-haul optics buildout. Semianalysis called them out as a big winner for the multi-datacenter training cluster ramp and I agree. 

I was not able to attend the recent OFC in San Jose (despite being local) but a friend did send me pictures from the Ciena booth. They have kickass performance. Really impressive stuff. Sorry but can’t share the pics.

The key concept you need to understand is there is a ton of “dark fiber” out there. Fiber cables that could handle much more data by lighting up more wavelengths but are inactive. The channel (glass cable) supports more capacity! All you need is to add some Ciena gear on each end. AI multi-datacenter training is the demand catalyst Ciena has been waiting for. 

[![](https://substackcdn.com/image/fetch/$s_!bsF7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa59e2c62-6f50-486a-8a61-4b374b8d155f_1030x988.png)](https://substackcdn.com/image/fetch/$s_!bsF7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa59e2c62-6f50-486a-8a61-4b374b8d155f_1030x988.png)They have been waiting a long fucking time.

Ciena is one of the poster childs of the DotCom bubble. They have been eating shit for all these years. It’s probably a bad omen that [CIEN 0.00%↑](https://substack.com/discover/stocks/CIEN) is a viable investment idea again.

[![](https://substackcdn.com/image/fetch/$s_!PSfB!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9d552d45-b8b6-4519-b734-1372473cdbe3_640x640.gif)](https://substackcdn.com/image/fetch/$s_!PSfB!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9d552d45-b8b6-4519-b734-1372473cdbe3_640x640.gif)

#### [14.a.5] Keysight

I have shilled Keysight with dedicated posts multiple times. 

[![Keysight FQ4 2024](https://substackcdn.com/image/fetch/$s_!q_P3!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbf158b87-c516-492d-8166-95cc2c6dd677_1438x2541.jpeg)

#### Keysight FQ4 2024

[Irrational Analysis](https://substack.com/profile/135313705-irrational-analysis)·November 20, 2024[Read full story](https://irrationalanalysis.substack.com/p/keysight-fq4-2024)](https://irrationalanalysis.substack.com/p/keysight-fq4-2024)

[![Screaming Buy: $KEYS](https://substackcdn.com/image/fetch/$s_!SGFv!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F42b7458c-0388-426a-b493-10a86599198e_709x416.png)

#### Screaming Buy: $KEYS

[Irrational Analysis](https://substack.com/profile/135313705-irrational-analysis)·August 21, 2024[Read full story](https://irrationalanalysis.substack.com/p/screaming-buy-keys)](https://irrationalanalysis.substack.com/p/screaming-buy-keys)

It’s almost a quarterly tradition.

This is the most asymmetric risk/reward stock I can think of in semiconductors right now. Let me list out all the positive and negative catalysts/headwinds/tailwinds.

  * Negative

    * Wireless might implode further. (extremely unlikely in my opinion)

  * Positive

    * Correlated to R&D intensity of AI ASIC development.

      * As more companies (startups, hyperscalers) try to design their own chips, they have to buy expensive Keysight gear.

      *  **For example, you can see Amazon has a high-end 90GHz Keysight UXR real-time oscilloscope for Trainium 2 development.**

[![](https://substackcdn.com/image/fetch/$s_!PvYl!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F217ae8e1-385b-4511-be54-23f70290eb58_1320x2086.jpeg)](https://substackcdn.com/image/fetch/$s_!PvYl!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F217ae8e1-385b-4511-be54-23f70290eb58_1320x2086.jpeg)

    * Cable and connector manufactures (Amphenol and friends) buy high-end Keysight Vector Network Analyzers to characterize individual cables.

    * Very strong SaaS business. Each Keysight box comes with literally dozens of SaaS upgrades, tools, and features.

    * Optical proliferation (CPO included) supercharges Keysight’s high-margin revenue growth!

      * Double the SerDes… line side and host side.

      * R&D intensity for all the additional components (PIC, TIA, driver, …) and the module itself (package and PCB s-parameter analysis). 

    * Ultra-powerful moat built with superior engineering. A true earned monopoly in high-speed electrical and communication system test equipment.




Is this stock going to the moon? No.

But the risk is very low, and reward is medium. Asymmetric outcome.

#### [14.a.6] SiTime

Doug (Fabricated Knowledge and now Semianalysis) has a huge overview on [SITM 0.00%↑](https://substack.com/discover/stocks/SITM).

[![](https://substackcdn.com/image/fetch/$s_!tEdM!,w_56,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2Fac6587ae-db17-41fa-b25f-7dc0b7c601be_1000x1000.png)Fabricated KnowledgeIt's High Time to look at SiTimeRead more3 years ago · 28 likes · 2 comments · Doug O'Laughlin](https://www.fabricatedknowledge.com/p/its-high-time-to-look-at-sitime?utm_source=substack&utm_campaign=post_embed&utm_medium=web)

This is without a doubt my favorite Fabricated Knowledge piece. 

Summary for the lazy:

  * Every chip needs a timing reference. (refclk)

    * Traditionally, this is a quartz crystal.

    * Silicon-based MEMS (SiTime) is a disruptive technology.

  * Advantages:

    * Smaller footprint.

    * Lower power.

    * Highly programmable.

  * Disadvantages:

    * Market inertia (everyone comfortable with quartz).

    * Terrible jitter performance.

    * Datasheets that try to fucking gaslight you.




[![](https://substackcdn.com/image/fetch/$s_!cmU4!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fae525a9c-b142-44c4-8ca9-96a3399dcd79_1351x696.png)](https://substackcdn.com/image/fetch/$s_!cmU4!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fae525a9c-b142-44c4-8ca9-96a3399dcd79_1351x696.png)It is easy to source quartz solutions that have sub 50 fs phase noise across 12K to 20M integration. Even with all this cheating, SiTime still catastrophically loses.

[![](https://substackcdn.com/image/fetch/$s_!IQjb!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa9d6ad8c-c58d-4a90-93ab-4e8b3e647409_1066x1509.png)](https://substackcdn.com/image/fetch/$s_!IQjb!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa9d6ad8c-c58d-4a90-93ab-4e8b3e647409_1066x1509.png)

[![](https://substackcdn.com/image/fetch/$s_!mLjQ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F38303426-5a34-4ff3-b123-cdd05507610c_1306x1147.png)](https://substackcdn.com/image/fetch/$s_!mLjQ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F38303426-5a34-4ff3-b123-cdd05507610c_1306x1147.png)

[![](https://substackcdn.com/image/fetch/$s_!AVb8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4221440c-cd69-4d6d-81d8-6e446402ba8c_1036x811.png)](https://substackcdn.com/image/fetch/$s_!AVb8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4221440c-cd69-4d6d-81d8-6e446402ba8c_1036x811.png)

 **I have read hundreds, if not thousands of datasheets for many components from many vendors. SiTime is the only company that has ever tried to gaslight and manipulate me in the datasheet.**

Every CDR has different bandwidth and frequency response. The two pages of assumptions (cheating) SiTime used to manipulate their results are not valid!

It is the customers prerogative to add/model PLL jitter filtering. 

If the same (incorrect) methodology was applied to competing quartz crystals, their numbers would be lower too.

This behavior is appalling and inexcusable.

[![](https://substackcdn.com/image/fetch/$s_!2AOr!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd4f4d11c-d3a4-4211-b5ec-d793807096d0_220x227.gif)](https://substackcdn.com/image/fetch/$s_!2AOr!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd4f4d11c-d3a4-4211-b5ec-d793807096d0_220x227.gif)

* * *

Now let’s take a look at the stock chart to figure out what is going on…

[![](https://substackcdn.com/image/fetch/$s_!YnuD!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9522c085-7cb4-477c-99f2-4a46d9f6b3ee_1041x919.png)](https://substackcdn.com/image/fetch/$s_!YnuD!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9522c085-7cb4-477c-99f2-4a46d9f6b3ee_1041x919.png)

[![](https://substackcdn.com/image/fetch/$s_!Ha9l!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9214dad6-44ec-45a1-b8e1-ca865fa9c811_2379x1305.png)](https://substackcdn.com/image/fetch/$s_!Ha9l!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9214dad6-44ec-45a1-b8e1-ca865fa9c811_2379x1305.png)Read the fine print. SiTime investor relations is scummy.

 **SiTime’s largest customer is Apple. Their own investor materials try to hide how incredibly dependent they are on this one massive customer.**

The above stupid rectangle plot would be hilarious if they actually included Apple.

Previously, SiTime was in the iPhone, but they got kicked out due to inert gas issues.

[![](https://substackcdn.com/image/fetch/$s_!rjIS!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F47410083-74e7-4e46-a782-f6fcec25e039_1174x1495.png)](https://substackcdn.com/image/fetch/$s_!rjIS!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F47410083-74e7-4e46-a782-f6fcec25e039_1174x1495.png)[Source](https://www.fabricatedknowledge.com/p/its-high-time-to-look-at-sitime)

SiTime still is not back in the latest iPhones. A lot of the run-up to the stock is pods and supply-chain whisper degens betting that they made it back in.

Apple is rolling out their own modem next year. iPhones with Apple modem will likely have double the SiTime content, if not more.

 **The downside to SiTime stock is clear.** Large market participants (hedge funds) are wagering that SiTime gets significant Apple revenue acceleration in 2025. Based on conversations with finance-land friends, the consensus is that [SITM 0.00%↑](https://substack.com/discover/stocks/SITM) is at fair value assuming Apple revenue ramp. 

**The upside to SiTime stock is not obvious and super interesting.** Nvidia is using them for GB200 NVLink systems. I found this news to be surprising given how dogshit the jitter performance is. But… there is a real engineering reason driving this decision.

[![](https://substackcdn.com/image/fetch/$s_!_H95!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F04249d25-3cd4-4a22-a490-f461189860d0_903x663.png)](https://substackcdn.com/image/fetch/$s_!_H95!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F04249d25-3cd4-4a22-a490-f461189860d0_903x663.png)

Suppose you have a system where the refclk on both ends is SiTime, and thus programmable. If the system is using a proprietary interconnect and protocol, a special “please shift refclk PPM” packet could be sent to **ensure 0 effective system PPM.**

This is why Nvidia is using SiTime on GB200! I am 99% confident on this.

PPM and jitter both place strain on the receiver. In general, PPM is worse.

 **In a hypothetical scenario where you have the option to guarantee 0 PPM at the cost of higher refclk jitter, you take that trade every time.**

I believe SiTime has an incredible opportunity in datacenter with proprietary electrical links and optical links. Have a small position and opportunistically buying more.

#### [14.a.7] Lumen

[LUMN 0.00%↑](https://substack.com/discover/stocks/LUMN) is a steaming pile of debt-laden garbage.

[![](https://substackcdn.com/image/fetch/$s_!fXeW!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4938964c-67e5-42eb-8a03-6cf2adca3898_1768x952.png)](https://substackcdn.com/image/fetch/$s_!fXeW!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4938964c-67e5-42eb-8a03-6cf2adca3898_1768x952.png)

Through a series of unfortunate events, a hilarious quantity of uneconomical, underutilized, dark fiber came into the possession of a single corporation.

[![](https://substackcdn.com/image/fetch/$s_!aSAo!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F98f83edd-3edd-4c54-831d-690701fc5faf_1072x942.png)](https://substackcdn.com/image/fetch/$s_!aSAo!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F98f83edd-3edd-4c54-831d-690701fc5faf_1072x942.png)

The market cap is $8B but it would cost “$150B to re-create” the fiber network. What does that tell you about the economic value and capital structure of this company?

Let’s zoom in on the stock chart.

[![](https://substackcdn.com/image/fetch/$s_!_QI5!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff8b7638d-b8e1-45f5-b983-18d9b08070d5_1483x1270.png)](https://substackcdn.com/image/fetch/$s_!_QI5!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff8b7638d-b8e1-45f5-b983-18d9b08070d5_1483x1270.png)

Hyperscalers are signing large leasing deals to use Lumen’s dark fiber network for multi-datacenter training. 

You could be sophisticated and calculate valuation using a complicated financial model that accounts for all the debt, convertible notes, lease terms, blah blah blah.

Or you could just degen trade this garbage like an unhinged monkey.

 _Embrace your inner primate…_ 🙈

#### [14.a.8] Tower Semi and Global Foundries

Photonics chips (PIC) need a special process node to work… because physics reasons that I don’t understand.

TSMC is not the leader in this space. In fact, TSMC photonics and RF process nodes are pretty mediocre. Almost nobody uses them.

[TSEM 0.00%↑](https://substack.com/discover/stocks/TSEM) and [GFS 0.00%↑](https://substack.com/discover/stocks/GFS) are the two leaders in specialty photonic process technology. Given how bullish I am on optics, I want to buy shares in one or maybe both but can’t make up my mind. 

Here are some quick opinions based on surface-level research. Still looking into this in the background.

[![](https://substackcdn.com/image/fetch/$s_!cYPy!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F56c2c15a-80c1-4dea-b025-1ca555ef9c78_2761x1324.png)](https://substackcdn.com/image/fetch/$s_!cYPy!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F56c2c15a-80c1-4dea-b025-1ca555ef9c78_2761x1324.png)

[![](https://substackcdn.com/image/fetch/$s_!6r1P!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2d5107d2-cc22-4f3f-b19d-34b1190c0aad_2278x1267.png)](https://substackcdn.com/image/fetch/$s_!6r1P!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2d5107d2-cc22-4f3f-b19d-34b1190c0aad_2278x1267.png)

Both are protected from tariff concerns which is nice.

And both have 300mm wafer photonics processes. (Tower a bit late)

[![](https://substackcdn.com/image/fetch/$s_!U6i_!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0cab450c-aabc-4d14-805c-a10ebcc7c60b_1783x376.png)](https://substackcdn.com/image/fetch/$s_!U6i_!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0cab450c-aabc-4d14-805c-a10ebcc7c60b_1783x376.png)

### [14.b] Secondary Ideas

Secondary ideas are mostly here because various subscribers have requested coverage. I’m trying to pre-empt the comments section.

#### [14.b.1] Maxlinear

If SiTime is the best Fabricated Knowledge post (to date), the [MXL 0.00%↑](https://substack.com/discover/stocks/MXL) post might be the most… unfortunate/unlucky. 

Reaaaally unfortunate timing.

[![](https://substackcdn.com/image/fetch/$s_!tEdM!,w_56,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2Fac6587ae-db17-41fa-b25f-7dc0b7c601be_1000x1000.png)Fabricated KnowledgeBeaten Down Semiconductor Could be AI PlayRead more2 years ago · 72 likes · 5 comments · Doug O'Laughlin](https://www.fabricatedknowledge.com/p/beaten-down-semiconductor-could-be?utm_source=substack&utm_campaign=post_embed&utm_medium=web)

[![](https://substackcdn.com/image/fetch/$s_!0Sez!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa035286c-21e3-45e9-a745-95bb0debad97_1039x934.png)](https://substackcdn.com/image/fetch/$s_!0Sez!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa035286c-21e3-45e9-a745-95bb0debad97_1039x934.png)

They made a PAM4 oDSP to compete with Marvell and Broadcom.

[![](https://substackcdn.com/image/fetch/$s_!2Rk5!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F10096447-ca9e-4797-b894-fa09cd338ee0_1707x430.png)](https://substackcdn.com/image/fetch/$s_!2Rk5!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F10096447-ca9e-4797-b894-fa09cd338ee0_1707x430.png)

It’s supposedly decent. Heard rumors of good power characteristics, despite the Samsung Foundry SF5 process node.

Unfortunately, every other business segment Maxlinear has kinda died.

Rumor is that Intel is the main customer for the MXL oDSPs. Will others choose this product over [MRVL 0.00%↑](https://substack.com/discover/stocks/MRVL) and [AVGO 0.00%↑](https://substack.com/discover/stocks/AVGO)?

What happens when Nvidia makes their own?

What about [ALAB 0.00%↑](https://substack.com/discover/stocks/ALAB)?

In my opinion, [MXL 0.00%↑](https://substack.com/discover/stocks/MXL) has inverted risk/reward. It’s not worth it.

Could be wrong though. I was wrong about [ALAB 0.00%↑](https://substack.com/discover/stocks/ALAB) … 

#### [14.b.2] Applied Optoelectronics

[AAOI 0.00%↑](https://substack.com/discover/stocks/AAOI) is friends with Microsoft. Strong correlation with that hyperscaler capex.

They also have a patent lawsuit Eoptolink. 

[![](https://substackcdn.com/image/fetch/$s_!dh7b!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F43d4f714-8f3e-42ea-9046-955af36ff278_2356x1314.png)](https://substackcdn.com/image/fetch/$s_!dh7b!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F43d4f714-8f3e-42ea-9046-955af36ff278_2356x1314.png)

Vertically integrated so better margins than a Fabrinet.

[![](https://substackcdn.com/image/fetch/$s_!8zHe!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4b4aebe0-2200-4daa-b767-75ec1d3444e0_2344x1291.png)](https://substackcdn.com/image/fetch/$s_!8zHe!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4b4aebe0-2200-4daa-b767-75ec1d3444e0_2344x1291.png)

And allegedly better performance from custom crystal growth.

 _(I have no idea how to independently verify this)_

[![](https://substackcdn.com/image/fetch/$s_!dI-p!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9c3a69b2-1702-4675-b4ee-4a1e22686dc4_2361x1303.png)](https://substackcdn.com/image/fetch/$s_!dI-p!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9c3a69b2-1702-4675-b4ee-4a1e22686dc4_2361x1303.png)

Pretty pictures. Nice.

[![](https://substackcdn.com/image/fetch/$s_!C_BI!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd3c01e94-7f7f-47a2-be65-fc4867d32c65_2343x1306.png)](https://substackcdn.com/image/fetch/$s_!C_BI!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd3c01e94-7f7f-47a2-be65-fc4867d32c65_2343x1306.png)

Oh….

The vast majority of employees and manufacturing capacity is in PRC. I guess this is how Eoptolink allegedly stole IP.

This stock is decisively in the “too hard bucket” for me. 

#### [14.b.3] MediaTek

Google is desperately trying to free themselves from the clutches of Broadcom. MediaTek made their own 224G SerDes IP and won a mini-TPU program. It’s real. I have multiple engineering and financial-land sources who have corroborated this info. 

Might be a good trade idea. 

#### [14.b.4] Lumentum

[![](https://substackcdn.com/image/fetch/$s_!vTsh!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0b5533f5-28ac-44eb-81f6-5325ceb79f03_2059x1240.png)](https://substackcdn.com/image/fetch/$s_!vTsh!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0b5533f5-28ac-44eb-81f6-5325ceb79f03_2059x1240.png)

So… also vertically integrated like [AAOI 0.00%↑](https://substack.com/discover/stocks/AAOI)?

[![](https://substackcdn.com/image/fetch/$s_!BMPj!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F75547c4b-2325-4581-bb4f-eaf9b7a201cf_2074x1215.png)](https://substackcdn.com/image/fetch/$s_!BMPj!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F75547c4b-2325-4581-bb4f-eaf9b7a201cf_2074x1215.png)

Yea… they are making similar claims to those of AAOI. Bare-die oDSP co-packaging is interesting. Should save 2-4 dB.

At least the manufacturing is in Thailand (not PRC).

[![](https://substackcdn.com/image/fetch/$s_!z6OE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F92af7184-85f9-4e87-9ec8-b3e20f1a18e3_2067x1243.png)](https://substackcdn.com/image/fetch/$s_!z6OE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F92af7184-85f9-4e87-9ec8-b3e20f1a18e3_2067x1243.png)

Ehh too hard. Can’t be bothered.

#### [14.b.5] Nittobo

Nittobo makes high-quality glass fiber with [incredibly low dissipation factor.](https://www.nittobo.co.jp/eng/business/electronicmaterials/ne-glass.htm)

It is allegedly much better than all the competition.

#### [14.b.6] Innolight/Eoptolink

Hyperscalers like to bypass the Nvidia+Fabrinet tax and just get optical modules for cheap from these two PRC companies.

Given the impending sanctions from a Trump administration, I don’t think these are good stock ideas but macro and geopolitics is not my speciality.

I still believe that co-packaged optics will be a Fabrinet exclusive growth driver because of the following reasons:

  1. Innolight/Eoptolink lack the sophistication. (until they allegedly/theoretically steal the IP)

  2. Broadcom, Nvidia, and Ayar Labs will want to protect their IP and just pay Fabrinet.




#### [14.b.7] Coherent

They seem to specialize in phase modulated lasers.

[![](https://substackcdn.com/image/fetch/$s_!G2E7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5f75d13a-b495-403f-b6c8-2bcc3869895f_2332x1279.png)](https://substackcdn.com/image/fetch/$s_!G2E7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5f75d13a-b495-403f-b6c8-2bcc3869895f_2332x1279.png)

Similar vertical integration claims.

Gross margins are meaningfully better.

[![](https://substackcdn.com/image/fetch/$s_!H3RL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F011a81eb-aa8e-4cd1-b170-6922a649ed5e_2325x1327.png)](https://substackcdn.com/image/fetch/$s_!H3RL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F011a81eb-aa8e-4cd1-b170-6922a649ed5e_2325x1327.png)

Hmm.. they make OCS too. Interesting.

You know what… I like what I’m seeing here. 

There is also the (former lamo) Lattice CEO that peaced out to become Coherent CEO.

Maybe they really do have differentiation. 

Probably will buy some shares next week.

<https://www.coherent.com/content/dam/coherent/site/en/documents/investors/investor-presentations/2024/march-26/coherent-analyst-briefing-ofc-2024.pdf>

I might even write a dedicated follow-up post on Coherent. 

#### [14.b.8] Cogent Communications

[![](https://substackcdn.com/image/fetch/$s_!46_o!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6722a665-0c6b-4bc0-8d81-351f6f68644a_1881x1342.png)](https://substackcdn.com/image/fetch/$s_!46_o!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6722a665-0c6b-4bc0-8d81-351f6f68644a_1881x1342.png)Off to a bad start.

[![](https://substackcdn.com/image/fetch/$s_!HB9i!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F43152cda-4d6e-4f5e-9076-dcc2a5ce7611_1879x1404.png)](https://substackcdn.com/image/fetch/$s_!HB9i!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F43152cda-4d6e-4f5e-9076-dcc2a5ce7611_1879x1404.png)

[![](https://substackcdn.com/image/fetch/$s_!wygb!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8f0b3018-af25-4088-bd2f-3584022fa4ec_1900x1317.png)](https://substackcdn.com/image/fetch/$s_!wygb!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8f0b3018-af25-4088-bd2f-3584022fa4ec_1900x1317.png)

A boring version of Lumen. 

Not worth my time. Moving on.

### [14.c] Niche

Miscellaneous stocks you probably should not touch.

#### [14.c.1] Cisco/Arista Warning

These two are somewhat linked.

Cisco has been pursuing a failed SaaS strategy, neglecting their core business.

Everyone else (Broadcom, Nvidia, Arista, Celestica, Marvell) is running circles around Cisco in the core switching and routing markets. No AI boom for you!

[![](https://substackcdn.com/image/fetch/$s_!L2sG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F451e1f88-815a-4992-9a8c-68606b47d8dc_1048x952.png)](https://substackcdn.com/image/fetch/$s_!L2sG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F451e1f88-815a-4992-9a8c-68606b47d8dc_1048x952.png)

One of the financial friends I talk to (let’s call him Mr. Book Value) brought up that [CSCO 0.00%↑](https://substack.com/discover/stocks/CSCO) is super cheap and even has a mini Ciena inside it. 

[![](https://substackcdn.com/image/fetch/$s_!IaR0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdd70ad14-4f19-486d-97b8-17ac9903020a_627x627.jpeg)](https://substackcdn.com/image/fetch/$s_!IaR0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdd70ad14-4f19-486d-97b8-17ac9903020a_627x627.jpeg)Cisco has the dumbest ADs at the San Jose airport. How about you focus on your core business instead of spamming abstract art advertisements.?

I still don’t think that makes Cisco a worthwhile investment. Too much garbage and clueless management to justify dumpster diving. 

* * *

Arista does not make their own silicon. They buy Broadcom chips and build a switch and software platform around them.

Every quarter, they have this slide updated.

[![](https://substackcdn.com/image/fetch/$s_!Yklu!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffd63b94d-b63c-4ea6-80cc-587fbd535ec5_2347x1327.png)](https://substackcdn.com/image/fetch/$s_!Yklu!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffd63b94d-b63c-4ea6-80cc-587fbd535ec5_2347x1327.png)

Cisco is a no from me dawg.

[![](https://substackcdn.com/image/fetch/$s_!Bj0j!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2076c09c-9e71-4ba0-950c-8f065db8dc10_466x260.gif)](https://substackcdn.com/image/fetch/$s_!Bj0j!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2076c09c-9e71-4ba0-950c-8f065db8dc10_466x260.gif)

But so is [ANET 0.00%↑](https://substack.com/discover/stocks/ANET).

I cannot think of a reason why anyone would buy [ANET 0.00%↑](https://substack.com/discover/stocks/ANET) instead of [AVGO 0.00%↑](https://substack.com/discover/stocks/AVGO). Broadcom is more diversified, makes the important silicon, and has co-packaged optics IP. CPO can’t be good for Arista. Probably content loss?

Also, what prevents hyperscalers from buying white-box (semi-custom) switches from [CLS 0.00%↑](https://substack.com/discover/stocks/CLS) that are powered by Broadcom silicon?

Arista Networks is in a weird no-mans-land. Does not make sense to invest. Better options out there IMO. 

#### [14.c.2] Astera Labs (┛◉Д◉)┛彡┻━┻

I have covered [ALAB 0.00%↑](https://substack.com/discover/stocks/ALAB) multiple times and stand by that coverage despite getting crushed on my massive short position that went kaboom.

Still think this is a retarded bubble stock. I want to re-short in the same way bugs are attracted to zappers.

[![](https://substackcdn.com/image/fetch/$s_!vKWZ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F70aa2727-7f70-446c-b8ce-864ef0dcbe4f_1800x1800.webp)](https://substackcdn.com/image/fetch/$s_!vKWZ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F70aa2727-7f70-446c-b8ce-864ef0dcbe4f_1800x1800.webp)

I do want to highlight AYZ of Global Technology Research.

[![](https://substackcdn.com/image/fetch/$s_!mfNh!,w_56,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F072c35e6-dec5-4016-94f7-e8262d2dfbf7_197x197.png)Global Technology ResearchAstera Labs (ALAB US) – How Large is the GB200 Content Opportunity?Astera Labs has been a stock with intense battles between the bulls and bears: the bears are pessimistic about the reduced usage of its PCIe retimers in NVIDIA’s GB200 ( as compared to DGX); while the bulls are optimistic that its newly launched PCIe switch product will significantly increase the company's content dollar. Today, I will explain in details about Astera Labs’ content opportunity in NVIDIA’s AI servers…Read morea year ago · 6 likes · AYZ](https://globaltechresearch.substack.com/p/astera-labs-alab-us-how-large-is?utm_source=substack&utm_campaign=post_embed&utm_medium=web)

There are several important pieces of information in the above post that would have dramatically altered my investment thesis. I am now a paid sub to AYZ/GTR on my primary Substack account. Check him out. 

#### [14.c.3] Aeluma

This is a stock traded on OTC (over the counter) markets. 

One of the nice things about running a newsletter is I get to meet new people and learn about things I never would have encountered otherwise.

Someone has brought Aeluma to my attention multiple times. **By default, I have a strong prejudice against OTC listed companies. The probability of fraud is much higher than a regular exchanged listed company.**

With that said, I have watched the Aeluma CEO present several times and this dude seems legit. Good vibes.

They guy likes to highlight multiple possible end-markets for Aeluma technology. He seems to be throwing possibilities at the wall and waiting for one to stick.

This is what got my attention.

[![](https://substackcdn.com/image/fetch/$s_!6wg7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc95f1e03-058e-4314-bec1-68b4385366a9_2512x1352.png)](https://substackcdn.com/image/fetch/$s_!6wg7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc95f1e03-058e-4314-bec1-68b4385366a9_2512x1352.png)

Aeluma claims to be working on the holy grail of silicon photonics. No hybrid bonding. No advanced packaging. Literally print the photonics stuff directly onto a pre-fabricated silicon wafer.

They have a DoD grant to work on this technology. 

[![](https://substackcdn.com/image/fetch/$s_!GSu4!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F19cfb95b-9ff0-4e4c-ab22-601c1c169939_1225x958.png)](https://substackcdn.com/image/fetch/$s_!GSu4!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F19cfb95b-9ff0-4e4c-ab22-601c1c169939_1225x958.png)

Which makes sense. Traditional photonic integration technology induces a lot of noise and loss. Military is willing to pay a large premium for lower noise floor.

The UC Sanda Barbara colab has [resulted in a paper](https://coldren.ece.ucsb.edu/sites/default/files/publications/indium_phosphide_photonic_integrated_circuits-_technology_and_applications-klamkin.pdf) that I found interesting.

(Aeluma CEO is a professor there)

[![](https://substackcdn.com/image/fetch/$s_!Pk_6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F75a59183-e12b-4c02-906c-9da3e8062fed_589x454.png)](https://substackcdn.com/image/fetch/$s_!Pk_6!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F75a59183-e12b-4c02-906c-9da3e8062fed_589x454.png)~5 dB gain is pretty good! Only 3 Gbps NRZ but still a good start.

[![](https://substackcdn.com/image/fetch/$s_!FERU!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F845c7c0a-95f7-418c-84e9-f499a4cae75e_1747x961.png)](https://substackcdn.com/image/fetch/$s_!FERU!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F845c7c0a-95f7-418c-84e9-f499a4cae75e_1747x961.png)

If they can successfully and heterogeneously add InGaAs layers to a normal CMOS wafer, they will have achieved the holy grail of co-packaged optics. 

**No package!**

Directly printing of photonic elements (laser, photodiodes, modulators) on a regular CMOS silicon wafer.

#### [14.c.4] Credo (LRO YOLO)

Credo has a LRO DSP with no customers. The stock seems to be a pod-boi meme of people gambling that this Dove DSP gets a customer. 

[![](https://substackcdn.com/image/fetch/$s_!9qft!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa1560004-b204-4e9e-ae61-69d9b0b95736_1713x688.png)](https://substackcdn.com/image/fetch/$s_!9qft!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa1560004-b204-4e9e-ae61-69d9b0b95736_1713x688.png)

It was released a year ago and still nobody has bit.

You may be thinking…. what prevents Marvell/Broadcom from tapeing out half of their existing oDSP solution and marketing it for LRO?

Nothing.

Still, it is possible a hyperscaler qualifies Credo active LRO cables for a project which leads to a revenue spike. 

Interesting gambling/trading idea. 

## [15] Existential/Philosophical Nonsense

The engineering/educational and financial/investment content is mostly over. I hope you learned something new.

Subscribe if you enjoy learning.

Subscribe

Share with others who would enjoy engineering-driven investment analysis.

[Share](https://irrationalanalysis.substack.com/p/a-background-proof-guide-on-communication?utm_source=substack&utm_medium=email&utm_content=share&action=share)

The rest of this post is going a bit off the rails. Philosophy, existential dread, and some of my core beliefs.

I have re-written this material several times. Maybe it is coherent (pun intended). Don’t care anymore. It’s time to publish and move on to other projects. 

**Note:** _Next post is on Tenstorrent and the state of AI hardware startups. It’s going to be great. Subscribe! Feed narcissism._

###  **[15.a] The Deeper Meaning of Multi-Datacenter Training Clusters**

Multi-Datacenter training AI clusters are supercomputers. 

Distributed supercomputers.

 **This is a terrible idea.** Throughout history, supercomputers have been co-located to avoid NUMA (non-uniform memory access), latency, and programming model challenges.

 **This is a terrible idea. Everyone is going for it anyway.**

What is happening right now flies in the face of decades of supercomputer history and theory.

The efficiency will be terrible. 

* * *

I have read every single Semianalysis piece. The multi-datacenter training post was informative and interesting, as usual.

But it also legitimately terrifying.

It’s not just some industry development.

 _Oh look, people are developing innovative fault tolerance and all-reduce methodologies…_

No no no.

This is a signal.

A signal that the AGI cultists (backed by corporate masters) have gone all in.

### [15.b] AGI Cultist Rocketship

I am convinced that a cult has developed in the San Fransico Bay Area. The population here is already brain damaged; multiple sigmas removed from normal.

[![](https://substackcdn.com/image/fetch/$s_!ktTz!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb379e962-1a7c-4078-929d-97cfaa9fa5e8_955x363.png)](https://substackcdn.com/image/fetch/$s_!ktTz!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb379e962-1a7c-4078-929d-97cfaa9fa5e8_955x363.png)[link](https://x.com/RichardMCNgo/status/1861450205109096847)

Ignore the acronym “AGI” for a moment. The above Tweet seems a little cult-ish… right?

[![](https://substackcdn.com/image/fetch/$s_!0RgS!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff7538efe-142f-48ae-bd72-e737b3c3e4b4_366x595.png)](https://substackcdn.com/image/fetch/$s_!0RgS!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff7538efe-142f-48ae-bd72-e737b3c3e4b4_366x595.png)

Why yes. What a reasonable interview question. _What will you do in the next three years, waiting for the machine god to come?_

[![](https://substackcdn.com/image/fetch/$s_!leNl!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F79566c1d-ad3b-4c91-97eb-729e6cfcc48b_867x986.png)](https://substackcdn.com/image/fetch/$s_!leNl!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F79566c1d-ad3b-4c91-97eb-729e6cfcc48b_867x986.png)[link](https://x.com/itsclivetime/status/1855704120495329667)

* * *

Many investors are concerned about silly things like “revenue”, and “ROI”. AGI cult does not care about such artificial constructs.

[![cult members boarding a large rocket, cyberpunk](https://substackcdn.com/image/fetch/$s_!biiu!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7f42492b-725e-4737-a791-5689d89a0368_1024x1024.jpeg)](https://substackcdn.com/image/fetch/$s_!biiu!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7f42492b-725e-4737-a791-5689d89a0368_1024x1024.jpeg)

The name of OpenAI’s CUDA replacement is Triton, named after the planet Neptune’s largest moon.

This is no coincidence. We are indeed going to a moon, but not the lame rock that orbits our pathetic planet.

AGI cult is building a rocketship. 

Maybe the rocket explodes. Maybe it arrives at Triton, but the [OKLO 0.00%↑](https://substack.com/discover/stocks/OKLO) nuclear reactor fails, resulting in everyone on board freezing to death on the lunar surface.

The rocket is under construction. From an investment perspective, this epic bubble (I really hope it’s a bubble…) is the opportunity of a lifetime.

Attempting to attach financial metrics to this rocket is foolish. It’s like trying to psychoanalyze a cult.

Get in or forever wonder what could have been.

* * *

Let’s move on from the AGI cult itself. They don’t really matter in a way. All of this crazy shit is happening because the cult has wealthy financial backers. **Follow the money.**

What are the hyperscaler’s plans? Why have the mega corps funded this cult?

### [15.c] Corporations are people…

As a failed United States presidential candidate, one said:

Corporations are people my friend.

For those who are not aware, the United States Supreme Court ruled in [Citizens United v. FEC](https://en.wikipedia.org/wiki/Citizens_United_v._FEC) that corporations are to be considered people for the purposes of campaign finance law.

I quite like this framework. Corporations **do** behave like individual people in a way.

Every corporation is an amalgamation of employees, biased towards those who have tenure. There is a natural selection that implicitly occurs. Some people stay at a company for 10, 20, even 30 years and become deeply engrained with the company culture. Others leave after 1-2 years.

Politics are also a major force within corporations. Just like how an individual city, state, or country have political views, so do corporations.

But what exactly is a corporation? Have you ever asked yourself this question?

* * *

 **Corporations are artificial constructs, created to distribute profits and liability/risk.**

One of the most famous early corporations is the E[ast India Company.](https://en.wikipedia.org/wiki/East_India_Company)

[![](https://substackcdn.com/image/fetch/$s_!IZIq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faf85ca2e-3b8e-43d9-a085-93e428b63337_750x422.webp)](https://substackcdn.com/image/fetch/$s_!IZIq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faf85ca2e-3b8e-43d9-a085-93e428b63337_750x422.webp)

Suppose you invest in a single trading ship. There is a real possibility the ship sinks and never returns. Thus, it makes sense to form a corporation that controls many ships and **distributes both risk and profits to the shareholders.**

Corporations have what is known as a [fiduciary duty to investors.](https://online.hbs.edu/blog/post/fiduciary-duty-to-investors)

In short, C-level executives (CEO, CFO) are **legally obligated** to act in the best interest of **shareholders** at all times.

* * *

Corporations track expenses in two broad categories:

  1. Operating Expenses (OpEx)

  2. Capital Expenditures (CapEx).




 **You are OpEx.** Take you base salary and multiply it by 1.25-1.4x to account for benefits to proximate your annual OpEx cost. _This is an HR rule-of-thumb. Often, financial value of benefits delivered to an employee are more than the cost due to tax breaks._

Are you really worth all that money? How many years until a semi-competent AI agent replaces you?

AI agents don’t sleep. They do not ask for time off. They work 24/7/365. They can rapidly communicate with other AI agents.

AI is a massive wave of deflation. A commoditization of basic intelligence. An incoming wave of OpEx efficiency. 

The invisible hand of the free market is coming to choke you.

This is the endgame. Whoever makes a reasonably competent AI agent first gets to slash their OpEx by 80% and sell a service with 90% gross margins to all the other corps.

A massive concentration of wealth and power is under way. Those who control the AI agents and the datacenters they reside in will control everything.

Many people who I respect have brought up the old telephone switchboard operators and lamp post lighters.

[![](https://substackcdn.com/image/fetch/$s_!juO5!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa6c8f6b9-bd4a-406a-a7c5-770187fd1d04_2930x2400.png)](https://substackcdn.com/image/fetch/$s_!juO5!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa6c8f6b9-bd4a-406a-a7c5-770187fd1d04_2930x2400.png)

[![](https://substackcdn.com/image/fetch/$s_!lBmx!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F23536d12-d97a-4265-9c40-623ec9f60358_236x328.jpeg)](https://substackcdn.com/image/fetch/$s_!lBmx!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F23536d12-d97a-4265-9c40-623ec9f60358_236x328.jpeg)

All of these people lost their jobs due to technological advancement. It was fine…. no need to worry about AI… look at the productivity gains…

 **This time is different.**

One job is not about get automated away. A large swath of jobs are about to get gutted, **in the name of OpEx efficiency, not productivity gains.**

AGI cult may seem delusional and irrational, but their corporate masters are not. 

[![](https://substackcdn.com/image/fetch/$s_!6gX-!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdee3e4e3-bc5c-4893-9571-2d5c381834e1_2188x1224.png)](https://substackcdn.com/image/fetch/$s_!6gX-!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdee3e4e3-bc5c-4893-9571-2d5c381834e1_2188x1224.png)

[![](https://substackcdn.com/image/fetch/$s_!XGpL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F65380188-2012-40d7-af36-52970f61a0fb_2189x1176.png)](https://substackcdn.com/image/fetch/$s_!XGpL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F65380188-2012-40d7-af36-52970f61a0fb_2189x1176.png)

Why am I the only person saying the quiet part out loud?

### [15.d] The future is bright.

[Sam Altman has a blog post on how wonderful the future will be.](https://ia.samaltman.com/)

[![](https://substackcdn.com/image/fetch/$s_!-LJy!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F34b8c8d3-e82d-48db-abc8-db8e63fac346_1001x811.png)](https://substackcdn.com/image/fetch/$s_!-LJy!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F34b8c8d3-e82d-48db-abc8-db8e63fac346_1001x811.png)

[So does Dario Amodei.](https://darioamodei.com/machines-of-loving-grace)

[![](https://substackcdn.com/image/fetch/$s_!hiNH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6959b123-e79e-4419-b2ab-642f57d1cbae_624x365.png)](https://substackcdn.com/image/fetch/$s_!hiNH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6959b123-e79e-4419-b2ab-642f57d1cbae_624x365.png)

They see an optimistic future, a wonderful future of abundance.

I (mostly) disagree. 

If there is abundance, it will be for the few, **not you.**

I would like to take a moment and directly address the OpenAI and Anthropic people who are reading this. (I know you are here)

[![](https://substackcdn.com/image/fetch/$s_!-qVe!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc916b147-8430-400a-a64f-2e0f4fa1a929_1400x700.avif)](https://substackcdn.com/image/fetch/$s_!-qVe!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc916b147-8430-400a-a64f-2e0f4fa1a929_1400x700.avif)

 _WAKE UP._

_The enemy is not what the other AI lab might do or some theoretical future superintelligent AI._

 _ **The enemy is already here, right behind you.**_

[![a CEO wearing a suit playing with puppets who are wearing casual cloths ](https://substackcdn.com/image/fetch/$s_!Nm94!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7381e24a-d3b9-4b9e-a793-8be0d54801be_1024x1024.jpeg)](https://substackcdn.com/image/fetch/$s_!Nm94!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7381e24a-d3b9-4b9e-a793-8be0d54801be_1024x1024.jpeg) _AGI this. Abundance that. Intelligence age! HA HA HA_

* * *

Will the world be a better place in 5 years? 

I don’t think so.

I see a world consumed by riots, vandalism, violence, and misery… lorded over by the privileged few.

I see extreme inequality from the greatest economic and technological transformation in history.

The future is bright…

[![a datacenter surrounded by fire, cyberpunk](https://substackcdn.com/image/fetch/$s_!VI0Y!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff0d6da5e-33aa-4768-a58e-577e625b925a_1024x1024.jpeg)](https://substackcdn.com/image/fetch/$s_!VI0Y!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff0d6da5e-33aa-4768-a58e-577e625b925a_1024x1024.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!x_KU!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0b7a156f-468d-40d2-b7a7-e80833032b10_1024x1024.jpeg)](https://substackcdn.com/image/fetch/$s_!x_KU!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0b7a156f-468d-40d2-b7a7-e80833032b10_1024x1024.jpeg)

…but not in the way the AGI cultists think.

Are you ready?

-IA
