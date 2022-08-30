---
title: diffusion model
linktitle: diffusio nmodel
type: book
date: '2019-05-05T00:00:00+01:00'
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 2
---

## Diffusion model

说到扩散模型，一般的文章都会提到能量模型（Energy-based Models）、得分匹配（Score Matching）、朗之万方程（Langevin Equation）等等，简单来说，是通过得分匹配等技术来训练能量模型，然后通过郎之万方程来执行从能量模型的采样。

从理论上来讲，这是一套很成熟的方案，原则上可以实现任何连续型对象（语音、图像等）的生成和采样。但从实践角度来看，能量函数的训练是一件很艰难的事情，尤其是数据维度比较大（比如高分辨率图像）时，很难训练出完备能量函数来；另一方面，通过朗之万方程从能量模型的采样也有很大的不确定性，得到的往往是带有噪声的采样结果。所以很长时间以来，这种传统路径的扩散模型只是在比较低分辨率的图像上做实验。

如今生成扩散模型的大火，则是始于2020年所提出的**[DDPM](https://link.zhihu.com/?target=https%3A//arxiv.org/abs/2006.11239)**（Denoising Diffusion Probabilistic Model），虽然也用了“扩散模型”这个名字，但事实上除了**采样过程**的形式有一定的相似之外，DDPM与传统基于朗之万方程采样的扩散模型可以说完全不一样，这完全是一个新的起点、新的篇章。

准确来说，DDPM叫“**渐变模型**”更为准确一些，扩散模型这一名字反而容易造成理解上的误解，传统扩散模型的能量模型、得分匹配、朗之万方程等概念，其实跟DDPM及其后续变体都没什么关系。有意思的是，DDPM的数学框架其实在ICML2015的论文**[《Deep Unsupervised Learning using Nonequilibrium Thermodynamics》](https://link.zhihu.com/?target=https%3A//arxiv.org/abs/1503.03585)**就已经完成了，但DDPM是首次将它在高分辨率图像生成上调试出来了，从而引导出了后面的火热。由此可见，一个模型的诞生和流行，往往还需要时间和机遇.



## **拆楼建楼**

实际上，相比于传统的扩散模型，DDPM实际上更像VAE而不是扩散模型。很多文章在介绍DDPM时，上来就引入转移分布，接着就是变分推断，一堆数学记号下来，先吓跑了一群人，再加之人们对传统扩散模型的固有印象，所以就形成了“需要很高深的数学知识”的错觉。事实上，DDPM也可以有一种很“大白话”的理解，它并不比有着“造假-鉴别”通俗类比的GAN更难。

首先，我们想要做一个像GAN那样的生成模型，它实际上是将一个随机噪声z变换成一个数据样本x的过程：
