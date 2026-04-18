---
layout: default
title: Home
---

<div class="hero">
  <img src="{{ site.baseurl }}/cover.jpg" alt="Boundaries 101 for Men" class="hero-cover">
  <h1>Boundaries 101 for Men</h1>
  <p class="tagline">Practical, no-nonsense coaching for men who want to build and protect their self-respect. Learn the skills most men were never taught.</p>
  
  <div class="platform-buttons">
    <a href="https://youtube.com/@Boundaries101forMen" class="platform-btn btn-youtube">&#9654; YouTube</a>
    <a href="https://open.spotify.com/show/2uoKNnuSgaH1G9shiOMIu8" class="platform-btn btn-spotify">&#9835; Spotify</a>
    <a href="https://music.amazon.com/podcasts/boundaries-101-for-men" class="platform-btn btn-amazon">&#9835; Amazon Music</a>
    <a href="{{ site.baseurl }}/feed.xml" class="platform-btn btn-rss">&#128226; RSS Feed</a>
  </div>
</div>

<h2>Latest Episodes</h2>

<ul class="episode-list">
{% for post in site.posts %}
  <li class="episode-card">
    <div class="episode-number">Episode {{ post.episode_number }}</div>
    <h3><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h3>
    <div class="episode-meta">
      {{ post.date | date: "%B %d, %Y" }}
      {% if post.tags.size > 0 %}
        &middot; {{ post.tags | first }}
      {% endif %}
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