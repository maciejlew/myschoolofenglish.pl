---
layout: blog
title: Blog
permalink: /blog/
---

<h1>{{ page.title }}</h1>

<div class="posts">
  {% for post in site.posts %}
    <article class="post">
      <h2>
        <a href="{{ post.url | relative_url }}">
          {{ post.title }}
        </a>
      </h2>

      <p class="post-date">
        {{ post.date | date: "%d.%m.%Y" }}
      </p>

      {% if post.excerpt %}
        <div class="post-excerpt">
          {{ post.excerpt }}
        </div>
      {% endif %}
    </article>
  {% endfor %}
</div>

