---
title: Intro Text2Image models which use MLLM (Flux_QWEN2VL)
author: LYK
date: 2024-12-04 19:00:00 +0800
categories: [Reading, Paper]
tags: [MLLM, Text2Image, Qwen, Qwen2VL, Qwen, Flux]
pin: true
published: true
description: So so excited to see the progress of Text2Image models which use MLLM. Expecting since 2023!!!
---

## Intro

非常高兴看到类似这样文章，LLM + DiT.  
2023年 ~ 2024年Q2，一直找类似的模型，因为LLM已经很成功了；但是SD、SDXL、SD3、SD3.5、Flux仍然抱着CLIP、T5不放。
这些文生图模型最难的问题不是生图不好看，而是生图和用户想要的不一致。  
不知道为什么没有人做这样的尝试？成本太高？不好训？
很高兴目前看到了希望：  
- 202409 Playground V3: [Playground v3: Improving Text-to-Image Alignment with Deep-Fusion Large Language Models](https://arxiv.org/abs/2409.10695)
- 202411 Qwen2VL-Flux: [https://github.com/erwold/qwen2vl-flux/blob/main/technical-report.pdf](https://github.com/erwold/qwen2vl-flux/blob/main/technical-report.pdf)

> Playground V3 已单独成篇，值得一看！[跳转链接](https://lyk0014.github.io/posts/Playground_v3/)

## 要解决什么问题？
文生图模型从2022年开始已经非常成功了，从娱乐向逐渐转向了生产向。  
但一直面临着**两个重大挑战**： 
1. 在整合参考图像时保持语义一致性和风格保真度
2. 生成过程提供细粒度控制  

**主要原因**：文本编码器的多模态理解能力有限，它们难以有效地弥合文本描述和视觉特征之间的语义差距

为了解决这个问题，有**两个成熟的方向**：
1. 专注于提高文本编码器的能力，像Stable Diffusion和FLUX.1这样的模型结合了T5-XXL和CLIP以获得更好的文本理解
2. 探索基于参考的生成，通过各种控制机制，如空间条件或注意力操作  

**目前仍然有很大提升空间。**

## 如何实现的？



## Reference



