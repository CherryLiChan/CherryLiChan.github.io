---
layout: article
title:  "装Jekyll主题Skinny Bones"
date:   2017-12-03 08:45:50 +0800
categories: posts rwd
image:
  teaser: Jekyll_skinny_bones.jpg
  feature: Jekyll_skinny_bones.jpg
---

## 本文是对搭建整个博客的声明，极有意义，故保留（文末有声明文章来源）

Jekyll 有不少第三方开发的主题可以用，这篇文章简介[Skinny Bones](https://github.com/mmistakes/skinny-bones-jekyll)。

{% include toc.html %}

## 为何选 Skinny Bones

Jekyll 有不少第三方开发的主题可以用，功能简单的到齐全的都有，这篇文章简单介绍一个难易适中的主题[Skinny Bones](https://github.com/mmistakes/skinny-bones-jekyll)做个起头。

之所以采用Michael Rose所设计的主题样式理由不少，其中包括他所有的样式都可以在[Github](https://github.com/)使用，他设计的这些作品多以开源MIT授权释出，所以若觉得好用，可以[在此鼓励他](https://mademistakes.com/support/)

设计师Michael Rose[他自己总结Skinny Bones 主题的特点](https://mademistakes.com/work/skinny-bones-jekyll/)有

- 兼容 GitHub Pages 页面  <br/> GitHub Pages compatible.
- 使用 "Sass" 构建的样式表可以轻松地帮助您的网站主题。需要Jekyll 2.x。<br/> Stylesheets built using Sass to help theme your site with ease. Requires Jekyll 2.x
- 使用数据文件, 便于自定义站点导航/页脚和支持多个作者。<br/> Data files for easier customization of the site navigation/footer and for supporting multiple authors.
- 含可选功能如 Disqus 评论, 目录, 社会共享链接, 和谷歌 AdSense 广告。<br/> Optional Disqus comments, table of contents, social sharing links, and Google AdSense ads.

## 如何用 Skinny Bones

Skinny Bones 的主题官网在Github Page上[mmistakes.github.io/skinny-bones-jekyll](https://mmistakes.github.io/skinny-bones-jekyll/getting-started/),有两种安装方式，一种是全新安装，另一种是对已有的Jekyll进行换主题的安装教程。

由於我打算就是要在Github 的个人页面使用重建一个新的Jekyll个人站点，我直接采取安装教程的第一个方案，步骤如下：

1. 直接 fork/clone [mmistakes/skinny-bones-jekyll](https://github.com/mmistakes/skinny-bones-jekyll)，这相当於安装教程第一个方案中的第1步
2. 在自己的项目hanteng/skinny-bones-jekyll改名成hanteng/hanteng.github.io，这相当於安装教程第一个方案中的第2步，并使用Github Desktop 下载至本地端 
3. 运行捆绑安装```bundle install```, 安装Jekyll和其所依赖的模块。
4. 更新 项目根目录中yml设定档```_config.yml```内容丶增加导航navigation丶增加文章/页面，如[我这里的编修Commit](https://github.com/hanteng/hanteng.github.io/commit/cf9691a940e8d9527d64553501a90991e9c5f1ab)

若你是第一次使用Jekyll，可以分别在本地和Github远端测试是否能正确运行：

## 本地运行测试
首先要确立你的Github项目在本地的路径，可在Github Desktop 中，先选定该项目，再点选菜单Repository，再点选其中的Show in Explorer，就可以查到你放哪了。

- 使用Ruby命令列，切换至该目录如```cd C:\Users\me\Documents\GitHub\hanteng.github.io```
- 执行捆绑执行```bundle exec jekyll serve```把jekyll 伺服器执行

执行效果如：
<pre class="highlight"><code>C:\Users\Hante\Documents\GitHub\hanteng.github.io>bundle exec jekyll serve
Configuration file: C:/Users/me/Documents/GitHub/hanteng.github.io/_config.yml
            Source: C:/Users/me/Documents/GitHub/hanteng.github.io
       Destination: C:/Users/me/Documents/GitHub/hanteng.github.io/_site
 Incremental build: disabled. Enable with --incremental
      Generating...
                    done in 1.64 seconds.
  Please add the following to your Gemfile to avoid polling for changes:
    gem 'wdm', '>= 0.1.0' if Gem.win_platform?
 Auto-regeneration: enabled for 'C:/Users/me/Documents/GitHub/hanteng.github.io'
Configuration file: C:/Users/me/Documents/GitHub/hanteng.github.io/_config.yml
    Server address: http://127.0.0.1:4000/
  Server running... press ctrl-c to stop.
</code></pre>

看到```Server running``` 字样代表运行成功，可以在```Server address```上执行使用，也就是在本地开一个浏览器输入该URL地址（上述為 ```http://127.0.0.1:4000/```）查看站点执行状况。

转载自：[廖汉腾老师的博客](https://hanteng.github.io/) » [点击阅读原文](https://hanteng.github.io/notes_tech/jekyll/jekyll_skinny-bones/)
