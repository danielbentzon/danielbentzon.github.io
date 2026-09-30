---
layout: default
title: Skriverier
permalink: /skriverier/
main_class: listeside
---
<div class="inner">
  <div class="tekst">
    <h1>Skriverier</h1>
    {% assign poster = site.skriverier | sort: 'date' | reverse %}
    <div class="post-grid">
      {% for p in poster %}
      <a class="post-kasse" href="{{ p.url | relative_url }}">
        <span class="post-titel">{{ p.title }}</span>
        <span class="dato small">{{ p.date | date: "%d.%m.%Y" }} &middot; {{ p.genre }}</span>
      </a>
      {% endfor %}
    </div>
  </div>
</div>
