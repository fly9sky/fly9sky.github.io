---
layout: default
permalink: /notes/
title: 读书
description: 余喜读书，每读必有札记，集合以待观之。
---

<ul class="post-list">
{% for note in site.notes reversed %}
    <li>
        <h2><a class="post-title" href="{{ note.url | prepend: site.baseurl }}">{{ note.title }}</a></h2>
        <p class="post-meta">创作时间：{{ note.date | date: '%B %-d, %Y - %H:%M' }} 最后更新：{{ note.updatedate | date: '%B %-d, %Y - %H:%M' }}</p>
        <p>{{ note.description }}</p>
        <hr/>
      </li>
{% endfor %}
</ul>