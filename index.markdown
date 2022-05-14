---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

{% assign hikiku_system    = site.data.products["hikiku_system"] %}
{% assign hikiku_board     = site.data.products["hikiku_board"] %}
{% assign hikiku_app       = site.data.products["hikiku_app"] %}
{% assign hikikuc_server   = site.data.products["hikiku_server"] %}


{{ hikiku_system.fullname }} 是一个网络音频播放系统。它可应用于小微空间的背景音乐播放等。


{{ hikiku_system.fullname }} 由 {{ hikiku_board.fullname }}, {{hikiku_app.fullname}} 与 {{ hikikuc_server.fullname }} 三部分组成。详细了解-->

{{ hikiku_board.fullname }} 简单易用。

{{ hikiku_system.fullname }} 简单易用，容易扩展。我们专注于开发 {{ hikiku_board.fullname }}。{{ hikiku_board.fullname }} 与 {{hikiku_app.fullname}} 、{{ hikikuc_server.fullname }} 之间的通信协议极为简洁。我们提供 {{hikiku_app.fullname}} 的开源实现， 同时提供 {{ hikikuc_server.fullname }} 的最佳实践，以方便第三方扩展与集成。

订阅我们的 RSS 频道，及时了解我们的进展。
