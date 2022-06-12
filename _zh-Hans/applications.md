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
---

应用.

{% assign hikiku_system    = site.data.products["hikiku_system"] %}

{% assign hikiku_widget    = site.data.products["hikiku_widget"] %}

{% assign hikiku_board     = site.data.products["hikiku_board"] %}

{% assign hikiku_http_source   = site.data.products["hikiku_http_source"] %}

{% assign hikiku_app       = site.data.products["hikiku_app"] %}


```mermaid
graph TB;
    A[{{ hikiku_http_source.fullname }}]
    B[{{ hikiku_board.fullname }}]
    C("互联网")
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

```mermaid
graph TB;
    A[{{ hikiku_http_source.fullname }}]
    C("互联网")
    D[{{ hikiku_widget.fullname }}]
    E[{{ hikiku_widget.fullname }}]
    F[{{ hikiku_widget.fullname }}]
    A-->C;
    C-->D;
    C-->E;
    C-->F;
```

```mermaid
graph TB;
    B[{{ hikiku_board.fullname }}]
    C("互联网")
    D[{{ hikiku_widget.fullname }}]
    E[{{ hikiku_widget.fullname }}]
    F[{{ hikiku_widget.fullname }}]
    G[{{ hikiku_app.fullname }}]
    B---C;
    C-->D;
    C-->E;
    C-->F;
    C---G;
```