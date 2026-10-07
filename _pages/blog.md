---
layout: blog
title: Blog
description: "Blog My School of English w Bytomiu: relacje z warsztatów, obozów językowych w Chester, wydarzeń szkolnych i inspiracje do nauki angielskiego."
permalink: /blog/
redirect_from:
  - /tag/kreatywne-lekcje-angielskiego/page/2
  - /tag/angielski-na-maturze
  - /tag/kreatywne-lekcje-angielskiego
  - /tag/szkola-jezykowa
  - /tag/beatrix-potter
  - /2018/08
  - /tag/muzyka
  - /type/image
  - /tag/bytom
  - /blog/2017/09/04/zapraszamy-juz-mozna.html
  - /blog/2017/10/07/poznajmy-sie-lepiej.html
  - /blog/2017/12/27/wesolych-swiat.html
  - /blog/2018/01/01/szczesliwego-nowego-roku.html
  - /blog/2018/01/12/bal-karnawalowy-w-my-school-of-english.html
  - /blog/2018/03/30/rozwijamy-talenty-po-angielsku.html
  - /blog/2018/04/10/absolutnie-magiczne-warsztaty-plastyczne-pani-agaty.html
  - /blog/2018/05/01/konkurs-talentow-w-my-school-of-english.html
  - /blog/2018/08/22/szkola-jezykowa-od-kuchni.html
  - /blog/2017/08/17/how-to-make-a-comedy.html
  - /author/gosia
  - /category/koncepty
  - /tag/inspiracja
  - /tag/literatura-dziecieca
  - /tag/literatura-anglosaska
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

