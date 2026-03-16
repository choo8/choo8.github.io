---
layout: page
title: Article Index
permalink: /articles/
---

{%- assign articles_by_topic = site.articles | group_by: "topic" -%}

{%- for topic_group in articles_by_topic -%}
## {{ topic_group.name }}

<ul class="post-list">
  {%- for article in topic_group.items -%}
  <li>
    <a class="post-link" href="{{ article.url | relative_url }}">
      {{ article.title | escape }}
    </a>
  </li>
  {%- endfor -%}
</ul>
{%- endfor -%}

