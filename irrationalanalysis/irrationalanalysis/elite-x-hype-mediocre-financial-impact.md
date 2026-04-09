# Elite X Hype, Mediocre Financial Impact

## Laptop/PC predictions, simple COGS+GM model, and the last thing Intel needs...

**Apr 27, 2024**

**Likes:** 0

# IMPORTANT:

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Please check the [‘about’ page](https://irrationalanalysis.substack.com/about) for a list of active positions.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice and readers should **always do their own research before investing in any security.**




* * *

Welcome to a post that has very little investment idea value but is a great opportunity for teaching yield harvesting and basic COGS/BOM cost analysis.

I am planning to write a detailed estimate of H100, B100, and Grace BOM cost but that is going to take a long time so here is something simple.

But first, some background.

[![](https://substackcdn.com/image/fetch/$s_!hGww!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5ef2dd03-c46a-4c9b-9f11-0cce2c13f8dc_1438x888.jpeg)](https://substackcdn.com/image/fetch/$s_!hGww!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5ef2dd03-c46a-4c9b-9f11-0cce2c13f8dc_1438x888.jpeg)https://investor.qualcomm.com/financial-information/proxy-statements/content/0001104659-18-002272/a17-28583_14defa14a.htm

The above slide is from a proxy SEC filing back in 2018 when [AVGO 0.00%↑](https://substack.com/discover/stocks/AVGO) was trying to acquire [QCOM 0.00%↑](https://substack.com/discover/stocks/QCOM) in a hostile takeover. Qualcomm claimed there was a ~1B dollar revenue opportunity for the next fiscal year (2019) and evil Hock Tan was going to throw it all away if he took over.

FY2023 has come and gone and Qualcomm’s “leading solution” for compute with “always on, 5G to cloud, GIGABIT+ speeds” **has effectively zero revenue.**

[![](https://substackcdn.com/image/fetch/$s_!n4TN!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3ca8f896-6a74-4427-ac61-23bbe9a6ca67_587x637.png)](https://substackcdn.com/image/fetch/$s_!n4TN!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3ca8f896-6a74-4427-ac61-23bbe9a6ca67_587x637.png)

Assuming the laptop/PC TAM is ~250M units/year, Qualcomm is decisively less than 0.1% share. 

[![](https://substackcdn.com/image/fetch/$s_!Nra7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdd08d20d-e25c-49da-9cb8-aa6925c0316a_1427x730.png)](https://substackcdn.com/image/fetch/$s_!Nra7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdd08d20d-e25c-49da-9cb8-aa6925c0316a_1427x730.png)

Qualcomm lumps together the tiny revenue they get from the 0.1% market-share, 7-year old product line into their “IoT” segment which is massively down YoY because the other meh businesses are imploding due to orthogonal reasons.

The new generation (X Elite // Hamoa) is going to be good though. Two years late but still good enough to gain single-digit market share from Intel. Microsoft finally has a passable x86 emulator (with x86-64 support) and Qualcomm invested in a real CPU microarchitecture (Nuvia Orion) instead of reyling on stock ARM (RTL) IP and delusionaly thinking consumers will forgive cripplingly slow performance because 5G 5G 5G 5G 5G!

For more information on instruction sets, including a detailed intuitive understanding of emulation, check out this post. 

[![Instruction Sets For Investors](https://substackcdn.com/image/youtube/w_728,c_limit/QMiubC6LdTA)

#### Instruction Sets For Investors

[Daud's Scout](https://substack.com/profile/135313705-dauds-scout)·October 7, 2023[Read full story](https://irrationalanalysis.substack.com/p/instruction-sets-for-investors)](https://irrationalanalysis.substack.com/p/instruction-sets-for-investors)

* * *

Here is my thesis:

  1. Qualcomm will go from < 0.1% market share in laptop/PC to 5% share by CY 2025.

  2. The stock will not move because sell-side has already priced this in. 

  3. All of Qualcomm’s share gains will be at the expense of [INTC 0.00%↑](https://substack.com/discover/stocks/INTC) who reeeeeeallly do not need another problem to deal with right now.




[![](https://substackcdn.com/image/fetch/$s_!R7aH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F248bbd97-a4a4-4858-91c4-f4a8695d96aa_817x626.png)](https://substackcdn.com/image/fetch/$s_!R7aH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F248bbd97-a4a4-4858-91c4-f4a8695d96aa_817x626.png)Source: Stacy Rasgon of Bernstein Research. Also hobby QCOM IR.

This analysis is completely wrong. 50% gross margin appears to be a random number Stacy made up. We can do better than this. :)

Charlie from Semiaccurate managed to get a decent [die measurement.](https://semiaccurate.com/2023/11/02/how-big-is-qualcomms-snapdragon-x-elite-soc/)

Using this die measurement, we can easily calculate the real BOM and gross margins assuming an ASP of $125. I have an spreadsheet attached with my base, bear, and bull cases. Feel free to download and play with yourself. 

* * *

[![](https://substackcdn.com/image/fetch/$s_!iIEC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F76c5a371-1d7f-4c83-80bf-9ec023a5b939_1205x704.png)](https://substackcdn.com/image/fetch/$s_!iIEC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F76c5a371-1d7f-4c83-80bf-9ec023a5b939_1205x704.png)

Using Charlie’s die measurement and an online [yield calculator](http://cloud.mooreelite.com/tools/die-yield-calculator/index.html), we get 286 good dies per wafer and 42 defective dies. This product is on a TSMC N4 process node which is a derivative of the 5nm-class N5. [Public information suggests a 17K per wafer ](https://www.techspot.com/news/86813-analysts-believe-single-tsmc-5nm-wafer-costs-17000.html#:~:text=According%20to%20CSET's%20model%2C%20a,7nm%20node%20reportedly%20costs%20%249%2C346)price back in 2020. Lets assume 20K per N4 wafer because inflation and the small PPA improvement from minor optimizations and a 2% mask shrink.

[![](https://substackcdn.com/image/fetch/$s_!0QXg!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2f65d46e-42d1-4126-b7fa-2b9e9968ea47_1440x353.webp)](https://substackcdn.com/image/fetch/$s_!0QXg!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2f65d46e-42d1-4126-b7fa-2b9e9968ea47_1440x353.webp)

Those 42 defective dies are not all lost. Through the magic of yield harvesting, semiconductor companies can salvage defective parts into sellable products at a lower tier. Notice how the “Snapdragon X Plus” has two fewer CPU cores. If the defect lands on 1/12 CPU cores, disable the broken one and an extra weak core. Sell the chip at a lower price. How many chips can be harvested from catastrophic defects depends on the design and die area of each functional block. Let’s make up a number and say 40% of defective dies can be harvested.

Now on to parametric yield.

[![](https://substackcdn.com/image/fetch/$s_!lChk!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe30dba6c-9a15-4dfa-a903-bf125c5304f6_414x228.jpeg)](https://substackcdn.com/image/fetch/$s_!lChk!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe30dba6c-9a15-4dfa-a903-bf125c5304f6_414x228.jpeg)

The clock speed and operating voltage of chips is a function of what comes back from the Fab. Deciding what voltage and clock speed a chip will run at is a business decision, not engineering. Like Intel, AMD, and Nvidia, Qualcomm has used parametric yield for product segmentation. Healthy chips that can run at a higher clock speed (with reasonable voltage) are premium SKUs. Each CPU core of each chip has it’s own volt-frequency curve. Some parts have CPU cores that can boost up to 4GHz while others have weak CPU cores that are locked to a uniform 3.4GHz.

Based on Qualcomm’s advertised SKU stack, clock speeds, and guaranteed boost clocks, I believe they are aggressively harvesting. Let’s say 95% of chips that make it this far can be “binned” into a sellable product.

Chips need to be packaged. Monolithic designs like what Qualcomm an AMD are selling are relatively easy to package on simple ABF substrates. Intel’s chiplet-based Meteor Lake uses complex and expensive packaging which effectively doubles their BOM cost when compared to the immediate competition.

Download my ghetto spreadsheet to see the final base/bear/bull numbers.

* * *

So what does this mean for Qualcomm stock?

Nothing really. It’s priced in.

After reviewing several sell-side models provided by friendly subscribers (thanks!) I have noticed a pattern. Everyone seems to be modeling ~20% YoY growth from Qualcomm’s IoT business segment in the first two quarters of 2025. Presumably, the vast majority of this growth is from laptop/PC going from < 0.1% joke to mid-single digit market share at gross margins accretive to the QCT average of ~30%.

Priced-in.

* * *

[INTC 0.00%↑](https://substack.com/discover/stocks/INTC) is dealing with a lot of problems right now…

[![Everything is \(not\) fine at Intel](https://substackcdn.com/image/fetch/$s_!YhFe!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F66a45246-dbe6-4f42-8cc7-b71bcdf7dfca_444x429.png)

#### Everything is (not) fine at Intel

[Daud's Scout](https://substack.com/profile/135313705-dauds-scout)·April 3, 2024[Read full story](https://irrationalanalysis.substack.com/p/everything-is-not-fine-at-intel)](https://irrationalanalysis.substack.com/p/everything-is-not-fine-at-intel)

The last thing Intel needs is for a competitor going from zero to meaningful market share in their core (pun intended) business at half their cost-basis.

[![](https://substackcdn.com/image/fetch/$s_!TOzp!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F256727c6-3fc2-43bd-80c0-d49893a8330e_259x194.jpeg)](https://substackcdn.com/image/fetch/$s_!TOzp!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F256727c6-3fc2-43bd-80c0-d49893a8330e_259x194.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!Jjd3!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F07ae90d6-731c-42d4-ac84-b3d5c9ace8af_1469x807.png)](https://substackcdn.com/image/fetch/$s_!Jjd3!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F07ae90d6-731c-42d4-ac84-b3d5c9ace8af_1469x807.png)

A competitor who is desperate enough to dump product at 32% gross margins (technically accretive) to gain share in a new market and claim progress on diversification away from Apple and handsets.

![](https://substackcdn.com/image/fetch/$s_!0Cy0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack.com%2Fimg%2Fattachment_icon.svg)

Ia Chip Bom Ex Laptop

224KB ∙ XLSX file

[Download](https://irrationalanalysis.substack.com/api/v1/file/23478329-c219-469b-96f5-f0b846b19153.xlsx)

[Download](https://irrationalanalysis.substack.com/api/v1/file/23478329-c219-469b-96f5-f0b846b19153.xlsx)

If you enjoyed this content, please consider subscribing.

Subscribe

Already subscribed? Thanks! Please consider sharing this post and/or spreadsheet.

[Share](https://irrationalanalysis.substack.com/p/elite-x-hype-mediocre-financial-impact?utm_source=substack&utm_medium=email&utm_content=share&action=share)
