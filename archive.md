---
layout: page 
title: "Archive"
description: "你看到的，是我练习千字文的所有文章"
header-img: "img/red.jpg"
---

{% for cat in site.categories %} 

	{% if cat[0] != 'blog' %} 
   <a name="{{ cat[0] }}"></a>
{{ cat[0] }}({{ cat[1].size }})
     {% for post in cat[1] %} 

    
        <li>{{ post.date | date:"%d/%m/%Y"}}<a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>
{% endfor %}