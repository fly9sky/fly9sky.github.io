---
layout: default
permalink: /writes/
title: 创作
description: 创作一些文章，读书笔记，杂文，感想之类的东西。
---

<ul class="post-list">
{% for write in site.writes reversed %}
    <li>
        <h2><a class="post-title" href="{{ write.url | prepend: site.baseurl }}">{{ write.title }}</a></h2>
        <p class="post-meta">创作时间：{{ write.date | date: '%B %-d, %Y - %H:%M' }} 最后更新：{{ write.updatedate | date: '%B %-d, %Y - %H:%M' }}</p>
        <p>{{ write.description }}</p>
        <hr/>
      </li>
{% endfor %}
</ul>