---
layout: default
title: Home
---

# Posts

{% if site.posts.size > 0 %}
  {% for post in site.posts %}
  <article>
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <small>{{ post.date | date: "%-d %B %Y" }}</small>
    {% if post.excerpt %}
      {{ post.excerpt }}
    {% endif %}
  </article>
  {% endfor %}
{% else %}
  <p>No posts yet.</p>
{% endif %}
