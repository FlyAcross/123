---
layout: page 
title: "Archive"
description: "你看到的，是我练习千字文的所有文章"
header-img: "img/red.jpg"
---

{% for category in site.categories %}
<h2>{{ category | first }}</h2>
<ul class="arc-list">

    {% for post in category.last %}
        <li>{{ post.date | date:"%d/%m/%Y"}}<a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>
{% endfor %}