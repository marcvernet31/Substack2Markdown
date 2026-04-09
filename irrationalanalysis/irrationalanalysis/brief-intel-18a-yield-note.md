# Brief Intel 18A Yield Note

## What the rumors really mean.

**Dec 08, 2024**

**Likes:** 0

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Please check the [‘about’ page](https://irrationalanalysis.substack.com/about) for a list of active positions.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice, and readers should **always do their own research before investing in any security.**

  * Feel free to contact me via email at: _irrational_analysis@proton.me_




* * *

## Contents:

  1. Intro

  2. A Car Analogy

  3. Intel Panther Lake Rumor

  4. Possible Outcomes

  5. Moronic Rorschach Test




### [1] Intro

There is this 10% yield rumor for Intel 18A making the rounds.

[![](https://substackcdn.com/image/fetch/$s_!w6z9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffff5f9e9-ac2c-4e2c-9d32-b8ffd672ba89_589x791.png)](https://substackcdn.com/image/fetch/$s_!w6z9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffff5f9e9-ac2c-4e2c-9d32-b8ffd672ba89_589x791.png)

First, the 10% yield rumor is coming from Korean press, full of delusional Samsung Foundry sympathizers. 

[![](https://substackcdn.com/image/fetch/$s_!0sf8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F917e38be-0208-4c25-8f55-406a20f8623b_606x616.png)](https://substackcdn.com/image/fetch/$s_!0sf8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F917e38be-0208-4c25-8f55-406a20f8623b_606x616.png)

Second, the Broadcom test chips were on PDK v0.7 so nitpicking this is a waste of everyone’s time.

Finally, almost everyone discussing this topic either has no idea what they are talking about or choses to selectively explain the situation.

[![](https://substackcdn.com/image/fetch/$s_!7yc-!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3112acce-0ca2-470a-b75a-236806f2b521_599x415.png)](https://substackcdn.com/image/fetch/$s_!7yc-!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3112acce-0ca2-470a-b75a-236806f2b521_599x415.png)

[![](https://substackcdn.com/image/fetch/$s_!F0vv!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5b04263b-7f76-4863-848f-8aed1beed92a_597x503.png)](https://substackcdn.com/image/fetch/$s_!F0vv!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5b04263b-7f76-4863-848f-8aed1beed92a_597x503.png)

### [2] A Car Analogy:

I will explain semiconductor yield with a car analogy.

Suppose you have a car factory. The cars are marketed with the following three parameters:

  1. Maximum cruising speed (mile-per-hour, MPH)

  2. Fuel efficiency at cruising speed (miles-per-gallon, MPG-F)

  3. Fuel efficiency in city driving (miles-per-gallon, MPG-C)

    1. Many stops and starts at lights and stop signs.

    2. Low (5-30 MPH typical speeds)




 _The semiconductor version of this analogy is:_

  1.  _Clock frequency at load. (F_MAX, all CPU/GPU cores working)_

  2.  _Power draw at load. (P_MAX, watts)_

  3.  _Power draw at idle/light load. (P_IDLE, some cores working)_

    1.  _A weighted average of real scenarios based on the target market and product type._

    2.  _Some cores active, lower power state, some IP blocks off, …_




For a car to be considered functional:

  1. The engine must turn on.

  2. The brakes must work with a minimum stopping power. (too low is a safety risk)

  3. The engine must not fail due to overheating.




Let’s say 80% of all cars produced the factory are functional.

In order to be competitive in the market, the product management and market research teams looked at competitors roadmaps and rumors and determined a set of goals.

  1. 60 MPH max cruising speed.

  2. 80 MPG efficiency at max cruising speed.

  3. 70 MPG efficiency for city driving.




Suppose 50% of cars produced by the factory meet these specifications. They can be sold as planned, without issue.

Thus, the overall product yield of the car factory is 80%*50% = 40%.

Suppose you build a second factory that outputs 99% functional cars, but the parametric yield is terrible. Only 5% of cars meet spec.

The other 95% have like 20 MPH max speed before overheating. They also guzzle gas, achieving a pitiful 30 MPG at high speed and 10 MPG in city driving.

You cannot sell this garbage. Nobody will buy it. Competition is much better.

### [3] Intel Panther Lake Rumor

Real rumor is this:

 **Panther Lake CPU core chiplet allegedly has overall yield of 10%.**

Intel cope on Twitter has people using the 0.4 defect density (D0) advertised by Intel publicly as a way of claiming this rumor is impossible.

Let’s do some quick math to illustrate why this rumor is absolutely plausible.

[![](https://substackcdn.com/image/fetch/$s_!Nxbg!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7b220551-91e3-4aff-ba36-3820c9049667_599x1034.png)](https://substackcdn.com/image/fetch/$s_!Nxbg!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7b220551-91e3-4aff-ba36-3820c9049667_599x1034.png)<https://x.com/DreadyBear/status/1865127585136476340>

[![](https://substackcdn.com/image/fetch/$s_!Fk8M!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6d971e60-50fc-4afe-b474-fa68fac0b765_1229x1291.png)](https://substackcdn.com/image/fetch/$s_!Fk8M!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6d971e60-50fc-4afe-b474-fa68fac0b765_1229x1291.png)From the above public tweet. **DIE 4 (the largest) is the CPU core chiplet.** All we care about is modeling the yield of that one chiplet. 

[![](https://substackcdn.com/image/fetch/$s_!9tEZ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4654d55c-c406-48a7-9748-e5cc9dab7b99_658x110.png)](https://substackcdn.com/image/fetch/$s_!9tEZ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4654d55c-c406-48a7-9748-e5cc9dab7b99_658x110.png)

As you can see, parametric yield matters a lot. 

I would like to remind everyone that this [0.4 defect-density number](https://www.intel.com/content/www/us/en/newsroom/opinion/continued-momentum-intel-18a.html) came in response to a [Reuters report.](https://www.reuters.com/technology/intel-manufacturing-business-suffers-setback-broadcom-tests-disappoint-sources-2024-09-04/) **Published on the same day.**

[![](https://substackcdn.com/image/fetch/$s_!S9WV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8fcffb5c-1c9a-483e-a2bc-7b7b11430d1b_866x801.png)](https://substackcdn.com/image/fetch/$s_!S9WV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8fcffb5c-1c9a-483e-a2bc-7b7b11430d1b_866x801.png)

[![](https://substackcdn.com/image/fetch/$s_!1xXQ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7c830158-c681-4383-a00e-36c70d970520_889x1026.png)](https://substackcdn.com/image/fetch/$s_!1xXQ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7c830158-c681-4383-a00e-36c70d970520_889x1026.png)

D0 is a closely guarded secret. 

[![](https://substackcdn.com/image/fetch/$s_!UF46!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5f9c601c-a0c9-4497-933b-e682b8239a34_848x473.png)](https://substackcdn.com/image/fetch/$s_!UF46!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5f9c601c-a0c9-4497-933b-e682b8239a34_848x473.png)

**TSMC has previously published D0 trend but stopped.**

There are no public or official D0 numbers for TSMC N3B (failed node) or TSMC N3E/P (very good node family).

Ask yourself why Intel felt the need to publish 18A D0 on the exact day they knew negative press was coming.

It’s because the average investor does not understand what parametric yield is.

### [4] Possible Outcomes

Let’s take a look at the Intel Lunar Lake SKU stack.

[![](https://substackcdn.com/image/fetch/$s_!2olG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F44b6ab25-e454-4bac-99a3-c6e43f271f77_1078x731.png)](https://substackcdn.com/image/fetch/$s_!2olG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F44b6ab25-e454-4bac-99a3-c6e43f271f77_1078x731.png)

Within semiconductors, there are two ways to “yield harvest”.

  1. Disable parts of the chip (typically CPU/GPU cores).

  2. Limit parts of the chip (typically CPU/GPU cores) to a lower clock frequency.




Intel, AMD, Nvidia, and many other semiconductor companies use yield harvesting. Certain consumer products, laptop/PC chips in particular use this tactic aggressively to maximize number of sellable chips. 

In this most recent example, Intel product management and competitive analysis groups looked at silicon data reports and made several decisions.

[![](https://substackcdn.com/image/fetch/$s_!O52u!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F60378d53-c807-430e-bcbe-35cd8f008cd8_869x588.png)](https://substackcdn.com/image/fetch/$s_!O52u!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F60378d53-c807-430e-bcbe-35cd8f008cd8_869x588.png)

  * A lower tier set of products will have a small number of functional blocks disabled.

    * Slightly fewer GPU cores.

    * 33% less SRAM.

  * Each descending SKU will have slightly lower CPU and GPU core speeds.




[![](https://substackcdn.com/image/fetch/$s_!kdWE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fce9c4a65-e4aa-4e8b-b22c-fd3a2d6fee4f_868x447.png)](https://substackcdn.com/image/fetch/$s_!kdWE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fce9c4a65-e4aa-4e8b-b22c-fd3a2d6fee4f_868x447.png)Example mock-up of an Intel Core Ultra 5 processor 238V.

Every design team runs simulations to estimate expected functional and parametric yield. The product management team uses this information alongside competitive market intelligence (guesses on what the competition will release) to set goals for designers. 

**These simulations depend on the process-development kit (PDK).**

If the PDK is wrong, the simulations are way off and reality hits hard.

Here are the options:

  1. Panther Lake re-spin and delay launch by 4-6 months minimum. Hope PDK is accurate this time. 

  2. Keep the existing power and performance goals, destroying gross margins.

  3. Lower goals, release a slow product with underwhelming battery life, get beaten to a pulp by the competition (AMD, MediaTek/Nvidia, Qualcomm).




There are non-engineering ways out of this mess. (#2 and #3)

### [5] Moronic Rorschach Test

Have you ever seen one of these?

[![](https://substackcdn.com/image/fetch/$s_!BNsT!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc91733fc-6539-4fa9-8c33-39345cb0bcff_736x482.jpeg)](https://substackcdn.com/image/fetch/$s_!BNsT!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc91733fc-6539-4fa9-8c33-39345cb0bcff_736x482.jpeg)

[This is called a Rorschach test.](https://en.wikipedia.org/wiki/Rorschach_test)

Psychiatric patients are asked “what do you see” when shown various inkblots.

 _For what it’s worth, I see a butterfly made of pine trees._

The current Intel 18A 10% yield rumor cycle feels like a Rorschach test.

  * Koreans/Samsung people see that Intel Foundry is failing just as hard as they are.

  * Intel fans cling to the 0.4 D0 number as if it will ward off the epic annihilation that is coming from this rumored disaster, if true.

  * Pat Gelsinger (praise be upon him) is posting on Twitter (he has some free time these days) trying to correct poorly informed non-technical people without describing the full situation.

    * Gelsinger is smart enough to know the difference between parametric and functional yield.

    * Like many in this industry, he is aware that Samsung Foundry has terrible parametric yield.

  * TSMC engineer meme accounts are also trolling without telling the full truth. That 60% alleged yield on TSMC N2 is probably a single ARM A72 (tiny) core with very relaxed PVT constraints.




We will find out next year what the parametric yields of Intel 18A are.

It shall be such fun.

Share to someone you know spreading mis-informed semiconductor yield information.

[Share](https://irrationalanalysis.substack.com/p/brief-intel-18a-yield-note?utm_source=substack&utm_medium=email&utm_content=share&action=share)

Subscribe if you want.

Subscribe
