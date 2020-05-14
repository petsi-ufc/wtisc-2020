---
layout: default
title: Palestras  
---

# Palestras 

{% assign sorted_pages = site.pages | sort:"date" %}
{% for page in sorted_pages %}
{% if page.categories contains 'palestra' %}
{% if page.passou == false %}
<div class="item"><h3><a href="{{ page.path}}">{{page.date | date: "%d/%m"}} | {{ page.title }}</a></h3></div>
    {{page.description}}
{% else %}
<div class="item"><s><h3><a href="{{ page.path}}">{{page.date | date: "%d/%m"}} | {{ page.title }}</a></h3></s></div>
> Esta palestra já passou, mas você pode ver ela na íntegra no nosso [canal do YouTube](https://www.youtube.com/channel/UCnktWER26p3YdGJMZULGPnw) 
{% endif %}
{% endif %}
{% endfor %}