# Primer: Switching Regulators and VRMs

## Why Monolithic Power stock has plummeted.

**Nov 15, 2024**

**Likes:** 0

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Please check the [‘about’ page](https://irrationalanalysis.substack.com/about) for a list of active positions.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice, and readers should **always do their own research before investing in any security.**

  * Feel free to contact me via email at: _irrational_analysis@proton.me_




* * *

[MPWR 0.00%↑](https://substack.com/discover/stocks/MPWR) has had a rough few weeks. 

[![](https://substackcdn.com/image/fetch/$s_!LGLi!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F830b151b-11ef-4aca-8523-7aba620c9276_1439x2822.jpeg)](https://substackcdn.com/image/fetch/$s_!LGLi!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F830b151b-11ef-4aca-8523-7aba620c9276_1439x2822.jpeg)

So rough, it is now down YTD and RSI is at 19. 

[![](https://substackcdn.com/image/fetch/$s_!A5Q3!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7be146d7-c25d-49e7-94d8-71f699b357db_595x497.png)](https://substackcdn.com/image/fetch/$s_!A5Q3!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7be146d7-c25d-49e7-94d8-71f699b357db_595x497.png)https://x.com/dylan522p/status/1856017671151878417

SemiAnalysis and Edgewater both had negative notes on Monolithic Power based on supply chain stuff. It’s kinda funny how this stock tanked ~40% off Nvidia allocation rumors alone.

This is an excellent excuse to explain switching regulators and VRMs.

## Contents:

  1. Switching Regulators and VRM

  2. PCB Analysis

  3. Walkthrough of Public [MPWR 0.00%↑](https://substack.com/discover/stocks/MPWR) Datasheet

  4. There is no moat… 




* * *

### [1] Switching Regulators and VRM

Here is a mediocre diagram I threw together in Visio.

[![](https://substackcdn.com/image/fetch/$s_!Vejf!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faaf63082-9bc9-43b0-85f4-56975d9bf22c_1529x540.png)](https://substackcdn.com/image/fetch/$s_!Vejf!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faaf63082-9bc9-43b0-85f4-56975d9bf22c_1529x540.png)The entire system (switching regulator + analog filter(s)) is called a “voltage regulation module” AKA VRM.

A switching regulator is a device that uses pulse-width modulated signals to step down DC voltage. Oversimplified, it is basically two very beefy transistors that can handle a lot of power.

[![](https://substackcdn.com/image/fetch/$s_!3mCc!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8e31412d-7714-45f7-8f10-9a0c3812a0d3_720x405.png)](https://substackcdn.com/image/fetch/$s_!3mCc!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8e31412d-7714-45f7-8f10-9a0c3812a0d3_720x405.png)[Source](https://forum.level1techs.com/t/vrms-the-what-why-and-how-they-operate/139560)

The output of the switching regulator (Point A) oscillates between the input voltage (V_IN) and ground. Modern switching regulators are highly programmable and have sophisticated current/voltage/temperature monitoring alongside a long list of safety features. This is because the failure mode is fire.

Obviously, shoving brief bursts of 12V into chips designed for ~1.2V is not going to end well. This is where the analog filter comes in.

Most VRM designs use a simple 1st-order LC (inductor + capacitor) filter.

[![](https://substackcdn.com/image/fetch/$s_!gYe8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F53a0e759-99ae-4d57-a11f-24b500b0f7b8_353x277.png)](https://substackcdn.com/image/fetch/$s_!gYe8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F53a0e759-99ae-4d57-a11f-24b500b0f7b8_353x277.png)Sample frequency response (Bode plot) of a basic 1st-order LC low-pass filter. Changing the values (size/ratio) of the capacitor and inductor gives different peaking cutoff frequencies.

The low-pass filter’s job is to smooth out the switching regulator output into something useable for the load chip.

Often, a single switching regulator is not good enough. The output voltage ripple is still too drastic.

This is where multi-phase designs come in.

[![](https://substackcdn.com/image/fetch/$s_!TS82!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3746f81a-081e-45a7-b9b6-ed7b1b6bba93_720x405.png)](https://substackcdn.com/image/fetch/$s_!TS82!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3746f81a-081e-45a7-b9b6-ed7b1b6bba93_720x405.png)[Source](https://forum.level1techs.com/t/vrms-the-what-why-and-how-they-operate/139560)

You take multiple switching regulators, place them in a small time offset from one another, and combine the filtered outputs at the end.

### [2] PCB Analysis

Here are some resources:

The big rectangles are inductors. Some designs use cylindrical electrolyte capacitors you may be familiar with. Other designs use high-performance (expensive) multi-layer ceramic capacitors, commonly referred to as MLCC.

Here is the fabled GB200 board that buy-side is salivating over. 

[![](https://substackcdn.com/image/fetch/$s_!AgDN!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F620e64b0-ac1a-44e0-acd1-dc71e8a2c239_1200x800.jpeg)](https://substackcdn.com/image/fetch/$s_!AgDN!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F620e64b0-ac1a-44e0-acd1-dc71e8a2c239_1200x800.jpeg)

Let’s zoom in…

[![](https://substackcdn.com/image/fetch/$s_!KRSY!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb12bb2dc-9295-41b6-974d-5a5f687bb092_445x299.png)](https://substackcdn.com/image/fetch/$s_!KRSY!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb12bb2dc-9295-41b6-974d-5a5f687bb092_445x299.png)

You can literally look at the board and spec sheet and reverse-engineer the entire VRM with ease.

High-power chips need a lot of VRM phases to smooth out ripple and deliver the power at reasonable efficiency. There exists a sweet spot.

### [3] Walkthrough of Public [MPWR 0.00%↑](https://substack.com/discover/stocks/MPWR) Datasheet

Let’s look at a Monolithic Power “100 Ampere” 12V to 1.2V DC-DC power stage [datasheet. ](https://www.monolithicpower.com/en/mpm3695-100.html)

[![](https://substackcdn.com/image/fetch/$s_!q94M!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F881933aa-19e1-4086-92ad-404f86ef38f1_914x503.png)](https://substackcdn.com/image/fetch/$s_!q94M!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F881933aa-19e1-4086-92ad-404f86ef38f1_914x503.png)

Notice how there are multiple curves. The switching speed and V_OUT have a meaningful impact on efficiency. 

Also notice that the peak efficiency is around 40A load current. Just because the power stage is marketed as “100A” does not mean anyone is actually going to run it at that kind of load.

 **This is why having multiple phases is so important.** Efficiency goes to shit if a power stage is overloaded.

[![](https://substackcdn.com/image/fetch/$s_!caoX!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F400e96df-e14e-4cb8-85a2-32686035322d_922x1146.png)](https://substackcdn.com/image/fetch/$s_!caoX!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F400e96df-e14e-4cb8-85a2-32686035322d_922x1146.png)

Modern power stages have many safety features. These are important. The failure mode is fire inside your expensive AI accelerator datacenter.

Automatic current and voltage regulation (monitoring and adjusting) is also important. High-performance GPU/ASIC/CPUs have significant transient load responses.

[![](https://substackcdn.com/image/fetch/$s_!M79h!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F837a5baf-4fb2-4490-825c-7438b4fa0ef8_2560x1440.jpeg)](https://substackcdn.com/image/fetch/$s_!M79h!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F837a5baf-4fb2-4490-825c-7438b4fa0ef8_2560x1440.jpeg)

Here are some oscilloscope measurements from the datasheet.

[![](https://substackcdn.com/image/fetch/$s_!xQzi!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9ff4853e-5d38-4436-b219-720699ed2250_939x1199.png)](https://substackcdn.com/image/fetch/$s_!xQzi!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9ff4853e-5d38-4436-b219-720699ed2250_939x1199.png)

The scope is in AC-coupling mode to highlight the spikes. Voltage spikes are bad. Monolithic Power is showcasing their product with a particular capacitor configuration to advertise that their solution is good.

[![](https://substackcdn.com/image/fetch/$s_!TdKS!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8474ec06-afca-48a2-9066-ebf7ccea5077_887x1181.png)](https://substackcdn.com/image/fetch/$s_!TdKS!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8474ec06-afca-48a2-9066-ebf7ccea5077_887x1181.png)

A block diagram of the power stage shows what kind of input filtering is built in. This helps board designers know how much they need to clean up V_IN (12V in this case). Integrated input filtering is a nice feature that saves precious board real estate.

### [4] There is no moat… 

In general, there are three major players in high-current DC-DC power stages.

  1. Monolithic Power

  2. Infineon

  3. Renesas




There are other companies that make switching regulators, such as Texas Instruments and Analog Devices. But they don’t make the super high-power stuff.

Earlier this year, I briefly owned [MPWR 0.00%↑](https://substack.com/discover/stocks/MPWR) shares, before realizing this is a stupid idea and liquidating the position at a 0.5% loss. **There is no moat.**

It takes roughly three engineers, one month (at most) to design out a power stage vendor in the event of price negotiations failing.

  1. Signal Integrity 

  2. Power Integrity

  3. Layout/Designer




Remember that efficiency curve at the very top of the datasheet?

[![](https://substackcdn.com/image/fetch/$s_!q94M!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F881933aa-19e1-4086-92ad-404f86ef38f1_914x503.png)](https://substackcdn.com/image/fetch/$s_!q94M!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F881933aa-19e1-4086-92ad-404f86ef38f1_914x503.png)

Let’s say Infineon has a similar power stage that hits peak efficiency at 35A instead of the 40A Monolithic Power provides.

I don’t know this. Infineon has most of their datasheets private because they are cowards.

All you need to do is… add more phases and run the inferior power stages at slightly lower load current.

[![](https://substackcdn.com/image/fetch/$s_!7f-S!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe92ffc01-92c9-4d01-80b3-c45a74af543c_922x1003.png)](https://substackcdn.com/image/fetch/$s_!7f-S!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe92ffc01-92c9-4d01-80b3-c45a74af543c_922x1003.png)Example power plane circled with red crayon.

PCBs have what are called “power planes”. A plane of copper that distributes DC voltage. Making the PCB bigger (to fit more phases) is not that difficult. 

Not as simple as “haha make power plane bigger”. Parasitics, EM coupling, and loop inductance are all problems that need simulation.

But it takes 3 engineers ~1 month to get all this work done.

The cost of switching regulators is capped. It is very easy to calculate when it makes sense to dump a supplier (Monolithic Power in this case) in favor of inferior products. **Designing out is easy. There is no moat.**

I find it very funny how many buyside folks bid up [MPWR 0.00%↑](https://substack.com/discover/stocks/MPWR) only to panic sell the moment supply-chain whispers invalidated their spreadsheets.

Clearly, none of these people had a clue what the hell Monolithic Power does or what they were buying.

Why was [MPWR 0.00%↑](https://substack.com/discover/stocks/MPWR) stock bid up to a forward P/E higher than [NVDA 0.00%↑](https://substack.com/discover/stocks/NVDA)? 

[![](https://substackcdn.com/image/fetch/$s_!tlP0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F242983c7-9954-4850-8834-3b7449883fe9_306x282.png)](https://substackcdn.com/image/fetch/$s_!tlP0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F242983c7-9954-4850-8834-3b7449883fe9_306x282.png)

Subscribe for engineering-driven investment analysis.

Subscribe

Share if you enjoyed.

[Share](https://irrationalanalysis.substack.com/p/primer-switching-regulators-and-vrms?utm_source=substack&utm_medium=email&utm_content=share&action=share)
