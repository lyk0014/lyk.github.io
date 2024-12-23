---
title: Processing AI Novel - Revision
author: LYK
date: 2024-12-05 19:00:00 +0800
categories: [AIA, AI Novel]
tags: [AI Novel, Thinking, Revision, Human Feedback, Peer Review]
pin: true
published: false
description: 技术方案 - 如何结合专业反馈（Human Feedback、Peer Review、Critic Agent）, 打造完整的网文内容生产系统
---

**项目名**：小说改写 - 又称：洗稿、仿写   
**目标**：用AI打造一套完整且自动化的内容生产系统（网文）  


## Intro
> 本文主要关注自动化流程中，人工介入应该如何流程化。<br>
> 人工介入包括：人工反馈、专家意见、评审Agent。<br>
> 如果Agent足够好，用Agent来代替人工，才是最终的自动化生产。


## 总体方案

| 改写方式 | 改写内容              | 原创程度 | 时间点      | 状态    |
|------|------------|---------|--------|----------|-------|
| 直翻   | 仅修改人设、背景           | 明确抄袭 | 20241209 |  Completed |
| 改写   | 章节粒度修改情节 |  合理借鉴 | 20241213 |  TODO |
| 重写   | 基于框架，从头开始创作小说     | 归属原创 | 20241227 |  TODO |
{: .table-striped .table-hover}


当前已发现问题：
1. 章纲生成错乱，与原作章节的章纲完全对不上？
2. 前面章节比较平，怎么替换部分章节的情节？


人工介入节点列表：
- 生成新书改写框架
- 新书大纲修改
- 人物小传调整
- 多章情节调整
- 章节间逻辑审核
- 剧本逻辑排查
- 小说润色
- 小说翻译审校


## 生成新书改写框架
> **问题：**现在有一本被完整拆解的书（大纲、章纲、人物小传），那么对于一个小白来讲，应该如何改才能找到灵感、形成思路，进而生成完整的改写框架？  
> **逐步拆解：**
> - 1.寻找灵感：
  - [可选] 人工给改写方向
  - CreativeAgent给出多个创意改编方向，对于（人设、情节、世界观）的一个点或多个点
  - 确定创意点 - 50字左右
> - 2.[可选] 确定改编思路：
  - 增加更多人工主观思路
> - 3.形成完整框架（基于以上两步）：
  - a. 生成改编前后设定对照表（主角、世界观、主线剧情、主题、配角、反派、叙事风格、情节亮点、文化适配性、英雄之旅）
  - b. 生成新书的特色亮点（设定的独特性、主题和深度、角色成长、叙事风格）
  - c. 生成主角的英雄之旅（坎贝尔的英雄之旅框架）
  - d. 新书的标签信息（类型、主题、情感、目标受众、市场）
  - e. 新书基本信息（书名、封面、宣传语）



## 新书的大纲修改
> **问题：**通常完整改写框架后，大纲是可以自动生成的；为避免特殊需要，列举下大纲的主要元素。
> 主要元素
- 故事概要：100字左右
- 主要人物介绍：包含正反派，1句话总结
- 主线剧情：200字左右
- 重要支线剧情：逐个列举，每个支线剧情100字左右
- 世界观设定：100字左右
- 故事发展脉络【可选】：100字左右概述
- 主题分析：50字左右
- 写作风格和基调：50字左右
- 英雄之旅：100字左右    
>
> 大纲这么算才1000字左右，有点少，按找专业人士的大纲，估计会在万字左右


## 人物小传调整
> **问题：**人设的调整是必然会发生的，现在调整一个主角的人设，可能会涉及到所有角色的连带调整、大纲调整、改写框架调整，怎么设置流程才能更方便小白调整呢？
> 前置信息：大纲、改编框架、人物小传-全部
> 当前调整流程：
1. **人设调整思路**：简洁地描述清楚调整哪个角色（或多个），为什么，想怎么调，期望达到什么效果
2. **迭代交互**：不满意就Chat，达到满意为止
3. **整理调整后的人物小传**：按指定格式输出（英雄定位、基本信息、性格特征、外貌描述、背景故事、角色关系、关键事件、角色成长）
4. **列举受影响的角色**：牵一发而动全身，整理其他受影响的角色，形成角色并形成表格（角色、影响分析、修改建议）
5. **逐个生成新版人物小传**：为受影响的每个角色，在原人物小传的基础上，优化生成完整人物小传
6. **生成新版的改编框架**：需要逐步生成（改编前后设定对比-注意是原书和最终版的对比、英雄之旅框架-详细、特色亮点、书籍标签、基础信息）
7. **生成新版故事大纲**：在上一版基础上，更新故事大纲


## 多章情节调整
> **问题：**情节的调整也是必然会发生的，通常需要调相邻多章才能保证情节的流畅。在哪一步调？怎么调？小白能处理吗？  
> **前置信息**：大纲、章纲、人物小传   
> **【假想】在哪一步调？**：在出新章纲之后，基于章纲进行调整   
> **【假想】上游需要跟着调吗？**：需要，大纲和人物小传都需要更新   
> **【假想】调整流程**：  
1. **选定章节**：选定需要调整的章节或章节范围
2. 给出调整方向：现在是什么情节，想改为什么情节；用100字左右描述清楚
3. 






## Reference
- 
