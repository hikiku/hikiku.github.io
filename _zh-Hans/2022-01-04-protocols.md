---
layout: article
titles:
    en      : &EN       Protocols
    en-GB   : *EN
    en-US   : *EN
    en-CA   : *EN
    en-AU   : *EN
    zh-Hans : &ZH_HANS  协议
    zh      : *ZH_HANS
    zh-CN   : *ZH_HANS
    zh-SG   : *ZH_HANS
    zh-Hant : &ZH_HANT  協議
    zh-TW   : *ZH_HANT
    zh-HK   : *ZH_HANT
    ko      : &KO       프로토콜
    ko-KR   : *KO
    fr      : &FR       Protocoles
    fr-BE   : *FR
    fr-CA   : *FR
    fr-CH   : *FR
    fr-FR   : *FR
    fr-LU   : *FR
    tr      : &TR       protokoller
lang: zh-Hans  #en, zh-Hans, zh-Hant
key: page-zh-Hans-protocols
permalink: /zh-Hans/protocols.html
show_date: false
show_title: false
article_section_navigator: false
aside:
    toc: false
---

{% assign hikiku_system    = site.data.products["hikiku_system"] %}

{% assign hikiku_widget    = site.data.products["hikiku_widget"] %}

{% assign hikiku_board     = site.data.products["hikiku_board"] %}

{% assign hikiku_http_source   = site.data.products["hikiku_http_source"] %}

{% assign hikiku_app       = site.data.products["hikiku_app"] %}

## 通信协议

```mermaid
graph TB
    A[{{ hikiku_http_source.fullname }}]
    B[{{ hikiku_board.fullname }}]
    C(("互联网"))
    D[{{ hikiku_widget.fullname }}]
    G[{{ hikiku_app.fullname }}]
    A==HTTP/HLS==>C
    B--MQTT---C
    C==HTTP/HLS==>D
    C--MQTT---D
    C--HTTP, WebSocket-->G
    G--SmartConfig-->D
```

- HTTP/HLS: 标准的 HTTP 或 HTTP Living Stream 码流。下载音乐，下载 PlayList。
- MQTT: 对 {{ hikiku_widget.fullname }} 的控制指令。
- HTTP, WebSocket：{{ hikiku_app.fullname }} 发出的控制指令。 例如： 设置音频输入、输出接口。
- SmartConfig：{{ hikiku_app.fullname }}发出的 Wi-Fi 配网指令。 Wi-Fi 配对， 设置 Server URL, Token。