---
layout: page
title: Episodes
permalink: /episodes/
---

All episodes of **Boundaries 101 for Men**, newest first.

<ul class="episode-list">
{% for post in site.posts %}
  <li class="episode-card">
    <div class="episode-number">Episode {{ post.episode_number }}</div>
    <h3><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h3>
    <div class="episode-meta">
      {{ post.date | date: "%B %d, %Y" }}
    </div>
    <p class="episode-excerpt">{{ post.description }}</p>
    <div class="episode-links">
      <a href="{{ post.url | prepend: site.baseurl }}">&#128214; Read article</a>
      {% if post.youtube_url %}
        <a href="{{ post.youtube_url }}">&#127909; Watch on YouTube</a>
      {% endif %}
    </div>
  </li>
{% endfor %}
</ul>