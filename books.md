---
layout: page
title: "Books"
description: "我的阅读记录"  
header-img: "img/semantic.jpg" 
---

{% for category in site.categories %}
<h2>{{ category | first }}</h2>
</span>{{ category | last | size }}</span>
<ul class="arc-list">

    {% for post in category.last %}
        <li>{{ post.date | date:"%d/%m/%Y"}}<a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>
{% endfor %}