---
layout: post
title: windows下安装及使用Ruby时遇到的一些问题及解决方法
date: 2017-12-01 00:00:00 +0800
description: 安装Ruby出现的状况及解决方法
img: ruby.png
categories: rwd
---
# 一、版本问题

截止我安装时,windows下最新版本为`Ruby2.3`，再帮别人安装发现我原来的方法不好用，经过了一番折腾了解到不同版本的安装略有不同

看官网2.4版本与之前2.3的版本的安装是有点差异的：
* 2.3版本的需要下载RubyInstaller和DevKit-mingw64
* 2.4版本之后，需要安装RubyInstaller和MSYS2 toolkit

请看[原文][原文]：

[原文]: https://rubyinstaller.org/downloads/

> WHICH DEVELOPMENT KIT?  
> Starting with Ruby 2.4.0 we use the MSYS2 toolkit as our development kit. It is required to build native C/C++ extensions for Ruby and is necessary for Ruby on Rails. Moreover it allows the download and usage of hundreds of Open Source libraries which Ruby gems can depend on.  
> Down this page, several and other versions of Development Kits (DevKit) are listed. Please download the right one for your version of Ruby:
> * Ruby 2.4.0 and newer: The MSYS2 DevKit is downloaded as the last step of the installation. It can be installed later per ridk install command.
> * Ruby 2.0.0 to 2.3.x (32bits): mingw64-32-4.7.2
> * Ruby 2.0.0 to 2.3.x (64bits): mingw64-64-4.7.2

## 1. 安装2.3及之前版本（DevKit的安装）
下载安装包，双击下载文件，指定解压路径，路径中不能有空格。如C:\DevKit。

解压完毕后进入到加压文件的命令行目录，输入命令ruby dk.rb init

再输入命令ruby dk.rb install

安装完成

## 2. 安装2.4及之后版本（MSYS2的安装）
下载RubyInstaller打开安装，安装最后会弹出一个cmd窗口，就是用来安装MSYS2的，`输入3`

MSYS2安装过程比较顺利，但是还没完，看MSYS2官网，安装后还需要升级一下核心的包。请看官网的[安装指南][安装指南]。这里不过多叙述。

[安装指南]: http://www.msys2.org/

# 二、安装模块
安装完对应版本的Ruby后可以先打开命令行，检查一下ruby的包管理器gem的安装:

```
C:\Users\Blackfood>gem -v
2.6.14
```
安装模块的过程类似python，`gem install [模块名]`，可见[老师教程][老师教程]

另附 [gem命令行详解][gem命令行详解]

[老师教程]: https://hanteng.github.io/notes_tech/jekyll/Ruby/

[gem命令行详解]: https://www.jianshu.com/p/728184da1699

# 三、其它
## Ruby中国镜像
### 为什么
>RubyGems 一直以来在国内都非常难访问到，在本地你或许可以翻墙，当你要发布上线的时候，你就很难搞了！
>这是一个完整 RubyGems 镜像，你可以用此代替官方版本，我们是完全基于 CDN 技术来实现，能确保几乎无延迟的同步。https://gems.ruby-china.org/

### 如何使用
```
$ gem sources --add https://gems.ruby-china.org/ --remove https://rubygems.org/
$ gem sources -l
https://gems.ruby-china.org
# 确保只有 gems.ruby-china.org
```