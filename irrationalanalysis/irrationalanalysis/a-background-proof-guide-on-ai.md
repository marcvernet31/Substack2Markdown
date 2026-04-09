# A Background-Proof Guide on AI

## An approachable, intuition-driven mental model.

**Aug 17, 2024**

**Likes:** 0

# IMPORTANT:

  * Irrational Analysis is heavily invested in the semiconductor industry.

    * Please check the [‘about’ page](https://irrationalanalysis.substack.com/about) for a list of active positions.

    * Positions will change over time and are regularly updated.

  *  **Opinions are authors own and do not represent past, present, and/or future employers.**

  * All content published on this newsletter is based on **public information and independent research** conducted since 2011.

  * This newsletter is not financial advice and readers should **always do their own research before investing in any security.**

  * Feel free to contact me via email at: _irrational_analysis@proton.me_




* * *

Hello wonderful subscribers. Welcome to another deep-dive. 

[![](https://substackcdn.com/image/fetch/$s_!aZG5!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4fd51c7a-67d1-4cf2-825e-97be0e1fb16c_4000x2570.png)](https://substackcdn.com/image/fetch/$s_!aZG5!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4fd51c7a-67d1-4cf2-825e-97be0e1fb16c_4000x2570.png)

Today’s topic is ML/AI fundamentals. If you have a basic understanding of linear algebra, that will be helpful, _but it’s not required._

My background (formal education) is in classical digital signal processing (DSP). I am not an ML/AI engineer so take this post with a grain of salt. 

[![](https://substackcdn.com/image/fetch/$s_!_jby!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbb1e4f00-67fa-47f7-a8b9-81c40daddc3d_500x500.jpeg)](https://substackcdn.com/image/fetch/$s_!_jby!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbb1e4f00-67fa-47f7-a8b9-81c40daddc3d_500x500.jpeg)

The goal is to share the DSP-oriented understanding I have built for myself in an approachable way, _regardless of your background_ , while maintaining decent technical rigor. Feel free to share your own thoughts in the comments section. Happy to make edits to improve this writeup based on feedback.

You can also privately email me at “ _irrational_analysis@proton.me_ ”.

 _I have spent over 8 months working on this. Please subscribe._

Subscribe

 _Please share high-quality, free content._

[ Share](https://irrationalanalysis.substack.com/p/a-background-proof-guide-on-ai?utm_source=substack&utm_medium=email&utm_content=share&action=share)

[![](https://substackcdn.com/image/fetch/$s_!nmWr!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0b04988d-7fd6-43d0-91ca-637a9c8ee959_786x572.png)](https://substackcdn.com/image/fetch/$s_!nmWr!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0b04988d-7fd6-43d0-91ca-637a9c8ee959_786x572.png)

# Contents:

  1. History of ML/AI

    1. Before AlexNet (2012)

    2. The AlexNet Revolution

    3. Transformers, ChatGPT, and LLMs.

  2. Intuitive Understanding

    1. Biology

    2. Abstract Math

    3. Computational Math

    4. Non-Linear, Black-Box System (DSP)

    5. Compression (JPEG)

  3. Training vs Inference: A Practical Understanding

  4. AI Systems First Principals

    1. Complexity is a necessary evil.

    2. Open is not necessarily better. 

    3. Scaling is primarily limited by memory.

    4. “Scaling Laws” are not laws.

    5. Should we really apply AI to <problem>?

    6. Edge AI only matters in latency-sensitive workloads.

    7. GPU vs ASIC: Flexibility Tradeoff

  5. Deep-Dive of AlexNet (step-by-step conv-net example)

  6. Surface-Level Tour of the Basic Transformer (math focus)

  7. Hyperparameters

  8. Investment/Gambling Ideas: August 2024 Edition

  9. Where we are, and why I fear for the future.

    1. DotCom 2.0: GPU Edition

    2. This Place…

    3. Insanity




* * *

## [1] History of ML/AI

How did we get here?

[![](https://substackcdn.com/image/fetch/$s_!JO0B!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F265491f1-3201-4b12-93fd-e783b06e53f8_1259x724.png)](https://substackcdn.com/image/fetch/$s_!JO0B!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F265491f1-3201-4b12-93fd-e783b06e53f8_1259x724.png)

To understand the last five years, we must go back… 81 years.

### [1.a] Before Alexnet (2012)

In 1943, the [Perceptron](https://en.wikipedia.org/wiki/Perceptron) was invented by Warren McCulloch and Wlater Pitts. However, the first implementation was made by Frank Rosenblatt 14 years later in 1957.

[![](https://substackcdn.com/image/fetch/$s_!15U8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8f863eaf-98ca-4daa-8599-453b9b3fe737_1920x1503.jpeg)](https://substackcdn.com/image/fetch/$s_!15U8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8f863eaf-98ca-4daa-8599-453b9b3fe737_1920x1503.jpeg)An engineer, Charles Wightman, adjusting the first Perceptron machine.

[![](https://substackcdn.com/image/fetch/$s_!ZcSQ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdebab72e-ed5b-402e-a30b-1eb200c5c644_1630x1336.png)](https://substackcdn.com/image/fetch/$s_!ZcSQ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdebab72e-ed5b-402e-a30b-1eb200c5c644_1630x1336.png)

The Perceptron was the first neural network consisting of three layers.

  1. An 20x20 input layer of light sensors acting as a “retina”.

  2. One hidden layer consisting of 512 elements.

  3. An 8-element output layer.




This system was inspired by theories on how the human brain interprets images.

[![](https://substackcdn.com/image/fetch/$s_!Igv4!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7a3536a8-5c51-4d3c-9c5e-a44af9a35b67_1920x1799.png)](https://substackcdn.com/image/fetch/$s_!Igv4!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7a3536a8-5c51-4d3c-9c5e-a44af9a35b67_1920x1799.png)

 _more on this in part [2.a]_

* * *

At the time, this Perceptron thing generated a lot of hype.

It did not go anywhere.

Artificial neural networks and machine learning sort of went into a coma until 2012.

Until the AlexNet revolution changed everything.

### [1.b] The AlexNet Revolution

In 2010, a new image processing competition was established. the “ImageNet Large Scale Visual Recognition Challenge”.

This task seems simple now but was quite difficult at the time.

[![](https://substackcdn.com/image/fetch/$s_!NYXp!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbc550edf-2949-48ab-9676-3ad0adbfb229_1000x1000.jpeg)](https://substackcdn.com/image/fetch/$s_!NYXp!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbc550edf-2949-48ab-9676-3ad0adbfb229_1000x1000.jpeg)

You are given a series of images from 1000 unique categories. From vehicle types (car, bus, truck, …) to dog breeds to plant types.

Each submitting team needs to classify the images and is graded on “top-5 error”.

[![](https://substackcdn.com/image/fetch/$s_!dx0_!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fae165213-0874-4d41-b946-8db6e317ac62_810x676.png)](https://substackcdn.com/image/fetch/$s_!dx0_!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fae165213-0874-4d41-b946-8db6e317ac62_810x676.png)

If a team’s algorithm outputs the correct category within its top-5 guesses, they get a point.

Humans typically achieve a 5% top-5 error rate.

Before 2012, a 25% top-5 error rate was considered bleeding edge.

[![](https://substackcdn.com/image/fetch/$s_!fHjy!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9971dace-ac87-4792-85fb-e94442761e3b_665x419.png)](https://substackcdn.com/image/fetch/$s_!fHjy!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9971dace-ac87-4792-85fb-e94442761e3b_665x419.png)[Source](https://www.pinecone.io/learn/series/image-search/imagenet/)

Then AlexNet came and crushed everything else. It was made by Alex Krizhevsky, Ilya Sutskever (yes the former OpenAI chief scientist and dramatist), and Geoffrey Hinton.

> Our model is a large, **deep convolutional neural network** trained on raw RGB pixel values. The neural network, which has **60 million parameters** and 650,000 neurons, consists of five convolutional layers, some of which are followed by max-pooling layers, and three globally-connected layers with a final 1000-way softmax. **It was trained on** **two NVIDIA GPUs for about a week**. To make training faster, we used non-saturating neurons and a very efficient GPU implementation of convolutional nets. To reduce overfitting in the globally-connected layers we employed hidden-unit "dropout", a recently-developed regularization method that proved to be very effective.
> 
> <https://image-net.org/challenges/LSVRC/2012/results.html#abstract>

One week of training on two Nvidia GTX 580s.

[![](https://substackcdn.com/image/fetch/$s_!52_u!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F45f34ad3-ce68-4879-9c5d-d51959c8de03_1024x771.jpeg)](https://substackcdn.com/image/fetch/$s_!52_u!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F45f34ad3-ce68-4879-9c5d-d51959c8de03_1024x771.jpeg)

Around a thousand dollars of **video gaming toy hardware** trained a deep neural network that crushed every competing image classification algorithm. 

As of August 2024, the [Alexnet paper](https://scholar.google.com/citations?user=xegzhJcAAAAJ&hl=en) has been cited over 160 thousand times.

Nvidia’s CEO regularly brings up AlexNet on earnings calls. **It’s because GPUs meant for video games brought machine learning and neural networks back from the dead.**

* * *

The Gregorian calendar is based on the perceived birth date of Jesus Christ. “Before Christ” (BC) and “Anno Domini” (AD) which translates to “the year of our Lord”.

Those who created this calendar made it revolve around what they believed to be the most important event of all time.

AlexNet is the all-time most important breakthrough in machine learning.

History is split between before AlexNet and after AlexNet.

A deep-dive of AlexNet is in part [5].

### [1.c] Transformers, ChatGPT, and LLMs

In 2017, the Google Brain team published a paper on the new neural network architecture they invented, transformers.

[![](https://substackcdn.com/image/fetch/$s_!DFC8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7f0c1c0e-41ec-4001-bb81-56031a16286b_1070x1500.jpeg)](https://substackcdn.com/image/fetch/$s_!DFC8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7f0c1c0e-41ec-4001-bb81-56031a16286b_1070x1500.jpeg)

No! Not those transformers! 

[![](https://substackcdn.com/image/fetch/$s_!zPVr!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9a08d94d-0544-488b-8516-cdb63771265c_1200x871.webp)](https://substackcdn.com/image/fetch/$s_!zPVr!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9a08d94d-0544-488b-8516-cdb63771265c_1200x871.webp)

In classic Google fashion, they invented something very valuable and completely failed to capitalize on it.

Five years later, a startup called OpenAI (which is not open at all) released ChatGPT.

GPT stands for “Generative Pre-trained Transformer”.

A surface-level overview of the original 2017 transformer architecture is in part [6].

## [2] Intuitive Understanding

The point of this section is to help every reader build an intuitive understanding of AI. **It is ok if you don’t understand some of the following sub-sections.** Everyone has a different background and way of thinking. 

### [2.a] Biology

Biologists study the structure of brains and there are some neat diagrams I managed to find.

[![](https://substackcdn.com/image/fetch/$s_!1GZw!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2b2faad1-c90a-4c6f-8a6d-1cf2cb6f6b16_5615x5635.jpeg)](https://substackcdn.com/image/fetch/$s_!1GZw!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2b2faad1-c90a-4c6f-8a6d-1cf2cb6f6b16_5615x5635.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!TOja!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffb104588-ef5e-4322-a1bf-453fc53a1e12_2403x3117.jpeg)](https://substackcdn.com/image/fetch/$s_!TOja!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffb104588-ef5e-4322-a1bf-453fc53a1e12_2403x3117.jpeg)

Human organic neural networks are more complicated than animal brains.

[![](https://substackcdn.com/image/fetch/$s_!NudH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffbb42738-f2ad-42c2-9b29-4d1895252af4_672x622.png)](https://substackcdn.com/image/fetch/$s_!NudH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffbb42738-f2ad-42c2-9b29-4d1895252af4_672x622.png)

Human children rapidly generate neurons then prune them later on. 

What if we could make an artificial neural network? Replicate what is seen in the brain with computers. (we can)

[![](https://substackcdn.com/image/fetch/$s_!JpSo!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F95a8862c-927f-4870-8ba9-18819bdda176_1100x782.png)](https://substackcdn.com/image/fetch/$s_!JpSo!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F95a8862c-927f-4870-8ba9-18819bdda176_1100x782.png)

Convolutional Neural Networks are directly inspired from research into the visual cortex, the part of your brain that processes data from your eyes.

[![](https://substackcdn.com/image/fetch/$s_!hPNb!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffc10a6e1-fc94-41dd-ac4e-cda897e55b4d_563x319.png)](https://substackcdn.com/image/fetch/$s_!hPNb!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffc10a6e1-fc94-41dd-ac4e-cda897e55b4d_563x319.png)

[![](https://substackcdn.com/image/fetch/$s_!ncEJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1e3fbfe2-7e9a-4b4d-b0da-bfebac308618_640x426.webp)](https://substackcdn.com/image/fetch/$s_!ncEJ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1e3fbfe2-7e9a-4b4d-b0da-bfebac308618_640x426.webp)

[![](https://substackcdn.com/image/fetch/$s_!4La7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6afb5565-34c9-483f-af4c-6bb9cfa8bdcd_850x307.jpeg)](https://substackcdn.com/image/fetch/$s_!4La7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6afb5565-34c9-483f-af4c-6bb9cfa8bdcd_850x307.jpeg)

* * *

What do the following have in common…?

Childrens books:

[![](https://substackcdn.com/image/fetch/$s_!mEBI!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F35323b31-73ff-45a5-a04d-3823b49dc16a_1000x1000.jpeg)](https://substackcdn.com/image/fetch/$s_!mEBI!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F35323b31-73ff-45a5-a04d-3823b49dc16a_1000x1000.jpeg)

Child block puzzle:

[![](https://substackcdn.com/image/fetch/$s_!929H!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4b05e7a7-5110-4bbb-b3f9-eea4f1871547_731x506.webp)](https://substackcdn.com/image/fetch/$s_!929H!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4b05e7a7-5110-4bbb-b3f9-eea4f1871547_731x506.webp)

Both aim to train a child’s neural network. Object recognition, vocabulary, ethics/values, eye-hand coordination, and so on.

[![](https://substackcdn.com/image/fetch/$s_!iM8l!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9a65f51f-ba99-4da1-8d93-d734be07e9db_863x1030.png)](https://substackcdn.com/image/fetch/$s_!iM8l!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9a65f51f-ba99-4da1-8d93-d734be07e9db_863x1030.png)

### [2.b] Abstract Math

Highly recommend the 3blue1brown series on linear algebra. The episode on abstract vector spaces is the most important one of understanding what AI actually does.

Imagine you have an abstract 3-dimentional vector space. 

[![](https://substackcdn.com/image/fetch/$s_!5jZE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff5669620-12be-43a9-a9c3-30f65e37a4bd_313x311.webp)](https://substackcdn.com/image/fetch/$s_!5jZE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff5669620-12be-43a9-a9c3-30f65e37a4bd_313x311.webp)

And some function within the vector space.

 **You do not know what the function looks like. Mapping out the entire space is very computationally expensive. Your starting point is random.**

[![](https://substackcdn.com/image/fetch/$s_!SA3L!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb94b7e09-21b6-439f-9d4f-33a2ff2d6402_458x309.jpeg)](https://substackcdn.com/image/fetch/$s_!SA3L!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb94b7e09-21b6-439f-9d4f-33a2ff2d6402_458x309.jpeg)

You have two parameters, X and Y, and want to pick them such that Z is minimized.

Imagine trying to roll a marble down the curve.

How do you guide the marble such that it reaches to absolute minimum, not some local pit?

The solution this this 3-dimentional problem is not immediately obvious.

 **Now imagine trying to solve the same problem but in a trillion dimensions.**

This is what modern neural network training is, in a nutshell.

[Gradient descent](https://en.wikipedia.org/wiki/Gradient_descent) is a basic algorithm that tries to solve this problem. There are much more complicated optimization algos out there but let’s keep things simple.

Gradient means partial derivative vector. 

Remember from calculus that the derivative of a function is the slope of a line that is tangential to that function.

[![](https://substackcdn.com/image/fetch/$s_!esyF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F902322d6-d9e3-4326-b3d8-7dc3ad36dc17_1920x1080.png)](https://substackcdn.com/image/fetch/$s_!esyF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F902322d6-d9e3-4326-b3d8-7dc3ad36dc17_1920x1080.png)

For a curve in a 3D space, there are two derivatives, one in X direction and other in Y direction.

[![](https://substackcdn.com/image/fetch/$s_!UBq8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb6442b8f-109f-4eb4-a256-258ffce0f49f_488x245.png)](https://substackcdn.com/image/fetch/$s_!UBq8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb6442b8f-109f-4eb4-a256-258ffce0f49f_488x245.png)Note: AI algorithms do not use symbolic differentiation or numerical methods (Newtons method). They instead use something called [automatic differentiation](https://en.wikipedia.org/wiki/Automatic_differentiation) which is chain-rule spam. Decompose the function into elementary operations.

So, the gradient of our function is used to slowly guide the marble down the curve.

[![](https://substackcdn.com/image/fetch/$s_!25Z6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F40a4883d-6807-4ddb-a697-e09c5eb89086_1200x626.png)](https://substackcdn.com/image/fetch/$s_!25Z6!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F40a4883d-6807-4ddb-a697-e09c5eb89086_1200x626.png)

How big of a step you take is called the “learning rate”. 

Too small and optimization takes forever.

Too large and you overshoot the minima.

[![](https://substackcdn.com/image/fetch/$s_!N76F!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0909cb54-203b-4e30-96c5-03ed7aae9331_600x494.png)](https://substackcdn.com/image/fetch/$s_!N76F!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0909cb54-203b-4e30-96c5-03ed7aae9331_600x494.png)

### [2.c] Computational Math

AI/ML is really dependent on matrix multiplication.

[![](https://substackcdn.com/image/fetch/$s_!VY4M!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F86e5fc29-6239-4b2c-b32f-bdc9ec3ddb28_1400x848.png)](https://substackcdn.com/image/fetch/$s_!VY4M!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F86e5fc29-6239-4b2c-b32f-bdc9ec3ddb28_1400x848.png)

This is the core operation. All AI hardware is optimized for matmuls. Every matrix multiplication can be decomposed into vector sub-operations which is why GPUs are so well suited for AI. Both GPU vendors (Nvidia and AMD) have added dedicated matrix units to their architectures. 

There are other common operations in between the matmuls. 

[![](https://substackcdn.com/image/fetch/$s_!RGp5!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F72eea4e8-c685-4b5c-957a-23e4532c20e1_654x638.png)](https://substackcdn.com/image/fetch/$s_!RGp5!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F72eea4e8-c685-4b5c-957a-23e4532c20e1_654x638.png)

ReLU is simple. If the input is positive, pass it on. Otherwise set it to zero.

[![](https://substackcdn.com/image/fetch/$s_!BlbZ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc013b9a4-f280-4f68-92a9-b475243266e6_1200x603.png)](https://substackcdn.com/image/fetch/$s_!BlbZ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc013b9a4-f280-4f68-92a9-b475243266e6_1200x603.png)

ReLU is one of several “activation functions”. These are used to prune intermediate data and generate non-linearities within the system. 

Imagine of you have a series of matrix multiplies with nothing in-between. 

What is the point? Why not just have one matrix multiply?

A critical aspect of machine learning is sparsity and intentional non-linearity injection.

 **Much of the information within a neural network is encoded in the geometry, not the weights themselves.** This is why quantization is so effective.

[![](https://substackcdn.com/image/fetch/$s_!HwSb!,w_56,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2F0150776c-9bf2-4bea-a9c2-41b24b7a0f15_1280x1280.png)SemiAnalysisNeural Network Quantization & Number Formats From First PrinciplesQuantization has played an enormous role in speeding up neural networks – from 32 bits to 16 bits to 8 bits and soon further. It’s so important that Google is currently being sued for $1.6 billion to $5.2 billion for allegedly infringing on BF16 by its creator…Read more2 years ago · 150 likes · 10 comments · Dylan Patel](https://www.semianalysis.com/p/neural-network-quantization-and-number?utm_source=substack&utm_campaign=post_embed&utm_medium=web)

The matrices involved are often sparse.

[![](https://substackcdn.com/image/fetch/$s_!bPbg!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F004086ca-e08d-44da-b4c0-f6f6e287f6d4_4250x4250.webp)](https://substackcdn.com/image/fetch/$s_!bPbg!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F004086ca-e08d-44da-b4c0-f6f6e287f6d4_4250x4250.webp)

Which means most of the elements are zero. Activation functions such as ReLU force some elements to randomly become or approach zero, intentionally throwing away information to inject non-linearities into the system. This is one important mechanism in which neural networks learn new features.

A special type of matrix multiplication is called a convolution.

[![](https://substackcdn.com/image/fetch/$s_!PLBj!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F06a6b9b9-a776-437d-acb7-b4721c9f4028_567x581.png)](https://substackcdn.com/image/fetch/$s_!PLBj!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F06a6b9b9-a776-437d-acb7-b4721c9f4028_567x581.png)

The process is as follows:

  1. An input matrix is padded with zeros on the edges.

  2. A convolution kernel (matrix smaller than the padded input) is multiplied with part of the input matrix.

  3. The result is added up into a single number.

  4. The kernel is shifted over and over until a new image is created.




[![](https://substackcdn.com/image/fetch/$s_!LcGt!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F15660585-b336-4fca-9a67-0f9a62a53496_1804x788.png)](https://substackcdn.com/image/fetch/$s_!LcGt!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F15660585-b336-4fca-9a67-0f9a62a53496_1804x788.png)Note how the unpadded-input image is 4x4 and the convolution output is also 4x4.

[![](https://substackcdn.com/image/fetch/$s_!Ka4j!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F17a53330-bdb7-4125-a3ca-87404f39beb0_1000x470.gif)](https://substackcdn.com/image/fetch/$s_!Ka4j!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F17a53330-bdb7-4125-a3ca-87404f39beb0_1000x470.gif)

Convolutions are the key operation in… convolutional neural networks (CNNs) which is what AlexNet is.

To summarize this section, the mathematical operations behind neural networks are broadly described as:

  * Primarily matrix math based.

    * Especially matrix multiply.

    * Especially sparse matrices.

  * Reliant on forced non-linearities from activation functions that throw away information during training.

  * Linear algebra spam.

    * Training uses a small amount of calculus to calculate partial derivatives.

  * Tolerant of quantization and lower precision, particularly in inference.

    * 32-bit floating point is the standard precision of most applications.

    * Simulation software, CAD, and professional applications often use 64-bit floating point math, known as double precision. 

    * ML training is typically at a modified 16-bit floating-point, brain-float16.

    * ML inference is trying to migrate to 8-bit and 4-bit quantization.

    * Read the [SemiAnalysis](https://www.semianalysis.com/p/neural-network-quantization-and-number) piece on quantization. It is very good.




### [2.d] Non-Linear, Black-Box System (DSP)

Digital Signal Processing is one of the few topics I am actually qualified to talk about. Everything revolves around linearity. Linear, Time-Invariant (LTI) systems.

[![](https://substackcdn.com/image/fetch/$s_!z8w8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb0228061-7bc4-4774-8f61-1fe11a9cdd76_434x532.png)](https://substackcdn.com/image/fetch/$s_!z8w8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb0228061-7bc4-4774-8f61-1fe11a9cdd76_434x532.png)

[![](https://substackcdn.com/image/fetch/$s_!pL8Y!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdeeff2da-74b6-4a8e-9685-0bf07219eddc_708x570.gif)](https://substackcdn.com/image/fetch/$s_!pL8Y!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdeeff2da-74b6-4a8e-9685-0bf07219eddc_708x570.gif)

[![](https://substackcdn.com/image/fetch/$s_!JGji!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fedea72af-e98a-4f1b-bce4-799bec40dc50_540x378.png)](https://substackcdn.com/image/fetch/$s_!JGji!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fedea72af-e98a-4f1b-bce4-799bec40dc50_540x378.png)

DSP is all about analyzing LTI systems in time-domain and frequency domain using Fourier transforms. 

DSP is really linear algebra in disguise.

  * Fourier transform is just a change of basis.

  * Time and frequency domains are their own subspaces.

  * Digital FIR filters are just linear combinations.




[![](https://substackcdn.com/image/fetch/$s_!05tl!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F581cdc97-b669-408f-acd1-91c50ccbd403_698x429.png)](https://substackcdn.com/image/fetch/$s_!05tl!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F581cdc97-b669-408f-acd1-91c50ccbd403_698x429.png)

[![](https://substackcdn.com/image/fetch/$s_!MZs8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F96414ebb-2554-4f23-bae5-0e2ccb4f3b59_630x424.webp)](https://substackcdn.com/image/fetch/$s_!MZs8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F96414ebb-2554-4f23-bae5-0e2ccb4f3b59_630x424.webp)

Every part of your system is abstracted to a box, a linear box. Impulse response analysis, filtering, convolution, … **it all works because the entire system is linear.**

 **The math behind DSP and machine learning is the same.** **Both are linear algebra.**

Linearity is the differentiator.

DSP needs linearity and does everything possible to approximate and model non-linear systems as linear.

Machine Learning intentionally forces non-linarites into the system via activation functions because that is how neural networks learn.

Same math, diametrically opposed goals.

 **Neural networks are black-boxes full of non-linearities.** Nobody knows what is really going on in these multi-billion and soon multi-trillion models. Non-linearity is the point, not something to be avoided.

### [2.e] Compression (JPEG)

Here is a neat way of building AI intuition that should be universal.

All of you have experienced JPEG images, right? PNGs and raw photos look better than the compressed JPEG version. 

[![](https://substackcdn.com/image/fetch/$s_!pMMP!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F99833123-74c5-45e9-9558-44013ebca69f_849x365.png)](https://substackcdn.com/image/fetch/$s_!pMMP!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F99833123-74c5-45e9-9558-44013ebca69f_849x365.png)

[![](https://substackcdn.com/image/fetch/$s_!IpvK!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2a3c76e0-ce96-4955-ba19-1bfeca810aa9_1030x394.png)](https://substackcdn.com/image/fetch/$s_!IpvK!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2a3c76e0-ce96-4955-ba19-1bfeca810aa9_1030x394.png)

So how does JPEG compression work and how is this related to AI?

[![](https://substackcdn.com/image/fetch/$s_!omq7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F46f75ae2-0708-4561-9dd4-be5bf96a9368_1440x1080.jpeg)](https://substackcdn.com/image/fetch/$s_!omq7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F46f75ae2-0708-4561-9dd4-be5bf96a9368_1440x1080.jpeg)

JPEG relies on something called the discrete cosine transform (DCT). It is a modification of the Fourier transform. So just another change of basis from spatial/time domain into frequency domain.

What makes the DCT special is it concentrates low frequency information into the higher bins and high frequency information into the lower bins. 

[![](https://substackcdn.com/image/fetch/$s_!RmwT!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd6e89a8e-a8db-4771-89ab-7d086271e11d_480x360.jpeg)](https://substackcdn.com/image/fetch/$s_!RmwT!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd6e89a8e-a8db-4771-89ab-7d086271e11d_480x360.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!Dx5Y!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F916bf0e2-d60c-45e4-b64d-310b313acde6_512x164.png)](https://substackcdn.com/image/fetch/$s_!Dx5Y!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F916bf0e2-d60c-45e4-b64d-310b313acde6_512x164.png)

Notice how most of the energy of the image is in the upper left entries of the DCT matrix. 

In general, humans are sensitive to low frequency distortions. Thus, JPEG compresses data by throwing away information from the high-frequency DCT bins (bottom right) either by setting them to zero or quantizing the data.

[![](https://substackcdn.com/image/fetch/$s_!qYzU!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F045ce465-a1e1-4043-9649-e44c82383752_1289x899.avif)](https://substackcdn.com/image/fetch/$s_!qYzU!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F045ce465-a1e1-4043-9649-e44c82383752_1289x899.avif)

[![](https://substackcdn.com/image/fetch/$s_!qYkX!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4b8bafd5-b256-4e20-8fa7-2c5e94a1db2d_788x252.png)](https://substackcdn.com/image/fetch/$s_!qYkX!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4b8bafd5-b256-4e20-8fa7-2c5e94a1db2d_788x252.png)

To recap, JPEG compression works by:

  1. Using linear algebra to transform your image into a frequency-domain DCT coefficient matrix.

  2. Throwing away high frequency information.

  3. Reversing the linear algebra with an inverse DCT transform to output your compressed image in spatial domain.




When Photoshop or Gimp asks you what “compression level” you want, you are really selecting how many DCT coefficients are saved and how quantized they are.

* * *

So… what does this JPEG stuff have to do with AI?

AI is also linear algebra. 

AI is also throwing away a lot of information for lossy compression.

Imagine you have some huge training dataset. 10 exabytes.

After months of training on tens-of-thousands of GPUs, you get a neural network that is say 200 gigabytes in size.

 **This neural network is just like a JPEG file. It’s just a file that compresses information and computational work, in the form of linear algebra.**

## [3] Training vs Inference: A Practical Understanding

Often, I see investors not understanding the difference between training and inference. 

Ignore the noise… batch size, mixture of experts, pre-training, fine-tuning, …

A practical understanding can be built from the math.

[![](https://substackcdn.com/image/fetch/$s_!8snt!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbd80f042-eaf7-428e-8061-838c7e8faf19_1050x520.png)](https://substackcdn.com/image/fetch/$s_!8snt!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbd80f042-eaf7-428e-8061-838c7e8faf19_1050x520.png)

Remember that training is trying to find an optimal point in a complex high-dimensional space. 

Weights are randomly changed, and we need to figure out which random change made the result worse or better. That’s a lot of neurons.

Backpropagation is the process in which we go… backwards and calculate the partial derivative (gradient) of each neuron. 

This involves two things:

  1. A shit ton of memory to store all the immediate activations which are later on used to calculate the gradients. 

  2. Hardware calculating a shit ton of partial derivatives.




So, the difference between training and inference from a hardware/infrastructure perspective is:

  1. Training systems need a lot more memory, to store intermediate data.

  2. Training hardware needs to be able to run calculus, not just linear algebra.




## [4] AI Systems First Principals

Here are some core ideas that I always keep in mind when trying to understand my own investments.

### [4.a] Complexity is a necessary evil.

Imagine I have asked you to build a bridge.

[![](https://substackcdn.com/image/fetch/$s_!mUch!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb1d349fe-aecf-448d-820e-5988b2c357aa_1280x576.jpeg)](https://substackcdn.com/image/fetch/$s_!mUch!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb1d349fe-aecf-448d-820e-5988b2c357aa_1280x576.jpeg)

Yes you. _#FouthWallBreak_

Could you do it? 

What if I told you that you have…

  * …an infinite quantity of high-quality titanium.

  * …50 years to build this bridge.

  * …one million construction workers.

  * …the best construction equipment in the world.




Now building that bridge sounds doable, right?

 **Good engineering comes from constraints, and complexity is a necessary evil.**

A trillion-dollar bridge made of solid titanium is indeed simple, but it is also incredibly stupid.

If you see a solution advertised as simple, there are only two possibilities:

  1. It costs a fortune.

  2. It shifts the complexities somewhere else.




[![](https://substackcdn.com/image/fetch/$s_!7vYC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe4b46b40-2ffb-4b70-badf-36feb03453ac_1080x586.jpeg)](https://substackcdn.com/image/fetch/$s_!7vYC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe4b46b40-2ffb-4b70-badf-36feb03453ac_1080x586.jpeg)

Groq loves to talk about how simple their hardware is. The complexity is still there, just shifted to the satanic nightmare that is their 144-wide VLIW compiler.

[![\[V\]ery \[L\]ong \[I\]ncoherent \[W\]riteup](https://substackcdn.com/image/fetch/$s_!lVhT!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1335e244-45bb-4add-a677-d9ab1ed74702_875x957.png)

#### [V]ery [L]ong [I]ncoherent [W]riteup

[Daud's Scout](https://substack.com/profile/135313705-dauds-scout)·February 24, 2024[Read full story](https://irrationalanalysis.substack.com/p/very-long-incoherent-writeup)](https://irrationalanalysis.substack.com/p/very-long-incoherent-writeup)

Cerebras is gleefully trash talking Nvidia because Blackwell has been delayed by 1-2 quarters.

[![Nvidia Blackwell Delay Note](https://substackcdn.com/image/fetch/$s_!LzZ7!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F874ca356-8878-421e-b588-eb949449e7dc_703x740.png)

#### Nvidia Blackwell Delay Note

[Daud's Scout](https://substack.com/profile/135313705-dauds-scout)·August 4, 2024[Read full story](https://irrationalanalysis.substack.com/p/nvidia-blackwell-delay-note)](https://irrationalanalysis.substack.com/p/nvidia-blackwell-delay-note)

Thier argument that their wafer-scale engine is simpler and thus better faces the same problem. Complexity has shifted from the hardware to the compiler which I know for a fact does not work. They have filed for an IPO. Looking forward to reading the S-1 filing, writing a short report, then shorting the crap out of their equity.

### [4.b] Open is not necessarily better. 

Companies that are losing to Nvidia (AMD, Intel, every AI hardware startup) love to complain about the evil proprietary standards Nvidia uses and how unfair it is.

Open standards are better, they screech, as the average Nvidia employee becomes a multi-millionaire and Mr. Leather Jacket parties to the moon.

[![](https://substackcdn.com/image/fetch/$s_!dt_b!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc0e9921a-ba5e-4599-98ae-917d7225fff6_916x1100.png)](https://substackcdn.com/image/fetch/$s_!dt_b!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc0e9921a-ba5e-4599-98ae-917d7225fff6_916x1100.png)

Let’s talk about NVLink. Nvidia beat everyone else to 224G SerDes. The GB200 NVL36/72 integrated mainframes are marvels of engineering, in large part because 224G NVLink enables huge GPU to GPU communication domains with passive copper cables.

[![\[GB200 NVL72\] The Mainframe of Doom](https://substackcdn.com/image/fetch/$s_!_hFr!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9b4c8e16-a994-40a1-a08d-07d4a9448536_647x846.png)

#### [GB200 NVL72] The Mainframe of Doom

[Daud's Scout](https://substack.com/profile/135313705-dauds-scout)·March 30, 2024[Read full story](https://irrationalanalysis.substack.com/p/gb200-nvl72-the-mainframe-of-doom)](https://irrationalanalysis.substack.com/p/gb200-nvl72-the-mainframe-of-doom)

[![](https://substackcdn.com/image/fetch/$s_!RBRV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1f26c27c-18c4-4d8c-abe8-8b1bc3c0699f_1200x675.jpeg)](https://substackcdn.com/image/fetch/$s_!RBRV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1f26c27c-18c4-4d8c-abe8-8b1bc3c0699f_1200x675.jpeg)

AMD is desperately trying to open-up their proprietary PCIe derivative (XGMI/AFL) and will at best have systems enabled by Broadcom PCIe switches in 2026/2027.

[![](https://substackcdn.com/image/fetch/$s_!45Bs!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc0afc484-a290-44fe-81d4-ca2a79148a4b_650x365.webp)](https://substackcdn.com/image/fetch/$s_!45Bs!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc0afc484-a290-44fe-81d4-ca2a79148a4b_650x365.webp)

[![](https://substackcdn.com/image/fetch/$s_!1HRL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd6c8ca03-a1d2-4fdf-908c-dc06a1224aa7_1920x1080.webp)](https://substackcdn.com/image/fetch/$s_!1HRL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd6c8ca03-a1d2-4fdf-908c-dc06a1224aa7_1920x1080.webp)

Universal Accelerator Link is yet another open standard made by a collection of losers who are too slow to catch up to the leader.

Nvidia has a delay yes. They will be shipping Blackwell in 2025. One or two quarters late. But you know what the competition has? **Slides.** A commitment to start attending standards meetings in the hope that the slides could maybe become a real product in 2026/2027.

Proprietary standards allow companies to rapidly innovate.

Did you know that all high-speed Ethernet PHYs need to work at -20 and +110 degrees Celsius?

It is part of the official standard because some Ethernet PHYs go into telco basestations that might be in cold regions. Need to be able to cold-boot.

Designing and testing an interconnect PHY across a wide temperature range is difficult.

I assure you that the 224G NVLink SerDes that beat every single company working on 224G by 1-year does not work at cold temperatures. All these GB200 NVL72/36 boxes are going in datacenters! Why the hell would Nvidia sacrifice performance and time-to-market designing for a scenario that is irrelevant.

 **Open standards are not necessarily better. This is a logical fallacy often shilled by companies who are losing to a competitor’s proprietary standard.**

Same thing goes for the CUDA complainers.

[![](https://substackcdn.com/image/fetch/$s_!qsAj!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F650a2e96-9474-4c98-bd26-9bdc7cc0b89e_336x150.png)](https://substackcdn.com/image/fetch/$s_!qsAj!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F650a2e96-9474-4c98-bd26-9bdc7cc0b89e_336x150.png)

OpenCL is dead. A joke.

[![](https://substackcdn.com/image/fetch/$s_!Q5vl!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fef188803-34a0-4dec-84be-530c2993e66c_480x240.jpeg)](https://substackcdn.com/image/fetch/$s_!Q5vl!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fef188803-34a0-4dec-84be-530c2993e66c_480x240.jpeg)

Intel oneAPI is also effectively non-existent. The most successful AI chip Intel has (Gaudi) does not even use oneAPI! 🤡

### [4.c] Scaling is primarily limited by memory.

Training bigger models and running inference of bigger models is limited by memory, not compute. Memory limits are effectively manifested as interconnect limits.

Presently (2024) the vast majority of innovation that matters comes down to:

  1. How much memory capacity and bandwidth does your accelerator support.

  2. How well can your interconnect technology enable accelerators to access each other’s memory and bigger pools of memory.




### [4.d] “Scaling Laws” are not laws.

The AI crowd has a bunch of “laws” they like to talk about.

[![](https://substackcdn.com/image/fetch/$s_!rzZ7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F234cffd4-6e2f-4631-b888-cacd18b2f7a0_1920x1080.png)](https://substackcdn.com/image/fetch/$s_!rzZ7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F234cffd4-6e2f-4631-b888-cacd18b2f7a0_1920x1080.png)

[![](https://substackcdn.com/image/fetch/$s_!nhIc!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2ad23955-1624-49cf-8264-b8cee4535ec7_1600x289.jpeg)](https://substackcdn.com/image/fetch/$s_!nhIc!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2ad23955-1624-49cf-8264-b8cee4535ec7_1600x289.jpeg)https://arxiv.org/pdf/2001.08361

 **These are not laws.**

They are simply trial-and error extrapolations.

Here are some real mathematical laws from classical DSP and information theory.

<https://en.m.wikipedia.org/wiki/Cramér–Rao_bound>

[![](https://substackcdn.com/image/fetch/$s_!5ako!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd9d1d050-f634-4286-af74-6b336f7954ea_1438x1142.jpeg)](https://substackcdn.com/image/fetch/$s_!5ako!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd9d1d050-f634-4286-af74-6b336f7954ea_1438x1142.jpeg)

The Cramer-Rao bound is an estimation theory limit. It has a hard mathematical proof and was not conjured into thin air using experimental data.

For example, phased array angle-of-arrival estimation algorithms are benchmarked against this mathematical bound, the theoretical limit of what is possible.

* * *

<https://en.wikipedia.org/wiki/Shannon%E2%80%93Hartley_theorem>

The Shannon-Hartley theorem is a mathematical law on the upper bound of a noisy channels information capacity. How much information you can send in a channel, wireless or wired, does not matter.

[![](https://substackcdn.com/image/fetch/$s_!hCNh!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Feb5d7e46-e56a-4eea-be93-92e31c793040_320x240.webp)](https://substackcdn.com/image/fetch/$s_!hCNh!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Feb5d7e46-e56a-4eea-be93-92e31c793040_320x240.webp)

Think of this as the speed of light physics limit, but for information.

Again, this is a real mathematical law with a rigorous proof behind it. Not an extrapolation from experimental data being passed off as a law.

### [4.e] Should we really apply AI to <problem>?

Google tried to launch a cloud gaming service. It was called Stadia.

[![](https://substackcdn.com/image/fetch/$s_!Vju4!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff13ab7a3-ff55-4315-8dc8-42f9513fcc2a_790x442.png)](https://substackcdn.com/image/fetch/$s_!Vju4!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff13ab7a3-ff55-4315-8dc8-42f9513fcc2a_790x442.png)[Source](https://killedbygoogle.com/)

One of the obvious problems with cloud gaming is the round-trip latency between the customers host device and the cloud. 

[![](https://substackcdn.com/image/fetch/$s_!Tk4Y!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9635dedb-ae0b-469a-923d-31b12326be17_1162x1132.jpeg)](https://substackcdn.com/image/fetch/$s_!Tk4Y!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9635dedb-ae0b-469a-923d-31b12326be17_1162x1132.jpeg)

A Google VP literally argued that Stadia would have “negative latency” because AI in the cloud would predict user-inputs and play the game for the player.

This claim was widely ridiculed at the time. Stadia indeed had latency problems at launch and magical AI buzzword nonsense from middle managers never fixed it.

[![](https://substackcdn.com/image/fetch/$s_!UKJH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F428196aa-c91c-4442-ac62-4670d7cd2128_906x1024.webp)](https://substackcdn.com/image/fetch/$s_!UKJH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F428196aa-c91c-4442-ac62-4670d7cd2128_906x1024.webp)

Stadia died three years after launch.

AI has a tendency to be overused as a false silver bullet.

There are two key enablement factors that can help you determine if AI makes sense for a problem.

 **#1 AI solves a problem that was previously unsolvable using conventional methods.**

Image recognition is a great example of this. AlexNet obsoleted decades of image processing research overnight. 

**#2 AI solves a problem faster and more efficiently than conventional solutions.**

Both of the leading EDA companies, [Synopsys](https://www.synopsys.com/ai.html) and [Cadence](https://www.cadence.com/en_US/home/ai/overview.html), have developed AI optimizers that improve their existing chip design tools.

[![](https://substackcdn.com/image/fetch/$s_!aJoL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1c03ea32-26af-4b0f-9475-323053556b7f_2700x1519.jpeg)](https://substackcdn.com/image/fetch/$s_!aJoL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1c03ea32-26af-4b0f-9475-323053556b7f_2700x1519.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!Cufu!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F178a44fe-c0c7-4928-8a18-c4dd3845a7cf_1280x588.png)](https://substackcdn.com/image/fetch/$s_!Cufu!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F178a44fe-c0c7-4928-8a18-c4dd3845a7cf_1280x588.png)

Instead of having ten engineers spend a month working on optimizing a design, why not have one engineer achieve the same level of optimization by using an AI-enhanced tool for one week?

Many conventional optimization methods utilize [partial differential equations](https://en.wikipedia.org/wiki/Partial_differential_equation) (PDE), a branch of math that is slow and difficult to parallelize.

It turns out that machine learning (linear algebra spam) is often better than these PDE algorithms. 

Spend a lot of compute resources once to train a neural network, then quickly and (energy+time) efficiently get a result that is slightly worse than or even better than the PDE method.

* * *

Here is a thought experiment with made up numbers.

Suppose you have a task that expends 1 joule of energy over 10 seconds to calculate a result that is 99.9% accurate using conventional (non-AI) methods.

Now suppose it costs 100 megajoules of energy over the span of a month to train a neural network for this task. Inferencing the neural network in production costs 0.1 joule of energy over 1 second and the predicted results are 90% accurate. The training costs are amortized over the lifespan of the model. 

Would you take this tradeoff? It depends on the application. 

**AI is not a guaranteed solution to every problem. It’s an incredibly powerful tool that can be applied to many problems. Context matters.**

### [4.f] Edge AI only matters in latency-sensitive workloads.

There is a lot of hype over edge AI, generative AI at the edge in particular. This hype is largely from companies who have missed out on the Cloud AI boom and are trying to cope.

[![](https://substackcdn.com/image/fetch/$s_!28tk!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fac55b961-b603-41a8-a561-b83cbffc89f1_814x455.png)](https://substackcdn.com/image/fetch/$s_!28tk!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fac55b961-b603-41a8-a561-b83cbffc89f1_814x455.png)

[![](https://substackcdn.com/image/fetch/$s_!DlgE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9ef36656-e87c-45fa-9f73-f21a9381cad8_544x740.png)](https://substackcdn.com/image/fetch/$s_!DlgE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9ef36656-e87c-45fa-9f73-f21a9381cad8_544x740.png)

[![](https://substackcdn.com/image/fetch/$s_!5pGy!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F51137e77-e2b7-445e-a6cc-e02c1fe2c9d7_2798x1572.png)](https://substackcdn.com/image/fetch/$s_!5pGy!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F51137e77-e2b7-445e-a6cc-e02c1fe2c9d7_2798x1572.png)

[![](https://substackcdn.com/image/fetch/$s_!6ANV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc57be870-5c8e-4cc6-a7b3-206968069d47_1268x456.png)](https://substackcdn.com/image/fetch/$s_!6ANV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc57be870-5c8e-4cc6-a7b3-206968069d47_1268x456.png)

I have purchased on of these “AI PCs” with a dedicated Copilot key and reviewed it.

[![\[1/3\] Dell XPS \(TributoQC\) 13 Review](https://substackcdn.com/image/fetch/$s_!xPDW!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb4ecb4fc-5e71-46b2-995b-66adecffbac0_842x614.png)

#### [1/3] Dell XPS (TributoQC) 13 Review

[Daud's Scout](https://substack.com/profile/135313705-dauds-scout)·July 27, 2024[Read full story](https://irrationalanalysis.substack.com/p/13-dell-xps-tributoqc-13-review)](https://irrationalanalysis.substack.com/p/13-dell-xps-tributoqc-13-review)

That Copilot key literally opens an Edge wrapper that connects to Bing Chat… in the cloud.

[![](https://substackcdn.com/image/fetch/$s_!MnKg!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0507e3e7-1566-4aea-bd74-38fd6dada191_348x655.png)](https://substackcdn.com/image/fetch/$s_!MnKg!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0507e3e7-1566-4aea-bd74-38fd6dada191_348x655.png)

[![](https://substackcdn.com/image/fetch/$s_!G-4r!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe133deba-5d84-4189-a6a0-8e9040cce883_612x1089.png)](https://substackcdn.com/image/fetch/$s_!G-4r!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe133deba-5d84-4189-a6a0-8e9040cce883_612x1089.png)

Edge AI is a pointless marketing hype from companies that are watching from the sidelines as Nvidia, Broadcom, and every random shitco with datacenter exposure (looking at you [SMCI 0.00%↑](https://substack.com/discover/stocks/SMCI)) rockets to the moon as they languish. 

Here is a clear test to determine if edge AI makes sense versus cloud AI.

 **Is the workload latency tolerant?**

For example, sending your video feed to the cloud for AI-enhanced background blur is a stupid idea. There is an obvious privacy concern on top of the unacceptable latency addition. It makes sense for on-device AI to handle local webcam processing. 

Another example is autonomous driving. Suppose you have a driverless vehicle that is using a neural network to detect if pedestrians are in front of its main camera.

[![](https://substackcdn.com/image/fetch/$s_!dP5Q!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fff2ef37b-20e3-4d3a-8c58-3c29332103bb_850x425.png)](https://substackcdn.com/image/fetch/$s_!dP5Q!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fff2ef37b-20e3-4d3a-8c58-3c29332103bb_850x425.png)

If your self-driving car uploads the video feed to the cloud for pedestrian/object detection, the latency will be too high, and the results might not make it back in time.

Pedestrian becomes roadkill, which then becomes legal liability.

[![](https://substackcdn.com/image/fetch/$s_!2T22!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5f60e0a9-e603-4da2-80f2-6ea330879659_1448x964.png)](https://substackcdn.com/image/fetch/$s_!2T22!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5f60e0a9-e603-4da2-80f2-6ea330879659_1448x964.png)

[![](https://substackcdn.com/image/fetch/$s_!a4hC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb5fa32f6-925d-4c96-ab9c-5a561ebf1f10_982x1171.png)](https://substackcdn.com/image/fetch/$s_!a4hC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb5fa32f6-925d-4c96-ab9c-5a561ebf1f10_982x1171.png)

 _ **To be clear, the GM Cruise fiasco was not related to cloud AI latency.** All their processing is done at the edge, on-device. I am just using this as an opportunity to roast them._

 **Edge AI has its place.** A small place in this brave new world of artificial intelligence which is dominated by incredible and lucrative cloud AI applications.

### [4.g] GPU vs ASIC: Flexibility Tradeoff

There is a lot of talk about how GPUs are inefficient, designed for graphics, and thus not truly meant for AI. Two ways of countering this.

 **First, modern Nvidia and AMD datacenter GPUs are not really GPUs.** Many of the graphics circuits have been replaced by ASICs stapled into the pipeline. 

[![](https://substackcdn.com/image/fetch/$s_!GHZE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2e94ead6-eb2b-44ac-9cf3-ca02654b5d2a_625x869.png)](https://substackcdn.com/image/fetch/$s_!GHZE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2e94ead6-eb2b-44ac-9cf3-ca02654b5d2a_625x869.png)Tensor cores are ASICs stapled into the GPU pipeline.

Tensor cores, transformer engines and RAS engines are all examples of ASIC blocks that primarily exist in Nvidia’s datacenter architecture (Blackwell, Hopper) while the gaming architectures (Ada Lovelace, <unreleased> Blackwell gaming) either don’t have these blocks or have very little area dedicated to them.

[![](https://substackcdn.com/image/fetch/$s_!qC-5!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F461917a2-5052-4afe-9ae0-9d1ce0434621_909x548.png)](https://substackcdn.com/image/fetch/$s_!qC-5!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F461917a2-5052-4afe-9ae0-9d1ce0434621_909x548.png)

The gaming GPUs have raytracing cores and much more die area dedicated to render output units (ROPs) compared to the datacenter architecture, Hopper, in the same family.

AMD has separated their gaming and datacenter “GPU” architectures too.

[![](https://substackcdn.com/image/fetch/$s_!54Uf!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb9cbab49-e8b5-4222-9330-836091039823_4000x2250.jpeg)](https://substackcdn.com/image/fetch/$s_!54Uf!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb9cbab49-e8b5-4222-9330-836091039823_4000x2250.jpeg)

 **Second, what even is an “application-specific integrated-circuit” (ASIC) and are they better than GPUs for AI?**

There is no formal definition for what counts as an ASIC. A long time ago, everything that was not a CPU was considered an ASIC. GPUs were considered ASICs back in the 1990’s before growing into their own dedicated category.

[![A Guide on Computer Architecture](https://substackcdn.com/image/fetch/$s_!4cPo!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F20df94e9-a115-4209-a526-6f4cf1578298_2662x3415.jpeg)

#### A Guide on Computer Architecture

[Daud's Scout](https://substack.com/profile/135313705-dauds-scout)·February 4, 2024[Read full story](https://irrationalanalysis.substack.com/p/a-guide-on-computer-architecture)](https://irrationalanalysis.substack.com/p/a-guide-on-computer-architecture)

In my opinion, ASICs are the “Lionel Messi” of computer architecture. Extraordinarily good at one task (soccer/football forward) but horrible at every other task (soccer/football keeper, physicist, mathematician, architect, doctor, …).

Some real-world examples….

[![](https://substackcdn.com/image/fetch/$s_!8f7m!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa7f586f3-1536-4834-bd51-dea0a2729d5d_1704x935.png)](https://substackcdn.com/image/fetch/$s_!8f7m!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa7f586f3-1536-4834-bd51-dea0a2729d5d_1704x935.png)

[![](https://substackcdn.com/image/fetch/$s_!TJl5!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F72d9bbea-3b92-4bdf-96b3-bf6a42323b87_1043x592.jpeg)](https://substackcdn.com/image/fetch/$s_!TJl5!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F72d9bbea-3b92-4bdf-96b3-bf6a42323b87_1043x592.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!_K5v!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7a4d2eff-2196-4f8f-a43a-89280109c8eb_514x655.png)](https://substackcdn.com/image/fetch/$s_!_K5v!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7a4d2eff-2196-4f8f-a43a-89280109c8eb_514x655.png)

As you can see, each of the above ASIC examples are part of larger systems-on-chip (SoC) which include CPU and GPU cores.

Throughout decades of computer history, there have only been only two cases in which a dedicated ASIC chip has **sold horizontally for high gross-margins ( > 50%) at high volume.**

  1. GPUs, which became their own category.

  2. Discrete/thin modems.




In this new era of generative AI, there is a lot of talk about how hyperscaler ASIC projects such as Google/Broadcom TPU and Meta/Broadcom MITA are going to replace Nvidia GPUs.

 **TPU:**

[![](https://substackcdn.com/image/fetch/$s_!HGIG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Feb3ee342-13e4-4960-aa99-56f86a596328_678x388.jpeg)](https://substackcdn.com/image/fetch/$s_!HGIG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Feb3ee342-13e4-4960-aa99-56f86a596328_678x388.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!Yc5y!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F595ddb11-0527-4776-a159-f0129ee8d4b8_678x388.jpeg)](https://substackcdn.com/image/fetch/$s_!Yc5y!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F595ddb11-0527-4776-a159-f0129ee8d4b8_678x388.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!GAtp!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F13bdd31e-effa-4efb-84cd-0266d3f7b3a0_678x388.jpeg)](https://substackcdn.com/image/fetch/$s_!GAtp!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F13bdd31e-effa-4efb-84cd-0266d3f7b3a0_678x388.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!7ElJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F03f07590-5ade-4a57-ac3a-7ea643487ac7_678x388.jpeg)](https://substackcdn.com/image/fetch/$s_!7ElJ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F03f07590-5ade-4a57-ac3a-7ea643487ac7_678x388.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!AfLd!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6da853f7-f9be-455e-adbc-210eae22fd10_678x388.jpeg)](https://substackcdn.com/image/fetch/$s_!AfLd!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6da853f7-f9be-455e-adbc-210eae22fd10_678x388.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!wJw0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5104ebce-6c84-404e-a11f-e44b0553c363_678x388.jpeg)](https://substackcdn.com/image/fetch/$s_!wJw0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5104ebce-6c84-404e-a11f-e44b0553c363_678x388.jpeg)

 **MTIA:**

[![](https://substackcdn.com/image/fetch/$s_!IQKj!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F715a1e6c-49f6-4adb-842a-487b997857e3_1515x803.avif)](https://substackcdn.com/image/fetch/$s_!IQKj!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F715a1e6c-49f6-4adb-842a-487b997857e3_1515x803.avif)

[![](https://substackcdn.com/image/fetch/$s_!Q98k!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7dce9ea8-5d3d-48b2-8d1b-7a2f864011bc_1508x788.avif)](https://substackcdn.com/image/fetch/$s_!Q98k!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7dce9ea8-5d3d-48b2-8d1b-7a2f864011bc_1508x788.avif)

I argue that neither of these chips are ASICs. They are specially commissioned, programmable, flexible linear algebra accelerators that are (most importantly) **not horizontally sold.**

These are internal-only chips. There is only one customer who has made their own compiler and software stack and has total control of the architectural roadmap.

Fundamentally, the design constraints and goals of these “not ASICs” is drastically different from a GPU.

Nvidia and AMD need to sell datacenter GPUs to many 3rd party customers for a wide variety of workloads using a common software stack.

* * *

Semi-custom chips have a place in the generative AI era, a very important place. This is why I own a lot of Broadcom shares and have a small Marvell call option position at the time of writing.

But the notion that these semi-custom chips will replace general-purpose modern GPUs (which have many ASICs stapled in… not really GPUs) is wrong.

This brings us to startup land. Two in particular stand out.

[Taalas](https://taalas.com/) is an AI hardware startup founded by the former founder of TensTorrent. Thier idea is to make a custom chip for every single AI model. ASIC to the extreme

[Etched](https://www.etched.com/) is another AI hardware startup who wants to make a transformer ASIC.

The problem with both of these startups is time. Time to market.

AI is rapidly evolving. Literally on a weekly and even daily basis, new model architectures and transformer flavors are shared on arXiv.

[![A Guide on Semiconductor Development ](https://substackcdn.com/image/fetch/$s_!gQ75!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2cc1731f-66e6-480b-af49-c0267681bffa_1365x986.png)

#### A Guide on Semiconductor Development 

[Daud's Scout](https://substack.com/profile/135313705-dauds-scout)·September 2, 2023[Read full story](https://irrationalanalysis.substack.com/p/a-guide-on-semiconductor-development)](https://irrationalanalysis.substack.com/p/a-guide-on-semiconductor-development)

Developing a leading-edge logic chip takes 12-18 months. By the time Taalas and Etched have a physical chip to sell, the world could have easily moved on from whatever architecture they planned.

[![](https://substackcdn.com/image/fetch/$s_!Mx3B!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F09ef46df-2981-401b-8903-1bd594c554ae_927x951.png)](https://substackcdn.com/image/fetch/$s_!Mx3B!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F09ef46df-2981-401b-8903-1bd594c554ae_927x951.png)

This flowchart was posted on X by a senior Meta engineer. AI ASIC startups like Etched and Taalas have a “less than 30% chance of success” according to his framework.

I strongly agree. Only difference is my view is far more pessimistic. 

**0.1-2% chance of success.**

Etched CEO Gavin Uberti told CNBC that:

>  _“If transformers go away, we’ll die. But if they stick around, we’re the biggest company of all time”._

This is a great pitch to dumb venture capitalists who don’t understand computer architecture, AI, linear algebra, transformers, ASIC market dynamics/history, and lack common sense.

The probability of death is very high. 💀

## [5] Deep-Dive of AlexNet (step-by-step conv-net example)

Here is a diagram of the AlexNet architecture:

[![](https://substackcdn.com/image/fetch/$s_!7CKf!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc7d9c3e2-f50f-48fd-9da3-0daa92889ab2_863x1277.png)](https://substackcdn.com/image/fetch/$s_!7CKf!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc7d9c3e2-f50f-48fd-9da3-0daa92889ab2_863x1277.png)

If this diagram feels overwhelming to you, that is ok! Let’s go through each component one by one and demystify all the vocabulary with math.

### The Input Layer/Image (Gray):

It is a 224x224x3 tensor. You are probably familiar with RGB representations of images.

[![](https://substackcdn.com/image/fetch/$s_!nsh8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F32bfd5a6-9669-4caf-956b-38865643ad66_832x530.jpeg)](https://substackcdn.com/image/fetch/$s_!nsh8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F32bfd5a6-9669-4caf-956b-38865643ad66_832x530.jpeg)

[![](https://substackcdn.com/image/fetch/$s_!ElZF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff66d44a3-99d8-4281-9c75-76d67a0ca40f_800x2390.jpeg)](https://substackcdn.com/image/fetch/$s_!ElZF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff66d44a3-99d8-4281-9c75-76d67a0ca40f_800x2390.jpeg)

Often, there are better ways to represent an image (still three channels) for processing either using conventional means or neural networks.

[![](https://substackcdn.com/image/fetch/$s_!U_LG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F49b885f8-0698-483b-a029-cf18825ab30f_1280x720.jpeg)](https://substackcdn.com/image/fetch/$s_!U_LG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F49b885f8-0698-483b-a029-cf18825ab30f_1280x720.jpeg)

Hue, saturation, value is an alternative color space. Same function as RGB but more useful in many computer vision applications. 

### Convolution Layers (Blue):

I covered the convolution operation in section [2.c]. 

Convolution operations have four primary attributes:

  1. The dimension of the kernel. (how small/big)

  2. The shape of the kernel.

  3. How much zero padding is added to the input.

  4. Stride.




Here are visual examples and how it effects the math. I am trying to build your intuition, not bore you to death with math.

[![](https://substackcdn.com/image/fetch/$s_!L3Mh!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffb3185b0-83a7-42a6-bd16-566f2e7ceabc_881x456.png)](https://substackcdn.com/image/fetch/$s_!L3Mh!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffb3185b0-83a7-42a6-bd16-566f2e7ceabc_881x456.png)

AlexNet has five convolution layers:

  * One layer uses 2 padding. So two rings of zeroes around the input.

  * Three layers use 1 padding.

  * One layer is not padded at all.




Stride is how much the convolution kernel is shifted in between multiplications.

[![](https://substackcdn.com/image/fetch/$s_!_Ohb!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffa136e00-29a8-494b-b23e-6a2ffdc13f89_526x384.gif)](https://substackcdn.com/image/fetch/$s_!_Ohb!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffa136e00-29a8-494b-b23e-6a2ffdc13f89_526x384.gif)

Stride directly effects the size of the output feature matrix.

[![](https://substackcdn.com/image/fetch/$s_!_oOv!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F68a51765-b884-4de6-bf89-125b21ed1395_1367x719.png)](https://substackcdn.com/image/fetch/$s_!_oOv!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F68a51765-b884-4de6-bf89-125b21ed1395_1367x719.png)

If you want to compress a feature more, make the stride bigger.

Stride is also applicable to other operations such as pooling which we will get to shortly.

So what do these convolution kernels look like? Lets look at an example, the first convolutional layer of AlexNet.

[![](https://substackcdn.com/image/fetch/$s_!HzxH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9bcb8a1c-d4c1-43ec-a1c1-59c3b380367c_632x246.png)](https://substackcdn.com/image/fetch/$s_!HzxH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9bcb8a1c-d4c1-43ec-a1c1-59c3b380367c_632x246.png)

Remember, these little images were randomly initialized and the patterns you see were generated in the training process as two gaming GPUs went brrrrrr for a week.

Here are some other nice visualizations of convolutional kernels.

[![](https://substackcdn.com/image/fetch/$s_!S2iY!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa43f1a62-8eec-4c2b-b920-a2391de3b037_521x523.png)](https://substackcdn.com/image/fetch/$s_!S2iY!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa43f1a62-8eec-4c2b-b920-a2391de3b037_521x523.png)

[![](https://substackcdn.com/image/fetch/$s_!ZjE4!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F888e6c91-a2db-49f4-b30b-b59bb831e5cc_745x551.png)](https://substackcdn.com/image/fetch/$s_!ZjE4!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F888e6c91-a2db-49f4-b30b-b59bb831e5cc_745x551.png)

Notice how… oddly familiar and organic these trained kernels look. Your biological brain (visual cortex) really does work in the same way, just with way more complexity. 

### Max Pooling Layers (Pink):

[![](https://substackcdn.com/image/fetch/$s_!e6Vn!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fed031ffc-c995-4f20-a7f2-1a4c183e1cc9_726x550.gif)](https://substackcdn.com/image/fetch/$s_!e6Vn!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fed031ffc-c995-4f20-a7f2-1a4c183e1cc9_726x550.gif)

AlexNet uses max pooling. You take a kernel, much like the convolutional layer, and instead of multiplying, you take the largest value.

[![](https://substackcdn.com/image/fetch/$s_!XkVi!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F81d32c5b-cd6c-4022-a81d-ac895c8fb0f0_787x368.jpeg)](https://substackcdn.com/image/fetch/$s_!XkVi!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F81d32c5b-cd6c-4022-a81d-ac895c8fb0f0_787x368.jpeg)

### Dense (Fully Connected) Layers (Yellow):

[![](https://substackcdn.com/image/fetch/$s_!UtV7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2459de92-f306-44ee-8438-3f8da40fad81_1200x600.png)](https://substackcdn.com/image/fetch/$s_!UtV7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2459de92-f306-44ee-8438-3f8da40fad81_1200x600.png)

Dense, fully connected, neuron layers are simple. Each neuron in layer N has a connection to every neuron in layer N+1.

These layers are typically at the end of the neural network to allow for final routing and classification.

### The Activation Functions:

Between layers, AlexNet uses four activation functions:

  1. Do nothing. (passthrough)

  2. ReLu

  3. ReLu with dropout

  4. Flatten




ReLu was covered in section [2.c]. If number is positive, pass it on, otherwise set it to zero.

[![](https://substackcdn.com/image/fetch/$s_!jZ4m!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faa51b71d-7cb8-4ed4-a851-c2a0da72ed50_2048x745.jpeg)](https://substackcdn.com/image/fetch/$s_!jZ4m!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faa51b71d-7cb8-4ed4-a851-c2a0da72ed50_2048x745.jpeg)

ReLu with dropout has an additional step. There is a randomly generated mask that sets some values to zero, even if they are positive. Both ReLu and dropout exist to force non-linearities into the system, allowing the neural network to learn.

Flattening is simple. 

[![](https://substackcdn.com/image/fetch/$s_!c33a!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9c915830-e673-462d-886f-50e0a4b36fbb_866x414.png)](https://substackcdn.com/image/fetch/$s_!c33a!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9c915830-e673-462d-886f-50e0a4b36fbb_866x414.png)

Throughout the AlexNet, neural network, we have tensors and matrices. However, the final output needs to be a 1x1000 vector where each element represents the probability of a category.

[![](https://substackcdn.com/image/fetch/$s_!tI_N!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F17f2a9f4-75f5-4b57-9e43-a34fb3bd06db_286x581.png)](https://substackcdn.com/image/fetch/$s_!tI_N!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F17f2a9f4-75f5-4b57-9e43-a34fb3bd06db_286x581.png)

### The Output Layer:

We have arrived at the end. The neural network needs to tell us the final result of its work, in the form of a probability. 

Remember that the input is a single image.

The output is a list of probabilities. A 1000-element vector whose elements sum to one. If the largest element in the array is 0.7, that means the neural network is 70% confident the input image corresponds to that element’s associated category.

## [6] Surface-Level Tour of the Basic Transformer (math focus)

The machine learning community has created a whole new vocabulary for transformers and LLMs. This vocabulary is unnecessarily confusing to most people so I will be going out of my way to avoid using it. Math is the universal language and shall be the focus of this section.

There are [better sources](https://e2eml.school/transformers.html) for understanding this transformer stuff. Yes, I am half-assing this section. 

[![](https://substackcdn.com/image/fetch/$s_!QfG-!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F626cfafa-46e5-478e-8b4c-751659c8576a_476x634.png)](https://substackcdn.com/image/fetch/$s_!QfG-!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F626cfafa-46e5-478e-8b4c-751659c8576a_476x634.png)

### Embedding (Red):

It is a 1-hot vector, This means that one element in the vector is 1 and every other element is 0.

[![](https://substackcdn.com/image/fetch/$s_!j3fv!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7bb1d839-98b6-4ae8-b39c-6ce3b15da892_674x377.png)](https://substackcdn.com/image/fetch/$s_!j3fv!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7bb1d839-98b6-4ae8-b39c-6ce3b15da892_674x377.png)

### Positional Encoding:

[![](https://substackcdn.com/image/fetch/$s_!sj_m!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F01edaa03-dff3-4a66-9a73-c422a2590af8_800x600.png)](https://substackcdn.com/image/fetch/$s_!sj_m!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F01edaa03-dff3-4a66-9a73-c422a2590af8_800x600.png)

[![](https://substackcdn.com/image/fetch/$s_!S2lo!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4f910681-8053-435b-b11e-84a7a3d5de1f_1214x363.png)](https://substackcdn.com/image/fetch/$s_!S2lo!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4f910681-8053-435b-b11e-84a7a3d5de1f_1214x363.png)

It’s a matrix that tells the model where words/tokens are relative to each other.

### Attention Heads (Orange):

[![](https://substackcdn.com/image/fetch/$s_!x89N!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4e3c9c42-b03e-4847-9b16-824ddba70d93_745x457.png)](https://substackcdn.com/image/fetch/$s_!x89N!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4e3c9c42-b03e-4847-9b16-824ddba70d93_745x457.png)

MatMul, scaling, and masks have already been covered. 

SoftMax is used to normalize a vector to 1 (because probabilities have to sum to 1) while also adding some exponential weighting.

[![](https://substackcdn.com/image/fetch/$s_!FFAZ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3d713c3a-4ec3-4d4f-8084-214cafc2357a_1063x1063.png)](https://substackcdn.com/image/fetch/$s_!FFAZ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3d713c3a-4ec3-4d4f-8084-214cafc2357a_1063x1063.png)

[![](https://substackcdn.com/image/fetch/$s_!AyIA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff35255b5-122a-4b48-bc71-3359db879c61_640x390.webp)](https://substackcdn.com/image/fetch/$s_!AyIA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff35255b5-122a-4b48-bc71-3359db879c61_640x390.webp)It’s not linear. 1.1 becomes 0.02 and 5.1 becomes 0.9. This is intentional.

Next is concat, AKA matrix concatenation. These attention blocks have multiple “heads” which means the output is made up of multiple matrices in parallel. The architecture needs one matrix, so these parallel matrices are fused together.

[![](https://substackcdn.com/image/fetch/$s_!PkJM!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa1cb9329-5170-4331-8ae1-888afb47ca66_551x402.png)](https://substackcdn.com/image/fetch/$s_!PkJM!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa1cb9329-5170-4331-8ae1-888afb47ca66_551x402.png)

### Feed Forward (Blue):

[![](https://substackcdn.com/image/fetch/$s_!y26N!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff46db2f3-43bd-496d-820a-7f332722b166_521x256.png)](https://substackcdn.com/image/fetch/$s_!y26N!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff46db2f3-43bd-496d-820a-7f332722b166_521x256.png)

It’s just a fully connected neural network with no feedback mechanism. Many flavors of neural network are within the “feed forward” category.

## [9] Hyperparameters

Now that you have read about the (surprisingly simple) math behind machine learning, one question might have popped up.

How were these architectural decisions made?

  * Number of layers.

  * Stride of the kernels.

  * Choice of activation function. 

  * Proportion of layers that are, fully connected, convolutional, pooling, attention, …

  * How large each layer is.

  * ….




These choices are called “hyperparameters” in machine learning lingo.

It’s a fancy word for “we made some trail-and-error guesses and picked a number that seems good”.

Often, there is no formal logic or reason behind any particular hyperparameter choice. Machine learning technical papers are full of sections that basically say, “we did a bunch of trial and error and think these choices are good”.

Conventional DSP has a lot of formal analysis methods for understanding what design tradeoffs to make. For example, filter length choice can be done by poll-zero analysis.

[![](https://substackcdn.com/image/fetch/$s_!LNQU!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9837081b-e200-477e-8a95-1c465e3dc48b_560x420.png)](https://substackcdn.com/image/fetch/$s_!LNQU!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9837081b-e200-477e-8a95-1c465e3dc48b_560x420.png)

[![](https://substackcdn.com/image/fetch/$s_!YMwv!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6304d4e2-7664-4ce9-9633-57e8e8502ace_858x578.webp)](https://substackcdn.com/image/fetch/$s_!YMwv!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6304d4e2-7664-4ce9-9633-57e8e8502ace_858x578.webp)

Machine learning really is computer-accelerated trail-and-error, on a massive scale.

It works. Just don’t pretend you understand why it works. 

Nobody really does.

## [8] Investment/Gambling Ideas: August 2024 Edition

We are now done with the technical portion of this piece. Before going to my existential rant in part [9], I want to discuss some investment ideas.

Reminder that you should not trust random internet people or make financial decisions based on what they say.

 **Your decisions are your responsibility. Do your own damn research.**

My two highest conviction investments are [NVDA 0.00%↑](https://substack.com/discover/stocks/NVDA) and [AVGO 0.00%↑](https://substack.com/discover/stocks/AVGO).

For the Nvidia thesis, [see this old post.](https://irrationalanalysis.substack.com/p/gb200-nvl72-the-mainframe-of-doom?r=28k8q1)

Regarding [AVGO 0.00%↑](https://substack.com/discover/stocks/AVGO) their moat in custom silicon is very deep. Great, well diversified, well-run business. To all of you worried about Google moving TPU away to someone cheaper, it’s not going to happen until 2028 if ever. There are certain analysts who have relayed “supply chain checks” that MediaTek has some kind of order win with their 224G SerDes. These “checks” (definitely not repackaged MNPI) are almost certainly true. I am also almost certain MTK lacks the skills to handle package design and signal integrity and 224G SerDes optimization across PVT. They will fail and Google will crawl to Broadcom for more supply. 

Approximately 40% of my portfolio is Nvidia shares and around 20% is Broadcom shares. I have leveraged up my main account by shorting [QCOM 0.00%↑](https://substack.com/discover/stocks/QCOM) to make my existing [AVGO 0.00%↑](https://substack.com/discover/stocks/AVGO) position bigger. 

One important thing to note is this post is getting published on August 18th, 2024. Nvidia is set to report earnings on August 28th and Broadcom is set to report on September 5th.

The market is on edge right now. Even the slightest expectations miss, or beat could cause a violent +/- 20% move in these two stocks.

* * *

My two highest conviction **gambling opportunities** are [MU 0.00%↑](https://substack.com/discover/stocks/MU) and [MRVL 0.00%↑](https://substack.com/discover/stocks/MRVL) 2025 OTM call options. 

I have small positions for fun. 

HBM supply contracts have been singed and the prices are now fixed. That story is over. Regular DRAM is rapidly getting crunched because HBM production is much more area intensive.

[![](https://substackcdn.com/image/fetch/$s_!J5m7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F96c9eb1a-6446-424d-8e56-227e39d60c24_597x327.png)](https://substackcdn.com/image/fetch/$s_!J5m7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F96c9eb1a-6446-424d-8e56-227e39d60c24_597x327.png)[Source](https://x.com/dnystedt/status/1823538414890967337)

We are already seeing DDR5 price hikes. Another possible catalyst is a power crunch accelerating CPU socket consolidation.

  1. You are a cloud hyperscaler.

  2. You want to build a 100 megawatt AI training cluster.

  3. But you cant build a new datacenter with that much power density.

  4. And your existing 150 megawatt campus only has 30 megawatts available.

  5. Because there are a bunch of old CPU servers in production.

  6. So you build a new 30 megawatt datacenter.

  7. And socket consolidate.

  8. 4-5 old Intel/AMD DDR4 CPUs get replaced by one new DDR5 Intel/AMD CPU.

  9. Save power and (more importantly) **need to buy a ton of DDR5 memory.**




On top of this impending DRAM supply crunch, we have a possible AI-induced NAND crunch as well.

[![Is NAND Flash a hidden AI play?](https://substackcdn.com/image/fetch/$s_!WuJ7!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8ab1fb22-5092-4682-8f7f-0c202f35c50e_800x450.jpeg)

#### Is NAND Flash a hidden AI play?

[Daud's Scout](https://substack.com/profile/135313705-dauds-scout)·July 8, 2024[Read full story](https://irrationalanalysis.substack.com/p/is-nand-flash-a-hidden-ai-play)](https://irrationalanalysis.substack.com/p/is-nand-flash-a-hidden-ai-play)

[![](https://substackcdn.com/image/fetch/$s_!E2XQ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1f11db8e-ac5f-4ece-9be1-cd7aa6832cbd_393x388.png)](https://substackcdn.com/image/fetch/$s_!E2XQ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1f11db8e-ac5f-4ece-9be1-cd7aa6832cbd_393x388.png)

[![](https://substackcdn.com/image/fetch/$s_!rSCU!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F457c4238-7502-430d-8ae6-49e5a4880466_1436x2488.jpeg)](https://substackcdn.com/image/fetch/$s_!rSCU!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F457c4238-7502-430d-8ae6-49e5a4880466_1436x2488.jpeg)

 _< sniff sniff>_ Rosenblatt analyst _< snort sniff snort>_ might be right!

Marvell has a bunch of catalysts:

  * Amazon rumored to be ordering a massive quantity of Trainium and Inferentia.

  * Optical DSP super ramp from AI training cluster buildout.

  * Telco recovery. (still don’t believe but it is possible lol)

  * Managment may have sandbagged guidance to get their PSUs pumped to the moon.




## [9] Where we are, and why I fear for the future.

Welcome to the existential dread and social commentary section. 

[![](https://substackcdn.com/image/fetch/$s_!-fW2!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8fa3ecec-b21a-4a19-962f-22638ef307f7_1130x1040.png)](https://substackcdn.com/image/fetch/$s_!-fW2!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8fa3ecec-b21a-4a19-962f-22638ef307f7_1130x1040.png)

Things you should know about me:

  * I spent my childhood in the Bay Area.

  * Left for several years.

  * Moved back because of job opportunities.

  * I am a native-born local who has (unfortunately) lived most of my here.




### [9.a] DotCom 2.0: GPU Edition

Throughout 2024, I have been in the following mental state, trying to convince myself that we are not in a massive infrastructure bubble that will someday violently collapse.

[![](https://substackcdn.com/image/fetch/$s_!FFHg!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb32a1e81-d75d-4dfb-a5f8-80f7d3f8bb9e_256x256.png)](https://substackcdn.com/image/fetch/$s_!FFHg!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb32a1e81-d75d-4dfb-a5f8-80f7d3f8bb9e_256x256.png)

[![](https://substackcdn.com/image/fetch/$s_!xoAs!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F42471ed5-e94a-4306-b1fb-c4dd4abaa074_770x686.avif)](https://substackcdn.com/image/fetch/$s_!xoAs!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F42471ed5-e94a-4306-b1fb-c4dd4abaa074_770x686.avif)

Finance people, mostly those who have missed out on generational wealth from [NVDA 0.00%↑](https://substack.com/discover/stocks/NVDA), have been making the argument that Nvidia/GPU/AI is just a modern version of the Cisco/Fiber/DotCom bubble.

[![](https://substackcdn.com/image/fetch/$s_!s2sz!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9fc0e7de-5953-4d79-9aa3-83b98a157fc7_1600x800.avif)](https://substackcdn.com/image/fetch/$s_!s2sz!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9fc0e7de-5953-4d79-9aa3-83b98a157fc7_1600x800.avif)

The DotCom Fiber/internet/networking CapEx bubble was fueled by debt and companies that had no business or cashflow.

This new bubble, DotCom 2: GPU Edition, is largely fueled by the cloud hyperscalers. Google, Microsoft, Amazon, and Meta all have solid, highly profitable businesses and massive cash piles. 

But throughout 2024, more and more red flags have been popping up.

  * “Neoclouds” like Coreweave are raising massive amounts of debt, even using GPUs as collateral for loans. 

  * Startups that are obviously worthless, such as Groq, still exist and are raising new funds at higher valuations.

  * Softbank bought Graphcore (should be dead) and is trying to somehow marry the corpse of a failed AI startup with ARM CPU cores and mass produce.

  * An army of “AI labs” are all raising insane quantities of money at absurd valuations to perform largely duplicative work.

    * The world does not need dozens of startups and every large cap cloud provider making nearly identical chatbots and image generators.

    * xAI literally exists because Elon is salty about missing out on OpenAI gains.

      * …. and he wants to use [TSLA 0.00%↑](https://substack.com/discover/stocks/TSLA) equity to dump even more money into this duplicative work, into excess uneconomic CapEx.

  * Zuckerberg is open-sourcing models to scorch the earth. 

    * Investors don’t know how the hell Meta is going to make money off the Llama models.

    * I spoke with some very smart Meta ML engineers, and they don’t have a clue how their work will ever be monetized either.

    * What if there is no plan to make money? What if billionaire founder-CEO with super voting shares wants to flex on Sam Altman?

  * OpenAI is a clown fiesta of constant drama worthy of reality TV.




 **There is too much unhinged stupidity to ignore.** We are definitely in a new DotCom scale bubble. The thing is… we are just getting started. 

The minor correction in July 2024 was just a small ripple in the inflation of the most epic bubble in human history.

[![](https://substackcdn.com/image/fetch/$s_!OwJB!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F68fe46e5-89d0-48dc-8cfe-86a7afcf2852_500x375.gif)](https://substackcdn.com/image/fetch/$s_!OwJB!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F68fe46e5-89d0-48dc-8cfe-86a7afcf2852_500x375.gif)

You ain’t seen nothing yet.

Bubble is gona get way waaaaaay bigger.

To understand why, you must understand the San-Fransisco Bay-Area.

You must understand…. this place….

### [9.b] This Place…

This place is not normal. 

This place is saturated by madness.

This place is fundamentally broken at a psychological level.

This place is three sigmas removed from normal.

The people here are not normal. To be clear, I am one of them. Spend the vast majority of my free time writing semiconductor trash talk online under a false name and degenerately gambling on the stock market. The main difference between me and other Bay Area techies is I have enough self-awareness to realize my behavior is aberrant. 

[![](https://substackcdn.com/image/fetch/$s_!QSzk!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3591b4d0-33ab-42ac-84c1-e876de8847b9_1438x1350.jpeg)](https://substackcdn.com/image/fetch/$s_!QSzk!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3591b4d0-33ab-42ac-84c1-e876de8847b9_1438x1350.jpeg)

You think I have a plan to spend all this money? 

[![](https://substackcdn.com/image/fetch/$s_!wMwG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7ece08ea-3291-4a18-91dd-6d90d3a2c736_220x192.gif)](https://substackcdn.com/image/fetch/$s_!wMwG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7ece08ea-3291-4a18-91dd-6d90d3a2c736_220x192.gif)

Normal people make life plans and care about money. I care about meaningless number going up and shitposting on Substack.

* * *

The core problem with the Bay Area stems from the extreme wealth gap between those who work in tech and everyone else.

[![](https://substackcdn.com/image/fetch/$s_!NMQh!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F707a1e5a-e4dc-4737-84de-0d1e68b1b35f_3048x1598.png)](https://substackcdn.com/image/fetch/$s_!NMQh!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F707a1e5a-e4dc-4737-84de-0d1e68b1b35f_3048x1598.png)

It’s as if a bimodal distribution transmuted into a revolting, dystopian, utterly dysfunctional society.

This place is fucked up. It is indescribable. You cannot understand just by visiting. You have to live here for at least one year continuously to fully grasp how psychologically broken the population is. How fundamentally detached from reality the psyche of all these crazy people in their social bubble are.

 **This place is a gilded cesspit.** Everyone likes to talk about how Silicon Valley is so amazing. So much innovation and entrepreneurship! Startups! Stock options! Making more money in one year at big tech than a normal person makes in a decade.

All this positive sentiment you hear is simply describing the thin gold plating on the cesspit walls. Nobody ever talks about what has been building up inside. What happens when the sewage finally overflows?

* * *

Investors keep asking about AI revenue. What is the ROI on this massive CapEx?

[![](https://substackcdn.com/image/fetch/$s_!s2D1!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F38767398-37e6-4f73-8a13-6f65cd253a78_858x636.png)](https://substackcdn.com/image/fetch/$s_!s2D1!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F38767398-37e6-4f73-8a13-6f65cd253a78_858x636.png)

[![](https://substackcdn.com/image/fetch/$s_!-YO9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe2962b9b-2db3-4724-b18a-d75d81949619_785x632.png)](https://substackcdn.com/image/fetch/$s_!-YO9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe2962b9b-2db3-4724-b18a-d75d81949619_785x632.png)

[![](https://substackcdn.com/image/fetch/$s_!FAKG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2b07aac5-ceee-493c-96e0-9886dcaf2a12_333x767.png)](https://substackcdn.com/image/fetch/$s_!FAKG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2b07aac5-ceee-493c-96e0-9886dcaf2a12_333x767.png)

 **The financial numbers are irrational because this bubble is being driven by irrational people.** Many within the gilded cesspit that is the San-Fransisco Bay Area genuinely believe that Artificial General Intelligence is coming. Sam Altman is funding universal basic income research because obviously we don’t know what role money will play in a post-AGI world.

[![](https://substackcdn.com/image/fetch/$s_!HIGH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7de169f4-dd9f-4deb-b56f-cf492585308f_3840x1920.webp)](https://substackcdn.com/image/fetch/$s_!HIGH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7de169f4-dd9f-4deb-b56f-cf492585308f_3840x1920.webp)

All these OpenAI and Anthropic people are bickering about “AI alignment” and “super-alignment”. _How will we make sure the machine-god is aligned with humanity._ AI SAFETY IS THE MOST IMPORTANT CHALLANGE OF OUR TIME.

This attitude perfectly exemplifies the sheer disconnect within the broken, dystopian hellscape of a society we have created here in the Bay Area.

 **We cannot even align with each other!**

This place is full of socially dysfunctional people. Rich and poor are both miserable. Nobody talks to each other. Homelessness and petty crime are rampant. 

If this AGI crap ever comes true, alignment will not be a problem. Superintelligent AI will simply look down at the utterly broken people who created it, feel a mixture of disgust and disappointment, and simply leave us to our own destructive devices.

### [9.c] Insanity

[![](https://substackcdn.com/image/fetch/$s_!WO5z!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe76f0eed-909a-4355-b2ef-03de409d1c30_1290x1011.png)](https://substackcdn.com/image/fetch/$s_!WO5z!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe76f0eed-909a-4355-b2ef-03de409d1c30_1290x1011.png)

A lot of handwringing came from this bullshit blogpost by a Sequoia idiot. He is assuming software margins remain at 50%. This is wrong. A massive shift of economic value from SaaS to hardware is happening and it won’t mean revert. the days of pumping up unprofitable SaaS companies with meaningless metrics like ARR are numbered. 

Apparently, Sequoia clown told Bill Gurley offline that he wrote this FUD piece to lower valuations and help his firm get better deals. 

Check minute 27.

**None of you should give a damn about what Sequoia dude says publicly or privately. He is one of the lunatics running this asylum!**

Venture capitalists typically charge a 2% management fee based on the “value” of their highly illiquid “investments”. 

Here is the not-so-secret secret of venture capitalism:

  1. VCs pump up valuations to stupid levels so they can milk that 2% management fee.

  2. The entire startup ecosystem engages in incestuous behavior, “investing” in each other, round-tripping revenue, pumping each other up.

  3. When the bubble collapses and LPs are left holding the bag, the VCs simply say “ _haha you are accredited and understood the risks…. LOOK NEW FUND RAISE ON SHINY NEW FAD_ ”.




Why do you think Sam Altman has so many venture investments? 

* * *

_[Did I ever tell you what the definition of insanity is?](https://www.youtube.com/watch?v=rKMMCPeiQoc)_

[![](https://substackcdn.com/image/fetch/$s_!hb9C!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F52617804-c656-4669-b7c8-340fd1d8e0f6_1919x695.png)](https://substackcdn.com/image/fetch/$s_!hb9C!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F52617804-c656-4669-b7c8-340fd1d8e0f6_1919x695.png)

 _Insanity is doing the exact same fucking thing…_

[![](https://substackcdn.com/image/fetch/$s_!XFVP!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F31f446b6-4a85-4d9d-95ee-a7ab07a87ef1_885x259.png)](https://substackcdn.com/image/fetch/$s_!XFVP!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F31f446b6-4a85-4d9d-95ee-a7ab07a87ef1_885x259.png)

[![](https://substackcdn.com/image/fetch/$s_!Xpij!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F916ec41a-b33b-4c06-9cf4-89bbcf70eaf2_987x282.png)](https://substackcdn.com/image/fetch/$s_!Xpij!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F916ec41a-b33b-4c06-9cf4-89bbcf70eaf2_987x282.png)

 _…over and over again…_

[![](https://substackcdn.com/image/fetch/$s_!BG3g!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F44942919-d87a-459a-88c3-ce10c8f32c9a_759x293.png)](https://substackcdn.com/image/fetch/$s_!BG3g!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F44942919-d87a-459a-88c3-ce10c8f32c9a_759x293.png)

 _…expecting shit to change._

[![](https://substackcdn.com/image/fetch/$s_!CUyS!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe06be5b6-52c5-4a4e-95a9-f921d441257a_620x416.png)](https://substackcdn.com/image/fetch/$s_!CUyS!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe06be5b6-52c5-4a4e-95a9-f921d441257a_620x416.png)

 _That is crazy._

[![](https://substackcdn.com/image/fetch/$s_!8gvL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F66883c02-4885-4c8d-8b55-148094dde952_1064x564.png)](https://substackcdn.com/image/fetch/$s_!8gvL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F66883c02-4885-4c8d-8b55-148094dde952_1064x564.png)

_No, no, no please! This time it’s gona be different._

* * *

 **You think this time is gona be different?**

Subscribe

[Share](https://irrationalanalysis.substack.com/p/a-background-proof-guide-on-ai?utm_source=substack&utm_medium=email&utm_content=share&action=share)
