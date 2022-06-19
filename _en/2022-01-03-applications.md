---
layout: article
titles:
    en      : &EN       Applications
    en-GB   : *EN
    en-US   : *EN
    en-CA   : *EN
    en-AU   : *EN
    zh-Hans : &ZH_HANS  应用
    zh      : *ZH_HANS
    zh-CN   : *ZH_HANS
    zh-SG   : *ZH_HANS
    zh-Hant : &ZH_HANT  應用
    zh-TW   : *ZH_HANT
    zh-HK   : *ZH_HANT
    ko      : &KO       애플리케이션
    ko-KR   : *KO
    fr      : &FR       Applications
    fr-BE   : *FR
    fr-CA   : *FR
    fr-CH   : *FR
    fr-FR   : *FR
    fr-LU   : *FR
    tr      : &TR       Uygulamalar
lang: en  #en, zh-Hans, zh-Hant
key: page-en-applications
permalink: /en/applications.html
show_date: false
show_title: false
article_section_navigator: false
aside:
    toc: true
---

{% assign hikiku_system    = site.data.products["hikiku_system"] %}

{% assign hikiku_widget    = site.data.products["hikiku_widget"] %}

{% assign hikiku_board     = site.data.products["hikiku_board"] %}

{% assign hikiku_http_source   = site.data.products["hikiku_http_source"] %}

{% assign hikiku_app       = site.data.products["hikiku_app"] %}

## Network Background Music

### Overview

```mermaid
graph TB;
    A[{{ hikiku_http_source.fullname }}]
    B[{{ hikiku_board.fullname }}]
    C(("Internet"))
    D[{{ hikiku_widget.fullname }}]
    E[{{ hikiku_widget.fullname }}]
    F[{{ hikiku_widget.fullname }}]
    G[{{ hikiku_app.fullname }}]
    A-->C;
    B---C;
    C---D;
    C---E;
    C---F;
    C---G;
```

* **{{ hikiku_http_source.fullname }}**：A HTTP/HLS music source
* **{{ hikiku_board.fullname }}**：An IoT platform
* **{{ hikiku_widget.fullname }}**：An audio playback device
* **{{ hikiku_app.fullname }}**：A mobile app for adjusting the audio device 

### Audio streams

```mermaid
graph TB;
    A[{{ hikiku_http_source.fullname }}]
    C(("Internet"))
    D[{{ hikiku_widget.fullname }}]
    E[{{ hikiku_widget.fullname }}]
    F[{{ hikiku_widget.fullname }}]
    A-->C;
    C-->D;
    C-->E;
    C-->F;
```

Audio is streamed from the **{{ hikiku_http_source.fullname }}** to **{{ hikiku_widget.fullname }}** via the Internet.

### Control signal

```mermaid
graph TB;
    B[{{ hikiku_board.fullname }}]
    C(("Internet"))
    D[{{ hikiku_widget.fullname }}]
    E[{{ hikiku_widget.fullname }}]
    F[{{ hikiku_widget.fullname }}]
    G[{{ hikiku_app.fullname }}]
    B---C;
    C---D;
    C---E;
    C---F;
    C---G;
```

Control signals are relayed from **{{ hikiku_app.fullname }}** via **{{ hikiku_board.fullname }}** to **{{ hikiku_widget.fullname }}**, or vice versa.