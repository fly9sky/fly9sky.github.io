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
        <p class="post-meta">{{ "创建时间：" | note.date | date: '%B %-d, %Y — %H:%M' }}</p>
        <p class="post-meta">{{ "最后更新时间：" | note.updatedate | date: '%B %-d, %Y — %H:%M' }}</p>
        <p>{{ note.description }}</p>
        <br/>
        <hr/>
      </li>
{% endfor %}
</ul>

<nav class="pagination" role="navigation">
  {% if paginator.previous_page %}
  <a class="previous pagination__newer btn btn-small btn-tertiary" href="{{ paginator.previous_page_path }}">&larr; 上一页</a>
  {% endif %}
  <span class="page_num pagination__page-number">{{ paginator.page }} / {{ paginator.total_pages }}</span>
  {% if paginator.next_page %}
  <a class="next pagination__older btn btn-small btn-tertiary" href="{{ paginator.next_page_path }}">下一页 &rarr;</a>
  {% endif %}
</nav>
