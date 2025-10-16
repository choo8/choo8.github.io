---
layout: page
title: Textbook Index
permalink: /textbooks/
---

<details open>
  <summary>📚 Browse Textbooks by Subject</summary>
  <div class="home" style="margin-top: 15px;">
    {%- assign textbooks_by_subject = site.textbooks | group_by: "subject" -%}
    
    {%- for subject_group in textbooks_by_subject -%}
      <h2>{{ subject_group.name }}</h2>
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
  </div>
</details>

<style>
  details {
    border: 1px solid #e8e8e8;
    border-radius: 5px;
    padding: 0.5rem 1rem;
    margin-bottom: 1rem;
  }
  summary {
    cursor: pointer;
    font-weight: bold;
  }
</style>