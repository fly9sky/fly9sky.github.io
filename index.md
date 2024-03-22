---
layout: default
permalink: /anthologies/
title: 文集
description: 文集
---

<ul class="post-list">
{% for anthology in site.anthologies reversed %}
    <li>
        <h2><a class="post-title" href="{{ anthology.url | prepend: site.baseurl }}">{{ anthology.title }}</a></h2>
        <p class="post-meta">创作时间：{{ anthology.date | date: '%B %-d, %Y - %H:%M' }} 最后更新：{{ anthology.updatedate | date: '%B %-d, %Y - %H:%M' }}</p>
        <p>{{ anthology.description }}</p>
        <hr/>
    </li>
{% endfor %}
</ul>
