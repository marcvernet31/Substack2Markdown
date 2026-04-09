# Dell Mega Leak Analysis

## Incredibly bullish for $QCOM. Terrifying for $INTC.

**May 15, 2024**

**Likes:** 0

# IMPORTANT:

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Please check the [‘about’ page](https://irrationalanalysis.substack.com/about) for a list of active positions.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice and readers should **always do their own research before investing in any security.**




* * *

I previously wrote this piece on Qualcomm’s upcoming laptop chips:

[![Elite X Hype, Mediocre Financial Impact](https://substackcdn.com/image/fetch/$s_!n4TN!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3ca8f896-6a74-4427-ac61-23bbe9a6ca67_587x637.png)

#### Elite X Hype, Mediocre Financial Impact

[Daud's Scout](https://substack.com/profile/135313705-dauds-scout)·April 27, 2024[Read full story](https://irrationalanalysis.substack.com/p/elite-x-hype-mediocre-financial-impact)](https://irrationalanalysis.substack.com/p/elite-x-hype-mediocre-financial-impact)

In light of the recent amazing Dell leak (PDF with 300+ slides) I have to completely change the conclusion and BOM analysis. **My base-case gross-margin is now 52%!**

![](https://substackcdn.com/image/fetch/$s_!0Cy0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack.com%2Fimg%2Fattachment_icon.svg)

Dell Leak Bom V2

1.54MB ∙ XLSX file

[Download](https://irrationalanalysis.substack.com/api/v1/file/f95e3c17-f032-4622-9fe3-cc8020f9a538.xlsx)

[Download](https://irrationalanalysis.substack.com/api/v1/file/f95e3c17-f032-4622-9fe3-cc8020f9a538.xlsx)

[![](https://substackcdn.com/image/fetch/$s_!DmRp!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1ffcbb23-7f8c-4022-9a35-358dd1d87d05_1797x1139.png)](https://substackcdn.com/image/fetch/$s_!DmRp!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1ffcbb23-7f8c-4022-9a35-358dd1d87d05_1797x1139.png)

The Dell leak PDF was publicly available on scribid.com [at this link](https://www.scribd.com/document/706718228/2023-0817-b-TQC-Plan-Phase-Exit-final-8-11-23-LPR-Approved) for several days.

Multiple news outlets reported on this leak. **Fair-use analysis of public info is fair game.** I will not re-upload the deck or include any private employee information. Various Dell employee names show up.

Lots of juicy info so let’s get started!

# PMIC Fiasco is Real… Still Crushing Intel in COGS

Charlie Demerjian of SemiAccurate [published an update on Qualcomm Oryon](https://www.semiaccurate.com/2023/09/26/whats-going-on-with-qualcomms-oryon-soc/) back in September 2023.

He basically accused Qualcomm of hilarious, self-induced incompetence driven by PMIC middle management. 

> You see those PMICs are as we keep saying, cell phone parts, specifically high end cell phone parts. **Because of this, they need a .6mm pitch HDI PCB** which is common in high end cell phones so no worry on availability. It is however priced for high end cell phones, IE very expensive per unit area. **Very very expensive compared to laptop and desktop PCBs but a high end cell phone doesn’t use much area, they are mostly battery inside, and they can carry that cost well.**
> 
> Yes Qualcomm’s force bundled PMICs require **four more board layers** to handle laptop currents needed for Oryon. If you thought a high end tight pitch cell phone PCB scaled up to laptop areas was expensive, four more layers blow out the BoM. **Remember that yield for boards scales down with layers, and not linearly.**

The Dell leak references MB material (motherboard material) several times as a major cost driver for the “carcass”. Appears to be Dell lingo for motherboard and case.

[![](https://substackcdn.com/image/fetch/$s_!-TaA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4a5811eb-f43e-44d3-854f-3e292b01c738_1279x127.png)](https://substackcdn.com/image/fetch/$s_!-TaA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4a5811eb-f43e-44d3-854f-3e292b01c738_1279x127.png)

Charlie claims that multiple OEMs were going to buy the QCOM PMICs and throw them away but were prevented from doing so.

>  **Yes, several OEMs were going to buy the PMICs and throw them away and put a cheap and more efficient off the shelf solution in it’s place.** The PCB costs would be a fraction of what they were with the Qualcomm solution, the power delivery would be more efficient, and the net result would be a cheaper and provably better device for the end user.
> 
> As you might have guessed, Qualcomm would have none of this. Flagrantly violating the first rule of holes, they kept digging much to the detriment of the OEMs. **Qualcomm told them that the SoC to PMIC protocols were proprietary and, purportedly, baked into the SoC.**

[![](https://substackcdn.com/image/fetch/$s_!rqzs!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F90632867-bf5c-4778-999c-c75f967ae4d9_1878x982.png)](https://substackcdn.com/image/fetch/$s_!rqzs!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F90632867-bf5c-4778-999c-c75f967ae4d9_1878x982.png)

> And that is exactly what Qualcomm did, shoveled money at the problem. Yup they are giving customers money to ‘offset’ the costs that the PMICs mandated, ’tis to laugh. **As it turns out, the money Qualcomm is giving the OEMs to offset this mess is said to be MORE than the cost of the PMICs so they are net losing money on the deal.**

To fix this PMIC mess, Charlie claims [QCOM 0.00%↑](https://substack.com/discover/stocks/QCOM) is providing a subsidy that is larger than the PMIC cost. 

[![](https://substackcdn.com/image/fetch/$s_!_N54!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F42bc7bd8-af6f-4056-8716-197d8d14b312_1774x1005.png)](https://substackcdn.com/image/fetch/$s_!_N54!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F42bc7bd8-af6f-4056-8716-197d8d14b312_1774x1005.png)

[![](https://substackcdn.com/image/fetch/$s_!m3D9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb2936b30-c323-4d8c-b20d-c389bfdfaa5d_876x954.png)](https://substackcdn.com/image/fetch/$s_!m3D9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb2936b30-c323-4d8c-b20d-c389bfdfaa5d_876x954.png)

**The Dell leak confirms Charlie’s reporting multiple times.**

  * Carcass cost increase of ~$100 from old Intel version to QC version.

  * $18 worth of cost on “motherboard material” AKA PCB.

  * PMIC chips included under “carcass” alongside other small surface-mount devices.

  * Qualcomm providing a $60 subsidy to Dell.




Despite the epic self-own, Qualcomm is still obliterating [INTC 0.00%↑](https://substack.com/discover/stocks/INTC) in BOM cost. **Intel is charging 2x the price for their inferior CPUs.** **Dell is still saving money on bill of materials BEFORE the subsidies are taken into account.** Imagine how much better this product launch would be if the PMIC fiasco never happened…

Qualcomm is going to talk up QCT gross-margin expansion once these products ship in volume ~H2 2024. It is important for investors to keep in mind that EPS is getting kneecapped because of the $60/unit subsidy needed to clean up self-inflicted, unnecessary stupidity. 

Marketing expense/subsidy to prop up gross-margins.

# Incredible Battery Life vs INTC

[![](https://substackcdn.com/image/fetch/$s_!z4EH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F116c630c-745d-42b3-b447-6eee340887ce_1857x1039.png)](https://substackcdn.com/image/fetch/$s_!z4EH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F116c630c-745d-42b3-b447-6eee340887ce_1857x1039.png)

Complete obliteration. I want to buy one of these laptops. 6-year-old Intel Kaby Lake unit needs an upgrade.

Meteor Lake battery life is basically on par with Alder Lake (ADL). Lunar lake not expected to be much better. Maybe 20% if Intel executes well.

 **QUALCOMM IS OFFERING ~DOUBLE REAL-WORLD BATTERY LIFE.**

 **BATTERY LIFE IS THE MOST IMAPACTFUL METRIC PEOPLE NOTICE.**

 **MASSIVE MARKET SHARE GAINS INCOMING.**

# Healthy Volume Projection

[![](https://substackcdn.com/image/fetch/$s_!nL10!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd19c883c-501f-4ac6-be37-1730eb273d63_1854x481.png)](https://substackcdn.com/image/fetch/$s_!nL10!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd19c883c-501f-4ac6-be37-1730eb273d63_1854x481.png)

One interesting tidbit is the Intel-powered predecessor was modeled as a 24-month lifecycle. Dell is modeling the new QC version with slightly lower lifetime units over 18 months. 

This implies the following:

  * Volume is expected to be healthy, on-par with Intel volumes.

  * Dell expects an updated V2 Orion from Qualcomm that presumably fixes the PMIC fail, allowing for a new version with cheaper PCB, better VRM efficiency, and better battery-life.




# 5G Evaluated and Skipped

This leak appears to be multiple slide decks across many months stapled together.

[![](https://substackcdn.com/image/fetch/$s_!EqeF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4e99776f-8def-4a87-9dbf-698c4a6f38a4_1120x621.png)](https://substackcdn.com/image/fetch/$s_!EqeF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4e99776f-8def-4a87-9dbf-698c4a6f38a4_1120x621.png)

An old slide from 2021 implies that 5G was evaluated.

[![](https://substackcdn.com/image/fetch/$s_!n6b3!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5b925a82-fd16-4003-bb6f-0103b817e8dc_1898x1060.png)](https://substackcdn.com/image/fetch/$s_!n6b3!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5b925a82-fd16-4003-bb6f-0103b817e8dc_1898x1060.png)

The final product is not going to include expensive, useless features nobody wants or asked for.

[![](https://substackcdn.com/image/fetch/$s_!n4TN!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3ca8f896-6a74-4427-ac61-23bbe9a6ca67_587x637.png)](https://substackcdn.com/image/fetch/$s_!n4TN!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3ca8f896-6a74-4427-ac61-23bbe9a6ca67_587x637.png)

# Interesting Noise Issue (fixed)

[![](https://substackcdn.com/image/fetch/$s_!1y2p!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa052bd01-5068-4028-b4e1-9bbb324fa0bf_1853x1052.png)](https://substackcdn.com/image/fetch/$s_!1y2p!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa052bd01-5068-4028-b4e1-9bbb324fa0bf_1853x1052.png)

Usually, inductors and switching regulators create acoustic noise. Never head of MLCC caps causing noise. Cool detail.

# Memory Speed Dependency

[![](https://substackcdn.com/image/fetch/$s_!1BTW!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F76fd11cb-002a-4090-b98d-ec6cc41776ae_1867x1032.png)](https://substackcdn.com/image/fetch/$s_!1BTW!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F76fd11cb-002a-4090-b98d-ec6cc41776ae_1867x1032.png)

There appears to be no attempt to validate memory speeds bellow 8400 MT/s. Orion appears to be dependent on top-bin, ultra-fast LPDDR5x. 

# Conclusion

I am now incredibly bullish [QCOM 0.00%↑](https://substack.com/discover/stocks/QCOM). They will probably achieve over 10% of laptop/PC market share by H2 2025. My base-case gross-margin is 52% although operating profit is going to crushed by the $60/unit PMIC apology subsidy. 

For V2, the subsidy will likely be gone, and ASP could probably increase to over $180 easily. Excellent 60% gross margins on significant, rapidly growing QCT revenue stream. Huge boost to diversification (away from handsets) narrative.

This story is enough for the stock to get re-rated on a higher multiple with surprise upside to FY2025 EPS. All it takes is 2-3 sell-siders (other than Stacy/Bernstein) to realize Qualcomm is going to eviscerate Intel.

Send your thoughts and prayers to Intel. They gona need it.

If you enjoyed this content, please consider subscribing.

Subscribe

Already subscribed? Thanks! Please consider sharing.

[Share](https://irrationalanalysis.substack.com/p/dell-mega-leak-analysis?utm_source=substack&utm_medium=email&utm_content=share&action=share)
