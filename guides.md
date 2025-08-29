---
layout: page
title: Guides
permalink: /guides/
---

This page lists the Guide pages for selected assignments and tasks:

{% assign guides_list = site.posts | where: "categories", "guides" %}

{% for guide in guides_list %}* [{{ guide.title }}]({{ guide.url | relative_url }}) {{ guide.date | date: "%e %B %Y" | lstrip }}
{% endfor %}
