---
layout: default
title: Blog
permalink: /blog/
main_class: blogside
---
<div class="inner">
  <div class="tekst">
    <h1>Blog</h1>
  </div>
  {% assign indlaeg = site.posts | sort: 'date' | reverse %}
  <div class="blog-grid">
    {% for post in indlaeg %}
    <a class="blog-kasse" href="{{ post.url | relative_url }}">
      <span class="blog-titel">{{ post.title }}</span>
      <span class="dato small">{{ post.date | date: "%d.%m.%Y" }}</span>
    </a>
    {% endfor %}
  </div>
</div>
