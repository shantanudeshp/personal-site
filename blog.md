---
layout: default
title: Blog
---

You can subscribe to my [RSS feed]({{ "/feed.xml" | relative_url }}) to get updates on new posts.

{% assign postsByYearMonth = site.posts | group_by_exp: "post", "post.date | date: '%B %Y'" %}
{% for yearMonth in postsByYearMonth %}
<h2 class="archive-heading">{{ yearMonth.name }}</h2>
<ul class="archive-list">
  {% for post in yearMonth.items %}
    <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
{% endfor %}

<div class="site-figure">
  <img src="{{ '/assets/ovid-among-scythians.webp' | relative_url }}" alt="Ovid Among the Scythians">
  <p class="figure-caption is-italic">Laudamus veteres, sed nostris utimur annis / We praise the elders, but we live in our own time</p>
</div>
