---
layout: default
permalink: /notes
title: 读书
description: 余喜读书，每读必有札记，集合以待观之。
---

<ol class="circle-list">
    {% for post in site.notes reversed %}
    <li>
        <h2><a class="post-title" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h2>
        <p>{{ post.description }}</p>
        <p class="post-meta">创作时间：{{ post.date | date: '%B %-d, %Y - %H:%M' }} 最后更新：{{ post.updatedate | date: '%B %-d, %Y - %H:%M' }}</p>
    </li>
    {% endfor %}
</ol>