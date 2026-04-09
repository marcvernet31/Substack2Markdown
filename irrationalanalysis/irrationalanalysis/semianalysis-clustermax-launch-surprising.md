# Semianalysis InferenceMAX Launch: Surprising Data

## A somewhat irrational take.

**Oct 10, 2025**

**Likes:** 0

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Please check the [‘about’ page](https://irrationalanalysis.substack.com/about) for a list of active positions.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice, and readers should **always do their own research before investing in any security.**

  * Feel free to contact me via email at: _irrational_analysis@proton.me_




* * *

Semianalysis just launched the best benchmark I have ever seen. Tied with old AnandTech CPU performance reviews and analysis.

<https://inferencemax.semianalysis.com/>

They have a post on the methodology. 

[![](https://substackcdn.com/image/fetch/$s_!HwSb!,w_56,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2F0150776c-9bf2-4bea-a9c2-41b24b7a0f15_1280x1280.png)SemiAnalysisInferenceMAX™: Open Source Inference BenchmarkingLLM Inference performance is driven by two pillars, hardware and software. While hardware innovation drives step jumps in performance every year through the release of new GPUs/XPUs and new systems, software evolves every single day, delivering continuous performance gains on top of these step jumps…Read more6 months ago · 51 likes · 1 comment · Kimbo Chen, Dylan Patel, Daniel Nishball, Cam Quilici, and Cheang Kang Wen](https://newsletter.semianalysis.com/p/inferencemax-open-source-inference?utm_source=substack&utm_campaign=post_embed&utm_medium=web)

Let’s play a game.

[![](https://substackcdn.com/image/fetch/$s_!8L6x!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2c65a5a5-7430-43e4-8ceb-87a2b80a60cc_480x252.gif)](https://substackcdn.com/image/fetch/$s_!8L6x!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2c65a5a5-7430-43e4-8ceb-87a2b80a60cc_480x252.gif)

 **I have not read the post on the methodology.** Going straight to the data blind assuming SA knows what they are doing and did not make any obvious mistakes. 

(a reasonable assumption)

While there are several options, I only care about one configuration.

[![](https://substackcdn.com/image/fetch/$s_!XPMq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fba624529-b31a-4c8d-ac3c-bf0d19fc3ffb_1208x254.png)](https://substackcdn.com/image/fetch/$s_!XPMq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fba624529-b31a-4c8d-ac3c-bf0d19fc3ffb_1208x254.png)

Reasoning (the most important workload) has high output-sequence length. Picking the highest ratio of OSL/ISL they have. If they had a 20:1 ratio run I would have picked that.

FP4 heavily favors Nvidia. Picking FP8 whenever possible.

Only care about cost from a rental perspective as this is the worst case scenario on pricing.

Here are the three models under this configuration down-selection:

[![](https://substackcdn.com/image/fetch/$s_!Uiy8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3eb1d517-74ba-4c53-9450-c08f9a7248a8_734x1190.png)](https://substackcdn.com/image/fetch/$s_!Uiy8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3eb1d517-74ba-4c53-9450-c08f9a7248a8_734x1190.png)

 **AMD has done surprisingly well,** despite serious technological disadvantages. Let’s take a look at the latest corporate gross margins of AMD and Nvidia.

[![](https://substackcdn.com/image/fetch/$s_!imI-!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9538eeb3-09b8-446a-a57c-665aa9e2bcb7_896x528.png)](https://substackcdn.com/image/fetch/$s_!imI-!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9538eeb3-09b8-446a-a57c-665aa9e2bcb7_896x528.png)

22% gap is quite large.

If AMD was to give away 10% of their own stock as a rebate, that would probably push down gross margins another 10-15% and take AMD from 1 win, 2 loss up to 3 win.

 **Intuitively, this is exactly what the OpenAI deal does.**

* * *

Let’s take a look at official AMD SEC filing. 

<https://ir.amd.com/financial-information/sec-filings/content/0001193125-25-230895/d28189d8k.htm>

[![](https://substackcdn.com/image/fetch/$s_!e7Nx!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F20c555d1-1d29-42db-a709-8726cc18f346_875x1311.png)](https://substackcdn.com/image/fetch/$s_!e7Nx!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F20c555d1-1d29-42db-a709-8726cc18f346_875x1311.png)

Warrant is basically a fancy call option.

If certain conditions are met, OpenAI gets AMD shares.

Amazon has been the most prolific user of this tactic. Astera Labs, Marvell, Fabrinet, AAOI, …

But Amazon’s shenanigans are nothing compared to what Sue Bae and Sama have cooked up.

The reason I hate these warrant deals is it messes with my investment process.

I care deeply about gross margins. It’s the first financial number I check. 

**These kinds of warrant deals are inherently distortive to gross margins.**

Here is a toy example.

[![](https://substackcdn.com/image/fetch/$s_!j3yJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd6108e22-5a74-4912-aa6d-e64b0826e91e_583x257.png)](https://substackcdn.com/image/fetch/$s_!j3yJ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd6108e22-5a74-4912-aa6d-e64b0826e91e_583x257.png)

Due to how these warrant deals are structured, they effectively act as a floating discount to products. 

If I sell you thing for $200 but hand you the right to buy 1 share of stock at $0.01 even though the trading price is $20.01/share at the time of you buying thing, that is a $20 effective discount.

 **WARRANT DEALS ARE SNEAKY DISCOUNTS**

* * *

Semianalysis is 40 people and they have three engineers working on this InferenceMax project. Dylan publicly said these numbers several times.

[![](https://substackcdn.com/image/fetch/$s_!NCu0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F58af3f3b-9e93-471d-b1c2-a323e0b79ff1_841x510.png)](https://substackcdn.com/image/fetch/$s_!NCu0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F58af3f3b-9e93-471d-b1c2-a323e0b79ff1_841x510.png)

OpenAI has over 6000 employees. 

Given how important inference economics are to OpenAI as a business, it is reasonable to assume that **OpenAI has somewhere between 30-300 full-time employees doing this same testing and analysis.**

This is a very reasonable conclusion. 

OpenAI knows their internal closed-source model workloads much better.

OpenAI knows their own tokenomics cost structure.

 **OPENAI KNOWS PRECISLY WHAT DISCOUNT (VIA WARRANT) IS NEEDED TO MAKE AMD HARDWARE ECONOMICALLY VIABLE.**

* * *

Nvidia has a blog post based on the Semianalysis InferenceMax data today.

<https://blogs.nvidia.com/blog/blackwell-inferencemax-benchmark-results/>

The message is clear:

[![](https://substackcdn.com/image/fetch/$s_!Yl0S!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6dda211b-e10b-4be7-bf6c-27cb999e93f6_12031x6870.png)](https://substackcdn.com/image/fetch/$s_!Yl0S!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6dda211b-e10b-4be7-bf6c-27cb999e93f6_12031x6870.png)

Our product is crazy profitable.

This is true. Great for Nvidia.

Now… I would like to remind everyone here that at the time of writing:

  * I own ~$240K worth of Nvidia shares at an average price of $13.91/share.

  * I own ~$87K worth of Nvidia call options at various strikes, expiration, and cost basis.

  *  **I have zero economic exposure to AMD.**




[![](https://substackcdn.com/image/fetch/$s_!n76x!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F64006b26-3438-404a-abe8-f52d9667e640_1440x777.webp)](https://substackcdn.com/image/fetch/$s_!n76x!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F64006b26-3438-404a-abe8-f52d9667e640_1440x777.webp)

InferenceMax Data has Clear and Obvious Conclusions:

  * Nvidia

    * Comically undervalued.

    * AI inference is crazy profitable on GB200 NVL72.

    * Demand is going thru the roof.

    * Nvidia has the most profitable hardware.

    * Nvidia systems have the most capabilities for the largest and best models.

    *  **NVL72 engineering benefits directly translate into massive profitability enablement.**

  * AMD

    *  **OpenAI warrant deal is genius.**

    * AMD actually going to hit $600/share ****eventually**** given the last tranche of warrants appear to vest upon stock hitting that strike price.




[![](https://substackcdn.com/image/fetch/$s_!wk5y!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2ad2f598-20c1-4d85-936d-6681dd7ddb76_471x632.png)](https://substackcdn.com/image/fetch/$s_!wk5y!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2ad2f598-20c1-4d85-936d-6681dd7ddb76_471x632.png)

 **I have massive financial incentive to tell you AMD sucks and yet I am unironically saying InferenceMAX is positive **both** Nvidia and AMD but for different reasons.**

[![](https://substackcdn.com/image/fetch/$s_!bo8u!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fae9865bf-657a-407a-b94c-db6d358393df_728x765.png)](https://substackcdn.com/image/fetch/$s_!bo8u!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fae9865bf-657a-407a-b94c-db6d358393df_728x765.png)

Sometimes, investing can be simple.

Subscribe for engineering-driven investment analysis.

Subscribe

Share with Nvidia and AMD employees. May their RSUs goto moon.

[Share](https://irrationalanalysis.substack.com/p/semianalysis-clustermax-launch-surprising?utm_source=substack&utm_medium=email&utm_content=share&action=share)
