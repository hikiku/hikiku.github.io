---
layout: page
title: Products
permalink: /products/
---

{% assign hikiku_system    = site.data.products["hikiku_system"] %}

{% assign hikiku_board     = site.data.products["hikiku_board"] %}

{% assign hikiku_app       = site.data.products["hikiku_app"] %}

{% assign hikiku_server   = site.data.products["hikiku_server"] %}

## {{ hikiku_board.fullname }}

一块音频播放PCB板：

- 尺寸：40 mm x 50 mm
- 电源：5V, USB 电源端口 (USB Power Port)
- Wi-Fi 连接
- MicroSD 插槽 (MicroSD Slot)
- 音频输出接口： BT, Line Out, Local Speaker
- 支持多种主流音频格式，包括 MP3、AAC、FLAC、WAV、OGG、OPUS、AMR、TS、ALC 和 G.711


## {{ hikiku_app.fullname }}

主要用于配置 {{ hikiku_board.fullname }}：

- 设置 Wi-Fi 参数
- 设置 Server URL, Token 
- 设置音频输出接口

## {{ hikiku_server.fullname }}

大多采用标准的 HTTP Server，例如：

- PWS
- IIS
- Apache
- NGINX
- ......

提供播放列表生成工具：

- PlayListGenerateTool
