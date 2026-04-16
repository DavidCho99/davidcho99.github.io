---
layout: page
title: Notes
permalink: /notes/
nav_section: Notes
nav_order: 10
description: "All notes and posts."
---

This is the running log of study notes, class notes, and build journals.

- Browse by category: [Categories]({{ '/categories/' | relative_url }})

## Recent posts

<ul>
  {% for post in site.posts limit:20 %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <small>({{ post.date | date_to_string }})</small>
    </li>
  {% endfor %}
</ul>

