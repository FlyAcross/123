---
layout: page
title: "Tags"
description: "哈哈，你找到了我的文章基因库"  
header-img: "img/semantic.jpg"  
---

## 基因列表
​	
<div class="row">
<div class="col-lg-8 col-lg-offset-2 col-md-10 col
-md-offset-1">
<!-- 标签云 -->
<div id='tag_cloud' class="tags">
{% for tag in site.tags %}
<a href="#{{ tag[0] }}" title="{{ tag[0] }}" 
 rel="{{ tag[1].size }}">{{ tag[0] }}</a>
{% endfor %}
</div>

<!-- 标签列表 -->
{% for tag in site.tags %}
<div class="one-tag-list">
<span class="fa fa-tag listing-seperator" id="{{ tag[0] }}">
<span class="tag-text">{{ tag[0] }}</span>
</span>

{% for post in tag[1] %}

  <li class="listing-item">

  <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>

  <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>

  </li>

{% endfor %}

{% endfor %}

</ul>






