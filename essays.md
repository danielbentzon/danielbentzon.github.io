---
layout: default
title: Essays
permalink: /essays/
main_class: listeside
---
<div class="inner">
  <div class="tekst">
    <h1>Essays</h1>
    {% assign essays = site.essays | sort: 'date' | reverse %}
    <div class="post-grid">
      {% for essay in essays %}
      <a class="post-kasse" href="{{ essay.url | relative_url }}">
        <span class="post-titel">{{ essay.title }}</span>
        <span class="dato small">{{ essay.date | date: "%d.%m.%Y" }}</span>
      </a>
      {% endfor %}
    </div>
  </div>
</div>
