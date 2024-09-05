---
layout: "page"
title: "Runner Room"
permalink: /running/
---

{% for post in site.categories.running %}
{%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
<span class="post-meta">{{ post.date | date: date_format }}</span>
<a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
<br>
{% endfor %}