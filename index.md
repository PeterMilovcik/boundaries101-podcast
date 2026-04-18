---
layout: default
title: Home
---

<div class="hero">
  <img src="{{ site.baseurl }}/cover.jpg" alt="Boundaries 101 for Men" class="hero-cover">
  <h1>Boundaries 101 for Men</h1>
  <p class="tagline">Practical, no-nonsense coaching for men who want to build and protect their self-respect. Learn the skills most men were never taught.</p>
  
  <div class="platform-buttons">
    <a href="https://youtube.com/@Boundaries101forMen" class="platform-btn btn-youtube" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-youtube"></i> YouTube</a>
    <a href="https://open.spotify.com/show/2uoKNnuSgaH1G9shiOMIu8" class="platform-btn btn-spotify" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-spotify"></i> Spotify</a>
    <a href="https://music.amazon.com/podcasts/boundaries-101-for-men" class="platform-btn btn-amazon" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-amazon"></i> Amazon Music</a>
    <a href="{{ site.baseurl }}/feed.xml" class="platform-btn btn-rss"><i class="fa-solid fa-rss"></i> RSS Feed</a>
  </div>
</div>

<div class="section-header">
  <h2>Latest Episodes</h2>
</div>

<ul class="episode-list">
{% for post in site.posts %}
  <li class="episode-card">
    <a href="{{ post.url | prepend: site.baseurl }}">
      <img src="{{ site.baseurl }}/thumbnails/{{ post.slug }}.jpg" alt="{{ post.title }}" class="episode-thumb" loading="lazy">
    </a>
    <div class="episode-card-content">
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
    </div>
  </li>
{% endfor %}
</ul>