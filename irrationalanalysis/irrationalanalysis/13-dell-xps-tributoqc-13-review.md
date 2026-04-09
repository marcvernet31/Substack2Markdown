# [1/3] Dell XPS (TributoQC) 13 Review

## Good laptop. Disappointing battery life and GPU performance.

**Jul 27, 2024**

**Likes:** 0

# IMPORTANT:

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Please check the [‘about’ page](https://irrationalanalysis.substack.com/about) for a list of active positions.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice and readers should **always do their own research before investing in any security.**




* * *

Welcome to part one of this three-part series on the Snapdragon X Elite laptop chip. 

[![](https://substackcdn.com/image/fetch/$s_!MEXx!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faf4e0580-93e0-45fc-9575-441648e84cca_1899x1003.png)](https://substackcdn.com/image/fetch/$s_!MEXx!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faf4e0580-93e0-45fc-9575-441648e84cca_1899x1003.png)

Which X Elite laptop did I buy? The Dell unit from the glorious mega-leak of course!

[![Dell Mega Leak Analysis](https://substackcdn.com/image/fetch/$s_!DmRp!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1ffcbb23-7f8c-4022-9a35-358dd1d87d05_1797x1139.png)

#### Dell Mega Leak Analysis

[Daud's Scout](https://substack.com/profile/135313705-dauds-scout)·May 15, 2024[Read full story](https://irrationalanalysis.substack.com/p/dell-mega-leak-analysis)](https://irrationalanalysis.substack.com/p/dell-mega-leak-analysis)

This post is part of a series:

  1.  **Review the laptop like a normal person. (you are here)**

  2. Detailed performance analysis of Microsoft’s x86-64 to aarch64 emulator using Visual Studio and Ghidra.

  3. Reverse-engineering of comical VRM/PMIC setup using an oscilloscope, and multimeter.

* * *




# Contents:

  1. General Thoughts

  2. Unexpectedly Poor Battery Life

  3. AI PC

    1. The Hoax of On-device AI

    2. Utter lack of use-cases, excluding video call background-blur.

    3. Failed execution by both Microsoft and Qualcomm.

  4. GPU/Gaming Performance

  5. Software Compatibility

  6. Teasers

* * *




### [1] General Thoughts

My previous laptop was a 2018 LG gram powered by an [Intel Kaby Lake part.](https://ark.intel.com/content/www/us/en/ark/products/122589/intel-core-i7-8550u-processor-8m-cache-up-to-4-00-ghz.html)

[![](https://substackcdn.com/image/fetch/$s_!5RMt!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Feb9ccbdb-bc6a-4614-a52d-2aa1d87b976a_2023x1431.png)](https://substackcdn.com/image/fetch/$s_!5RMt!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Feb9ccbdb-bc6a-4614-a52d-2aa1d87b976a_2023x1431.png)

This chip is really a Skylake+++ architecture on Intel’s 14nm++++++ process node. Back when Intel’s 10nm node (now re-branded as Intel 7) was spontaneously combusting in spectacular fashion.

The old LG Gram had a meh IPS screen, wobbly hinge, significant chassis flex, an annoying barrel-style power plug, and only 8GB of RAM.

My Dell XPS (Tributo QC) is the opposite. Incredible OLED screen, sturdy hinge, solid chassis, USB-C power input with a compact brick, and 16 GB of RAM.

Overall, a great machine. Happy with my purchase. 

Two oddities to call out:

  1. The touchbar is annoying. I hate not having physical keys for ESC and DEL.

  2. The touchpad is hidden underneath the chassis. Took some getting used to but it is quite nice. Pleasent design and utility for easy cleaning.




### [2] Unexpectedly Poor Battery Life

I have used this laptop for around 100-150 hours and my average battery life is 6-8 hours. This is with light use. Web browsers, Discord, some Python, light photo editing, 

The fan almost never spins up.

Laptop stays cool the entire time.

OLED displays consume a lot more power than IPS… but that can’t explain the unexpectedly poor battery life.

Interesting how this laptop chip appears to be powered at least 56 switching regulators and 18 LDOs…

[![](https://substackcdn.com/image/fetch/$s_!Cqzg!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F69f7cf57-8fd2-4b90-a4b6-9b88e71753a1_870x663.png)](https://substackcdn.com/image/fetch/$s_!Cqzg!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F69f7cf57-8fd2-4b90-a4b6-9b88e71753a1_870x663.png)

[![](https://substackcdn.com/image/fetch/$s_!bO4T!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F743bd95a-362e-41ab-993e-6c6ed039de56_791x510.png)](https://substackcdn.com/image/fetch/$s_!bO4T!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F743bd95a-362e-41ab-993e-6c6ed039de56_791x510.png)

There are 7 of these PMIC chips on the motherboard alongside several other QCOM power-related chips.

Seems a bit excessive. Even if there are 18 separate supply rails.

What if Semiaccurate/Charlie is right? What if QCOM really did ham-fist a horribly inefficient solution upon laptop OEMs, piss them off, then provide “marketing” dollars as compensation, incinerating profitability while maintaining superficial accretive gross margins to QCT?

[![](https://substackcdn.com/image/fetch/$s_!_6yw!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7cb59cd4-6fad-48ac-ba25-4283a89407b2_884x487.png)](https://substackcdn.com/image/fetch/$s_!_6yw!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7cb59cd4-6fad-48ac-ba25-4283a89407b2_884x487.png)Source: Stacy Rasgon of Bernstein Research. Also hobby QCOM investor relations. I have circled my opinion on what will happen. **Need to back-substitute 14% gross margin instead of Stacy’s 50% because of PMIC self-own apology subsidy.**

[![Dell Mega Leak Analysis](https://substackcdn.com/image/fetch/$s_!DmRp!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1ffcbb23-7f8c-4022-9a35-358dd1d87d05_1797x1139.png)

#### Dell Mega Leak Analysis

[Daud's Scout](https://substack.com/profile/135313705-dauds-scout)·May 15, 2024[Read full story](https://irrationalanalysis.substack.com/p/dell-mega-leak-analysis)](https://irrationalanalysis.substack.com/p/dell-mega-leak-analysis)

[![](https://substackcdn.com/image/fetch/$s_!EtCc!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F51ef415c-6354-4639-89a9-6650582bfb34_1797x1139.png)](https://substackcdn.com/image/fetch/$s_!EtCc!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F51ef415c-6354-4639-89a9-6650582bfb34_1797x1139.png)

Stacy is assuming 50% gross-margin out of thin air apparently. I calculated ~52% gross margin ($74 gross profit per chip) using public die measurements and other public information. **However, all these assumptions ignore the $60 “marketing” subsidy QCOM is providing to laptop OEMs.**

QCOM management will surely hype how accretive X Elite is to QCT gross margins but operating profit will not move. **In fact, this whole fiasco will be dilutive to operating profit margin!**

Is this new, hyped-up, diversification AI PC chip accretive or dilutive to earnings?

Gross margin of 52% or 14%? Adding the $60/chip subsidy back into COGS makes the numbers far less attractive.

* * *

Here is a snippet from a Monolithic Power switching regulator datasheet.

[![](https://substackcdn.com/image/fetch/$s_!IZpD!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F308e60d1-36b9-40a6-b8d4-5af8006d81c3_885x512.png)](https://substackcdn.com/image/fetch/$s_!IZpD!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F308e60d1-36b9-40a6-b8d4-5af8006d81c3_885x512.png)

As you can see, efficiency changes based on how much current is loaded onto a single regulator. This part is marketed as 100A but is most efficient in the 20-50A range.

Qualcomm does not publish public datasheets.

[![](https://substackcdn.com/image/fetch/$s_!rcFb!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0d03a6ee-cdb4-4ad2-90a9-10634e780239_1230x502.png)](https://substackcdn.com/image/fetch/$s_!rcFb!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0d03a6ee-cdb4-4ad2-90a9-10634e780239_1230x502.png)

Which is fine. I will just reverse-engineer the performance characteristics of these PMIC chips with a multimeter and oscilloscope. 

We will get to the bottom of this mystery, unexpectedly poor battery life. 😈

### [3] AI PC

[![](https://substackcdn.com/image/fetch/$s_!x6W6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb11de3e8-c767-472b-8827-a912b95f9a16_3000x4000.jpeg)](https://substackcdn.com/image/fetch/$s_!x6W6!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb11de3e8-c767-472b-8827-a912b95f9a16_3000x4000.jpeg)

The marketing push behind “AI PCs” is rather aggressive. 

#### [3.a] The Hoax of On-device AI

After going out of my way to try and use the on-device AI capabilities of this “AI PC”, the only rational conclusion is this entire thing is a hoax.

[![](https://substackcdn.com/image/fetch/$s_!Iea_!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcdf71924-f6c3-439e-814b-df13dd568548_4000x3000.jpeg)](https://substackcdn.com/image/fetch/$s_!Iea_!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcdf71924-f6c3-439e-814b-df13dd568548_4000x3000.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!3soO!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F02a705e2-1b62-4d68-97a2-2e0f0c979169_406x618.png)](https://substackcdn.com/image/fetch/$s_!3soO!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F02a705e2-1b62-4d68-97a2-2e0f0c979169_406x618.png)

[![](https://substackcdn.com/image/fetch/$s_!gnTR!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6bbd7773-0e92-412f-818c-1d9f506f3c17_352x656.png)](https://substackcdn.com/image/fetch/$s_!gnTR!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6bbd7773-0e92-412f-818c-1d9f506f3c17_352x656.png)

[![](https://substackcdn.com/image/fetch/$s_!9-h7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F820f81b5-8aa3-4958-9d6c-a3dc4d1d4ae1_4000x3000.jpeg)](https://substackcdn.com/image/fetch/$s_!9-h7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F820f81b5-8aa3-4958-9d6c-a3dc4d1d4ae1_4000x3000.jpeg)🤡

The much-hyped Copilot key literally does not use the on-device NPU. Not once.

[![](https://substackcdn.com/image/fetch/$s_!yAYI!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0cf453fa-7cb8-4064-894f-9a56b2f81708_4000x3000.jpeg)](https://substackcdn.com/image/fetch/$s_!yAYI!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0cf453fa-7cb8-4064-894f-9a56b2f81708_4000x3000.jpeg)The Copilot key is mapped to “pwahelper”, a lazy edge wrapper.

It is really just a shortcut to an Edge wrapper window that connects to Bing Chat. Amusingly, Edge extension settings don’t show up in this half-assed wrapper. So can’t toggle my dark-mode extension. Have to open edge itself to change that.

#### [3.b] Utter lack of use-cases, excluding video call background-blur.

I had one goal. Use the on-device NPU to do something, anything other than AI enhanced video call background-blur. 

[![](https://substackcdn.com/image/fetch/$s_!vtac!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F730f069b-35b4-473c-ad4d-6e254587bef8_466x612.png)](https://substackcdn.com/image/fetch/$s_!vtac!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F730f069b-35b4-473c-ad4d-6e254587bef8_466x612.png)

Paint co-creator sucks. Tried it on the demo unit at Best Buy. On my actual unit, it won’t run because of “security”. What the hell is the point of on-device AI if I have to send all my data to the cloud for security? Might as well just use the cloud for much higher-quality image generation.

But then… a ray of hope. A real use-case!

[![](https://substackcdn.com/image/fetch/$s_!wOgd!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F145395bb-3a27-4299-9853-8acb257e6307_621x516.png)](https://substackcdn.com/image/fetch/$s_!wOgd!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F145395bb-3a27-4299-9853-8acb257e6307_621x516.png)

On-device live translation.

Let’s try it. Here is a Chinese TechTuber’s video on the legendary Snapdragon 810.

[![](https://substackcdn.com/image/fetch/$s_!MWvN!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7efe06c8-9c78-49bc-99cf-1f788eca058f_2077x1615.png)](https://substackcdn.com/image/fetch/$s_!MWvN!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7efe06c8-9c78-49bc-99cf-1f788eca058f_2077x1615.png)

And Eurika! The NPU is actually working.

[![](https://substackcdn.com/image/fetch/$s_!vgqG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F36002b97-004b-462a-aa76-993e9b22c232_691x512.png)](https://substackcdn.com/image/fetch/$s_!vgqG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F36002b97-004b-462a-aa76-993e9b22c232_691x512.png)

Not at full, glorious 45 TOPS. But hey, at least it is active.

[![](https://substackcdn.com/image/fetch/$s_!xPDW!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb4ecb4fc-5e71-46b2-995b-66adecffbac0_842x614.png)](https://substackcdn.com/image/fetch/$s_!xPDW!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb4ecb4fc-5e71-46b2-995b-66adecffbac0_842x614.png)Special thanks to a friend for the translation.

The translation itself was not good. Apparently, a lot of similes were used and that confused the AI.

Also tried to [install OpenAI Whisper](https://github.com/openai/whisper/tree/main).

[![](https://substackcdn.com/image/fetch/$s_!JfLR!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd6c83c21-23fa-40d6-9083-2fe14e5c994a_1725x793.png)](https://substackcdn.com/image/fetch/$s_!JfLR!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd6c83c21-23fa-40d6-9083-2fe14e5c994a_1725x793.png)

Wasted an hour trying to get this to work. Gave up. 

#### [3.c] Failed execution by both Microsoft and Qualcomm.

This whole AI PC farce is an embarrassment. As a lifelong Windows and Android user who has never owned a single Apple product, I look forward to the launch of Apple Intelligence, the real on-device AI implementation.

Copilot+ is a have-baked, mediocre, disappointing marketing hoax. Massive opportunity of [AAPL 0.00%↑](https://substack.com/discover/stocks/AAPL) to release true on-device intelligence, instead of the junk [MSFT 0.00%↑](https://substack.com/discover/stocks/MSFT) and [QCOM 0.00%↑](https://substack.com/discover/stocks/QCOM) ended up dragging across the finish line.

### [4] GPU/Gaming Performance

Given that this is Qualcomm’s first real product on Windows, it is fair to set expectations very low. I chose some games that are light to see if they run at 60 FPS stable.

Unfortunately, driver flaws seem to be holding back the GPU hardware.

  * Poly Bridge 2 (2020)

    * Unity Engine

    * 46 FPS on a blank level….




[![](https://substackcdn.com/image/fetch/$s_!rDeq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc8ebf134-3b00-4437-bb13-ac74032a292b_2880x1800.jpeg)](https://substackcdn.com/image/fetch/$s_!rDeq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc8ebf134-3b00-4437-bb13-ac74032a292b_2880x1800.jpeg)

  * Against the Storm (2023)

    * Unity Engine

    * 22 FPS on a blank level….




[![](https://substackcdn.com/image/fetch/$s_!LQtI!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F993b36e0-854a-4281-b9c0-65616c1c44e8_2880x1800.jpeg)](https://substackcdn.com/image/fetch/$s_!LQtI!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F993b36e0-854a-4281-b9c0-65616c1c44e8_2880x1800.jpeg)

  * Spelunky 2 (2023)

    * Proprietary Game Engine

    * 60 FPS locked. Butter Smooth




[![](https://substackcdn.com/image/fetch/$s_!Loy7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff4831f57-1a41-4a63-9397-1eea66ddc2fa_2880x1800.jpeg)](https://substackcdn.com/image/fetch/$s_!Loy7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff4831f57-1a41-4a63-9397-1eea66ddc2fa_2880x1800.jpeg)

  * Frostpunk (2018)

    * Liquid Engine

    * 7 FPS….




[![](https://substackcdn.com/image/fetch/$s_!AOx1!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff625b9ad-1c11-4953-99cb-86fd7ef90889_2880x1800.jpeg)](https://substackcdn.com/image/fetch/$s_!AOx1!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff625b9ad-1c11-4953-99cb-86fd7ef90889_2880x1800.jpeg)

  * Dishonored (2012)

    * Unreal Engine 3

    * 27 FPS…. in a low-poly, indoor area




[![](https://substackcdn.com/image/fetch/$s_!1QOv!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5a3dfd70-d11b-4a78-8f87-a068abe9c188_2880x1800.jpeg)](https://substackcdn.com/image/fetch/$s_!1QOv!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5a3dfd70-d11b-4a78-8f87-a068abe9c188_2880x1800.jpeg)

I would be disappointed in these results, but I have a gaming desktop with an RTX 4090 so don’t care. 

### [5] Software Compatibility

Microsoft has finally put in some real effort into their x86-64 to aarch64 emulator and it shows. Everything I tried to install and run worked.

Unfortunately, there are some performance problems. The most annoying of which is Discord. 

Discord is an Electron app. This means it is essentially a re-packaged Chrome browser. It runs very slowly, with noticeable lag when switching channels or just basic UI usage.

### [6] Teasers

I have very ambitious plans for testing and analyzing this laptop.

There is a software reverse-engineering tool called Ghidra. 

[![](https://substackcdn.com/image/fetch/$s_!9THN!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F365f30b5-9de7-436c-ba1e-fb23622a509c_686x287.png)](https://substackcdn.com/image/fetch/$s_!9THN!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F365f30b5-9de7-436c-ba1e-fb23622a509c_686x287.png)

[![](https://substackcdn.com/image/fetch/$s_!e0lo!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa1abd92d-7ef6-47d3-845d-5e172ed91971_3424x1173.png)](https://substackcdn.com/image/fetch/$s_!e0lo!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa1abd92d-7ef6-47d3-845d-5e172ed91971_3424x1173.png)

Ghidra + Visual Studio + my monkey brain will eventually generate some useful insights into how this emulator works.

* * *

As for the VRM and PMIC reverse-engineering…

[![](https://substackcdn.com/image/fetch/$s_!FQ64!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3b5cf3a1-f82f-40a7-9200-be4b823732b2_3000x4000.jpeg)](https://substackcdn.com/image/fetch/$s_!FQ64!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3b5cf3a1-f82f-40a7-9200-be4b823732b2_3000x4000.jpeg)

I need to remove the entire cooling system in order to probe everything. Will borrow an oscilloscope from a friend for detailed analysis. Still trying to figure out how to mount this AMD cooler. Might just let gravity hold it in place lol.

Let’s find out how inefficient these PMICs really are. 

Subscribe for future emulator and VRM analysis.

Subscribe

Share to other people who might like this.

[Share](https://irrationalanalysis.substack.com/p/13-dell-xps-tributoqc-13-review?utm_source=substack&utm_medium=email&utm_content=share&action=share)
