# GTC 2025: Co-Packaged Optics Switching

## Transceiver exposed companies and Arista in deep shit.

**Mar 19, 2025**

**Likes:** 0

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Please check the [‘about’ page](https://irrationalanalysis.substack.com/about) for a list of active positions.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice, and readers should **always do their own research before investing in any security.**

  * Feel free to contact me via email at: _irrational_analysis@proton.me_




* * *

I am writing this very quickly before heading over to downtown SJ for meetings and parties.

(quality is low… sorry lol)

[![](https://substackcdn.com/image/fetch/$s_!MjmI!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faad49a9e-3c9b-4591-ade5-121147c1572f_1470x885.png)](https://substackcdn.com/image/fetch/$s_!MjmI!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faad49a9e-3c9b-4591-ade5-121147c1572f_1470x885.png)

[![](https://substackcdn.com/image/fetch/$s_!-wqM!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb65d5fe1-62c1-43a1-b0f9-0e6208e3c5ee_480x415.png)](https://substackcdn.com/image/fetch/$s_!-wqM!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb65d5fe1-62c1-43a1-b0f9-0e6208e3c5ee_480x415.png)Jensen Huang roasting optical transceivers. 3/18/2025

[![](https://substackcdn.com/image/fetch/$s_!Ld96!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6f96b0aa-30e8-4563-95fd-0efe6d45fb72_1557x871.png)](https://substackcdn.com/image/fetch/$s_!Ld96!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6f96b0aa-30e8-4563-95fd-0efe6d45fb72_1557x871.png)

Let’s talk about TSMC COUPE.

[![](https://substackcdn.com/image/fetch/$s_!ClP2!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5e869328-4680-49ef-ab44-7f1c3c4f6a6e_423x346.png)](https://substackcdn.com/image/fetch/$s_!ClP2!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5e869328-4680-49ef-ab44-7f1c3c4f6a6e_423x346.png)

[![](https://substackcdn.com/image/fetch/$s_!1dtI!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd72553f8-3263-4857-9066-803f8d395237_421x421.png)](https://substackcdn.com/image/fetch/$s_!1dtI!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd72553f8-3263-4857-9066-803f8d395237_421x421.png)

Optical things (resonators, phase detectors, photodiodes, modulators, waveguides…) need to be on a special process node. A photonic process node.

The chip with all the optics bits is called photonics IC or PIC.

But the PIC is very Finkey. There needs to be an electrical signal that is at just the right voltage for this to work.

Thus, we have the electrical IC, aka EIC.

This chip is built on a normal logic node and has one job. Make sure the electrical signal going in/out of the PIC is just right.

Why not directly drive the PIC from the ASIC you might be thinking?

  1. Even with (most) advanced packaging, the electrical signal coming out of the ASIC gets too fucked up to directly drive. (this is consensus opinion not my opinion)

    1. The true silver bullet is directly hybrid bonding the PIC to the ASIC.

    2. Hybrid bonding PIC to ASIC brings many challenges such as impedance mis-match, reliability, cost, and so on…

  2. Many elements on the PIC are controlled by thermals. Tiny heaters. 




The caveman way of integrating an EIC and PIC is to use some form of vanilla packaging (RDL).

COUPE is different.

[![](https://substackcdn.com/image/fetch/$s_!tqDq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F226543cf-f933-4227-a8ed-6e38d85e722b_686x575.png)](https://substackcdn.com/image/fetch/$s_!tqDq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F226543cf-f933-4227-a8ed-6e38d85e722b_686x575.png)

TSMC hybrid bonds the EIC and PIC.

This is really fucking good.

[![](https://substackcdn.com/image/fetch/$s_!v7gG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F02f1c481-79cb-4b68-8190-784c84a84aa3_439x232.png)](https://substackcdn.com/image/fetch/$s_!v7gG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F02f1c481-79cb-4b68-8190-784c84a84aa3_439x232.png)

[![](https://substackcdn.com/image/fetch/$s_!nTRw!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4aa66b8e-ae59-4112-9085-a8fb03448af9_295x243.png)](https://substackcdn.com/image/fetch/$s_!nTRw!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4aa66b8e-ae59-4112-9085-a8fb03448af9_295x243.png)

Parasitic capacitance very bad. It causes so many problems for the package designer and SerDes design.

COUPE has 85% less parasitic capacitance.

[![](https://substackcdn.com/image/fetch/$s_!E2rl!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2ff6a8f0-9fa4-4786-8e27-6d44255916bd_457x208.png)](https://substackcdn.com/image/fetch/$s_!E2rl!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2ff6a8f0-9fa4-4786-8e27-6d44255916bd_457x208.png)

Insertion loss is basically zero. The 0.2 dB gain is not that big of a deal though.

20 dB of extra return loss is MASSIVE. 

Here is an analogy I keep using with the finance friends. It seems to work.

Imagine you are a singer.

[![](https://substackcdn.com/image/fetch/$s_!m9Vx!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa9d82a67-88b0-43aa-80ac-60b2c39f348f_2000x1333.webp)](https://substackcdn.com/image/fetch/$s_!m9Vx!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa9d82a67-88b0-43aa-80ac-60b2c39f348f_2000x1333.webp)

You have a big audience.

One way of making sure everyone hears you is to sing louder.

But at some point, your voice will become distorted and certain frequency tones (high notes… baratone… whatever) become distorted. The quality of your voice becomes shit.

In general, this is a fixable problem. With proper training, you can make the muscles in your vocal cords stronger, allowing you to sing louder at the same musical quality.

But what if the venue has echos?

That is a much more difficult problem to solve…. right?

insertion loss == how weak signal become

return/reflection loss == how much signal echo

Communication systems need DSP/retiming mostly to deal with reflections. 

[![](https://substackcdn.com/image/fetch/$s_!3HTD!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F76ce5080-b06e-4cf1-8e3b-9f956f1784e0_367x285.png)](https://substackcdn.com/image/fetch/$s_!3HTD!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F76ce5080-b06e-4cf1-8e3b-9f956f1784e0_367x285.png)

The peak of package impedance is moved to higher frequencies. This is very nice. 

[![](https://substackcdn.com/image/fetch/$s_!wF8j!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F533857f5-234b-4db2-9428-59a0a9a7e399_406x532.png)](https://substackcdn.com/image/fetch/$s_!wF8j!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F533857f5-234b-4db2-9428-59a0a9a7e399_406x532.png)

Circuits are intrinsically sensitive to power supply noise. This is called PSRR.

COUPE makes the noise much lower which is great.

 **Sidenote:** _I would not take the energy efficiency plot from this TSMC paper too seriously. There are many variables at play here and the baseline they have is not realistic. It’s better but there are way too many factors to just take that 40% number at face value._

In summary (wana hammer this home):

  * COUPE insertion loss nice but whatever.

  * COUPE return loss fucking mazing.

  * Supply noise performance very nice. Adds margin to system.




* * *

[![](https://substackcdn.com/image/fetch/$s_!2aEI!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F09afcc19-f059-402a-8369-d0d3a9ea78f9_1030x867.png)](https://substackcdn.com/image/fetch/$s_!2aEI!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F09afcc19-f059-402a-8369-d0d3a9ea78f9_1030x867.png)

[![](https://substackcdn.com/image/fetch/$s_!U76f!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb43af8e7-19b7-4a64-b4ab-e127d01124eb_1101x544.png)](https://substackcdn.com/image/fetch/$s_!U76f!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb43af8e7-19b7-4a64-b4ab-e127d01124eb_1101x544.png)

[![](https://substackcdn.com/image/fetch/$s_!CCpO!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffec59320-43b8-427a-a269-6dced1c1ac29_988x637.png)](https://substackcdn.com/image/fetch/$s_!CCpO!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffec59320-43b8-427a-a269-6dced1c1ac29_988x637.png)

It took three levels of zoom to get to the important bit.

They are using micro-ring modulations. 

For now, all you need to know is these micro-ring things are EXTREAMLY SENSITIVE to temperature.

They are literally controlled by temperature. 

This is why silicon photonic engine cannot be hybrid bonded directly on top of the switch chip.

I have been doing a lot of research into CPO because…. reasons.

Can you guess why I have been so busy recently?

 _If someone could get Lightmatter to talk to me that would be great. Wana complete due-diligence._

Will write a detailed primer on CPO once I have time. There is a placeholder on my calendar but again… very busy. Both dayjob busy and other efforts. 

[![](https://substackcdn.com/image/fetch/$s_!Rox7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2f6db5e8-c68f-42ec-a6ea-a67e52ea09a4_1156x604.png)](https://substackcdn.com/image/fetch/$s_!Rox7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2f6db5e8-c68f-42ec-a6ea-a67e52ea09a4_1156x604.png)

[![](https://substackcdn.com/image/fetch/$s_!2tr7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbfc312b4-dfbd-4aea-8eda-41646fd5fa44_1378x645.png)](https://substackcdn.com/image/fetch/$s_!2tr7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbfc312b4-dfbd-4aea-8eda-41646fd5fa44_1378x645.png)

COUPE is where the hybrid bonding happens and this is why CPO in this form is possible.

And now you know why the switch chip cannot directly drive PIC. It is too far away. EIC is needed to re-shape and amplify the signal.

[![](https://substackcdn.com/image/fetch/$s_!gZPJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F206201be-c3de-43e0-8cdb-875bec9b74fb_1020x763.gif)](https://substackcdn.com/image/fetch/$s_!gZPJ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F206201be-c3de-43e0-8cdb-875bec9b74fb_1020x763.gif)

You can build TIA (basic class of amplifier) and more advanced multi-stage, highly configurable/tunable CTLE on the EIC. 

Lots of options. Again, details in the upcoming (at some point lol) CPO mega-post.

* * *

[![](https://substackcdn.com/image/fetch/$s_!Gg6v!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7124c70a-c6bf-4788-a8cb-e83fb8a6c2a5_1189x821.png)](https://substackcdn.com/image/fetch/$s_!Gg6v!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7124c70a-c6bf-4788-a8cb-e83fb8a6c2a5_1189x821.png)

The laser sources are pluggable. This is because they are super unreliable. 

Primary point of failure. Serviceability of the light/laser source is a must.

[![](https://substackcdn.com/image/fetch/$s_!2VWN!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F727d25da-ea15-45e1-89f9-56504004901a_1059x709.png)](https://substackcdn.com/image/fetch/$s_!2VWN!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F727d25da-ea15-45e1-89f9-56504004901a_1059x709.png)

[![](https://substackcdn.com/image/fetch/$s_!5zfG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F978cab64-f438-4df7-b6c2-f0e05b4c0d3a_431x543.png)](https://substackcdn.com/image/fetch/$s_!5zfG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F978cab64-f438-4df7-b6c2-f0e05b4c0d3a_431x543.png)

Subscribe for engineering-driven investment analysis.

Subscribe

Share with $ANET longs.

[Share](https://irrationalanalysis.substack.com/p/gtc-2025-co-packaged-optics-switching?utm_source=substack&utm_medium=email&utm_content=share&action=share)
