---
layout: default
title: Episodes
permalink: /episodes/
---

<div class="episodes-hero">
  <h1><i class="fa-solid fa-headphones"></i> All Episodes</h1>
  <p class="episodes-subtitle">{{ site.posts | size }} episodes &mdash; newest first</p>
</div>

<ul class="episode-list">
{% for post in site.posts %}
  <li class="episode-card">
    <div class="episode-number">
      Episode {{ post.episode_number }}
      {% if forloop.first %}<span class="latest-badge">Latest</span>{% endif %}
    </div>
    <h3><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h3>
    <div class="episode-meta">
      {{ post.date | date: "%B %d, %Y" }}
      {% if post.duration_minutes %}<span class="episode-duration">&middot; {{ post.duration_minutes }} min</span>{% endif %}
    </div>
    <p class="episode-excerpt">{{ post.description }}</p>
    <div class="episode-links">
      <a href="{{ post.url | prepend: site.baseurl }}" class="episode-link-read"><i class="fa-solid fa-book-open"></i> Read article</a>
      {% if post.youtube_url %}
        <a href="{{ post.youtube_url }}" class="episode-link-youtube" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-youtube"></i> Watch on YouTube <i class="fa-solid fa-arrow-up-right-from-square"></i></a>
      {% endif %}
    </div>
  </li>
{% endfor %}
</ul>