# ISSCC 2025: Ultra High-Speed SerDes

## Broadcom bulls may have a minor concern.

**Feb 20, 2025**

**Likes:** 0

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Please check the [‘about’ page](https://irrationalanalysis.substack.com/about) for a list of active positions.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice, and readers should **always do their own research before investing in any security.**

  * Feel free to contact me via email at: _irrational_analysis@proton.me_




* * *

# Contents:

  1. A warning on performance claims.

  2. MediaTek N4 212.5G: The one that failed.

  3. Korea+IBM Exotic FDM 112G




* * *

### [1] A warning on performance claims.

Every presentation has multiple performance claims. These claims are not comparable against each other and are frankly useless individually as well.

Temperature, effective-return-loss (ERL), and power supply scheme are critical variables that are in artificially favorable states. Cherry-picked TT (typical-typical) parts are also used.

 **All of these demos are at room temperature, often with active cooling.**

Real production parts will be at 90-110C hot spot die temp. Most of the setups looked like 30-40C die temp at most. 

**All of these demos likely use cherry-picked TT parts of unusually good performance.**

[![](https://substackcdn.com/image/fetch/$s_!XAIz!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2fb27459-1877-4d51-a245-43a97ff01a02_1463x822.jpeg)](https://substackcdn.com/image/fetch/$s_!XAIz!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2fb27459-1877-4d51-a245-43a97ff01a02_1463x822.jpeg)

 **All of these demos use clean channels with minimal reflections.** This places less strain of the receiver equalizer. 

Most of these demos use **over-built VRM (voltage supply) setups** that have minimal ripple, mitigating PSRR (power-supply rejection ratio) issues.

[![](https://substackcdn.com/image/fetch/$s_!vqy1!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1f479938-6e2e-467c-8f7b-8434528327db_500x500.jpeg)](https://substackcdn.com/image/fetch/$s_!vqy1!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1f479938-6e2e-467c-8f7b-8434528327db_500x500.jpeg)

Take these demos with a very large grain of salt…

### [2] MediaTek N4 212.5G: The one that failed.

Many institutional investors have expressed concern about Google’s attempts to free themselves from the clutches of Hock Tan (Broadcom). There was a rumor circulating over a year ago that MediaTek had won TPU v6E (small/inference). I did not care because it was obvious MTK would fail on their first attempt at 224G-class SerDes, especially on TSMC N4. 

Turns-out, I was right. They did fail. Google had to crawl back to Broadcom for a special extra order of “inference-optimized” TPU v6P. Now the rumor is that MTK has won TPU V7E on TSMC N3P. 

Let’s take a look at the SerDes that failed. The SerDes that ruined Googles diversification plans last year. 

[![](https://substackcdn.com/image/fetch/$s_!zwTg!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F523f746b-2b71-45fe-96af-e7718fa39009_226x249.png)](https://substackcdn.com/image/fetch/$s_!zwTg!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F523f746b-2b71-45fe-96af-e7718fa39009_226x249.png)

Lots of interesting bits. Will give my opinion on probability of success for the N3 SerDes at the end.

[![](https://substackcdn.com/image/fetch/$s_!vS2i!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2cf80971-5f39-4333-84da-f5489ab0b611_2152x2460.jpeg)](https://substackcdn.com/image/fetch/$s_!vS2i!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2cf80971-5f39-4333-84da-f5489ab0b611_2152x2460.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!lsnh!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc8725dc1-afd2-4ae1-bd4f-b245d97c60ba_2312x2708.jpeg)](https://substackcdn.com/image/fetch/$s_!lsnh!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc8725dc1-afd2-4ae1-bd4f-b245d97c60ba_2312x2708.jpeg)

They added an extra 2-TAP FFE into the final MUX. **This is super weird.**

Harms area of the final MUX. Blows up transmitter analog power. Requires over-building of the driver to compensate for the 10% swing loss. 

I assume the “1/10th size” means the second FFE tap can only be 0 (off) or -0.1 weight (normalized to 1).

The fact that they only enable this hack for speeds above 100G indicates to me this thing is a power hog.

[![](https://substackcdn.com/image/fetch/$s_!72Ak!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3242651c-c121-4ab8-b1d4-e70cb471be84_2204x2364.jpeg)](https://substackcdn.com/image/fetch/$s_!72Ak!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3242651c-c121-4ab8-b1d4-e70cb471be84_2204x2364.jpeg)

The receiver is pretty boring… except for the 32-tap floating DFE.

Crazy excessive. 

[![](https://substackcdn.com/image/fetch/$s_!TMDh!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb6504c36-998d-487c-944e-2c4cbe38ff77_2540x1308.jpeg)](https://substackcdn.com/image/fetch/$s_!TMDh!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb6504c36-998d-487c-944e-2c4cbe38ff77_2540x1308.jpeg)

They really do have two slicers lmao.

No real system is going to have this many strong reflections. The clocking for this setup must be a nightmare. Why have they done this?

[![](https://substackcdn.com/image/fetch/$s_!hPCG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe5896b4e-92bc-4b31-bbeb-85e869b7daeb_2248x2400.jpeg)](https://substackcdn.com/image/fetch/$s_!hPCG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe5896b4e-92bc-4b31-bbeb-85e869b7daeb_2248x2400.jpeg)

They added capacitive-based gain into the buffers isolating the ADC interleaves from the CTLE. This leads to nasty reflections. Very strange tradeoff. I’m not sure if this is clever design or a hammer trying to crack an egg.

[![An Asian man cracking a giant silicon egg with a hammer, cartoon](https://substackcdn.com/image/fetch/$s_!uUi4!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F97079de4-f76a-4bb9-a1f1-846a163a577d_1024x1024.jpeg)](https://substackcdn.com/image/fetch/$s_!uUi4!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F97079de4-f76a-4bb9-a1f1-846a163a577d_1024x1024.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!Q6ma!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F07392861-5fcf-47c8-a62c-a4bd79c124e3_2452x1344.jpeg)](https://substackcdn.com/image/fetch/$s_!Q6ma!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F07392861-5fcf-47c8-a62c-a4bd79c124e3_2452x1344.jpeg)

This jitter number is insanely good. I almost can’t believe it.

[![](https://substackcdn.com/image/fetch/$s_!CibO!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe55a3968-379a-4a37-9625-e1031f4ae38a_2396x1316.jpeg)](https://substackcdn.com/image/fetch/$s_!CibO!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe55a3968-379a-4a37-9625-e1031f4ae38a_2396x1316.jpeg)

Fractional PLL phase noise looks great. Great job to whoever worked on this.

JTOL was done at 38dB insertion loss instead of the 40 dB they should have used. Whatever it’s fine. Probably someone was in a rush.

Integrated phase noise is using extreme settings lmao. **They are flexing on everyone with these jitter numbers.** Incredible stuff.

[![](https://substackcdn.com/image/fetch/$s_!dSkG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3bbf4534-e773-412e-b447-ea29b14e5d6d_3644x1916.png)](https://substackcdn.com/image/fetch/$s_!dSkG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3bbf4534-e773-412e-b447-ea29b14e5d6d_3644x1916.png)

This is a very clean channel at extremely favorable conditions. Don’t take it too seriously.

[![](https://substackcdn.com/image/fetch/$s_!ELnx!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe5f47967-884d-481b-8ec6-c9c537687fbb_1112x741.png)](https://substackcdn.com/image/fetch/$s_!ELnx!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe5f47967-884d-481b-8ec6-c9c537687fbb_1112x741.png)

* * *

 **Overall, I am very impressed with MediaTek’s 224G-class SerDes.**

Before this presentation my gut feeling probability of success for MTK TPU V7E in late 2026 was ~30%.

I now believe there is an 80% probability they succeed in taking this business from Broadcom.

Institutional investors who are bullish Broadcom should probably hedge and buy some MediaTek ($2454.TW) stock. 

Broadcom is still a great long-term investment. I recently bought more shares and have no intention of selling. 

[![](https://substackcdn.com/image/fetch/$s_!TFx1!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F10f2d681-3d3f-4bb9-a485-8724bfef7799_755x464.png)](https://substackcdn.com/image/fetch/$s_!TFx1!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F10f2d681-3d3f-4bb9-a485-8724bfef7799_755x464.png)

Sell-side is wrong assigning full V7 win to [AVGO 0.00%↑](https://substack.com/discover/stocks/AVGO). Multi-sourcing will start late 2026 or early 2027…. probably. There is still a ~20% chance MediaTek screws this up.

[![](https://substackcdn.com/image/fetch/$s_!gk6G!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcf963c4c-704c-4ea0-b994-b5ce9397cf65_780x1076.png)](https://substackcdn.com/image/fetch/$s_!gk6G!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcf963c4c-704c-4ea0-b994-b5ce9397cf65_780x1076.png)

Broadcom keeps winning more and more designs using their epic 3.5D platform.

Who cares if Google moves some volume away? Not me!

 _(obviously professional investors need to care about this… have fun.. notmyproblem)_

Also shoutout to Taiwan friends. MediaTek is the best stock from your home country. Yes, really. MTK > TSMC as an investment IMO.

The only reason I have not bought $2454.TW is that WeBull does not support Taiwanese securities. Literally do not have time nor the capital to manage multiple levered accounts. Have fun friends.

[![](https://substackcdn.com/image/fetch/$s_!RoY0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F978c4585-e143-4b20-82a9-44f1dbcca208_619x410.png)](https://substackcdn.com/image/fetch/$s_!RoY0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F978c4585-e143-4b20-82a9-44f1dbcca208_619x410.png)

### [3] Korea+IBM Exotic FDM 112G

Ok this one is super cool but probably useless from an investment perspective. 

[![](https://substackcdn.com/image/fetch/$s_!UXLN!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0edbc3ee-19c1-4207-b6b0-49232a06a899_2344x2348.jpeg)](https://substackcdn.com/image/fetch/$s_!UXLN!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0edbc3ee-19c1-4207-b6b0-49232a06a899_2344x2348.jpeg)

Holy crap. FFT and OFDM in high-speed wireline! This is crazy. Buckle up!

[![](https://substackcdn.com/image/fetch/$s_!gkVQ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5cf05116-89e7-4aae-9ab9-7a44552cc8e0_2200x2364.jpeg)](https://substackcdn.com/image/fetch/$s_!gkVQ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5cf05116-89e7-4aae-9ab9-7a44552cc8e0_2200x2364.jpeg)

Ok so phase rotation of the QAM constellation is mapped to channels/sub-carriers. Clever way of avoiding phase noise obliterating the constellation lmao.

[![](https://substackcdn.com/image/fetch/$s_!lSVn!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd8ce31fd-e156-4ce9-99bf-82962f5f263e_2444x2588.jpeg)](https://substackcdn.com/image/fetch/$s_!lSVn!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd8ce31fd-e156-4ce9-99bf-82962f5f263e_2444x2588.jpeg)

Basic stuff commonly used in wireless. Interesting that they used a block of zeros instead of Zadoff-Chu sequence.

[![](https://substackcdn.com/image/fetch/$s_!ROsf!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff7161518-e8de-45b1-86e7-adbe89857448_2584x2780.jpeg)](https://substackcdn.com/image/fetch/$s_!ROsf!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff7161518-e8de-45b1-86e7-adbe89857448_2584x2780.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!5k6I!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc7bbdd06-5443-49a4-a9af-51a5a265bd7f_2528x2748.jpeg)](https://substackcdn.com/image/fetch/$s_!5k6I!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc7bbdd06-5443-49a4-a9af-51a5a265bd7f_2528x2748.jpeg)

I honestly have no clue what these four slides mean but they seem important. 

[![](https://substackcdn.com/image/fetch/$s_!mDm7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2623bfd3-468c-43f3-9c59-5a84fd20825f_2564x2844.jpeg)](https://substackcdn.com/image/fetch/$s_!mDm7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2623bfd3-468c-43f3-9c59-5a84fd20825f_2564x2844.jpeg)

Ok so they are using Zadoff-Chu sequence. But… it is XNOR-ed with input data? WTF??????

Allowing for small shift in CP detector is probably a good tradeoff. Wish they had data on how much performance is lost vs the area reduction.

[![](https://substackcdn.com/image/fetch/$s_!o9Np!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6bb32b57-4c99-4c81-82cc-009b4e22238c_2584x2776.jpeg)](https://substackcdn.com/image/fetch/$s_!o9Np!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6bb32b57-4c99-4c81-82cc-009b4e22238c_2584x2776.jpeg)

Clever FFT engine design to save area and power.

[![](https://substackcdn.com/image/fetch/$s_!IEqn!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe6dd5734-9c11-486c-b39a-4f048f460d3a_2652x1452.jpeg)](https://substackcdn.com/image/fetch/$s_!IEqn!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe6dd5734-9c11-486c-b39a-4f048f460d3a_2652x1452.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!fMhe!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8317817b-7128-41c3-badf-17c0a5f13b4c_2104x1192.jpeg)](https://substackcdn.com/image/fetch/$s_!fMhe!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8317817b-7128-41c3-badf-17c0a5f13b4c_2104x1192.jpeg)

No commercial test equipment supports this crazy architecture. They had to set up an exotic FPGA and **probe station.** Just measuring this system was a huge challenge by itself. Bravo!!!!!!!!!!!!!!!!!!!! 

[![](https://substackcdn.com/image/fetch/$s_!p5bx!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F15f0515b-da32-446c-b43d-1188e25af7d9_2060x2096.jpeg)](https://substackcdn.com/image/fetch/$s_!p5bx!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F15f0515b-da32-446c-b43d-1188e25af7d9_2060x2096.jpeg)

Very curious where the notch at OFDM symbol 48 comes from. Is if due to the channel materials or the circuitry? 

Constellations are impressive given how exotic this idea is. BER of 4E-4 is respectable for a crazy mad-scientist innovative architecture.

 **Great job to everyone who worked on this!!!!!!!!!!!!!!!!!!**

Subscribe for engineering-driven investment analysis.

Subscribe

Share?

[Share](https://irrationalanalysis.substack.com/p/isscc-2025-ultra-high-speed-serdes?utm_source=substack&utm_medium=email&utm_content=share&action=share)
