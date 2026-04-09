# Gelsinger's Heroic Amputations

## Very positive news for Intel.

**Sep 17, 2024**

**Likes:** 0

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Please check the [‘about’ page](https://irrationalanalysis.substack.com/about) for a list of active positions.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice, and readers should **always do their own research before investing in any security.**

  * Feel free to contact me via email at: _irrational_analysis@proton.me_




* * *

[INTC 0.00%↑](https://substack.com/discover/stocks/INTC) is up ~18% in the last five trading days.

[![](https://substackcdn.com/image/fetch/$s_!wDr9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcb521a09-0209-452f-9bb7-0008098666f1_1439x2822.jpeg)](https://substackcdn.com/image/fetch/$s_!wDr9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcb521a09-0209-452f-9bb7-0008098666f1_1439x2822.jpeg)

Some of this rally is shorts getting absolutely rekt. 😈

[![](https://substackcdn.com/image/fetch/$s_!U5sB!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb0fcccbe-5605-477c-9292-8fcfd8c00eb8_551x481.png)](https://substackcdn.com/image/fetch/$s_!U5sB!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb0fcccbe-5605-477c-9292-8fcfd8c00eb8_551x481.png)Visual approximation of Pat “Galaxy-Brain” Gelsinger shattering the returns of short-selling tourists.

But a lot of this move is due to very positive news. Let’s go over it.

[![](https://substackcdn.com/image/fetch/$s_!P308!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F44213f72-b864-4e84-aa68-8540fbfb3688_991x192.png)](https://substackcdn.com/image/fetch/$s_!P308!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F44213f72-b864-4e84-aa68-8540fbfb3688_991x192.png)

New $3B in funding (incremental/orthogonal) on top of existing CHIPS money. Somewhat expected. By far the least interesting piece of news out there.

[![](https://substackcdn.com/image/fetch/$s_!vquA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fed899f7c-fc5e-4f29-8c51-2bb7cf62e4bd_1022x415.png)](https://substackcdn.com/image/fetch/$s_!vquA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fed899f7c-fc5e-4f29-8c51-2bb7cf62e4bd_1022x415.png)

First, my guess on what this “AI fabric chip” is for AWS.

Trainium and Inferentia have no Ethernet on-die. Everything is PCIe. There is a need for a NIC that acts like a high-end/high-bandwidth Nitro for Amazon’s AI ASICs, which are semi-custom from [MRVL 0.00%↑](https://substack.com/discover/stocks/MRVL) and fabbed by [TSM 0.00%↑](https://substack.com/discover/stocks/TSM).

Here are the four possibilities:

  1. Designed by Intel NEX (Mount Evans Group or similar).

  2. Designed by Amazon.

  3. Semi-custom designed by Marvell and Amazon.

  4. Semi-custom designed by Amazon with Intel PCIe PHY and PMA IP.




My guess is #4. Nobody other than Intel has PCIe IP on 18A. In order for this AWS AI fabric chip to come out in any reasonable amount of time, it has to use Intel internal interface IP. Amazon likes to customize their Nitro NICs (used for CPU security/virtualization/fabric acceleration) so I doubt Intel Design has much influence over anything other than interface IP and packaging assistance.

As for the custom Xeon 6, I believe it is a modified Granit Rapids. Given Amazon’s great success with Graviton, it makes no sense for them to commission a customized Sierra Forest. This kind of deal is not new. Cooper Lake was a custom Xeon family made for [META 0.00%↑](https://substack.com/discover/stocks/META) that added BF16 and some minor NoC updates to Skylake+ (Cascade Lake).

[![](https://substackcdn.com/image/fetch/$s_!uOKT!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F785c740e-006e-4e07-bb8e-0175c4fc1a92_995x456.png)](https://substackcdn.com/image/fetch/$s_!uOKT!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F785c740e-006e-4e07-bb8e-0175c4fc1a92_995x456.png)

Wholly owned subsidiary allows for more funding to directly go to the Fabs. Great! One step closer to a full separation a-la AMD/GloFo.

[![](https://substackcdn.com/image/fetch/$s_!WBf-!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffd24d0c1-ce2d-4ec1-a036-14ce760c871c_1010x574.png)](https://substackcdn.com/image/fetch/$s_!WBf-!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffd24d0c1-ce2d-4ec1-a036-14ce760c871c_1010x574.png)

The EU Fabs are basically canceled. Claiming that there is a “2-year delay” is just a tactic to keep the EU clowns pacified. 

Halting startup of the Malaysia advanced packaging facility is a direct admission that there is high-volume 3rd-party demand for IFS advanced packaging. EMIB and Foveros have only recently gotten proper industry-standard EDA design flows.

[![](https://substackcdn.com/image/fetch/$s_!v8ij!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F11e87a39-43ec-4f71-9cdf-6bb8c84520a9_1019x597.png)](https://substackcdn.com/image/fetch/$s_!v8ij!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F11e87a39-43ec-4f71-9cdf-6bb8c84520a9_1019x597.png)

In general, re-orgs are a precursor to layoffs. If there are any Intel employees within the groups that have been moved into larger orgs reading this, your heads are at risk of being efficiently sacrificed to the shareholders. 

New upper management that you roll up to has been given a budget. They have to cut to meet that budget. You are the new expenses in their org. 

Remember what happened when Raja was fired and AXG got re-orged into CCG and DCAI?

[![](https://substackcdn.com/image/fetch/$s_!KwNH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F43ddd2ca-157d-4a20-aeca-b3cf6694efd6_621x377.png)](https://substackcdn.com/image/fetch/$s_!KwNH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F43ddd2ca-157d-4a20-aeca-b3cf6694efd6_621x377.png)

[![](https://substackcdn.com/image/fetch/$s_!sSEN!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F375d9d63-ddc9-42db-b111-b27ced7917ef_1002x259.png)](https://substackcdn.com/image/fetch/$s_!sSEN!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F375d9d63-ddc9-42db-b111-b27ced7917ef_1002x259.png)Guess who is going to make these difficult decisions. (the upper management of the big org your tiny org has been yeeted into)

Friendly warning.

Subscribe for more timely analysis, with the occasional meme.

Subscribe

Share the memes.

[Share](https://irrationalanalysis.substack.com/p/gelsingers-heroic-amputations?utm_source=substack&utm_medium=email&utm_content=share&action=share)
