---
layout: post
title: 信息可视化期末专案
date: 2018-01-06 17:49:20 +0300
description: 经常旅行的人一定非常关心酒店的好坏，下面用了两张图表来分析全国各大连锁酒店的评分
img: 
categories: infovis
---

## 酒店在全国六大地区的分布状况，评分状况，GDP之间的关系
出门在外，很多人都会住快捷酒店，在国内快捷酒店的品牌有很多，我用高德地图搜索了六个关键词：`7天` `汉庭` `如家` `莫泰` `锦江之星` `速8`，找到约5000笔数据。

----

### 六个快捷酒店在全国六大地区的分布

<iframe src="https://public.tableau.com/views/_18800/sheet2?:embed=y&:display_count=yes&publish=yes&publish=yes/Dashboard1?:showVizHome=no&:embed=true" height="600px" width="800px" scrolling="no" frameborder="0"></iframe>

----

### 六个快捷酒店在全国六大地区的占比

圆饼图，从六大地区分别酒店数量占比看出各个品牌在不同地区的投入侧重。比如：速8酒店在西北地区的数量占33%，而在华东地区的数量只占14%，由此可见速8酒店在西北投入力度较大

<iframe src="https://public.tableau.com/views/_18800/1?:embed=y&:display_count=yes&publish=yes&publish=yes/Dashboard1?:showVizHome=no&:embed=true" height="600px" width="800px" scrolling="no" frameborder="0"></iframe>

----

### 快捷酒店的数量及评分状况与地区经济（GDP）的相关性分析

我想知道，会不会一个地方的经济越发达，快捷酒店的数量就越多

在搜索数据的时候，我提出了以下问题：
- 快捷酒店的数量是否与经济发达程度有关？
- 酒店评分高低是否与经济发达程度有关有关？

<iframe src="https://public.tableau.com/views/_18800/GDP_2?:embed=y&:display_count=yes&publish=yes&publish=yes&publish=yes/Dashboard1?:showVizHome=no&:embed=true" height="600px" width="800px" scrolling="no" frameborder="0"></iframe>

----

## 结论

- 华东地区的酒店最多。
- 各大酒店在不同地区的投入侧重是不同的，但不是所有酒店都在华东地区数量最多。
- 地区的GDP也不是影响酒店数量的绝对因素，在GDP最高的华北地区，酒店数量只有GDP第二高的华东地区的三分之一。
- 评分和GDP呈比较明显的正相关，也就是GDP越高评分越高，评分虽有高低，差距并不大。

**数据来源**：高德地图，国家数据网