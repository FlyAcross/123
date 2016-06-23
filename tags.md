---
layout: page
title: "Tags"
description: "哈哈，你找到了我的文章基因库"  
header-img: "img/semantic.jpg"  
---

<div id='tag_cloud'>

{% for tag in site.tags %}

<a href="#{{ tag[0] }}" title="{{ tag[0] }}" rel="{{ tag[1].size }}">{{ tag[0] }}</a>

{% endfor %}

</div>

<hr>

<!-- 标签列表 -->
{% for tag in site.tags %}
<h3><div class="one-tag-list"></h3>
<span class="fa fa-tag listing-seperator" id="{{ tag[0] }}">
<h3><span class="tag-text">{{ tag[0] }}</span></h3>
</span>

{% for post in tag[1] %}

  <li class="listing-item">

  <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>

  <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>

  </li>

{% endfor %}

{% endfor %}








