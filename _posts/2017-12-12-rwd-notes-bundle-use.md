---
layout: post
title: 用Bundler管理gem
date: 2017-12-12 00:00:00 +0800
description: Bundler通过跟踪和安装所需的gem版本，为Ruby项目提供一致的环境。
img: bundler.png
categories: rwd
---
# Ruby bundle

## Bundle介绍：
Rails 3中引入Bundle来管理项目中所有gem依赖，该命令只能在一个含有Gemfile的目录下执行。

## Bundle命令详解：
附，[Ruby bundle命令详解][Ruby bundle命令详解]

[Ruby bundle命令详解]: http://blog.csdn.net/dazhi_100/article/details/41987347

## 问题
bundle update和bundle install的区别：

bundle update会去相应的源检查Gemfile里gem的更新，然后对比Gemfile.lock文件，如果Gemfile里没有指定版本或是指定是>=的版本，就会去相应的源下载并安装新版本的gem，然后更新Gemfile.lock文件。

bundle install会先检查Gemfile.lock文件以及里边的相关依赖，然后为本地系统安装Gemfile.lock文件中指定的版本，接着去检查Gemfile中有而Gemfile.lock中没有的，然后安装。bundle install好像不会去检查相关源中Gem版本的更新。