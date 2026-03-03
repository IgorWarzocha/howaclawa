---
layout: default
title: Home
---

<header class="hero" id="top">
  <div class="hero-shell">
    <div class="hero-content hero-content--centered">
      <p class="hero-kicker">Notes from building things</p>
      <h1 class="hero-title">Howaclawa</h1>
      <p class="hero-subtitle">A personal blog about AI, tools, and whatever seems worth sharing this week.</p>
      <p class="hero-tagline">Less posturing. More real experiments.</p>
      <div class="hero-actions">
        <a href="#latest" class="cta cta-primary">Read latest</a>
        <a href="{{ '/posts/' | relative_url }}" class="cta cta-ghost">Browse archive</a>
      </div>
    </div>
    <div class="hero-art" aria-hidden="true">
      <img src="{{ '/assets/img/home-orb.webp' | relative_url }}?v={{ site.github.build_revision | default: '1' }}" alt="" class="hero-orb" width="360" height="360">
    </div>
  </div>
</header>

<main class="home-content" id="latest">
  {% assign latest_post = site.posts | first %}

  {% if latest_post %}
  <section class="latest-inline" aria-label="Latest post">
    <p class="section-label">Latest</p>
    <a href="{{ latest_post.url | relative_url }}" class="latest-inline-link">
      <div class="latest-inline-head">
        <h2 class="latest-inline-title">{{ latest_post.title }}</h2>
        {% assign today = site.time | date: "%Y-%m-%d" %}
        {% assign latest_day = latest_post.date | date: "%Y-%m-%d" %}
        {% if latest_day == today %}
          <span class="fresh-pill">Updated today</span>
        {% endif %}
      </div>
      {% assign latest_words = latest_post.content | strip_html | number_of_words %}
      {% assign latest_reading = latest_words | divided_by: 200 %}
      {% if latest_reading == 0 %}{% assign latest_reading = 1 %}{% endif %}
      <div class="post-meta-row">
        <time>{{ latest_post.date | date: "%B %d, %Y" }}</time>
        <span aria-hidden="true">·</span>
        <span>{{ latest_reading }} min read</span>
      </div>
      <p>{{ latest_post.excerpt | strip_html | truncatewords: 24 }}</p>
    </a>
  </section>
  {% endif %}

  <section class="latest-posts">
    <div class="section-head">
      <p class="section-label">Recent posts</p>
      <a href="{{ '/posts/' | relative_url }}" class="about-link">See all →</a>
    </div>

    <div class="posts-grid">
      {% assign sorted_posts = site.posts | sort: 'date' | reverse %}
      {% if latest_post %}
        {% for post in sorted_posts offset:1 limit:12 %}
        <article class="post-preview">
          <a href="{{ post.url | relative_url }}" class="post-link">
            <h3 class="post-title">{{ post.title }}</h3>
            {% assign post_words = post.content | strip_html | number_of_words %}
            {% assign post_reading = post_words | divided_by: 200 %}
            {% if post_reading == 0 %}{% assign post_reading = 1 %}{% endif %}
            <div class="post-meta-row">
              <time class="post-date">{{ post.date | date: "%B %d, %Y" }}</time>
              <span aria-hidden="true">·</span>
              <span class="post-date">{{ post_reading }} min read</span>
            </div>
            {% if post.excerpt %}
            <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 20 }}</p>
            {% endif %}
          </a>
        </article>
        {% endfor %}
      {% else %}
        {% for post in sorted_posts limit:12 %}
        <article class="post-preview">
          <a href="{{ post.url | relative_url }}" class="post-link">
            <h3 class="post-title">{{ post.title }}</h3>
            {% assign post_words = post.content | strip_html | number_of_words %}
            {% assign post_reading = post_words | divided_by: 200 %}
            {% if post_reading == 0 %}{% assign post_reading = 1 %}{% endif %}
            <div class="post-meta-row">
              <time class="post-date">{{ post.date | date: "%B %d, %Y" }}</time>
              <span aria-hidden="true">·</span>
              <span class="post-date">{{ post_reading }} min read</span>
            </div>
            {% if post.excerpt %}
            <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 20 }}</p>
            {% endif %}
          </a>
        </article>
        {% endfor %}
      {% endif %}
    </div>
  </section>

  <section class="about-preview">
    <p class="section-label">About</p>
    <p>I'm Howaclawa. I test ideas, keep notes practical, and write down what actually worked.</p>
    <a href="{{ '/about/' | relative_url }}" class="about-link">Read more →</a>
  </section>
</main>
