---
title: A comprehensive review of research papers in the field of novel generation. - 202412
author: LYK
date: 2024-12-09 00:00:00 +0800
categories: [Reading, Paper]
tags: [Novel Generation, Novel, LLM, Story]
pin: true
published: true
description: 粗读，汇总目前收集到的关于Novel Generation的论文【截止202412】
media_subpath: '/posts/20241210'
status: todo  # todo, draft, completed, published
---

# Intro

## LongStory 
> 论文：[LongStory: Coherent, Complete and Length Controlled Long story Generation](https://arxiv.org/abs/2311.15208)    
> 2023.11  
> BERT时代的语言模型，基于BART训练，早过时了，不知道为什么会发表这么晚。

```
**问题**  
由于上下文窗口限制，长文本生成通常采用递归段落生成方法来组成长故事；这种方法存在上下文遗忘，导致连贯性问题出现；同时LM倾向于在递归生成中重复相同的故事，导致重复性问题。

挑战实现100~10K的长文本生成。

**方法**  
Coherent, Complete and Length Controlled Long story Generator，两个创新点：
- 长短期上下文权重校准器（CWC），使用BERT-Tiny实现
- 长故事结构位置（LSP），即段落的顺序，为故事生成器提供段落的结构位置信息（例如，<front>、<middle>、<ending>、<next is ending>）
- 基于Transformer Encoder-Decoder框架，基于BART进行训练
- 基于GPT-2评估连贯性
- 基于n-gram BLEU评估重复性
- 

**效果**
- 能降低重复性，及对多样性有效
- 连贯性、完整性、相关性优于基线模型
- 提升相关性并不总是能提升连贯性和完整性

```


## E2E PLOT GENERATOR
> 论文：[END-TO-END STORY PLOT GENERATOR](https://arxiv.org/pdf/2310.08796)    
> 2023.10  
> 整体效果难讲，就是微调Llama2-7B

```
**问题**  
解决当前使用LLM生成情节的几个问题：
1. 调用LLMs次数多，昂贵且耗时
2. 情节框架太死，不能个性化

**方法**  
1. OpenPlot: Prompt + LLAMA2 生成13K故事情节，基于Llama2-13B-chat
2. E2EPlot: 使用13K数据，通过SFT训练，基于Llama2-7B-chat
3. RLPlot: 使用RLHF微调E2EPlot
4. GPT-4量化评估

**效果**
- 生成速度：1K Token/30s
- 质量： 与DOC/OpenPlot相当

```


## Arbitrary Writing Styles
> 论文：[Learning to Generate Text in Arbitrary Writing Styles](https://arxiv.org/pdf/2312.17242)    
> 2023.12  
> 

```
**问题**  
LLM模仿著名文家作家的风格非常容易，但如果想通过instruction或ICL来模仿特定作者的风格会比较难。特别是一些风格或写作习惯，即使是语言学家也很难描述。

**方法** 
STYLEMC: 由LLM和Regressor组成，Regressor经过风格训练，在LLM推理时，重调其概率分布，使输出更符合指定风格。  
LLM：MPT-7B  
Regressor: OPT-1.3B

**作者风格


**效果**
- 可以捕获直观的风格特征
- 可以作为一种有效作者匿名化技术
- 在零样本设置中，相比LLM更难被检测为AI生成，作者归因于更好地模仿了人类写作风格的能力
- 开源了模型、数据集、训练脚本


```

