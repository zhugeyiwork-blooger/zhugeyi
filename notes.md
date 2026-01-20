---
layout: page
title: 学习笔记目录
permalink: /notes/
---

这里记录了我从科研实战中积累的技术经验与算法笔记。

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



/* 1. 设置 GitHub 风格的代码字体 */
code, pre {
  font-family: ui-monospace, SFMono-Regular, "SF Mono", Menlo, Consolas, "Liberation Mono", monospace !important;
  font-size: 13.6px !important;
}

/* 2. 模拟 VS Code Dark+ 的代码块外观 */
.highlight {
  background: #1e1e1e !important; /* VS Code 深色背景 */
  color: #d4d4d4 !important;
  border-radius: 6px;
  padding: 16px;
  overflow: auto;
  position: relative; /* 为右上角按钮定位 */
  margin-top: 30px !important; /* 为顶部语言标签留出空间 */
}

/* VS Code 风格的语法高亮颜色微调 (Rouge 兼容) */
.highlight .keyword { color: #569cd6; } /* 关键字 */
.highlight .string  { color: #ce9178; } /* 字符串 */
.highlight .comment { color: #6a9955; font-style: italic; } /* 注释 */
.highlight .number  { color: #b5cea8; } /* 数字 */
.highlight .function{ color: #dcdcaa; } /* 函数名 */

/* 3. 代码块顶部的语言标签样式 */
.code-header {
  position: absolute;
  top: -25px;
  left: 0;
  background: #333;
  color: #aaa;
  font-size: 12px;
  padding: 2px 8px;
  border-radius: 4px 4px 0 0;
  text-transform: uppercase;
}

/* 4. 复制按钮样式 */
.copy-button {
  position: absolute;
  top: 8px;
  right: 8px;
  background: rgba(255, 255, 255, 0.1);
  border: 1px solid rgba(255, 255, 255, 0.2);
  color: #ccc;
  border-radius: 4px;
  padding: 4px 8px;
  font-size: 12px;
  cursor: pointer;
  transition: all 0.2s;
}
.copy-button:hover {
  background: rgba(255, 255, 255, 0.2);
  color: #fff;
}
