---
title: APK反编译
date: 2018-05-09 10:25:48
tags: [随笔,android]
categories: Android开发
---
在学习Android开发的过程你，你往往会去借鉴别人的应用是怎么开发的，那些漂亮的动画和精致的布局可能会让你爱不释手，作为一个开发者，你可能会很想知道这些效果界面是怎么去实现的。这时，你便可以对改应用的APK进行反编译查看。

## 下载工具：
### [apkTool下载地址](https://bitbucket.org/iBotPeaches/apktool/downloads/)
### [dex2jar下载地址](https://sourceforge.net/projects/dex2jar/files/)
### [jd-gui下载地址](http://jd.benow.ca/)

### 工具介绍：
    apktool作用：资源文件获取，可以提取出图片文件和布局文件进行使用查看
    dex2jar作用：将apk反编译成java源码（classes.dex转化成jar文件）
    jd-gui作用：查看APK中classes.dex转化成出的jar文件，即源码文件
 ![icon](https://ws1.sinaimg.cn/large/d7c2c7e3gy1fr4xqm4ingj20o9068mxc.jpg)
 
## 反编译流程
### 获取资源文件
    将需要反编译的APK文件放到apktool文件夹下，打开命令行界面（运行-CMD） ，输入以下命令：java -jar apktool.jar d -f 1.apk
![icon1](https://ws1.sinaimg.cn/large/d7c2c7e3gy1fr4xminol8j20k50b0gmf.jpg)  
 
    可以得到一个叫1的文件夹，打开后就是我们想要的资源文件
![icon2](https://ws1.sinaimg.cn/large/d7c2c7e3gy1fr4xhpss7uj20lp08ht99.jpg)

### 获取代码
    将要反编译的APK后缀名改为.rar或者 .zip，并解压，得到其中的classes.dex文件（它就是java文件编译再通过dx工具打包而成的），如下图所示：
![icon3](https://ws1.sinaimg.cn/large/d7c2c7e3gy1fr4xs4nh7ej20lp08ht99.jpg)
    
    将获取到的classes.dex放到之前解压出来的工具【dex2jar-2.0】文件夹内，如下图所示:
![icon4](https://ws1.sinaimg.cn/large/d7c2c7e3gy1fr4xueaumtj20rp0gagnu.jpg)

    在命令行下定位到dex2jar.bat所在目录，输入"d2j-dex2jar classes.dex"，效果如下：
![icon4](https://ws1.sinaimg.cn/large/d7c2c7e3gy1fr4y3by0ujj20eh05n0ss.jpg)

    dex2jar.bat classes.dex时，dex2jar.bat不是本地或外部命令。需要将dex2jar.bat加入到环境变量中。如下图：
 ![icon5](https://ws1.sinaimg.cn/large/d7c2c7e3gy1fr4y5u4vbkj20ah05fq2v.jpg)
 
    运行jd_gui打开刚刚生成的classes-dex2jar.jar就能看到代码。如下图：
 ![icon6](https://ws1.sinaimg.cn/large/d7c2c7e3gy1fr4y8oeps5j20vx0fedhf.jpg)
 
 ## 反编译软件Android Killer
    以上就“Android反编译”比较传统的教程。刚接触反编译的时候，我也是从这些教程慢慢学起的。在后来的学习过程中，我接触到比较方便操作的Android反编译。在这，我将使用的过程写下来，贡献给有需的朋友。
    我推荐大家使用的Android反编译的软件是Android Killer。
    其实这个软件就是对以上博客提到的操作进行一系列的封装。打开这个软件你就可以发现这些熟悉的反编译工具。
[Android Killer下载地址](http://ftp-new-pc.pconline.com.cn/bf00342cab8742714a0d8ca5b4b96ca5/pub/download/201010/pconline1483963572680.zip)
    
    下载后直接运行exe就可以了，操作十分简便。这软件还有好多功能，在这不一一列出了，有兴趣的朋友自己慢慢摸索。