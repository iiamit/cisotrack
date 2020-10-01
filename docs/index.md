---
layout: main
title: main
single_page: true
---
<div class="frontpage"> 
    {% assign sorted_pages = site.pages | sort:"order" %}
    {% for entry in sorted_pages %}
        {% if entry.in_frontpage %}
            {{ entry.content | raw }}
        {% endif %}
    {% endfor %}
</div>