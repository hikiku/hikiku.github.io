---
layout: article
titles:
  en      : &EN       About
  en-GB   : *EN
  en-US   : *EN
  en-CA   : *EN
  en-AU   : *EN
  zh-Hans : &ZH_HANS  关于
  zh      : *ZH_HANS
  zh-CN   : *ZH_HANS
  zh-SG   : *ZH_HANS
  zh-Hant : &ZH_HANT  關於
  zh-TW   : *ZH_HANT
  zh-HK   : *ZH_HANT
  ko      : &KO       소개
  ko-KR   : *KO
lang: en  #en, zh-Hans, zh-Hant
key: page-zh-Hans-about
permalink: /zh-Hans/about.html
show_title: false #true, false
---


{% assign hikiku_system    = site.data.products["hikiku_system"] %}

{% assign hikiku_widget    = site.data.products["hikiku_widget"] %}

{% assign hikiku_board     = site.data.products["hikiku_board"] %}

{% assign hikiku_http_sink   = site.data.products["hikiku_http_sink"] %}

{% assign hikiku_app       = site.data.products["hikiku_app"] %}


{{ hikiku_system.fullname }} 是一个创新开放的互联网音频播放系统。

{{ hikiku_system.fullname }} 整个系统包括硬件设备 {{ hikiku_widget.fullname }} 、管理平台 {{ hikiku_board.fullname }}、 用户应用 {{ hikiku_app.fullname }} 等。

{{ hikiku_widget.fullname }} 简单易用，可以播放来自于互联网的音频，也可播放本地 Micro SD 卡的音乐文件。{{ hikiku_widget.fullname }} 可以通过本地喇叭直接输出音乐，也可通过 Line Out, BT 等连接已有的音频播放设备。

可以使用 {{ hikiku_board.fullname }} 管理整个系统。

可以使用 {{ hikiku_app.fullname }} 个性化调节应用。

{{ hikiku_system.fullname }} 可应用于网络背景音乐播放、网络广播、本地音乐桥接等。

我们专注于提升系统的开放能力。{{ hikiku_system.fullname }} 通信协议开放，简洁且易于扩展。

我们专注于 {{ hikiku_widget.fullname }} 的开发，同时提供 {{hikiku_board.fullname}} 、{{hikiku_app.fullname}} 的开源实现， 与 {{ hikiku_http_sink.fullname }} 的最佳实践，以方便第三方扩展与集成。

请订阅我们的 RSS 频道，及时了解我们的进展。


Just say something about yourself. :+1:

{% highlight javascript %}
(() => console.log('hello, world!'))();
{% endhighlight %}
