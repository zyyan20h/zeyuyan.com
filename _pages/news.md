---
layout: default
title: News
permalink: /news/
---

# News

<ul class="news-list">
  {% for item in site.data.news %}
    {% include news-item.html item=item %}
  {% endfor %}
</ul>