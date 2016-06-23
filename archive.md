---
layout: page 
title: "Archive"
description: "你看到的，是我练习千字文的所有文章"
header-img: "img/red.jpg"
---

<ul class="posts">

    {% for post in site.posts %}
    {% capture m %}{{post.date | date:"%m"}}{% endcapture %}
    {% if month != m %}
    {% assign month = m %}
    <li class="listing-seperator">{{ post.date | date:"%Y-%m" }}</li>
    {% endif %}
    <li class="listing-item">
    <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
    <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
    </li>
    {% endfor %}
</ul>