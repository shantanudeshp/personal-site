---
layout: default
title: Blog
---

# Blog Posts

<ul class="post-list">
{% for post in site.posts %}
  <li>
    <h3 class="post-title">
      <a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
    </h3>
    <p class="post-meta">{{ post.date | date: "%B %d, %Y" }}</p>
    <p>{{ post.excerpt | strip_html | truncatewords: 50 }}</p>
  </li>
{% endfor %}
</ul>