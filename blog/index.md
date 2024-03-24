---
title: Blog
description: This is the blog.
override:tags: [primary]
pagination:
    data: collections.blog
    size: 3
    alias: pagination
---
{%- for item in pagination %}
- <a href="{{ item.url }}">{{ item.data.description }}</a>
{% endfor -%}
