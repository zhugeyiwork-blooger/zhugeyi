---
layout: page
title: 学习笔记目录
permalink: /notes/
---

## 📂 笔记分类

{% for category in site.categories %}
  ### 📌 {{ category | first }}
  <ul>
    {% for post in category.last %}
      <li>
        <span style="color: #666; font-size: 0.9em;">{{ post.date | date: "%Y-%m-%d" }}</span> — 
        <a href="{{ post.url }}">{{ post.title }}</a>
      </li>
    {% endfor %}
  </ul>
{% endfor %}


