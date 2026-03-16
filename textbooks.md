---
layout: page
title: Textbook Index
permalink: /textbooks/
---

{%- assign textbooks_by_subject = site.textbooks | group_by: "subject" -%}

{%- for subject_group in textbooks_by_subject -%}
## {{ subject_group.name }}

<ul class="post-list">
  {%- for textbook in subject_group.items -%}
  <li>
    <a class="post-link" href="{{ textbook.url | relative_url }}">
      {{ textbook.title | escape }}
    </a>
  </li>
  {%- endfor -%}
</ul>
{%- endfor -%}