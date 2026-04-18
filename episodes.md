---
layout: page
title: Episodes
permalink: /episodes/
---

All episodes of **Boundaries 101 for Men**, newest first.

<ul class="episode-list">
{% for post in site.posts %}
  <li class="episode-card">
    <div class="episode-number">
      Episode {{ post.episode_number }}
      {% if forloop.first %}<span class="latest-badge">Latest</span>{% endif %}
    </div>
    <h3><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h3>
    <div class="episode-meta">{{ post.date | date: "%B %d, %Y" }}</div>
    <p class="episode-excerpt">{{ post.description }}</p>
    <div class="episode-links">
      <a href="{{ post.url | prepend: site.baseurl }}">📖 Read article</a>
      {% if post.youtube_url %}
        <a href="{{ post.youtube_url }}" target="_blank">🎥 Watch on YouTube</a>
      {% endif %}
    </div>
  </li>
{% endfor %}
</ul>