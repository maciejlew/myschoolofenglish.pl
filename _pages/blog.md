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
  - /2018/08/22/szkola-jezykowa-od-kuchni.html
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
  # nowe: tagi
  - /tag/angielski
  - /tag/angielski-w-bytomiu
  - /tag/angielski-bytom/page/3
  - /tag/angielski-z-mama
  - /tag/szkola-jezykowa/page/2
  - /tag/szkola-jezykowa-w-bytomiu
  - /tag/certyfikaty
  - /tag/christmas
  - /tag/czytelnictwo
  - /tag/karnawal-dla-dzieci
  - /tag/koniec-roku
  - /tag/kraina-jezior
  - /tag/lekcja-biologii-po-angielsku
  - /tag/pasja-do-angielskiego
  - /tag/wydawnictwo-usborne
  - /tag/zawod-lektora-angielskiego
  - /tag/zapisy-do-szkoly-jezykowej/feed
  # nowe: kategorie i paginacja
  - /category/aktualnosci
  - /category/aktualnosci/page/4
  - /page/5
  # nowe: formaty wpisów
  - /type/image/page/2
  - /type/gallery
  - /type/video
  - /type/audio
  # nowe: archiwa dat
  - /2017/02
  - /2018/01
  - /2018/05
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

