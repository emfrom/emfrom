---
layout: page
title: Writing
permalink: /writing/
description: Original writing, notes, and things worth keeping.
nav_order: 3
---

A growing archive of original writing. Posts are written in Markdown and added to the site automatically when published.

{% if site.posts.size > 0 %}
<ol class="post-list archive-list">
  {% for post in site.posts %}
    <li class="post-row">
      <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%b %d, %Y" }}</time>
      <a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
      {% if post.description %}<p>{{ post.description | escape }}</p>{% endif %}
    </li>
  {% endfor %}
</ol>
{% else %}
<p class="quiet-note">The archive is empty for now. Check back when there’s something new to read.</p>
{% endif %}
