---
layout: page
title: Labs
permalink: /labs/
---

This page lists the lab activities:

{% assign labs_list = site.posts | where: "categories", "labs" | sort: due %}

| Title and Link | Solution Key | Due Date | Canvas link |
| -------- | ---- | ---- | -- |
{% for lab in labs_list %}| [{{ lab.title }}]({{ lab.url | relative_url }}) | {% if lab.key %}[Key]({{ site.url }}{{ site.baseurl }}/posts/{{ lab.key }}){% endif %} | {{ lab.due | date: "%e %B %Y" | lstrip }} | [Canvas link]({{ lab.canvas-link }}) |
{% endfor %}
