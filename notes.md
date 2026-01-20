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

---

### 🛠️ 建议分类体系
根据您的研究背景，建议使用以下 `categories` 标签来撰写笔记：

* **机器学习 (ML)**：涉及 CNN、GNN、PyTorch 模型训练等。
* **蛋白质科学 (Structural-Biology)**：涉及 ESMfold、Alphafold3、GROMACS 等工具的使用。
* **生物信息学 (Bioinformatics)**：涉及 WGCNA、宏基因组、转录组分析等。
* **数据处理 (Data-Science)**：涉及 Python (pandas)、R 语言、Shell 脚本自动化等。
