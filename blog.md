---
layout: default
title: Blog
permalink: /blog/
main_class: listeside
---
<div class="inner">
  <div class="tekst">
    <h1>Blog</h1>
    {% assign indlaeg = site.posts | sort: 'date' | reverse %}
    <div class="post-grid">
      {% for post in indlaeg %}
      <a class="post-kasse" href="{{ post.url | relative_url }}">
        <span class="post-titel">{{ post.title }}</span>
        <span class="dato small">{{ post.date | date: "%d.%m.%Y" }}</span>
      </a>
      {% endfor %}
    </div>
  </div>
</div>
