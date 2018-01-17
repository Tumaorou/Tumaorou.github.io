---
layout: post
title: "+_+ 编码错误？仿佛回到Python"
date: 2018-01-01 20:32:20 +0300
img: gbk.jpg
description: 为什么下载了一个外国人做的模版会出现GBK的编码错误，难道是我用的中国的电脑吗
categories: rwd
---
## 错误如下： 
`Error:  incompatible character encodings: GBK and UTF-8`

这啥？encoding？

一位知乎老哥的解释：
>你的项目名或者样式文件名可能带有**中文**，检查一下是否有**中文**的命名！~

于是把文件夹所有的东西找遍了都没见到一个中国字，甚至改了Ruby的配置文件，还是显示编码错误。好不容易找到一个漂亮的主题难道就这么认栽吗

---

## 解决方法
哪里有中文呢，在我百思不得其解之时，突然想到

`C:\Users\学生\Desktop\Tumaorou.github.io`

原来是文件目录里的用户名是中文的，于是把文件移到英文目录下问题就解决了