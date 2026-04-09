# Memory Madness

## Crazy start to 2026.

**Jan 16, 2026**

**Likes:** 0

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice and readers should **always do their own research before investing in any security.**

  * Feel free to contact me via email at: _irrational_analysis@proton.me_




* * *

The first two weeks of 2026 have been crazy. 

My recent 2026 Irrational Ideas post (Dec 21st, 2025) has been doing well so I thought a brief update would be helpful.

  1. Ended up buying both Camtek and Onto. (changed my mind… Samsung HBM4 ramp is well correlated with Onto)

  2. Buying Semtech next week as I still need to wait a few more days for wash sale rule to pass. (Sold Macom early and too salty to buy back in)

  3. I am long Arista now lol. This is on a whim. 

  4. Cerebras is going to be a long once they IPO. Suicidal short at this point after the OpenAI deal. Have a much longer deep-dive into Groq/Cerebras/D-Matrix/SambaNova soon… been very busy.




Also, the semicap post was perfectly timed. Gotta gloat that one.

Now on to the topic of today’s brief note… **memory.**

Two interesting datapoints. First, this Keybank update slide.

[![](https://substackcdn.com/image/fetch/$s_!xbfB!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0ab54b17-5b39-4f75-aa3d-c42fb2f3d54a_1440x1136.webp)](https://substackcdn.com/image/fetch/$s_!xbfB!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0ab54b17-5b39-4f75-aa3d-c42fb2f3d54a_1440x1136.webp)

I am a Qualcomm perma-bear but this info is so much worse than my wildest bearish fever dreams.

[![](https://substackcdn.com/image/fetch/$s_!MUNC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4f4152da-3ee1-43b5-86e7-4f0fa74ce130_626x625.png)](https://substackcdn.com/image/fetch/$s_!MUNC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4f4152da-3ee1-43b5-86e7-4f0fa74ce130_626x625.png)

Some background before returning to the root cause (memory).

Qualcomm has recently shifted strategy on the premium tier. There are now two versions.

For 2025 launch smartphones, the 8G5 “Elite” is the flagship while the regular 8G5 has been cut down in the following ways:

  1. Cut 1/3 of GPU cores and reduce cache from 18 MB to 2MB.

  2. Cut down modem from x85 to x80.

  3. Reduce CPU core clock from 4.6 GHz to 3.8 GHz.




All of these changes are classic yield harvesting (binning) tactics. This is very common in other consumer electronics segments (laptop CPU, gaming GPU) and its smart business to start applying this practice to smartphones.

The problem is that the financial pressures are collapsing the SKU stack.

 **Key (PUN INTENTED) KeyBanc Claims:**

  1. ASP of 8G6 is up 20% over 8G5.

  2. Binned-down 8G6 “lite” is same price as 8G5.

  3.  **Many Chinese smartphone OEMs are choosing the 8G6 “lite”.**

  4.  **Qualcomm is allegedly considering a 5-10% price cut to the 8G6.**




Presumably, the 8G6 “lite” has similar yield harvesting tactics that reduce critical area (cut GPU cores, cut active SRAM) and reduce FMAX requirements (lower GPU/CPU clock, cut modem features).

OEMs choosing the lower-end SKU in significant volume flies in the face of the core narrative Qualcomm management has been trying to push for years.

We don’t have to go back that far. How about the last earnings call from November 5th, 2025?

[![](https://substackcdn.com/image/fetch/$s_!iUC7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3c144097-5474-4a09-a558-9f9524162d95_913x522.png)](https://substackcdn.com/image/fetch/$s_!iUC7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3c144097-5474-4a09-a558-9f9524162d95_913x522.png)

[![](https://substackcdn.com/image/fetch/$s_!qi6a!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F680d476f-5657-4a67-aa07-2e1501e13952_914x527.png)](https://substackcdn.com/image/fetch/$s_!qi6a!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F680d476f-5657-4a67-aa07-2e1501e13952_914x527.png)

Ah yes, “competition between the OEMs drives [demand for more premium chips].”

Well… looks like the OEMs have all decided the upcoming chips are too expensive.

 **Content growth is grinding to a halt because of memory.**

Amusingly, none of this is Qualcomm’s fault. They are just one of the biggest losers of higher DRAM prices.

[![](https://substackcdn.com/image/fetch/$s_!r2G6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F69965a2c-a625-42aa-9d10-9937e8d9a5fb_588x1201.png)](https://substackcdn.com/image/fetch/$s_!r2G6!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F69965a2c-a625-42aa-9d10-9937e8d9a5fb_588x1201.png)

[![X avatar for @getpeid](https://substackcdn.com/image/fetch/$s_!t8Ff!,w_40,h_40,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fpbs.substack.com%2Fprofile_images%2F1938553071950258176%2Fe35-o35P.jpg)Carl Pei@getpeidhttps://t.co/ynfCSXu0Yh2:30 AM · Jan 14, 2026 · 91K Views

* * *

58 Replies · 42 Reposts · 459 Likes](https://x.com/getpeid/status/2011264565598912657)

Downgrading specs. Economic value shifting from Qualcomm/MediaTek to Samsung/SK/Micron.

Someone on sell-side should ask Qualcomm management what happens to QCT gross margins when the cost of TSMC N2 wafers goes up and all the customers chose to de-spec the SoC. Really, I want to see how they spin this. Years of shilling “demand for more compute drives more Qualcomm content” is about to blow up lmao.

* * *

The other datapoint on memory I find very interesting is an insider buy by a Micron director. Normally, I don’t take insider activity too seriously, but this one is crazy.

[![](https://substackcdn.com/image/fetch/$s_!wdPX!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fce7f10c2-8bf9-4286-95d7-68bc5f218929_588x673.png)](https://substackcdn.com/image/fetch/$s_!wdPX!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fce7f10c2-8bf9-4286-95d7-68bc5f218929_588x673.png)

[![X avatar for @ResearchQf](https://substackcdn.com/image/fetch/$s_!Q0I_!,w_40,h_40,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fpbs.substack.com%2Fprofile_images%2F1983279202397827072%2FIxHBgZ-4.jpg)QF Research@ResearchQfMark Liu, $MU board member and former Co-CEO of $TSM, bought ~$8 million of MU on the open market this week. He purchased 23,200 shares on Tues and Wed at ~$337 and now owns 25,910 shares, at least on a direct basis. This is the largest open market purchase since at least 2023. ![](https://pbs.substack.com/media/G-yhSc6bIAAb3w6.jpg)1:50 PM · Jan 16, 2026 · 8.08K Views

* * *

3 Replies · 6 Reposts · 71 Likes](https://x.com/ResearchQf/status/2012160574654697858?s=20)

Let’s look up this guy. 

[![](https://substackcdn.com/image/fetch/$s_!b9y5!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F200ca9ce-d718-446c-901f-b8c6ba3ef0c5_807x750.png)](https://substackcdn.com/image/fetch/$s_!b9y5!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F200ca9ce-d718-446c-901f-b8c6ba3ef0c5_807x750.png)

Ok so he is a talented engineer that has decades of experience with semiconductor cycles as former TSMC co-CEO.

And this dude just spent $8M of HIS OWN MONEY buying Micron shares. This is not a stock option or compensation! His own cash money.

I have spent the last 6 months looking at the Micron chart in anguish.

[![](https://substackcdn.com/image/fetch/$s_!FRH_!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4424fc0f-87a6-459e-96e1-b512e698e541_627x1145.webp)](https://substackcdn.com/image/fetch/$s_!FRH_!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4424fc0f-87a6-459e-96e1-b512e698e541_627x1145.webp)

You see those crayon lines? This is how I guess what strike I want to use for options. Those lines are leftover from May 2025 when I chickened out.

Micron director has finally forced me off the sidelines. Back-in, but at small size with covered calls for protection. Same thing on Sandisk.

[![the mad hatter is scrambling to gather memory sticks. He is unhappy.](https://substackcdn.com/image/fetch/$s_!PfAh!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6203e883-56f1-42e4-a3f7-ab2f456e510b_540x540.jpeg)](https://substackcdn.com/image/fetch/$s_!PfAh!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6203e883-56f1-42e4-a3f7-ab2f456e510b_540x540.jpeg)

* * *

Trading account snapshot at the time of writing.

[![](https://substackcdn.com/image/fetch/$s_!m-yt!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F139e29e9-7231-4165-b32c-a04af6058c63_808x1041.webp)](https://substackcdn.com/image/fetch/$s_!m-yt!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F139e29e9-7231-4165-b32c-a04af6058c63_808x1041.webp)

[![](https://substackcdn.com/image/fetch/$s_!__Je!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcd957114-854f-4c90-bc44-d701b00dc2fd_1055x1041.webp)](https://substackcdn.com/image/fetch/$s_!__Je!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcd957114-854f-4c90-bc44-d701b00dc2fd_1055x1041.webp)

[![](https://substackcdn.com/image/fetch/$s_!Akgq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb8bf8b73-7355-4bf7-b610-7e0d16761c9d_847x1041.webp)](https://substackcdn.com/image/fetch/$s_!Akgq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb8bf8b73-7355-4bf7-b610-7e0d16761c9d_847x1041.webp)

[![](https://substackcdn.com/image/fetch/$s_!aNL9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6513ca35-d7d5-43b1-b6d3-624778690d32_762x1041.webp)](https://substackcdn.com/image/fetch/$s_!aNL9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6513ca35-d7d5-43b1-b6d3-624778690d32_762x1041.webp)

[![](https://substackcdn.com/image/fetch/$s_!nr4y!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F30fbe2a9-bfc7-4ce1-aa6a-8fb55c545714_768x1041.webp)](https://substackcdn.com/image/fetch/$s_!nr4y!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F30fbe2a9-bfc7-4ce1-aa6a-8fb55c545714_768x1041.webp)

[![](https://substackcdn.com/image/fetch/$s_!D2OA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F00b1c28b-2822-43d1-936b-9d19f841570b_1440x501.webp)](https://substackcdn.com/image/fetch/$s_!D2OA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F00b1c28b-2822-43d1-936b-9d19f841570b_1440x501.webp)

Subscribe for engineering-driven investment analysis.

Subscribe

Share?

[Share](https://irrationalanalysis.substack.com/p/memory-madness?utm_source=substack&utm_medium=email&utm_content=share&action=share)
