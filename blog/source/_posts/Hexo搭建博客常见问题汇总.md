---
title: Hexo搭建博客常见问题汇总
date: 2018-05-08 18:02:16
tags: [随笔,Hexo]
---
虽然现在早就不再是博客的时代了，但是一直都想搭个自己的博客网站，有个专属自己地方能分享记录自己的思考，资源和学习成果，可以把琐碎的东西总结归纳然后写出来。刚好GitHub可以免费提供服务器，就百度了下Github博客搭建，网上很多Hexo+Github搭建博客的文章。如题，这篇文章的目的并不是讲解如何搭建一个Hexo博客，而是记录我在搭建博客过程中遇到的问题，并给出我的解决方法。 

## 前期工作
### [node.js安装](https://nodejs.org/en/download/current/)
### [Git安装](https://git-scm.com/downloads)
### [Github账户注册](https://github.com/)
### [软件安装完成可以参考这篇文章检查下是否正确](https://www.cnblogs.com/fengxiongZz/p/7707219.html)

## 常见问题
### 问题1
Github账户注册和新建项目，项目必须要遵守格式：账户名.github.io，不然接下来会有很多麻烦。并且需要勾选Initialize this repository with a README
![icon1](https://ws1.sinaimg.cn/large/d7c2c7e3gy1fr42d7typtj20y00kmmyb.jpg)
### 问题2
绑定域名,要使用SSH而不要用Https。打开Github，点击Downloader可以得到下面的地址。
![icon2](https://ws1.sinaimg.cn/large/d7c2c7e3gy1fr42g08f8mj20i307odg5.jpg)
修改_config.yml
![icon3](https://ws1.sinaimg.cn/large/d7c2c7e3gy1fr42i9lbfjj20ge041mx2.jpg)
### 问题3
输入cd ~/.ssh，检查不到.ssh的文件夹。我卡在这好久，以为什么东西没有安装好。后来发现，要在Desktop下生成才可以，在Hexo下无效。
具体可以参考[Git /.ssh](https://blog.csdn.net/meimeilive/article/details/80076394)

回看一下好像也没什么难的，一步步按着教程来就可以了，有什么不懂的网上查一下就OK了。

