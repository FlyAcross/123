---
layout: page
title: "Books"
description: "我的阅读记录"  
header-img: "img/semantic.jpg" 
---

<div id='keywords1_cloud'>

{% for keywords1 in site.keywords1s %}

<a href="#{{ keywords1[0] }}" title="{{ keywords1[0] }}" rel="{{ keywords1[1].size }}">{{ keywords1[0] }}</a>

{% endfor %}

</div>

<!-- 标签列表 -->

{% for keywords1 in site.keywords1s %}

<div class="one-keywords1-list">

<span class="fa fa-keywords1 listing-seperator" id="{{ keywords1[0] }}">

<span class="keywords1-text">{{ keywords1[0] }}</span>

</span>

{% for post in keywords1[1] %}

  <li class="listing-item">

  <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>

  <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>

  </li>

{% endfor %}

{% endfor %}








