---
layout: page
title: 个人简介
---

# 欢迎来到我的学术主页

我是 **朱葛懿** ，目前是**安徽农业大学**生物学专业的硕士研究生（2023.09 - 2026.07）。

我致力于将**人工智能与机器学习算法**应用于复杂的生物学问题。我的研究涵盖了宏基因组学、蛋白质结构预测以及药物分子设计等多个前沿领域 。

## 🔬 研究领域与项目经验

### 1. 机器学习驱动的功能基因挖掘 
* **黄曲霉菌研究**：开发基于物种基因组信息的机器学习模型，通过 Python 脚本重构蛋白质结构域矩阵，成功筛选并验证了与菌丝横隔产生的相关基因 。
* **热稳定性预测**：利用 **ESMfold**、ProtT5 等蛋白质语言模型构建特征矩阵，结合 CNN、GNN 等深度学习算法预测蛋白质的热稳定性 。

### 2. 深度学习与药物设计 
* **酶进化预测**：构建深度学习模型预测还原胺化酶的最优突变体，结合 Alphafold3 与 GROMACS 进行结合自由能计算 。
* **药物从头设计**：联用生成对抗网络 (ORGAN) 与分子对接技术，针对慢性粒细胞白血病相关蛋白设计 PPI 抑制剂 。

## 💻 技术栈

* **编程与自动化**：熟练使用 **Linux (Conda/Docker)** 环境配置，擅长利用 **Shell** 构建自动化分析流程，精通 **Python** 与 **R** 进行数据处理与科研绘图 。
* **算法与模型**：熟练运用 **PyTorch**、Transformer、随机森林等算法进行分类与回归模型的开发与优化 。
* **组学分析**：掌握宏基因组 Illumina 数据分析、细菌基因组二/三代数据分析及有参转录组分析流程 。

## 📚 科研成果

目前以**共第一作者**身份在国际主流期刊发表多篇论文：
* **Genomics (2025)**: *Decoding oxygen preference: Machine learning discovers functional genes in Bacteria*.
* **J Chem Inf Model (2025)**: *Deep Learning-Driven Discovery of Novel Antimicrobial Peptides...*.
* **BMC Genomics (2025)**: *Machine learning prediction of bacterial optimal growth temperature...*.

## ✉️ 联系方式

* **Email**: zhugeyi.work@gmail.com
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
