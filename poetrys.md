---
layout: page
permalink: /poetrys/
title: 诗歌
description: 平常写作的一些小诗，聚集起来供大家欣赏。
---

<ul class="post-list">
{% for poem in site.poetrys reversed %}
    <li>
        <h2><a class="poem-title" href="{{ poem.url | prepend: site.baseurl }}">{{ poem.title }}</a></h2>
        <p class="post-meta">{{ poem.date | date: '%B %-d, %Y — %H:%M' }}</p>
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
