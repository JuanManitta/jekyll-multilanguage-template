---
layout: home

title: Inicio
description: Inicio

language: es
language_reference: home
---

<img src="/assets/img/dark-logo.png" alt="">


<!-- <div style="padding: 1.5rem;">
    <div class="flex">
        <p>You can choose your preferred language to navigate through the site.</p>

    </div>
    <hr style="opacity: 0.1;">
  </div>
   -->
{% assign posts=site.posts | where: "language", page.language %}

<ul class="post-item-list">
  {% for post in posts %}
    <li class="post-item">
        <a class="post-item-title" href="{{ post.url }}">{{ post.title }}</a>
      {{ post.excerpt }} <a class="post-item-excerpt" href="{{ post.url }}">read more</a>
    </li>
  {% endfor %}
</ul>

