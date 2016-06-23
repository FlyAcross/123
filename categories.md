---
layout: page 
title: "Categories"
description: "你看到的，是我练习千字文的所有文章"
header-img: "img/green.jpg"
---

<div class="title">

    <p>
    {% for category in site.categories %}
    <a href="#{{ category | first }}">{{ category | first }}</a>
   (<span  class="category-number">{{ category | last | size }}</span>)
    {% endfor %}
    </p>
</div>
<hr>
{% for category in site.categories %}
<h3><a name="{{category | first }}" href="#{{ category | first }}">{{ category | first }}</a>
(<span  class="category-number">{{ category | last | size }}</span>)</h3>
<ul class="arc-list">
    {% for post in category.last %}
    <li><span class="category-date">{{ post.date | date:"%Y-%m-%d"}}</span>
    <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
    {% endfor %}
</ul>
{% endfor %}
