---
layout: article
title:  "关于搭建此博客的那些事儿"
date:   2017-12-02 21:14:24 +0800
categories: posts rwd
image:
  teaser: 搭建博客.jpg
  feature: 搭建博客.jpg
---

本文是我搭建此博客的一些笔记，多方面参考后的成果，如有不足，欢迎指正。

{% include toc.html %}

## Ruby

- Ruby是一种纯粹的面向对象编程语言，是"程序员的最佳朋友"。
- Ruby 的特性与 Smalltalk、Perl 和 Python 类似。Perl、Python 和 Smalltalk 是脚本语言。Smalltalk 是一个真正的面向对象语言。Ruby，与 Smalltalk 一样，是一个完美的面向对象语言。使用 Ruby 的语法比使用 Smalltalk 的语法要容易得多。

#### 安装Ruby

1. 点击下载安装下载包：[rubyinstaller-2.4.2-2-*64.exe](http://www.ruby-lang.org/en/downloads/) 
2. 按顺序依次1、2、3，分别安装
3. 完成安装后，点击键盘：win+R
4. 输入PowerShell并回车打开
5. 在Powershell界面输入“gem install bundle”
6. 输入 gem install jekyll


#### 相关教程：
- [菜鸟教程里ruby的教程](http://www.runoob.com/ruby/ruby-tutorial.html)
- [Ruby China](https://ruby-china.org/)
- [ruby rails girl](http://railsgirls.com/)

## Jekyll

- Jekyll 是一个简单的博客形态的静态站点生产机器。它有一个模版目录，其中包含原始文本格式的文档，通过 Markdown （或者 Textile） 以及 Liquid 转化成一个完整的可发布的静态网站，你可以发布在任何你喜爱的服务器上。Jekyll 也可以运行在 GitHub Page 上，也就是说，你可以使用 GitHub 的服务来搭建你的项目页面、博客或者网站，而且是完全免费的

- 使用 Jekyll 搭建博客之前要确认下本机环境，Git 环境（用于部署到远端）、[Ruby](http://www.ruby-lang.org/en/downloads/) 环境（Jekyll 是基于 Ruby 开发的）、包管理器 [RubyGems](http://rubygems.org/pages/download)                
	- 如果你是 Mac 用户，你就需要安装 Xcode 和 Command-Line Tools了。下载方式 Preferences → Downloads → Components。

- Jekyll 是一个免费的简单静态网页生成工具，可以配合第三方服务例如： Disqus（评论）、多说(评论) 以及分享 等等扩展功能，Jekyll 可以直接部署在 Github（国外） 或 Coding（国内） 上，可以绑定自己的域名。[Jekyll中文文档](http://jekyll.bootcss.com/)、[Jekyll英文文档](https://jekyllrb.com/)、[Jekyll主题列表](http://jekyllthemes.org/)。

- 使用了 Jekyll 你会发现如果你想使用多台电脑发博客都很方便，只要把远端 github 仓库里的博客 clone 下来，写文章后再提交就可以了，
	
- jekyll的目录结构以及具体的作用可以参考 [官网文档](http://jekyll.com.cn/docs/structure/) 
	
- [jekyll在GitHub上的链接](https://github.com/jekyll)
	
#### 安装 jekyll

```     
$ gem install jekyll     
```    

创建博客

```    
$ jekyll new myBlog    
```   

进入博客目录

```
$ cd myBlog  
```

启动本地服务

```
$ jekyll serve
```

在浏览器里输入： [http://localhost:4000](http://localhost:4000)，就可以看到你的博客效果了。

![](/images/image1.png)

so easy !

下载安装好后进入文档的 **_config.yml** 里面，修改成你想看到的信息，重新 jekyll server ，刷新浏览器就可以看到你刚刚修改的信息了。

到此，博客初步搭建算是完成了，

## GitHub

- 博客部署到远端的一种方法及其必要工具。
	
- 这里讲的是部署到 Github Page 创建一个 github 账号，然后创建一个跟你账户名一样的仓库，如我的 github 账户名叫 [cherrylichan](https://github.com/cherrylichan)，我的 github 仓库名就叫 [cherrylichan.github.io](https://github.com/cherrylichan/cherrylichan.github.io)，创建好了之后，把刚才建立的 myBlog 项目 push 到 username.github.io仓库里去（username指的是你的github用户名），检查你远端仓库已经跟你本地 myBlog 同步了，然后你在浏览器里输入 username.github.io ，就可以访问你的博客了。

## 编写文章

- 所有的文章都是 _posts 目录下面，文章格式为 mardown 格式，文章文件名可以是 .mardown 或者 .md。

- 编写一篇新文章很简单，你可以直接从 _posts/ 目录下复制一份出来 `2018-01-03-增加打赏功能.md` ，修改名字为 2017-12-03-jekyll_skinny-bones.md ，注意：文章名的格式前面必须为 2016-10-16- ，日期可以修改，但必须为 年-月-日- 格式，后面的 article1 是整个文章的连接 URL，如果文章名为中文，那么文章的连接URL就会变成这样的：https://cherrylichan.github.io/posts/rwd/%E5%A2%9E%E5%8A%A0%E6%89%93%E8%B5%8F%E5%8A%9F%E8%83%BD/#%E6%96%B9%E6%B3%95%E4%B8%80 ， 所以建议文章名最好是英文的或者阿拉伯数字。 


- 双击 2017-12-03-jekyll_skinny-bones.md 打开

```
---
layout: XX布局（如此文里的article）
title:  "XX标题"
date:   年-月-日- 时:分:秒 +0800
categories: nav分类（如infovis）等
image:
  teaser: XX.jpg（png/svg/gif等）
  feature: XX.jpg（png/svg/gif等）
---

正文
...

```

**title:** 显示的文章名， 如：title: 我的第一篇文章                    
**date:**  显示的文章发布日期，如：date: 2016-10-16                          
**categories:** 导航分类，如：categories: infovis
**layout:**  文章使用的布局，如：layout: article
**image:**  显示的图片

**注意：** 文章头部格式必须为上面的，.... 就是文章的正文内容。

我写文章使用的是 **Sublime Text2 编辑器**，如果你对 markdown 语法不熟悉的话，可以看看[作业部落的教程](https://www.zybuluo.com/) 


## 使用我的博客模板

虽然博客部署完成了，你会发现博客太简单不是你想要的，如果你喜欢我的模板的话，可以使用我的模板。

首先你要获取的我博客，[Github项目地址](https://github.com/cherrylichan/cherrylichan.github.io.git)，你可以直接[点击下载博客](https://github.com/cherrylichan/cherrylichan.github.io/archive/master.zip)，进去cherrylichan.github.io/ 目录下， 使用命令部署本地服务 

```
$ jekyll server   
```

## 如果你本机没配置过任何jekyll的环境，可能会报错

```
/Users/xxxxxxxx/.rvm/rubies/ruby-2.2.2/lib/ruby/site_ruby/2.2.0/rubygems/core_ext/kernel_require.rb:54:in `require': cannot load such file -- bundler (LoadError)
	from /Users/xxxxxxxx/.rvm/rubies/ruby-2.2.2/lib/ruby/site_ruby/2.2.0/rubygems/core_ext/kernel_require.rb:54:in `require'
	from /Users/xxxxxxxx/.rvm/gems/ruby-2.2.2/gems/jekyll-3.3.0/lib/jekyll/plugin_manager.rb:34:in `require_from_bundler'
	from /Users/xxxxxxxx/.rvm/gems/ruby-2.2.2/gems/jekyll-3.3.0/exe/jekyll:9:in `<top (required)>'
	from /Users/xxxxxxxx/.rvm/gems/ruby-2.2.2/bin/jekyll:23:in `load'
	from /Users/xxxxxxxx/.rvm/gems/ruby-2.2.2/bin/jekyll:23:in `<main>'
	from /Users/xxxxxxxx/.rvm/gems/ruby-2.2.2/bin/ruby_executable_hooks:15:in `eval'
	from /Users/xxxxxxxx/.rvm/gems/ruby-2.2.2/bin/ruby_executable_hooks:15:in `<main>'

```

原因： 没有安装 bundler ，执行安装 bundler 命令

```

$ gem install bundler

```


提示： 

```
Fetching: bundler-1.13.5.gem (100%)
Successfully installed bundler-1.13.5
Parsing documentation for bundler-1.13.5
Installing ri documentation for bundler-1.13.5
Done installing documentation for bundler after 5 seconds
1 gem installed

```

再次执行 $ jekyll server  ，提示

```

Could not find proper version of jekyll (3.1.1) in any of the sources
Run `bundle install` to install missing gems.

```

跟着提示运行命令

```
$ bundle install
```

这个时候你可能会发现 bundle install 运行卡主不动了。

如果很长时间都没任何提示的话，你可以尝试修改 gem 的 source

```
$ gem sources --remove https://rubygems.org/
$ gem sources -a http://ruby.taobao.org/
$ gem sources -l
*** CURRENT SOURCES ***

http://ruby.taobao.org

```

再次执行命令 $ bundle install，发现开始有动静了

```
Fetching gem metadata from https://rubygems.org/...........
Fetching version metadata from https://rubygems.org/..
Fetching dependency metadata from https://rubygems.org/.
。。。
Installing jekyll-watch 1.3.1
Installing jekyll 3.1.1
Bundle complete! 3 Gemfile dependencies, 17 gems now installed.
Use `bundle show [gemname]` to see where a bundled gem is installed.

```

bundler安装完成，后再次启动本地服务 

```
$ jekyll server

```

继续报错

```
Configuration file: /Users/tendcloud-Caroline/Desktop/cherrylichan.github.io/_config.yml
  Dependency Error: Yikes! It looks like you don't have jekyll-sitemap or one of its dependencies installed. In order to use Jekyll as currently configured, you'll need to install this gem. The full error message from Ruby is: 'cannot load such file -- jekyll-sitemap' If you run into trouble, you can find helpful resources at http://jekyllrb.com/help/! 
jekyll 3.1.1 | Error:  jekyll-sitemap

```
表示 当前的 jekyll 版本是 3.1.1 ，无法使用 jekyll-sitemap 

解决方法有两个

1. 打开当前目录下的 _config.yml 文件，把 gems: [jekyll-paginate,jekyll-sitemap] 换成 gems: [jekyll-paginate] ，也就是去掉jekyll-sitemap。

2. 升级 jekyll 版本，我当前的是 jekyll 3.1.2 。

修改完成后保存配置，再次执行

```
$ jekyll server

```
提示

```
Configuration file: /Users/baixinpan/Desktop/OpenSource/Mine/Page-Blog/cherrylichan.github.io-github/_config.yml
            Source: /Users/baixinpan/Desktop/OpenSource/Mine/Page-Blog/cherrylichan.github.io-github
       Destination: /Users/baixinpan/Desktop/OpenSource/Mine/Page-Blog/cherrylichan.github.io-github/_site
 Incremental build: disabled. Enable with --incremental
      Generating... 
                    done in 0.901 seconds.
 Auto-regeneration: enabled for '/Users/baixinpan/Desktop/OpenSource/Mine/Page-Blog/cherrylichan.github.io-github'
Configuration file: /Users/baixinpan/Desktop/OpenSource/Mine/Page-Blog/cherrylichan.github.io-github/_config.yml
    Server address: http://127.0.0.1:4000/
  Server running... press ctrl-c to stop.

```

表示本地服务部署成功。

在浏览器输入 [127.0.0.1:4000](127.0.0.1:4000) ， 就可以看到[cherrylichan.io](http://cherrylichan.io)博客效果了。

## 修改成你自己的博客

* 如果你想使用我的模板请把 _posts/ 目录下的文章都去掉。
* 修改 _config.yml 文件里面的内容为你自己的。

然后使用 git push 到你自己的仓库里面去，检查你远端仓库，在浏览器输入 username.github.io 就会发现，你有一个漂亮的主题模板了。      

## 关于本博客的头文件说明
#### Portfolio  Web作品集

```
---
layout: article
title:  "XX"
date:   2017-9-13 0:49:50 +0800
categories: portfolio
image:
  teaser: XX.png
  feature: XX.png
---
```

#### Infovis  信息可视化作品集

```
---
layout: article
title:  "AAA"
date:   2017-9-29 22:07:50 +0800
categories: infovis visualization
image:
  teaser: AAA.png
  feature: AAA.png
---
```

#### posts/rwd  Web笔记

```
---
layout: article
title:  "BBB"
date:   2017-12-01 22:07:50 +0800
categories: posts rwd
image:
  teaser: BBB.svg
  feature: BBB.svg
---
```

#### posts/infovis  信息可视化笔记

```
---
layout: article
title:  "CCC"
date:   2018-1-3 14:01:50 +0800
categories: posts infovis
image:
  teaser: CCC.png
  feature: CCC.png
---
```

## “总览”效果：
```
{% include toc.html %}
```

<br>
转载请注明：[黎婵的博客](https://cherrylichan.github.io/) » [点击阅读原文](https://cherrylichan.github.io/posts/rwd/first-step/)
