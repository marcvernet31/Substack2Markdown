# Logic Foundry Slash and Burn

## Have faith in Lip-Bu Tan's flamethrower.

**Apr 22, 2025**

**Likes:** 0

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Please check the [‘about’ page](https://irrationalanalysis.substack.com/about) for a list of active positions.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice, and readers should **always do their own research before investing in any security.**

  * Feel free to contact me via email at: _irrational_analysis@proton.me_




* * *

Leading edge logic foundries are in strange spot right now. Engineering reality appears to be diverging from financial/investment outlook.

Let’s start with my own biases first:

  * TSMC

    * I was a longtime [TSM 0.00%↑](https://substack.com/discover/stocks/TSM) shareholder across many accounts.

    * Every single share I owned was liquidated after “Liberation Day” stupidity was announced. Booked a lot of long-term profits and sitting on cash.

    * Waiting to buy back in once things settle down.

  * Intel:

    * I have a small position and trade it frequently.

    * Write covered calls. Trade in and out. 

  * Samsung Electronics

    * No access to Korean equity markets.




[![](https://substackcdn.com/image/fetch/$s_!oBc3!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F16ecfaf7-1073-49c4-93ed-380de1b2b0d2_1439x729.jpeg)](https://substackcdn.com/image/fetch/$s_!oBc3!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F16ecfaf7-1073-49c4-93ed-380de1b2b0d2_1439x729.jpeg)

To those of you who thought Intel would be insulated from tariffs…

[![](https://substackcdn.com/image/fetch/$s_!A5uW!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F99bf09e6-7849-45ae-83d2-482e6ffbc035_1440x3088.jpeg)](https://substackcdn.com/image/fetch/$s_!A5uW!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F99bf09e6-7849-45ae-83d2-482e6ffbc035_1440x3088.jpeg)

Lol no. 

Let’s go over some recent news before stock opinions.

## Intel Products has reserved TSMC N2 capacity.

I have been waiting for this rumor to finally circulate more publicly.

[![](https://substackcdn.com/image/fetch/$s_!VVhQ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb0c04ffb-780b-47b8-82c6-18d091c2de9a_595x252.png)](https://substackcdn.com/image/fetch/$s_!VVhQ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb0c04ffb-780b-47b8-82c6-18d091c2de9a_595x252.png)https://x.com/dnystedt/status/1914488460075000145

[![](https://substackcdn.com/image/fetch/$s_!o3Cr!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6639cdd8-4b56-48cf-960d-e322fd0a484c_590x263.png)](https://substackcdn.com/image/fetch/$s_!o3Cr!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6639cdd8-4b56-48cf-960d-e322fd0a484c_590x263.png)https://x.com/Jukanlosreve/status/1914477624132575274

Nova Lake is the successor to Panther Lake. So target H2 2026.

It is very amusing to see how the Intel shills keep moving the goalposts as new information re-affirms how fucked 18A is right now.

  1. 18A is good! Panther Lake is ramping on-time.

  2. Ok nevermind Panther Lake is delayed but 18A is still better than TSMC N2 because of a bullshit density number published in a bullshit conference paper.

  3. Intel is dual-sourcing Nova Lake. 18A is still fine.




18A is busted in its current state. Next generation 18A-P will fix many of the PDK problems _(missing libraries, missing device characterizations, poor leakage, high process variation)_ but it will take time.

18A-P will be good in 2027. In the meantime, Intel themselves (products group) know they cannot survive with regular 18A. 

## Most public claims are bullshit.

[![](https://substackcdn.com/image/fetch/$s_!rtm6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F01c502c2-ac2b-4f1f-a68b-30e1c00032ef_600x1286.png)](https://substackcdn.com/image/fetch/$s_!rtm6!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F01c502c2-ac2b-4f1f-a68b-30e1c00032ef_600x1286.png)

Transistor density numbers are often cited as a way of comparing process nodes. Often, this density number is for a single structure such as SRAM.

This is not a viable method of comparing leading edge logic nodes.

The only reliable method is to port an IP block (CPU core, ASIC block, PCIe PHY) or an entire product (smartphone SoC, AI ASIC) from one process node to another.

When a new node comes out, every design company does this internally. Onces designers have a feel for the PDK, they make adjustments to optimize the design for that particular process node.

There are many complex tradeoffs. Here is an example scenario that may be helpful for your mental model.

Project is 30% analog, 20% SRAM, 50% digital logic.

New process node (porting target) has the following attributes:

  * 10% higher (better) SRAM density.

  * 5% lower (better) leakage power on digital logic.

  * 10% lower (worse) max switching frequency of digital logic cells.

  * High variation for analog devices. (MOSCAP, MIMCAP, high-metal inductors)




Public marketing claims, conference papers, and TechInsights retards reports all claim that new process node is 10% better. Look at the scanning-electron microscope pictures of SRAM cells!

[![](https://substackcdn.com/image/fetch/$s_!FhN8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F725e0ad0-4387-4934-a267-584cb7b48ef2_720x717.png)](https://substackcdn.com/image/fetch/$s_!FhN8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F725e0ad0-4387-4934-a267-584cb7b48ef2_720x717.png)

In reality the new process node is meaningfully worse in terms of area of a real product.

  * Lower max switching frequency of transistors requires designers to blow up digital logic area to achieve target clock speeds.

  * High analog device variation requires significant analog area increase and much higher leakage power for the analog blocks.




## Engineering Reality

Intel 18A is not competitive with TSMC N3P at this time. It will be competitive late 2026 if Intel makes (realistically achievable) improvements to the PDK.

Intel 18A-P will be competitive with TSMC N3P in ****2027**** on PPA (power, performance, area) and can even compete with TSMC N2 on cost.

 **Intel 18A has real traction (test chips, serious evaluations) but this is at an R &D level.** Revenue comes mid to late 2026 and only for modest-scale projects.

Samsung Foundry SF3 is an unmitigated disaster. There is almost zero activity on this node. **PPA is worse than TSMC N5** (yes N5, not N4P… it really is that bad).

SF2 is vaporware and really just a re-brand of SF3. Samsung Foundry is basically trying to fix SF3 and decided it to re-name it. **SF2 is not a “2nm-class” process node like TSMC N2 or Intel 14A.**

## Investment Corner

I want to buy back into [TSM 0.00%↑](https://substack.com/discover/stocks/TSM) at some point. 

[![](https://substackcdn.com/image/fetch/$s_!BF_F!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F724575aa-75ee-4299-9f28-a49ec5b3d793_1440x3088.jpeg)](https://substackcdn.com/image/fetch/$s_!BF_F!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F724575aa-75ee-4299-9f28-a49ec5b3d793_1440x3088.jpeg)

It’s not there yet.

As for Intel, let’s look at their Price/Book ratio.

[![](https://substackcdn.com/image/fetch/$s_!UT-t!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc29b602c-243a-408f-a3b3-0af339fe669e_1439x2345.jpeg)](https://substackcdn.com/image/fetch/$s_!UT-t!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc29b602c-243a-408f-a3b3-0af339fe669e_1439x2345.jpeg)

As you can see, the PB is less than one. Finance people (~half of audience) know what this means. Let me explain this for everyone else.

Imagine you have a bakery. 

This bakery has some intrinsic value. (assets)

  * The land it was built on.

  * The building itself.

  * Equipment in the kitchen. 

  * Recipes and methods. (intellectual property // trade secrets)

  * Brand. (reputation amongst the locals)




Your bakery also has debt. (liabilities)

  * Mortgage.

  * Money you own to the wheat farmer.

  * Wages you need to pay to employees at the end of the month.




Combine all of the above and you get book value. 

Now imagine your bakery is publicly traded. The share price is determined by investor demand.

There are three possibilities:

  1. Shares trade for > 1x book value, implying that investors thing the business is worth something in the long term.

  2. Shares trade at 1x book value. Investors don’t think much of the company but recognize the assets are marked appropriately. 

  3. Shares trade at < 1x book value. **The bakery is on fire.**




[![a bakery on fire. No firefighters or people.](https://substackcdn.com/image/fetch/$s_!Xqbf!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5b1485f5-7200-4b83-a23c-9dac1347a25d_1024x1024.jpeg)](https://substackcdn.com/image/fetch/$s_!Xqbf!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5b1485f5-7200-4b83-a23c-9dac1347a25d_1024x1024.jpeg)

[INTC 0.00%↑](https://substack.com/discover/stocks/INTC) is an attractive defensive investment for the following reasons:

  * It probably can’t get much worse. 

  * Lip-Bu Tan is going to slash CapEx, preserving book value.

    * Spending money of 18A Fabs nobody is going to use (in volume before 2027) is a great way of lighting book value on fire.

    * Depreciation expense on semicap is very high.

  * Lip-Bu Tan is probably going to fire 40-50% of Intel. This will also preserve book value as Intel tries to survive.

  * Once 18A-P is working, Intel stock can easily re-rate to 2-3x book value.

    * Global Foundries and Tower Semiconductor both trade around 1.3-2x P/B.

    * A well-run and resurgent Intel (via 18A-P results and 14A hype) deserves a valuation premium over [GFS 0.00%↑](https://substack.com/discover/stocks/GFS) and [TSEM 0.00%↑](https://substack.com/discover/stocks/TSEM).




[![](https://substackcdn.com/image/fetch/$s_!ikep!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff8920ee9-6e2f-41aa-ade2-4f40340e7a36_597x598.png)](https://substackcdn.com/image/fetch/$s_!ikep!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff8920ee9-6e2f-41aa-ade2-4f40340e7a36_597x598.png)

I have faith in Lip-Bu Tan’s flamethrower.

Ashes make great fertilizer. 

It’s time to [slash and burn.](https://en.wikipedia.org/wiki/Slash-and-burn)

Subscribe for engineering-driven investment analysis.

Subscribe

Share with future ashes?

[Share](https://irrationalanalysis.substack.com/p/logic-foundry-slash-and-burn?utm_source=substack&utm_medium=email&utm_content=share&action=share)
