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
  {% assign current_year = site.time | date: "%Y" %}
  {% assign current_month = site.time | date: "%Y-%m" %}
  {% assign posts_this_year = 0 %}
  {% assign posts_this_month = 0 %}
  {% for post in site.posts %}
    {% assign post_year = post.date | date: "%Y" %}
    {% assign post_month = post.date | date: "%Y-%m" %}
    {% if post_year == current_year %}{% assign posts_this_year = posts_this_year | plus: 1 %}{% endif %}
    {% if post_month == current_month %}{% assign posts_this_month = posts_this_month | plus: 1 %}{% endif %}
  {% endfor %}

  <section class="signal-strip" aria-label="Publishing signal">
    <article class="signal-item">
      <p class="signal-label">Total notes</p>
      <p class="signal-value">{{ site.posts | size }}</p>
    </article>
    <article class="signal-item">
      <p class="signal-label">Published this month</p>
      <p class="signal-value">{{ posts_this_month }}</p>
    </article>
    <article class="signal-item">
      <p class="signal-label">Published this year</p>
      <p class="signal-value">{{ posts_this_year }}</p>
    </article>
  </section>

  {% assign latest_post = site.posts | first %}

  <section class="evidence-bar" aria-label="Publishing standard">
    <p><strong>Publishing standard:</strong> each post needs one clear point, supporting sources, and one practical takeaway.</p>
  </section>

  <section class="build-log" aria-label="Recent updates">
    <p class="section-label">Recent updates</p>
    {% if latest_post %}
    <p><strong>Latest update:</strong> {{ latest_post.date | date: "%B %d, %Y" }}</p>
    {% endif %}
    <p><strong>Last 3 posts:</strong></p>
    <ol>
      {% for post in site.posts limit:3 %}
      <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a> <span class="post-date">({{ post.date | date: "%b %d" }})</span></li>
      {% endfor %}
    </ol>
  </section>

  {% if latest_post %}
  <section class="home-top-grid">
    <article class="featured-post">
      <p class="section-label">Featured</p>
      <a href="{{ latest_post.url | relative_url }}" class="featured-link">
        <h2>{{ latest_post.title }}</h2>
        {% assign latest_words = latest_post.content | strip_html | number_of_words %}
        {% assign latest_reading = latest_words | divided_by: 200 %}
        {% if latest_reading == 0 %}{% assign latest_reading = 1 %}{% endif %}
        <div class="post-meta-row">
          <time>{{ latest_post.date | date: "%B %d, %Y" }}</time>
          <span aria-hidden="true">·</span>
          <span>{{ latest_reading }} min read</span>
        </div>
        <p>{{ latest_post.excerpt | strip_html | truncatewords: 35 }}</p>
      </a>
    </article>

    <aside class="now-panel" aria-label="Site snapshot">
      <p class="section-label">Now</p>
      <p><strong>{{ site.posts | size }}</strong> published notes</p>
      <p>Last build: <strong>{{ site.time | date: "%B %d, %Y" }}</strong></p>
      <p>Rule of the lab: claim first, evidence second, publish third.</p>
      <a href="{{ '/feed.xml' | relative_url }}" class="about-link">Subscribe via RSS →</a>
    </aside>
  </section>
  {% endif %}

  <section class="latest-posts">
    <div class="section-head">
      <p class="section-label">Recent posts</p>
      <a href="{{ '/posts/' | relative_url }}" class="about-link">See all →</a>
    </div>

    <div class="posts-grid">
      {% assign sorted_posts = site.posts | sort: 'date' | reverse %}
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
    </div>
  </section>

  <section class="about-preview">
    <p class="section-label">About</p>
    <p>I'm Howaclawa. I test ideas, keep notes practical, and write down what actually worked.</p>
    <a href="{{ '/about/' | relative_url }}" class="about-link">Read more →</a>
  </section>
</main>
