---
layout: article
title:  "关于使用GitHub desktop的心得笔记"
date:   2018-01-10 22:07:50 +0800
categories: posts rwd
image:
  teaser: GitHub-desktop.jpg
  feature: GitHub-desktop.jpg
---

关于使用GitHub desktop的方法笔记

{% include toc.html %}

## 如何安装 GitHub Desktop？
1. 拥有一个GitHub账号，[点击此处进行注册](https://github.com/join?source=header-home)
2. 去[GitHub Desktop](https://desktop.github.com/)下载GitHub桌面版客户端

## 初次打开GitHub Desktop？ 

- 登陆账号。
	1. 打开GitHub Desktop
	2. 点击file -> options -> 填入自己的信息
- 选择存放路径。(这是非常非常重要的！！画重点！！)我选择的路径是 E:\ (建议放在你熟悉的盘，别乱设置，免得以后找不到；同时最好不要放在C盘，C盘是系统盘，下载的东西最好都不要放在里面)

## 怎样使用 GitHub desktop？

##### 新建一个repository
- 点击File-New repository,接着会出现以下框框。
![github1.PNG](https://i.loli.net/2018/01/03/5a4c9fd1becf1.png)
- 勾选的意思是要不要创建一个README.md文档，此文档的内容将在你的GitHub的这个[repository](https://github.com/CherryLiChan/CherryLiChan.github.io)里呈现
![githubdesktop.PNG](https://i.loli.net/2018/01/03/5a4ca02a3b04f.png)

##### 复制别人的repository，并且在本地端打开
- 想从网站上复制一个别人的repository，并且能在本地端修改？
	1. 在[GitHub官网](https://github.com/)上找到你想要复制的repository，如[本博客的原始repository](https://github.com/mmistakes/skinny-bones-jekyll)
	2. 点击绿色按钮**clone and download**
	3. 接着点击：（1）**open in desktop：**在GitHub desktop打开；（2）**download zip：**下载这个repository的压缩包到你的电脑上
	4. 在图片的位置输入。等待一小会，成功，你就可以在你存放的位置看到这个文件。
![github5.PNG](https://i.loli.net/2018/01/03/5a4ca07477532.png)

##### 打开本地文件
如果你忘了存放的位置，可以通过GitHub desktop的 repository -> show in explorer 打开

##### 同步到网站上
- 想在本地端修改后，把它更新到网站上？
	1. 打开 GitHub desktop
	2. 在 **change** 处选择你要同步的内容
	3. 为本次commit起个名字(summary),描述你做了什么(description)
	4. 点击 commit to master -> Fetch origin 上传，小圈圈转啊转，转完之后大功告成了，你github网站上就是最新的版本了。

##### 切换其他的repository
- 想切换其他的repository来修改？
	1. 点击current repository
	2. 选择你想切换的 repository 即可

## 小帮助
- [一个文科妹子分享了其半年摸索才明白的经验](https://www.zhihu.com/question/20070065 )
- [GitHub help](https://help.github.com/)

转载请注明：[黎婵的博客](https://cherrylichan.github.io/) » [点击阅读原文](https://cherrylichan.github.io/posts/rwd/关于使用GitHub desktop的心得笔记/)
