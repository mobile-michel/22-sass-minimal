---
title: Documentation
description: This is the documentation pages.
override:tags: [primary]
pagination:
    data: collections.doc
    size: 3
    alias: pagination
---
{%- for item in pagination %}
- <a href="{{ item.url }}">{{ item.data.description }}</a>
{% endfor -%}
