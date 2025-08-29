---
layout: page
title: Assignments
permalink: /assignments/
---

This page lists the assignments, which are major steps in the term project:

{% assign assignments = site.posts | where: "categories", "assignments" %}

| Assignment | Due Date | Canvas Link |
| ------ | ------ | ------ |
{% for assignment in assignments %}| [{{ assignment.title }}]({{ assignment.url | relative_url }}) | {{ assignment.due | date: "%e %B" | lstrip }} | {% if assignment.canvas-link %}[Canvas link]({{ assignment.canvas-link }}){% endif %} |
{% endfor %}