# Partial Mea Culpa: Sandisk and Marvell

## Updates on a few wrong calls.

**Oct 01, 2025**

**Likes:** 0

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Please check the [‘about’ page](https://irrationalanalysis.substack.com/about) for a list of active positions.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice, and readers should **always do their own research before investing in any security.**

  * Feel free to contact me via email at: _irrational_analysis@proton.me_




* * *

I generally do not edit old posts unless there is a confusing typo.

Some of my calls this year related to Sandisk and Marvell have turned out to be wrong. (SOME… not everything)

Let’s go over them.

* * *

# Contents:

  1. Sandisk

    1. High-Bandwidth Flash is Still Retarded

    2. 100% QLC (no SLC cache) SSD Makes Sense

    3. Wave of AI Video Slop: Incredible NAND Demand Driver

  2. Marvell

    1. 1.6T Transceiver Situation: Featuring Wrong Barclays Note

    2. Marvell Alaska (AEC Re-Timer) Apparently Good (likely $1B+ “XPU attach” opp)

    3. Meta Side-ASIC-Project: Very Likely Marvell Over MediaTek

    4. Ethernet Switching (Innovium): Path to Growth via Upscale AI

    5. Trainum 3 Word Games




* * *

## [1] Sandisk

I pitched Sandisk (WDC at the time) as a short at the beginning of the year and boy was that a terrible call.

This is despite and earlier post calling out AI video generation as a possible NAND flash catalyst…

And yet I covered the Sandisk investor day in an extremely bearish tone.

Technical background on NAND flash and the overall industry is spread out through these three old posts. Not going to re-write stuff. Please go to backlog to get basic background. 

### [1.a] High-Bandwidth Flash is Still Retarded

I still hate HBF. Not going to waste time discussing this meme technology with less endurance than cheap toilet paper soaked in diarrhea. 

Check out [Vikram Sekar](https://open.substack.com/users/124411709-vikram-sekar?utm_source=mentions)’s coverage. 

[![](https://substackcdn.com/image/fetch/$s_!9JlA!,w_56,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa409d69d-ca10-4bfe-a1fc-f8d291690566_185x185.png)Vik's NewsletterHigh Bandwidth Flash: NAND’s Bid for AI MemoryWelcome to a 🔒 subscriber-only deep-dive edition 🔒 of my weekly newsletter. Each week, I help investors, professionals and students stay up-to-date on complex topics, and navigate the semiconductor industry…Read more7 months ago · 22 likes · 4 comments · Vikram Sekar](https://www.viksnewsletter.com/p/high-bandwidth-flash-nands-bid-for-ai?utm_source=substack&utm_campaign=post_embed&utm_medium=web)

### [1.b] 100% QLC (no SLC cache) SSD Makes Sense

For a variety of reasons, I have a rather extreme negative bias towards QLC NAND. Mentally, I view TLC as the “farthest” logical scaling should go.

  1. Write endurance of QLC is dogshit.

  2. Performance of QLC is dogshit. (4K random IOPS)

  3. QLC has significant ECC burden compared to TLC.

  4. Logic complexity for resolving charge levels of QLC is too high.

  5. All drives need an SLC cache anyway and allocating some QLC capacity as a “soft” SLC cache is stupid and severely harms endurance.




[![](https://substackcdn.com/image/fetch/$s_!Vvk7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0476ca94-ab84-4162-9eac-6faad80b38fd_1673x929.png)](https://substackcdn.com/image/fetch/$s_!Vvk7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0476ca94-ab84-4162-9eac-6faad80b38fd_1673x929.png)

Frankly was blinded by my hatred of QLC and Sandisk unironically floating PLC as viable technology.

The bonding strategy greatly mitigates points #2, #3, and #4.

Market trends and clever engineering (on algo side) mitigate #1 and #5.

[![](https://substackcdn.com/image/fetch/$s_!hjSa!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd765f3ff-f739-49f3-9bb1-b1e959787e17_1664x845.png)](https://substackcdn.com/image/fetch/$s_!hjSa!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd765f3ff-f739-49f3-9bb1-b1e959787e17_1664x845.png)

[![](https://substackcdn.com/image/fetch/$s_!qcsM!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4d4583e7-7e7c-4563-9c8e-77a77ac7beda_1666x850.png)](https://substackcdn.com/image/fetch/$s_!qcsM!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4d4583e7-7e7c-4563-9c8e-77a77ac7beda_1666x850.png)

[![](https://substackcdn.com/image/fetch/$s_!Ibst!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcca9e742-9ab9-49ba-837c-426804ad5561_1653x846.png)](https://substackcdn.com/image/fetch/$s_!Ibst!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcca9e742-9ab9-49ba-837c-426804ad5561_1653x846.png)

[![](https://substackcdn.com/image/fetch/$s_!zoku!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd7559f37-97b7-45b2-a26e-baf3c5c94e26_1676x944.png)](https://substackcdn.com/image/fetch/$s_!zoku!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd7559f37-97b7-45b2-a26e-baf3c5c94e26_1676x944.png)

[![](https://substackcdn.com/image/fetch/$s_!XNKC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1fbfa6c6-befc-42a6-ae12-deb8351a0dcd_1665x896.png)](https://substackcdn.com/image/fetch/$s_!XNKC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1fbfa6c6-befc-42a6-ae12-deb8351a0dcd_1665x896.png)

[![](https://substackcdn.com/image/fetch/$s_!hLQv!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fec394f5b-19fb-45a6-b215-0b6f6f4097f3_1666x895.png)](https://substackcdn.com/image/fetch/$s_!hLQv!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fec394f5b-19fb-45a6-b215-0b6f6f4097f3_1666x895.png)

[![](https://substackcdn.com/image/fetch/$s_!mZAV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1a9f68c6-ee00-4092-964e-637c853f9f8e_1664x893.png)](https://substackcdn.com/image/fetch/$s_!mZAV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1a9f68c6-ee00-4092-964e-637c853f9f8e_1664x893.png)

Engineering is about tradeoffs. Have to admit that Sandisk appears to have made the right (smart) tradeoffs to build the best HIGH CAPACITY, tolerable performance SSD for AI slop video generation.

PCIe gen5 interface is going to bottleneck the crap out of this SSD but that is not the point.

Hyperscalers and AI labs going buy tons of these drives for….

  * Extreme capacity density.

  * Acceptable write performance and endurance for AI video generation

  * Acceptable read performance using clever software RAID/striping.

  * Unbeatable cost because QLC NAND with no SLC cache and prob a tiny amount of DRAM cache.




Sandisk recently announced a 256 TB version of this product. They have a winner. I was super wrong to trash their “QLC scaling first, layer scaling last” engineering strategy.

### [1.c] Wave of AI Video Slop: Incredible NAND Demand Driver

Sora 2 is here and looks amazing.

So much garbage video is going to be generated, in an exponential growth kind of way. 

We about to get multiple “YouTubes” worth of NAND demand hitting all at once. 

At the time of writing, I hold no economic position in Sandisk but planning on buying call options this week.

## [2] Marvell

Out of all the stocks out there, institutional investors ask me about Marvell the most.

Retail investors, do not touch Marvell. This ticker is a hedge fund warzone.

Rumors are gona push this stock +/- 20% in one day multiple times over the next 18 months. 

### [2.a] 1.6T Transceiver Situation: Featuring Wrong Barclays Note

A particular Barclays note prompted this section.

>  _“We stopped at 8 module vendors, and only saw 2 instances of MRVL 1.6T DSP used in two different configurations (1 FRO, 1 TRO). MRVL also did not publicly display the 1.6T solution at the booth nor did we see a full production display (with specs). Multiple vendors mentioned that the DSP is 1W worse from a power perspective vs AVGO. 800G will still be the volume node for next year, but we think its clear now the company will face much higher competition at 1.6T.”_
> 
> -Barclays ECOC Note

[![](https://substackcdn.com/image/fetch/$s_!3NoR!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F73e6f2a1-0a8b-4cca-8544-7e14c7a6eb94_823x313.png)](https://substackcdn.com/image/fetch/$s_!3NoR!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F73e6f2a1-0a8b-4cca-8544-7e14c7a6eb94_823x313.png)Ignore LRO. Messes up comparisons. Also… **this is a massive TSEM bull case in table form LOL.**

The bearish rumors on Marvell/Inphi 1.6T 3nm DSP are frankly getting out of hand.

Barclays is really nitpicking here. 

Marvell showed this chip with live demo at OFC like 6 months ago.

It was kinda bad at e-9 with aggressive active cooling. Additionally, I called out a major regression in Marvell’s 1.6T DSP when they moved from N5 to N3.

[![Marvell Managment is Bluffing Bank of America Securities](https://substackcdn.com/image/fetch/$s_!CJXA!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb1cc27e3-04f3-4d2f-807b-f268df73bf49_812x353.png)

#### Marvell Managment is Bluffing Bank of America Securities

[Irrational Analysis](https://substack.com/profile/135313705-irrational-analysis)·June 15, 2025[Read full story](https://irrationalanalysis.substack.com/p/marvell-managment-is-bluffing-bank)](https://irrationalanalysis.substack.com/p/marvell-managment-is-bluffing-bank)

Yes… there were problems. **Marvell fixed them.**

I do not buy the “firmware update” claim. They had to have re-spun the chip to fix some kind of hardware issue (inductive coupling?). But whatever, mistakes happen and they recovered. 

Performance at room temperature between MRVL and AVGO 1.6T is effectively a tie now.

Anything 1e-11 is effectively “burst free” which is what matters. Barclays also omits that Nvidia is using Marvell 1.6T DSP for their massive transceiver ramp.

(I was wrong on this BTW)

My logic that ring == internal Nvidia DSP was wrong. A driver from Semtech or Macom is enough to boost the swing to drive rings.

So… the most important transceiver (by volume) is Nvidia and Marvell has this socket.

There were problems with TDECQ and BER regression, but Marvell re-spun the chip and seems to have fixed them, significantly closing the performance gap with AVGO.

Additionally, Barclays complaining about 1W of extra power at room temp is really nitpicky. Guys, even at operational temp, lets say DSP goes up to 2W penalty comparing MRVL to AVGO.

2/30 = 7%

Nobody is making decisions based on a 7% power efficiency gap. Chill out.

Two key metrics matter:

  1. Can the transceiver run error free post-FEC at half RS-FEC?

  2. Strategically reducing reliance on Broadcom.




Even the most bearish case of Marvell/Broadcom going from 80/20% share to 50/50% share in 1.6T is fine. Growth is so massive that Marvell will print money off this.

 _Some share loss is gong to happen. No way 80/20 split stays. Broadcom will bundle the crap out of their oDSP with custom-ASIC and Tomahawk 6 switches via JDM (joint development manufacturing)._

oDSP is by far the highest gross-margin product Marvell sells. This revenue is way better than custom ASIC (which everyone obsesses about) given how pressured margins are in that business.

Marvell oDSP (Inphi group) is fine. Legit the best BU over there. There were problems and they got fixed.

### [2.b] Marvell Alaska (AEC Re-Timer) Apparently Good (likely $1B+ “XPU attach” opp)

[![](https://substackcdn.com/image/fetch/$s_!lQN8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe2f753c5-91e8-4ddd-a125-e09538a41fd4_1472x661.png)](https://substackcdn.com/image/fetch/$s_!lQN8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe2f753c5-91e8-4ddd-a125-e09538a41fd4_1472x661.png)<https://investor.marvell.com/2025-04-01-Marvell-Extends-Connectivity-Leadership-with-AEC-Ecosystem-Demonstrations-at-OFC-2025>

I saw this demo live at OFC and it was not great TBH. FEC symbol 9 errors with aggressive active cooling.

But again, it appears that Marvell fixed whatever problem was there. _Perhaps a similar electromagnetic coupling to PLL that the oDSP probably had?_

Multiple sources tell me that Broadcom’s 800G (8x100G) AEC chip is way too power hungry, and they are locked out of this generation.

These same sources tell me that Marvell has won a major win at Amazon for 800G AEC with Alaska. This is confirmed. Not sure what took so long. I guess tuning the SerDes to reliably handle short reach channels was time consuming?

Buy-side… when Marvell management tells out about that “$1B+ XPU attach” opportunity, its AEC with Amazon.

Credo has been getting away with highway robbery, and someone (FINALLY) is going after them.

Long Marvell, short Credo is a fun idea. Too afraid to put my own money into this trade, especially because of the volatility Marvell is going to see from the endless Alchip/Trainium3 rumor mill.

### [2.c] Meta Side-ASIC-Project: Very Likely Marvell Over MediaTek

There are rumors that Meta is shopping around of a “small” AI ASIC at both MediaTek and Marvell.

I feel like Marvell has a 90% probability of winning this project because of their 64G D2D PHY.

They presented really good data at Hot Chips 2025. You can find coverage here.

[![](https://substackcdn.com/image/fetch/$s_!4UBM!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fba7c49db-8614-4b86-869e-ee385784e450_1637x927.png)](https://substackcdn.com/image/fetch/$s_!4UBM!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fba7c49db-8614-4b86-869e-ee385784e450_1637x927.png)

This PHY IP is very very good. The data is even at high temperature (presumably 110C or 125C).

216 lanes active so massive crosstalk. Incredible BER.

It would be interesting to know what insertion loss at 16GHz was used for this testing.

If Marvell D2D IP can handle 5-7 dB of insertion loss at Nyquist, they can use CoWoS-R for packaging. Worse performance than CoWoS-L but way cheaper.

If the D2D IP can only handle 2-3 dB insertion loss, then it needs CoWoS-L or EMIB which is fine. Performance is still exceptional.

Being able to handle CoWoS-R loss at a power efficiency penalty would push this from “great” to “amazing”.

I have sent at least three finance-person mules to go ask Marvell this specific question and each time did not get an answer.

 _(hope Micron management enjoyed all the finance people asking about internal DRAM-node-based HBM4 base die parametric yield at 11 Gbps)_

[![](https://substackcdn.com/image/fetch/$s_!-iHP!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff78c9179-c8a3-4837-a536-51aec6875191_1240x402.png)](https://substackcdn.com/image/fetch/$s_!-iHP!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff78c9179-c8a3-4837-a536-51aec6875191_1240x402.png)

:(

Anyway, Meta potential mini-AI-ASIC design win is heavily in favor of Marvell rather than MediaTek specifically because of the Marvell D2D PHY IP IMO.

### [2.d] Ethernet Switching (Innovium): Path to Growth via Upscale AI

Ethernet switching silicon is effectively a duopoly between Broadcom and Nvidia.

Cisco is off in la-la-land sniffing glue. IDK what going on over there.

Marvell has Innovium and it frankly has not been going well. Part of the problem was the Cadence N7 SerDes Innovium was using at the time Marvell acquired Innovium.

 _(ask around… you will hear funny stories)_

Latest switches use internal Marvell SerDes to be clear.

The other (ongoing) problem is a lack of a software partner.

Nvidia is vertically integrated and makes all the software bells-and-whistles for their switches. 

Despite having a large software department, Broadcom does not make all the necessary software for their Tomahawk and Jericho switches.

This is outsourced to Arista (who applies 60%+ margin on top…) or the Hyperscalers who write their own custom stack and have CLS apply 10% margin on white-box switch.

Apparently, this lack of a software/ODM/ecosystem partner has really hurt Marvell/Terralynx/Innovium switches.

Amusingly, there are two startups that are in this specific space, one of whom is closely aligned with Marvell.

Nexthop is a bunch of ex-Arista people who are trying to undercut Arista. Do same thing but at fraction of the price.

Upscale AI is “Nexthop but for Marvell and other ppl switch chips”.

[![](https://substackcdn.com/image/fetch/$s_!sEwt!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F77fa08f8-73f3-4691-b969-32650db5f309_1309x569.png)](https://substackcdn.com/image/fetch/$s_!sEwt!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F77fa08f8-73f3-4691-b969-32650db5f309_1309x569.png)

 **To be clear, I think UALink is a dead spec.** Only hope is if Amazon picks the UALink track for Trainium 4. I think they go with NVLink Fusion.

In that Trn4 track, Astera Labs will make the UALink switch.

 **Marvell’s opportunity is Ultra Ethernet.**

Right now, Marvell’s switching division is not doing great. Only modest volume at Amazon. The 51.2T product was late to market and again… software partner problem.

They have a shot at going from rounding error to serious 3rd player with Upscale AI’s help. Industry wants a real 3rd player in high-end Ethernet switching and it’s not gona be Cisco.

Not going to comment on the “0.5B” switching revenue target. Just saying things not well now but can become good. The potential is there.

### [2.e] Trainum 3 Word Games

[![](https://substackcdn.com/image/fetch/$s_!IEX9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F304f2454-a2b8-4ad3-a828-88228d377d5a_697x213.png)](https://substackcdn.com/image/fetch/$s_!IEX9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F304f2454-a2b8-4ad3-a828-88228d377d5a_697x213.png)

<https://jp-morgan-fireside-chat-with-marvell-ceo-matt-sep-2025.open-exchange.net/>

There was an exchange between Harlan Sur and Matt Murphy that was… whatever not gona beat a dead horse. 

[![](https://substackcdn.com/image/fetch/$s_!XTa-!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0bc73e09-ec17-4a19-8c6e-e3bc97ca4e7a_498x413.gif)](https://substackcdn.com/image/fetch/$s_!XTa-!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0bc73e09-ec17-4a19-8c6e-e3bc97ca4e7a_498x413.gif)

I look forward to the next 6 months of rumors out of Taiwan on who won the mythical Trn3 socket.

Subscribe for engineering-driven investment analysis.

Subscribe

Share?

[Share](https://irrationalanalysis.substack.com/p/partial-mea-culpa-sandisk-and-marvell?utm_source=substack&utm_medium=email&utm_content=share&action=share)
