---
layout: page
title: Math
permalink: /math/
---

<p>
  Looking for the ML-focused version? See <a href="{{ '/math-for-ml/' | relative_url }}">Math for ML</a>.
</p>

{% assign math_posts = site.categories.Math | sort: "date" | reverse %}

{% if math_posts and math_posts.size > 0 %}
  <ul>
    {% for post in math_posts %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <small>({{ post.date | date_to_string }})</small>
      </li>
    {% endfor %}
  </ul>
{% else %}
  <p>No math posts yet.</p>
{% endif %}
