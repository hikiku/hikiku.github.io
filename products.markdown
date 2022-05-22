---
layout: page
title: Products
permalink: /products/
---

{% assign hikiku_system    = site.data.products["hikiku_system"] %}

{% assign hikiku_widget    = site.data.products["hikiku_widget"] %}

{% assign hikiku_board     = site.data.products["hikiku_board"] %}

{% assign hikiku_http_sink   = site.data.products["hikiku_http_sink"] %}

{% assign hikiku_app       = site.data.products["hikiku_app"] %}


## {{ hikiku_widget.fullname }}

音频播放小设备：

- 尺寸：40 mm x 50 mm
- 电源：5V, USB 电源端口 (USB Power Port)
- Wi-Fi 连接
- MicroSD 插槽 (MicroSD Slot)
- 音频输出接口： BT, Line Out, Local Speaker
- 支持多种主流音频格式，包括 MP3、AAC、FLAC、WAV、OGG、OPUS、AMR、TS、ALC 和 G.711


## {{ hikiku_http_sink.fullname }}

采用标准的 HTTP Server，例如：

- PWS
- IIS
- Apache
- NGINX
- ......

提供播放列表生成工具：

- PlayListGenerateTool


## {{ hikiku_app.fullname }}

主要用于配置 {{ hikiku_board.fullname }}：

- 设置 Wi-Fi 参数
- 设置 Server URL, Token 
- 设置音频输出接口


## {{ hikiku_board.fullname }}

- 设备管理 {{ hikiku_widget.fullname }}
- 用户管理 {{ hikiku_app.fullname }}

