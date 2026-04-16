---
layout: page
title: Project
permalink: /project/
---

{% assign project_posts = site.categories.Project | sort: "date" | reverse %}

{% if project_posts and project_posts.size > 0 %}
  <ul>
    {% for post in project_posts %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <small>({{ post.date | date_to_string }})</small>
      </li>
    {% endfor %}
  </ul>
{% else %}
  <p>No project posts yet.</p>
{% endif %}

