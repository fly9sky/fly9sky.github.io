---
layout: default
permalink: /poetrys/
title: 诗集
description: 平常写作的一些小诗，聚集起来供大家欣赏。
---

<ul class="post-list">
{% for poetry in site.poetrys reversed %}
    <li>
        <h2><a class="post-title" href="{{ poetry.url | prepend: site.baseurl }}">{{ poetry.title }}</a></h2>
        <p class="post-meta">创作时间：{{ poetry.date | date: '%B %-d, %Y - %H:%M' }} 最后更新：{{ poetry.updatedate | date: '%B %-d, %Y - %H:%M' }}</p>
        <p>{{ poetry.description }}</p>
        <hr/>
    </li>
{% endfor %}
</ul>
