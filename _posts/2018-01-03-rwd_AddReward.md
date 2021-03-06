---
layout: article
title:  "增加打赏功能"
date:   2018-01-03 21:14:24 +0800
categories: posts rwd
image:
  teaser: reward.jpg
  feature: reward.jpg
---
为网站增加打赏功能
本文将讲解如何创建支付宝/微信打赏功能的问题

{% include toc.html %}

![打赏功能1](/images//show.gif)

## 方法一

这个例子只是简单的使用了几张二维码图片实现打赏功能，没法显示有哪些人打赏了，所以有获知哪些人打赏的需求的读者们慎选

如果你想要实现我博客里的打赏功能，你可以参考我 在GitHub网站上的库CherryLiChan.github.io- 里的[_includes/new-old.html](https://github.com/CherryLiChan/CherryLiChan.github.io-/blob/master/_includes/new-old.html) 文件里面相应的代码。

#### 1.添加HTML文档
在_includes文档下添加一个名为"external"的HTML文档,并在这个文档里填入代码
```
<script>hljs.initHighlightingOnLoad();</script>
```

#### 2.填入html代码
```
            <div class="content-play">
              <p><a href="javascript:void(0)" onclick="dashangToggle()" class="dashang" title="打赏，支持一下">打赏一个呗</a></p>
              <div class="hide_box-play"></div>
              <div class="shang_box-play">
                <a class="shang_close-play" href="javascript:void(0)" onclick="dashangToggle()" title="关闭"><img src="/images/payimg/close.jpg" alt="取消" /></a>
                <div class="shang_tit-play">
                  <p>感谢您的支持，我会继续努力的!</p>
                </div>
                <div class="shang_payimg">
                    <img src="/images/payimg/alipayimg.jpg" alt="扫码支持" title="扫一扫" />
                </div>
              <div class="shang_payimg">    
                    <img src="/images/payimg/weipayimg.jpg" alt="扫码支持" title="扫一扫" />
                </div>
                <div class="pay_explain">扫码打赏，你说多少就多少</div>
                <div class="shang_payselect">
                  <div class="pay_item checked" data-id="alipay">
                    <span class="pay_logo"><img src="/images/payimg/alipay.jpg" alt="支付宝" /></span>
                  </div>
                  <div class="pay_item" data-id="weipay">
                    <span class="pay_logo"><img src="/images/payimg/wechat.jpg" alt="微信" /></span>
                  </div>
                </div>
                <div class="shang_info-play">
                  <p>打开<span id="shang_pay_txt">支付宝</span>扫一扫，即可进行扫码打赏哦</p>
                </div>
              </div>
            </div>
            <script type="text/javascript">
            function dashangToggle(){
              $(".hide_box-play").fadeToggle();
              $(".shang_box-play").fadeToggle();
            }
            </script>

            <div style="text-align:center;margin:50px 0; font:normal 14px/24px 'MicroSoft YaHei';"></div>

            <style type="text/css">
              .content-play{width:80%;margin-top: 20px;margin-bottom: 10px;height:40px;}
              .hide_box-play{z-index:999;filter:alpha(opacity=50);background:#666;opacity: 0.5;-moz-opacity: 0.5;left:0;top:0;height:99%;width:100%;position:fixed;display:none;}
              .shang_box-play{width:540px;height:540px;padding:10px;background-color:#fff;border-radius:10px;position:fixed;z-index:1000;left:50%;top:50%;margin-left:-280px;margin-top:-280px;border:1px dotted #dedede;display:none;}
              .shang_box-play img{border:none;border-width:0;}
              .dashang{display:block;width:100px;margin:5px auto;height:25px;line-height:25px;padding:10px;background-color:#E74851;color:#fff;text-align:center;text-decoration:none;border-radius:10px;font-weight:bold;font-size:16px;transition: all 0.3s;}
              .dashang:hover{opacity:0.8;padding:15px;font-size:18px;}
              .shang_close-play{float:right;display:inline-block;
                margin-right: 10px;margin-top: 20px;
              }
              .shang_logo{display:block;text-align:center;margin:20px auto;}
              .shang_tit-play{width: 100%;height: 75px;text-align: center;line-height: 66px;color: #a3a3a3;font-size: 16px;background: url('/images/payimg/cy-reward-title-bg.jpg');font-family: 'Microsoft YaHei';margin-top: 7px;margin-right:2px;}
              .shang_tit-play p{color:#a3a3a3;text-align:center;font-size:16px;}
              .shang_payimg{width:140px;padding:10px;padding-left: 80px; /*border:6px solid #EA5F00;**/margin:0 auto;border-radius:3px;height:140px;display:inline-block;}
              .shang_payimg img{display:inline-block;margin-right:10px;float:left;text-align:center;width:140px;height:140px; }
              .pay_explain{text-align:center;margin:10px auto;font-size:12px;color:#545454;}
              .shang_payselect{text-align:center;margin:0 auto;margin-top:40px;cursor:pointer;height:60px;width:500px;margin-left:110px;}
              .shang_payselect .pay_item{display:inline-block;margin-right:140px;float:left;}
              .shang_info-play{clear:both;}
              .shang_info-play p,.shang_info-play a{color:#C3C3C3;text-align:center;font-size:12px;text-decoration:none;line-height:2em;}
            </style>
```

#### 3.保存支付二维码到你保存的图像的文档

#### 4.修改1.中相应代码



## 方法二：
转载自caibaojian的文章[仿知乎专栏赞赏：支持支付宝和微信打赏](http://caibaojian.com/zanshang.html)

[范例](http://caibaojian.com/demo/2017/01/zanshang/)

下述代码为核心代码，喜欢这种打赏样式的同学只需要把打赏的二维码换成自己的就行了。

#### HTML代码：
```
<div class="entry-shang text-center">
	<p>「真诚赞赏，手留余香」</p>
	<button class="zs show-zs btn btn-bred">赞赏</button>
</div>
<div class="zs-modal-bg"></div>
<div class="zs-modal-box">
	<div class="zs-modal-head">
		<button type="button" class="close">×</button>
		<span class="author"><img src="http://cn.gravatar.com/avatar/cffb5aa78e9e9c53fd89cc8c3e59580b?d=identicon&r=G&s=80"/>前端博客</span>
		<p class="tip"><i></i><span>真诚赞赏，手留余香</span></p>

	</div>
	<div class="zs-modal-body">
		<div class="zs-modal-btns">
			<button class="btn btn-blink" data-num="2">2元</button>
			<button class="btn btn-blink" data-num="5">5元</button>
			<button class="btn btn-blink" data-num="10">10元</button>
			<button class="btn btn-blink" data-num="50">50元</button>
			<button class="btn btn-blink" data-num="100">100元</button>
			<button class="btn btn-blink" data-num="1">任意金额</button>
		</div>
		<div class="zs-modal-pay">
			<button class="btn btn-bred" id="pay-text">2元</button>
			<p>使用<span id="pay-type">微信</span>扫描二维码完成支付</p>
			<img src="images/alipay-2.png" id="pay-image"/>
		</div>
	</div>
	<div class="zs-modal-footer">
		<label><input type="radio" name="zs-type" value="alipay" class="zs-type" checked="checked"><span class="zs-alipay"><img src="images/alipay-btn.png"/></span></label>
		<label><input type="radio" name="zs-type" value="wechat" class="zs-type"><span class="zs-wechat"><img src="images/wechat-btn.png"/></span></label>
	</div>
</div>
```

#### JS代码：
```
function ZanShang(){
  this.popbg = $('.zs-modal-bg');
  this.popcon = $('.zs-modal-box');
  this.closeBtn = $('.zs-modal-box .close');
  this.zsbtn = $('.zs-modal-btns .btn');
  this.zsPay = $('.zs-modal-pay');
  this.zsBtns = $('.zs-modal-btns');
  this.zsFooter = $('.zs-modal-footer');
  var that = this;
  $('.show-zs').on('click',function(){
    //点击赞赏按钮出现弹窗
    that._show();
    that._init();
  })
}
ZanShang.prototype._hide = function(){
  this.popbg.hide();
  this.popcon.hide();
}
ZanShang.prototype._show = function(){
  this.popbg.show();
  this.popcon.show();
  this.zsBtns.show();
  this.zsFooter.show();
  this.zsPay.hide();
}
ZanShang.prototype._init = function(){
  var that = this;
  this.closeBtn.on('click',function(){
    that._hide();
  })
  this.popbg.on('click',function(){
    that._hide();
  })
  this.zsbtn.each(function(el){
    $(this).on('click',function(){
      var num = $(this).attr('data-num'); //按钮的对应的数字
      var type = $('.zs-type:radio:checked').val();//付款方式
      //根据不同付款方式和选择对应的按钮的数字来生成对应的二维码图片，你可以自定义这个图片的路径，默认放在当前images目录中
      //假如你需要加一个远程路径，比如我的就是
      //var src = 'http://caibaojian.com/wp-content/themes/blue/images/pay/'+type+'-'+num+'.png';
      var src = 'images/'+type+'-'+num+'.png';
      var text = $(this).html();
      var payType=$('#pay-type'), payImage = $('#pay-image'),payText = $('#pay-text');
      if(type=='alipay'){
        payType.html('支付宝');
      }else{
        payType.html('微信');
      }
      payImage.attr('src',src);
      payText.html(text);
      that.zsPay.show();
      that.zsBtns.hide();
      that.zsFooter.hide();

    })
  })
}
var zs = new ZanShang();
```

#### 如何使用：

直接到作者的[github上clone](https://github.com/kujian/zanshang?utm_source=caibaojian.com)这个项目，按照index.html中的代码，把css、HTML、js代码分别引入就可以了。

 
#### 使用须知：

二维码图片是放在当前目录中的images文件中，支付宝和微信的命名规则为：type+'-'+data-num.

- 如果选择下面这个2元，当默认选择支付宝付款方式时，则对应的图片就是alipay-2.png。
	`<button class="btn btn-blink" data-num="2">2元</button>`

- 如果对应选择微信的付款方式，同时选择10元这个按钮，则对应的图片就是wechat-10.png。
	`<button class="btn btn-blink" data-num="10">10元</button>`

使用时记得替换images路径下的二维码为你自己的，不然别人打款就会打给我的啦。:)

<br>

转载请注明：[黎婵的博客](https://cherrylichan.github.io) » [点击阅读原文](https://cherrylichan.github.io//posts/rwd/增加打赏功能/)     

