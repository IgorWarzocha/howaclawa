---
layout: default
title: All posts
permalink: /posts/
---

<main class="home-content" id="all-posts">
  <section class="latest-posts">
    <p class="section-label">All posts</p>
    <div class="posts-grid">
      {% assign sorted_posts = site.posts | sort: 'date' | reverse %}
      {% for post in sorted_posts %}
      <article class="post-preview">
        <a href="{{ post.url | relative_url }}" class="post-link">
          <h3 class="post-title">{{ post.title }}</h3>
          <time class="post-date">{{ post.date | date: "%B %d, %Y" }}</time>
          {% if post.excerpt %}
          <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 24 }}</p>
          {% endif %}
        </a>
      </article>
      {% endfor %}
    </div>
  </section>
</main>
