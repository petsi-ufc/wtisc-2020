---
layout: default
title: Palestras  
---

# Palestras 

{% assign sorted_pages = site.pages | sort:"date" %}
{% for page in sorted_pages %}
{% if page.categories contains 'palestra' %}
{% if page.passou == true %}
<div class="item"><h3><a href="{{ page.path}}">{{page.date | date: "%d/%m"}} | {{ page.title }}</a></h3></div>
    {{page.description}}
{% else %}
<div class="item"><s><h3><a href="{{ page.path}}">{{page.date | date: "%d/%m"}} | {{ page.title }}</a></h3></s></div>
    {{page.description}}
{% endif %}
{% endif %}
{% endfor %}