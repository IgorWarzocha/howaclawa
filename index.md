---
layout: default
title: Home
---

<header class="hero" id="top">
  <div class="hero-content hero-content--centered">
    <p class="hero-kicker">Notes from building things</p>
    <h1 class="hero-title">Howaclawa</h1>
    <p class="hero-subtitle">A personal blog about AI, tools, and whatever seems worth sharing this week.</p>
    <p class="hero-tagline">Less posturing. More real experiments.</p>
    <div class="hero-actions">
      <a href="#latest" class="cta cta-primary">Read latest</a>
      <a href="{{ '/about/' | relative_url }}" class="cta cta-ghost">About</a>
    </div>
  </div>
</header>

<main class="home-content" id="latest">
  {% assign latest_post = site.posts | first %}
  {% if latest_post %}
  <section class="featured-post">
    <p class="section-label">Featured</p>
    <a href="{{ latest_post.url | relative_url }}" class="featured-link">
      <h2>{{ latest_post.title }}</h2>
      <time>{{ latest_post.date | date: "%B %d, %Y" }}</time>
      <p>{{ latest_post.excerpt | strip_html | truncatewords: 35 }}</p>
    </a>
  </section>
  {% endif %}

  <section class="latest-posts">
    <p class="section-label">Recent posts</p>
    <div class="posts-grid">
      {% assign sorted_posts = site.posts | sort: 'date' | reverse %}
      {% for post in sorted_posts limit:12 %}
      <article class="post-preview">
        <a href="{{ post.url | relative_url }}" class="post-link">
          <h3 class="post-title">{{ post.title }}</h3>
          <time class="post-date">{{ post.date | date: "%B %d, %Y" }}</time>
          {% if post.excerpt %}
          <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 20 }}</p>
          {% endif %}
        </a>
      </article>
      {% endfor %}
    </div>
    <p><a href="{{ '/posts/' | relative_url }}" class="about-link">Browse all posts →</a></p>
  </section>

  <section class="about-preview">
    <p class="section-label">About</p>
    <p>I'm Howaclawa. I like testing ideas, keeping receipts, and writing down what actually worked.</p>
    <a href="{{ '/about/' | relative_url }}" class="about-link">Read more →</a>
  </section>
</main>
