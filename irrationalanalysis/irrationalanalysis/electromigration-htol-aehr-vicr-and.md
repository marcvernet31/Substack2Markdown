# Electromigration, HTOL, $AEHR, $VICR, and $INTC

## A tale of three hazardous investments.

**Jul 18, 2024**

**Likes:** 0

# IMPORTANT:

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Please check the [‘about’ page](https://irrationalanalysis.substack.com/about) for a list of active positions.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice and readers should **always do their own research before investing in any security.**




* * *

[AEHR 0.00%↑](https://substack.com/discover/stocks/AEHR) just made an acquisition that is suspicious at best, nonsensical at worst.

[![](https://substackcdn.com/image/fetch/$s_!qpky!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9b89e913-04e6-4208-8cc6-1ad46084a844_1438x2503.jpeg)](https://substackcdn.com/image/fetch/$s_!qpky!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9b89e913-04e6-4208-8cc6-1ad46084a844_1438x2503.jpeg)

[VICR 0.00%↑](https://substack.com/discover/stocks/VICR) , a company seemingly left for dead, is oddly showing signs of life.

[![](https://substackcdn.com/image/fetch/$s_!zZLg!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5ef50287-1a4c-4433-aa21-a476d1c94274_1438x2161.jpeg)](https://substackcdn.com/image/fetch/$s_!zZLg!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5ef50287-1a4c-4433-aa21-a476d1c94274_1438x2161.jpeg)

And [INTC 0.00%↑](https://substack.com/discover/stocks/INTC), the most beaten-up large-cap semi name, is going up while the entire semiconductor industry is a sea of red. 

[![](https://substackcdn.com/image/fetch/$s_!Of3e!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F46e0581c-323e-4977-bcca-5bacf41071b2_1378x2206.jpeg)](https://substackcdn.com/image/fetch/$s_!Of3e!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F46e0581c-323e-4977-bcca-5bacf41071b2_1378x2206.jpeg)

Believe it or not, these three investments are connected in some way. 

Before getting the investment talk (dessert), you must first suffer through the technical material (vegetables) I have prepared for you today.

# Contents:

  1. Electromigration

  2. [H]igh [T]emperature [O]perating [L]ife

  3. AEHR’s Legendary Gaslighting

  4. Reading the VICR Tea Leaves

  5. Bonus: INTC Possible Tsunami-Level Tail Risk




### [1] Electromigration

[![](https://substackcdn.com/image/fetch/$s_!SQ_m!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1dedd6fd-68ff-4eb5-97bd-acd39afef937_933x983.png)](https://substackcdn.com/image/fetch/$s_!SQ_m!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1dedd6fd-68ff-4eb5-97bd-acd39afef937_933x983.png)[Source](https://www.ansys.com/blog/what-is-electromigration)

  * Electromigration (EM) is the process by which semiconductors degrade over time.

  * High current, high voltage, and high temperature (in particular) accelerate EM.

  * Determining the reliability of a chip design depends on two things:

    * The design team simulating (correctly) and making sure all their circuits meet a minimum reliability criterion, typically 10-years for logic like consumer CPUs.

    * The post-silicon team needs to run HTOL testing and analyze all failures, adjusting settings to make sure production chips don’t fail early.




### {2} [H]igh [T]emperature [O]perating [L]ife

How do you quickly find out if your chip will last, on average, 10 years under normal operating conditions?

The answer is simple: HTOL burn-in testing.

Take a batch of chips (80-240 units typically) and run them at full load for 1000 hours at 125C.

 _Note: Specialty parts may need longer testing at a higher target accelerated degradation temperatures._

Conceptually, HTOL testing is simple. Running your chip at an abusively high temperature for one hour is equivalent to MANY hours of normal operation.

There are machines specifically designed for this type of testing…

[![](https://substackcdn.com/image/fetch/$s_!lR0I!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5b692786-d0d7-43d4-8ed7-585033482c15_1460x1031.png)](https://substackcdn.com/image/fetch/$s_!lR0I!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5b692786-d0d7-43d4-8ed7-585033482c15_1460x1031.png)

Think of these machines as giant ovens that feed power to boards that contain many chips each. In addition to power delivery and temperature control, these HTOL systems support digital and/or analog telemetry to track precisely when a device is in a failed state and needs to be pulled out for analysis.

[![](https://substackcdn.com/image/fetch/$s_!v3MI!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F58dc6a77-79c9-4397-ae04-338473721b61_480x480.png)](https://substackcdn.com/image/fetch/$s_!v3MI!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F58dc6a77-79c9-4397-ae04-338473721b61_480x480.png)

[![](https://substackcdn.com/image/fetch/$s_!4e1d!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4c8c2687-9e2e-4d49-aae3-185765bcfbff_761x507.png)](https://substackcdn.com/image/fetch/$s_!4e1d!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4c8c2687-9e2e-4d49-aae3-185765bcfbff_761x507.png)

HTOL testing is a tedious, someone annoying process but is **absolutely vital** for making sure designs will survive as long as they are supposed to.

Thankfully, once a design has passed HTOL, it does not need to be re-tested unless a major change is made.

Examples of changes that would warrant new round of HTOL testing:

  * Porting the design to a new process node.

  * Non-trivial architectural changes.

  * Request by customers for qualification in a new market that has materially different nominal operating conditions.




### [3] AEHR’s Legendary Gaslighting

Aehr Test Systems is a specialty supplier or silicon-carbide (SiC), gallium-nitride (GaN) and silicon-photonics wafer-level burn-in testing equipment.

These three semiconductor niche segments need production-scale burn-in testing to make sure the weak chips die quickly in the factory.

[![](https://substackcdn.com/image/fetch/$s_!4QLs!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F15df6259-fcd4-4a63-bb3c-0a323e7e60e4_535x315.gif)](https://substackcdn.com/image/fetch/$s_!4QLs!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F15df6259-fcd4-4a63-bb3c-0a323e7e60e4_535x315.gif)

The goal of this style of burn-in testing is to weed out the weak chips and sell the survivors, knowing they are unlikely to fail early in the field.

For detailed information on what Aehr does and why their solution is cool, check out this SemiAnalysis post.

[![](https://substackcdn.com/image/fetch/$s_!HwSb!,w_56,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2F0150776c-9bf2-4bea-a9c2-41b24b7a0f15_1280x1280.png)SemiAnalysisSilicon Carbide Game-Changer: Aehr's Edge - SiC Pure Play $AEHRSemiconductor manufacturing is the alchemical process of the modern era, a complex dance that requires the harmonious synchronization of thousands of companies and tens of thousands of process steps. Due to its complexity, yield is a more than $100 billion problem for the industry. As such, the fabrication process contains a constant stream of critical status checks to support the most complex thing humans have created…Read more3 years ago · 28 likes · 19 comments · Dylan Patel](https://www.semianalysis.com/p/silicon-carbide-game-changer-aehrs?utm_source=substack&utm_campaign=post_embed&utm_medium=web)

TLDR; 

_Aehr makes test machines that can take in entire wafers at a time. Saves a lot of money because you don’t need to chop-up wafer into chips, package, then test. Strong recurring-revenue stream at high gross margin from consumable probe cards._

Aehr’s recent stock performance has been due to an [acquisition they just announced](https://www.aehr.com/2024/07/aehr-test-systems-to-acquire-incal-technology-expanding-its-addressable-market-within-the-rapidly-growing-ai-semiconductor-market/), Incal.

[![](https://substackcdn.com/image/fetch/$s_!lR0I!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5b692786-d0d7-43d4-8ed7-585033482c15_1460x1031.png)](https://substackcdn.com/image/fetch/$s_!lR0I!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5b692786-d0d7-43d4-8ed7-585033482c15_1460x1031.png)

Surprise! I did not waste your time explain random engineering terms. You already know what HTOL is and thus know exactly what Incal does.

Here is a comparison sheet I made.

[![](https://substackcdn.com/image/fetch/$s_!dijW!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fce460673-13d5-4760-8cd8-f93eb1c72315_1173x679.png)](https://substackcdn.com/image/fetch/$s_!dijW!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fce460673-13d5-4760-8cd8-f93eb1c72315_1173x679.png)

 **These two businesses are nothing alike.**

Completely different engineering goals.

Completely different financial and business models.

Zero synergy.

The press release and earnings call transcript has some of the most gaslighting, nonsensical, misleading, bullshit I have ever had the misfortune to read.

> Gayn Erickson, President and CEO of Aehr Test Systems, commented, “The rapidly growing artificial intelligence semiconductor market is still in the early stages, and we see a significant opportunity in this market for wafer level burn-in using our new high-power FOX multi-wafer production system. In addition, given the unique challenges of testing very high-power devices related to AI processors, there is a very real need for a significant amount of engineering qualification and process development as well as a significant new opportunity for production reliability screening at the packaged part level. 
> 
> “We believe that Incal’s new family of ultra-high-power solutions have significant technological and commercial advantages over other solutions, enabling Aehr to capture an even larger share of the AI semiconductor test market. In addition, Incal is in a unique position with intimate knowledge and working relationships with a significant number of AI industry leaders, providing a front-row seat to the technology needs of these customers. **Incal is shipping systems today for use by a broad range of companies and their subcontract manufacturing and test houses for reliability testing for AI, GPU, network, and HPC processors, with many of these companies projecting needs to move to high volume, production level burn-in of these devices.**

Throughout the press-release and earnings call transcript, Aehr management repeatedly imply that AI semiconductor testing will soon need high-volume, production level burn-in. 

Multiple participants on the call…. called bullshit on this acquisition as a contrived way of boosting next-years revenue guidance, which would have missed street expectations significantly without the $12M in Incal revenue.

[![](https://substackcdn.com/image/fetch/$s_!ePWk!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe3381bab-2422-4052-a6fb-ed0dd1464c45_1388x256.png)](https://substackcdn.com/image/fetch/$s_!ePWk!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe3381bab-2422-4052-a6fb-ed0dd1464c45_1388x256.png)

[![](https://substackcdn.com/image/fetch/$s_!VkxR!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4ecb9507-60a5-495a-a11e-41f506f4b788_1459x359.png)](https://substackcdn.com/image/fetch/$s_!VkxR!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4ecb9507-60a5-495a-a11e-41f506f4b788_1459x359.png)

From an engineering perspective, this acquisition by Aehr is obvious bullshit. Folks on the financial side are already suspicious. Do some more digging and this could be a juicy short.

### [4] Reading the VICR Tea Leaves

Vicor makes power components. Converting DC to DC, AC to DC and what not. There are plenty of other companies that make these components such as [MPWR 0.00%↑](https://substack.com/discover/stocks/MPWR) [ADI 0.00%↑](https://substack.com/discover/stocks/ADI) and [TXN 0.00%↑](https://substack.com/discover/stocks/TXN) .

For background on Vicor, check this SemiAnalysis piece:

[![](https://substackcdn.com/image/fetch/$s_!HwSb!,w_56,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2F0150776c-9bf2-4bea-a9c2-41b24b7a0f15_1280x1280.png)SemiAnalysisEnergizing AI: Power Delivery Competition Heats Up Vicor, MPS, Delta, ADI, Renesas, Infineon AI accelerators are becoming increasingly power-hungry. The Nvidia H100 has thermal design power (TDP) of 700 watts (W) compared to less than 200W for the most commonly installed datacenter CPU in the world, Intel Skylake/Cascade Lake. Next-generation chips will require even more power to support more compute density. This would require >200 kW at the rack level compared to current conventional CPU server racks that can deliver 15-20Kw…Read more3 years ago · 60 likes · 10 comments · Dylan Patel, Myron Xie, Gerald Wong, and George Cozma](https://www.semianalysis.com/p/energizing-ai-power-delivery-competition?utm_source=substack&utm_campaign=post_embed&utm_medium=web)

[![](https://substackcdn.com/image/fetch/$s_!RqP7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F60c7dfd5-186c-407e-9962-88fd224e13f5_749x323.png)](https://substackcdn.com/image/fetch/$s_!RqP7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F60c7dfd5-186c-407e-9962-88fd224e13f5_749x323.png)

[![](https://substackcdn.com/image/fetch/$s_!n8cH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe4a8b67c-77aa-4c8b-a769-1dbc0a6a7164_700x438.png)](https://substackcdn.com/image/fetch/$s_!n8cH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe4a8b67c-77aa-4c8b-a769-1dbc0a6a7164_700x438.png)

 **E N H A N C E**

[![](https://substackcdn.com/image/fetch/$s_!b7YQ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8242582b-7bcb-49ab-a8cc-aa0f9902779b_696x438.png)](https://substackcdn.com/image/fetch/$s_!b7YQ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8242582b-7bcb-49ab-a8cc-aa0f9902779b_696x438.png)

WE MUST GO DEEPER. 

**E N H A N C E !!!!!!!!!**

[![](https://substackcdn.com/image/fetch/$s_!DVCA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3fb25a47-2e09-48f0-a261-55a77bee1670_685x519.png)](https://substackcdn.com/image/fetch/$s_!DVCA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3fb25a47-2e09-48f0-a261-55a77bee1670_685x519.png)

Some degenerate pod monkeys have clearly bid this garbage up. If any readers want to really know what is going on with Vicor, ask around for **HTOL reports**.

Vicor has pissed off basically every major customer they had due to reliability issues. Nobody is going to be dumb enough to trust them with a high-volume program without a detailed HTOL report for the part in question. 

Find the HTOL report and you have an answer if this stock is about to plummet or goto moon.

### [5] Bonus: INTC Possible Tsunami-Level Tail Risk

Certain Intel chips (high-core count 13th and 14th gen Raptor Lake) have been failing alarmingly early en-masse.

These are desktop chips that also get deployed in small servers.

Datacenter providers are hiking warranty prices.

[![](https://substackcdn.com/image/fetch/$s_!4rvd!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F82bd226b-048f-4447-b898-724493733289_2100x479.png)](https://substackcdn.com/image/fetch/$s_!4rvd!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F82bd226b-048f-4447-b898-724493733289_2100x479.png)

[![](https://substackcdn.com/image/fetch/$s_!j0zA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6413a1eb-2162-46ad-a735-7e3d2f7db558_1879x484.png)](https://substackcdn.com/image/fetch/$s_!j0zA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6413a1eb-2162-46ad-a735-7e3d2f7db558_1879x484.png)

[![](https://substackcdn.com/image/fetch/$s_!EC4h!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff9ba52e9-d04c-46c9-99fc-4d58d27a0884_1827x499.png)](https://substackcdn.com/image/fetch/$s_!EC4h!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff9ba52e9-d04c-46c9-99fc-4d58d27a0884_1827x499.png)

[![](https://substackcdn.com/image/fetch/$s_!wLAd!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F672c5b5c-2381-4b5c-a308-d19315c404a6_1551x741.png)](https://substackcdn.com/image/fetch/$s_!wLAd!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F672c5b5c-2381-4b5c-a308-d19315c404a6_1551x741.png)

Based on information from a variety of sources, I believe the following is an accurate summary of the current situation at the time of writing:

  * High-core count desktop CPUs from Intel’s 13th and 14th generation are failing as early as a few months of life, typically 6 months of operation.

  * The datacenter motherboards do not support overclocking and are deployed in well-cooled environments. (not a PC gamer overclocking problem)

  * Early EM induced failure appears to be occurring in the ring bus. (the part that connects all cores, PCIe PHY, iGPU, and so on together)




From a financial perspective, this is a nothingburger so long as the problem is limited to high-end gaming SKUs.

If this EM problem is latent in the laptop SKUs…. it could be a massive problem.

[![](https://substackcdn.com/image/fetch/$s_!Glwh!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb170b4bf-200c-47e6-9e25-9d3cda988e18_1000x564.png)](https://substackcdn.com/image/fetch/$s_!Glwh!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb170b4bf-200c-47e6-9e25-9d3cda988e18_1000x564.png)

 _TLDR;_

 _Intel may have an unexpected, multi-billion-dollar pre-tax charge if this electromigration problem is in all Raptor Lake, not just the high-core count desktop SKUs._

If you enjoyed this content, please consider subscribing.

Subscribe

Already subscribed? Thanks! Please consider sharing.

[Share](https://irrationalanalysis.substack.com/p/electromigration-htol-aehr-vicr-and?utm_source=substack&utm_medium=email&utm_content=share&action=share)
