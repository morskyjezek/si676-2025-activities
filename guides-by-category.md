---
layout: page
title: Guides by Topic
permalink: /guides-by-category/
published: true
---

{% comment %}create a list of posts that are in the guides category{% endcomment %}
{% assign guides = site.posts | where: "categories", "guides" %}

{% comment %}identify unique categories from the guide posts and exclude 'activities' posts{% endcomment %}
{% assign unique_categories = "" | split: "" %}
{% for post in guides %}
  {% for category in post.categories %}
    {% unless category == "activities" or category == "guides" %}
      {% unless unique_categories contains category %}
        {% assign unique_categories = unique_categories | push: category %}
      {% endunless %}
    {% endunless %}
  {% endfor %}
{% endfor %}

{% comment %}create a list of the categories and number of posts in each{% endcomment %}
<h2>Topics</h2>
<ul>
{% for category in unique_categories %}
  {% assign category_posts = guides | where_exp: "post", "post.categories contains category" %}
  <li><a href="#{{ category | downcase | url_escape | strip | replace: ' ', '-' }}">{{ category | camelcase}}</a></li>
{% endfor %}
</ul>

{% comment %}create headings for each category, then list posts in that category{% endcomment %}
<h2>Guides by Topic</h2>
{% for category in unique_categories %}
  <h3 id="{{ category | downcase | url_escape | strip | replace: ' ', '-' }}">{{ category | capitalize }}</h3>
  <ul>
    {% assign category_posts = guides | where_exp: "post", "post.categories contains category" %}
    {% for post in category_posts %}
        <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}