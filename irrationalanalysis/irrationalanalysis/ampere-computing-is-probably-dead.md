# Ampere Computing is probably dead.

## Almost all their customers have gone vertical. No path forward.

**May 20, 2024**

**Likes:** 0

# IMPORTANT:

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Please check the [‘about’ page](https://irrationalanalysis.substack.com/about) for a list of active positions.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice and readers should **always do their own research before investing in any security.**




* * *

Ampere Computing is a datacenter CPU startup with some interesting history. They had a 2024 update video recently:

Based on this video and my prior understanding, I now believe that Ampere Computing is dead and in denial. 

# Background

Ampere Computing was founded in 2017 by a group of ex-Intel employees who left during the great Krzanich brain drain. Their goal was to develop a “cloud-native” datacenter CPU based on ARM architectures.

[![](https://substackcdn.com/image/fetch/$s_!UEmh!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9d5dd29f-0c6b-45e6-8ee4-96e7d37c2865_1920x1080.png)](https://substackcdn.com/image/fetch/$s_!UEmh!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9d5dd29f-0c6b-45e6-8ee4-96e7d37c2865_1920x1080.png)

[![](https://substackcdn.com/image/fetch/$s_!5GRu!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F93dc09bb-f413-4455-85a2-bff6927ce889_1920x1080.png)](https://substackcdn.com/image/fetch/$s_!5GRu!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F93dc09bb-f413-4455-85a2-bff6927ce889_1920x1080.png)

What is “cloud-native”? It is a marketing term for datacenter CPUs with the following attributes:

  1. Predictable performance. Every CPU core runs at a stable clock speed. 

  2. Linear scaling with respect to core count per socket.

  3. Low power per core.




These attributes matter for cloud workloads because of how public clouds virtualize CPU cores for customer instances. Suppose you have a physical CPU with 64 cores. The 64 cores are virtualized so 16 customers who each use 4 virtualized CPU cores in their respective instance. If customer #1 is running a heavy floating-point workload, they generate a lot of heat trying to boost their vCPU clock speed. Neighbors have performance adversely effected 

All of the claims Ampere Computing make are true. Thier products have a clear advantage for cloud-first workloads (virtualization heavy). **The problem is… almost all their customers have gone vertical!**

[![](https://substackcdn.com/image/fetch/$s_!JU4Q!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb0d617ca-66c6-47a1-ac8f-e41865f2f15c_764x448.png)](https://substackcdn.com/image/fetch/$s_!JU4Q!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb0d617ca-66c6-47a1-ac8f-e41865f2f15c_764x448.png)

On the ARM (ISA) side, Microsoft and Google recently went vertical with Neoverse CSS chiplets provided by ARM (RTL). Amazon has been making their own SoC for a long time now. Nvidia Grace is going to rapidly expand market share with GB200 NVL36/72. 

In x86-land, Intel and AMD have both responded with great products. Intel has Sierra Forrest coming soon with Clearwater Forest as a follow-up. AMD has Bergamo which is really good.

Ampere Computing set out to fill a niche market and succeeded in getting all their competitors ****AND CUSTOMERS**** to join the market.

[![](https://substackcdn.com/image/fetch/$s_!V4-E!,w_1456,c_limit,f_auto,q_auto:good,fl_lossy/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb5e7bdcf-3498-43e1-8f7a-8de6e064c7e9_498x415.gif)](https://substackcdn.com/image/fetch/$s_!V4-E!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb5e7bdcf-3498-43e1-8f7a-8de6e064c7e9_498x415.gif)

 **Oracle is the only large customer Ampere Computing has left.**

This is because Oracle has heavily invested in the startup, leading multiple funding rounds. Oracle’s pocketbook closed a while ago which is why [Ampere Computing tried to IPO back in December 2022](https://amperecomputing.com/press/ampere-announces-confidential-submission-of-draft-registration-statement-for-proposed-initial-public-offering) but chickened out.

# 2024 Copium Update

[![](https://substackcdn.com/image/fetch/$s_!SdUc!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe5931eb0-3e93-414a-985c-7e854717bc63_794x438.png)](https://substackcdn.com/image/fetch/$s_!SdUc!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe5931eb0-3e93-414a-985c-7e854717bc63_794x438.png)

They don’t have anything. HAHAHAHAHAHAHA

[![](https://substackcdn.com/image/fetch/$s_!pxIT!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7dff8cd2-9030-4895-b02c-73eaaecee45b_2101x756.png)](https://substackcdn.com/image/fetch/$s_!pxIT!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7dff8cd2-9030-4895-b02c-73eaaecee45b_2101x756.png)

To this day, Ampere Computing has disclosed zero meaningful technical info on their custom “cloud CPU microarchitecture” or “AI features”. ARM (RTL), Nvidia, Intel, and AMD all release detailed information about their technology.

[![](https://substackcdn.com/image/fetch/$s_!y4il!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6e0248a3-1d64-433d-9977-3d02f25a1b94_800x450.jpeg)](https://substackcdn.com/image/fetch/$s_!y4il!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6e0248a3-1d64-433d-9977-3d02f25a1b94_800x450.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!pl4Z!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa42ae4c6-3174-4ebf-9d97-ebfebfbf2d8b_1400x678.png)](https://substackcdn.com/image/fetch/$s_!pl4Z!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa42ae4c6-3174-4ebf-9d97-ebfebfbf2d8b_1400x678.png)

[![](https://substackcdn.com/image/fetch/$s_!69mg!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0005f364-463c-44d8-aa4e-e4df168a58ad_951x575.jpeg)](https://substackcdn.com/image/fetch/$s_!69mg!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0005f364-463c-44d8-aa4e-e4df168a58ad_951x575.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!EYCj!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7809a2cd-5a38-4f46-b787-8223eeb85550_456x260.png)](https://substackcdn.com/image/fetch/$s_!EYCj!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7809a2cd-5a38-4f46-b787-8223eeb85550_456x260.png)

[![](https://substackcdn.com/image/fetch/$s_!wGAc!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe1c69941-6bd7-4fd2-ac18-8ce3088ee407_960x540.png)](https://substackcdn.com/image/fetch/$s_!wGAc!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe1c69941-6bd7-4fd2-ac18-8ce3088ee407_960x540.png)

When companies vaguely claim they have innovative features but refuse to provide any meaningful technical information… IT MEANS THEY DONT HAVE ANYTHING. 

[![](https://substackcdn.com/image/fetch/$s_!j-Vw!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5f635c63-2b27-4b2f-a5e6-fda4026a111f_220x124.gif)](https://substackcdn.com/image/fetch/$s_!j-Vw!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5f635c63-2b27-4b2f-a5e6-fda4026a111f_220x124.gif)

[![](https://substackcdn.com/image/fetch/$s_!e8rq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Feea6ad32-5895-4435-a404-4c6513f7baca_1235x837.png)](https://substackcdn.com/image/fetch/$s_!e8rq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Feea6ad32-5895-4435-a404-4c6513f7baca_1235x837.png)

The 256-core part is a straight process tech port from N5 to N3E/N3P. No uarch improvements. They were already behind and will be much more behind soon once AMD and Intel launch Turin-Dense and Clearwater-Forest respectively. 

ARM (RTL) will provide a Neoverse N4/V4 CSS chiplet that beats Ampere Computing at their own game by H2 2025. CSS V3/N3 almost certainly already beats Ampere Computing mythical custom “we wont tell you any details” uarch as is. Notice how there are zero TCO benchmarks against CSS chiplet products.

* * *

Silicon ages like milk. You race against the competition on choke to death on their dust.

You smell that? Rancid milk.

You hear that? Ampere Computing coughing like a chain-smoking coal miner.

If you enjoyed this content, please consider subscribing.

Subscribe

Already subscribed? Thanks! Please consider sharing.

[Share](https://irrationalanalysis.substack.com/p/ampere-computing-is-probably-dead?utm_source=substack&utm_medium=email&utm_content=share&action=share)
