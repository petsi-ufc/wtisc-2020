---
layout: default
title: Palestras  
---

# Palestras 

{% assign sorted_pages = site.pages | sort:"date" %}
{% for page in sorted_pages %}
{% if page.categories contains 'palestra' %}
<div class="item"><h3><a href="{{ page.path}}">{{page.date | date: "%m/%d"}} | {{ page.title }}</a></h3></div>
    {{page.description}}
{% endif %}
{% endfor %}