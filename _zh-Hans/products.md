---
layout: article
titles:
    en      : &EN       Products
    en-GB   : *EN
    en-US   : *EN
    en-CA   : *EN
    en-AU   : *EN
    zh-Hans : &ZH_HANS  产品
    zh      : *ZH_HANS
    zh-CN   : *ZH_HANS
    zh-SG   : *ZH_HANS
    zh-Hant : &ZH_HANT  產品
    zh-TW   : *ZH_HANT
    zh-HK   : *ZH_HANT
    ko      : &KO       제품
    ko-KR   : *KO
    fr      : &FR       Produit
    fr-BE   : *FR
    fr-CA   : *FR
    fr-CH   : *FR
    fr-FR   : *FR
    fr-LU   : *FR
    tr      : &TR       Ürün
lang: zh-Hans  #en, zh-Hans, zh-Hant
key: page-zh-Hans-products
permalink: /zh-Hans/products.html
show_date: false
show_title: false
aside:
    toc: true
---


{% assign hikiku_system    = site.data.products["hikiku_system"] %}

{% assign hikiku_widget    = site.data.products["hikiku_widget"] %}

{% assign hikiku_board     = site.data.products["hikiku_board"] %}

{% assign hikiku_http_source   = site.data.products["hikiku_http_source"] %}

{% assign hikiku_app       = site.data.products["hikiku_app"] %}


## {{ hikiku_widget.fullname }}

音频播放装置：

- 尺寸：40 mm x 50 mm
- 电源：5V, USB 电源端口 (USB Power Port)
- Wi-Fi 连接
- BT 连接
- MicroSD 插槽 (MicroSD Slot)
- 音频输出接口： BT, Line In/Out, Local Speaker
- 支持多种主流音频格式，包括 MP3、AAC、FLAC、WAV、OGG、OPUS、AMR、TS、ALC 和 G.711


## {{ hikiku_http_source.fullname }}

HTTP/HLS 网络音频源，使用通用的 HTTP Server，例如：

- PWS
- IIS
- Apache
- NGINX

提供播放列表生成工具：

- PlayListGenerateTool


## {{ hikiku_app.fullname }}

音频装置调节手机应用，主要用于配置 {{ hikiku_widget.fullname }}：

- 设置 Wi-Fi 参数
- 设置 Server URL, Token 
- 设置音频输入、输出参数


## {{ hikiku_board.fullname }}

IoT 平台软件：

- 设备管理 {{ hikiku_widget.fullname }}
- 用户管理 {{ hikiku_app.fullname }}

