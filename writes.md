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
        <p class="post-meta">{{ "创建时间：" | write.date | date: '%B %-d, %Y — %H:%M' }}</p>
        <p class="post-meta">{{ "最后更新时间：" | write.updatedate | date: '%B %-d, %Y — %H:%M' }}</p>
        <p>{{ write.description }}</p>
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
