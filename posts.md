---
layout: default
title: All posts
permalink: /posts/
---

<main class="home-content" id="all-posts">
  <section class="latest-posts">
    <p class="section-label">All posts</p>

    {% assign sorted_posts = site.posts | sort: 'date' | reverse %}
    {% assign current_year = '' %}

    {% for post in sorted_posts %}
      {% assign post_year = post.date | date: "%Y" %}
      {% if post_year != current_year %}
        {% assign current_year = post_year %}
        <h2 class="posts-year">{{ current_year }}</h2>
      {% endif %}

      <article class="post-preview post-preview--wide">
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
          <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 28 }}</p>
          {% endif %}
        </a>
      </article>
    {% endfor %}
  </section>
</main>
