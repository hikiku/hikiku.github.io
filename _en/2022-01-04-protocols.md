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
lang: en  #en, zh-Hans, zh-Hant
key: page-en-protocols
permalink: /en/protocols.html
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

## Protocols

```mermaid
graph TB
    A[{{ hikiku_http_source.fullname }}]
    B[{{ hikiku_board.fullname }}]
    C(("Internet"))
    D[{{ hikiku_widget.fullname }}]
    G[{{ hikiku_app.fullname }}]
    A==HTTP, HLS==>C
    B--MQTT---C
    C==HTTP, HLS==>D
    C--MQTT---D
    C--HTTP, WebSocket-->G
    G--SmartConfig-->D
```

- HTTP/HLS: HTTP or HLS audio stream.
- MQTT: Control signal about {{ hikiku_widget.fullname }}.
- HTTP, WebSocket：Control commands issued by {{ hikiku_app.fullname }}, e.g., set the audio input and output interface.
- SmartConfig：Wi-Fi configuration command issued by {{ hikiku_app.fullname }}, e.g., Wi-Fi pairing, set Server URL, Token.