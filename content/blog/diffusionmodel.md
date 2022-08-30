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

