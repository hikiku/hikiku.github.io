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
lang: zh-Hans  #en, zh-Hans, zh-Hant
key: page-zh-Hans-applications
permalink: /zh-Hans/applications.html
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

## 网络背景音乐

### 系统示意图

```mermaid
graph TB;
    A[{{ hikiku_http_source.fullname }}]
    B[{{ hikiku_board.fullname }}]
    C(("互联网"))
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

* {{ hikiku_http_source.fullname }}：HTTP/HLS 网络音频源
* {{ hikiku_board.fullname }}：IoT 平台软件
* {{ hikiku_widget.fullname }}：音频播放装置
* {{ hikiku_app.fullname }}：音频装置调节手机应用

### 音频流

```mermaid
graph TB;
    A[{{ hikiku_http_source.fullname }}]
    C(("互联网"))
    D[{{ hikiku_widget.fullname }}]
    E[{{ hikiku_widget.fullname }}]
    F[{{ hikiku_widget.fullname }}]
    A-->C;
    C-->D;
    C-->E;
    C-->F;
```

音频流自 {{ hikiku_http_source.fullname }} 经互联网，传送至 {{ hikiku_widget.fullname }}。

### 控制指令

```mermaid
graph TB;
    B[{{ hikiku_board.fullname }}]
    C(("互联网"))
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

控制信号自 {{ hikiku_app.fullname }} 经 {{ hikiku_board.fullname }} 中转 ，传送至 {{ hikiku_widget.fullname }}， 或者反之。