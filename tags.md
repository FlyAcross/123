---
layout: page
title: "Tags"
description: "哈哈，你找到了我的文章基因库"  
header-img: "img/semantic.jpg"  
---

## 基因列表
{% include JB/setup %}

<ul class="tag_box inline">
  {% assign tags_list = site.tags %}  
  {% include JB/tags_list %}
</ul>


{% for tag in site.tags %} 
  <h2 id="{{ tag[0] }}-ref">{{ tag[0] }}</h2>
  <ul>
    {% assign pages_list = tag[1] %}  
    {% include JB/pages_list %}
  </ul>
{% endfor %}