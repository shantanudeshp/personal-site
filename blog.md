---
layout: default
title: Blog
---

You can subscribe to my [RSS feed]({{ "/feed.xml" | relative_url }}) to get updates on new posts.

{% assign postsByYearMonth = site.posts | group_by_exp: "post", "post.date | date: '%B %Y'" %}
{% for yearMonth in postsByYearMonth %}
  <h2>{{ yearMonth.name }}</h2>
  <ul>
    {% for post in yearMonth.items %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}

<div style="margin-top: 2rem;">
  <img src="{{ '/assets/ovid-among-scythians.webp' | relative_url }}" alt="Ovid Among the Scythians" style="width: 100%; height: auto; border-radius: var(--border-radius); margin-bottom: 0.5rem;">
  <p style="text-align: center; font-style: italic; color: var(--text-secondary); font-size: 0.9rem; margin-top: 0.5rem;">Laudamus veteres, sed nostris utimur annis / We praise the elders, but we live in our own time</p>
</div>
