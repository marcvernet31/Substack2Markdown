# Nvidia Blackwell Delay Note

## Understanding the engineering behind the news.

**Aug 04, 2024**

**Likes:** 0

# IMPORTANT:

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Please check the [‘about’ page](https://irrationalanalysis.substack.com/about) for a list of active positions.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice and readers should **always do their own research before investing in any security.**

* * *




Nvidia is delaying Blackwell by at least three months due to design flaws related packaging. Monday is going to be spicy to say the least.

Over half of my holdings are Nvidia shares, and I have no intention to sell. There are only two reasons in which I sell a stock:

  1. The reason for my original investment changes.

  2. Need money in real life.




Nvidia is technologically years ahead of the competition. Short term, its gona get really volatile and real ugly. Not selling my shares. 

I have sold covered calls against the vast majority of my [NVDA 0.00%↑](https://substack.com/discover/stocks/NVDA) position though. 

[![](https://substackcdn.com/image/fetch/$s_!imkS!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff2b203b1-fc19-480f-b4af-c53d6654429e_1439x715.jpeg)](https://substackcdn.com/image/fetch/$s_!imkS!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff2b203b1-fc19-480f-b4af-c53d6654429e_1439x715.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!PTBJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F216d5450-d80d-46ca-9f54-7ada295354d8_552x818.png)](https://substackcdn.com/image/fetch/$s_!PTBJ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F216d5450-d80d-46ca-9f54-7ada295354d8_552x818.png)

Looking forward to seeing these call options I wrote expire worthless. 🙃

* * *

So what is happening? To understand, you must have a basic grasp of how packaging works.

[![](https://substackcdn.com/image/fetch/$s_!EL6S!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fff8e58a1-4027-409a-a1c4-b64ad59558ce_965x741.png)](https://substackcdn.com/image/fetch/$s_!EL6S!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fff8e58a1-4027-409a-a1c4-b64ad59558ce_965x741.png)

Blackwell needs CoWoS-L, as opposed to the CoWoS-S used by prior Nvidia GPUs.

So why is there a difference? Simplistically… bump pitch. AKA how far the little contact pads are away from each other.

CoWoS-S diagram with micro-bumps highlighted:

[![](https://substackcdn.com/image/fetch/$s_!C2Vl!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5757f9b6-63b2-4b66-8818-cdf3f351fb87_588x619.png)](https://substackcdn.com/image/fetch/$s_!C2Vl!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5757f9b6-63b2-4b66-8818-cdf3f351fb87_588x619.png)

CoWoS-L with the challenging micro-bumps highlighted:

[![](https://substackcdn.com/image/fetch/$s_!XoDV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa3bb9e8c-c3c8-44d5-a678-f02eaf223eb7_1568x463.png)](https://substackcdn.com/image/fetch/$s_!XoDV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa3bb9e8c-c3c8-44d5-a678-f02eaf223eb7_1568x463.png)

CoWoS-L has the following pros and cons:

  * Pros:

    * More density for additional signaling, say for a 10TB/s die-to-die interface.

    * Better power integrity, and thus power delivery, and thus power efficiency at a system level.

  * Cons:

    * Higher difficulty manufacturing, leading to lower yields.

    * Higher risk of thermal-induced degradation, causing micro-bumps to crack over time and thus cause reliability issues.




Smaller bumps are harder to line up.

Things expand as they get hot and contract when they cool down. Smaller bumps can handle less mechanical stress from thermal cycles.

You can see where problems might arise.

And so they have! 

* * *

What does this mean for the future? Is the supposed 3-month delay plausible, or could it be worse?

To understand, you must understand how chips are made:

[![A Guide on Semiconductor Development ](https://substackcdn.com/image/fetch/$s_!gQ75!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2cc1731f-66e6-480b-af49-c0267681bffa_1365x986.png)

#### A Guide on Semiconductor Development 

[Daud's Scout](https://substack.com/profile/135313705-dauds-scout)·September 2, 2023[Read full story](https://irrationalanalysis.substack.com/p/a-guide-on-semiconductor-development)](https://irrationalanalysis.substack.com/p/a-guide-on-semiconductor-development)

[![](https://substackcdn.com/image/fetch/$s_!7uto!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0838a685-de79-4704-bb47-3e6fb6bcd443_579x283.webp)](https://substackcdn.com/image/fetch/$s_!7uto!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0838a685-de79-4704-bb47-3e6fb6bcd443_579x283.webp)

[![](https://substackcdn.com/image/fetch/$s_!1zNt!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fee302fda-72c9-4549-aa0a-f6b0c56acc3b_684x454.png)](https://substackcdn.com/image/fetch/$s_!1zNt!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fee302fda-72c9-4549-aa0a-f6b0c56acc3b_684x454.png)

Chips have layers. Transistors at bottom. Each layer above gets larger/thicker. Eventually, the top of the chip is finished off an this is called the “bump out”.

[![](https://substackcdn.com/image/fetch/$s_!ezo-!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8fc174d2-16fc-468e-8151-936206f05b4f_940x612.png)](https://substackcdn.com/image/fetch/$s_!ezo-!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8fc174d2-16fc-468e-8151-936206f05b4f_940x612.png)

In general, chips have many duplicate bumps for power, ground, and even signaling, even though in-silicon layers short these bumps.

For example, you could be feeding the same supply voltage into four neighboring bumps, even though the silicon itself shorts all four of these bumps in layer M15 or whatever.

Why do this? The answer is complicated electromagnetic technobabble.

Bad things happen if a lot of current is shoved through one tiny bump.

Bad things happen if a signal bump is not surrounded by ground bumps.

* * *

Nvidia claims the delay will be three months or more. My theory is they are going to re-spin the logic dies and change the bump-out. Some bumps can be removed, spaced out, fiddled with. A three-month delay tracks with a re-do of the top metal layers of the logic die to accommodate a new bump-out with better yield and reliability margins. 

From an investment perspective, nothing has changed for me other than two actions I took last week:

  1. Sold covered calls against the vast majority of my [NVDA 0.00%↑](https://substack.com/discover/stocks/NVDA) position.

  2. Covered my [AMD 0.00%↑](https://substack.com/discover/stocks/AMD) short, rotating into a [QCOM 0.00%↑](https://substack.com/discover/stocks/QCOM) short.




AMD is an attractive gambling opportunity now. I kinda want tp degen buy calls because this Blackwell delay will juice MI300/325X order volumes for the next few quarters. 

[![](https://substackcdn.com/image/fetch/$s_!LzZ7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F874ca356-8878-421e-b588-eb949449e7dc_703x740.png)](https://substackcdn.com/image/fetch/$s_!LzZ7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F874ca356-8878-421e-b588-eb949449e7dc_703x740.png)

In the most recent earnings call, AMD CEO Dr. Lisa Su claimed they had visibility into 2025 for their datacenter GPU business. At the time I thought this was either delusional nonsense or materially false statements. It seems like Su bae already knew about the Blackwell delay….

[![](https://substackcdn.com/image/fetch/$s_!XvQI!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F386a7c71-367c-4b89-938e-64b4d8764092_422x253.png)](https://substackcdn.com/image/fetch/$s_!XvQI!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F386a7c71-367c-4b89-938e-64b4d8764092_422x253.png)

Subscribe for free, engineering-driven investment analysis.

Subscribe

Share to make the subscriber dashboard numbers go up, even as portfolio value plumets. 

[Share](https://irrationalanalysis.substack.com/p/nvidia-blackwell-delay-note?utm_source=substack&utm_medium=email&utm_content=share&action=share)
