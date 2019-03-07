---
layout: page
title: "Archive"
description: "写点什么"
header-img: "img/orange.jpg"
---

# Data
gavatar: img/favicon.png # 浏览器地址栏小图标，可自定义更改
favicon: img/favicon.png # 浏览器地址栏小图标，可自定义更改

<ul class="listing">
{% for post in site.posts %}
  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
  {% if year != y %}
    {% assign year = y %}
    <li class="listing-seperator">{{ y }}</li>
  {% endif %}
  <li class="listing-item">
    <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
    <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>