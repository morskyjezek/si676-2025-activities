---
layout: page
title: Keys
permalink: /keys/
---

This page lists the key to the lab activities:

{% assign keys_list = site.posts | where: "categories", "keys" | sort: due %}

{% if keys_list.size > 0 %}
| Title and Link | Assigned Date | Due Date |
| ------ | ------ | ------ |
{% for key in keys_list %}| [{{ key.title }}]({{ key.url | relative_url }}) | {{ key.assigned | date: "%e %B %Y" | lstrip }} | {{ key.due | date: "%e %B %Y" | lstrip }} |
{% endfor %}

{% else %}
No keys are currently published. Assignment keys will appear here when available.
{% endif %}