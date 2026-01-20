---
layout: post
title: "Python 实践：利用 Pandas 处理转录组表达矩阵"
date: 2026-01-19
categories: 数据处理
---

# 基因表达数据的自动化清洗流程

在进行 **WGCNA** 网络构建或功能基因定位之前，处理原始的表达矩阵（Count Matrix）是至关重要的一步。本文展示了如何利用 **Python** 提高数据清洗效率。

## 1. 实验背景
在研究**杨树张力木（Tension Wood）**发育或**拟南芥冷胁迫**响应时，我们通常会得到包含数万个基因的表达矩阵。在分析前，必须剔除那些在所有样本中几乎不表达的“背景噪音”基因。

## 2. 核心分析代码

下面的代码演示了如何使用 `pandas` 库快速过滤低表达基因，并对数据进行初步的标准化：

```python
import pandas as pd
import numpy as np

def clean_expression_matrix(file_path):
    # 1. 加载基因表达矩阵 (行名为 GeneID，列名为 SampleID)
    df = pd.read_csv(file_path, index_col=0)
    print(f"原始矩阵维度: {df.shape}")

    # 2. 过滤：保留在至少 3 个样本中表达量 (TPM/FPKM) > 1 的基因
    keep_indices = (df > 1).sum(axis=1) >= 3
    df_filtered = df[keep_indices]

    # 3. 对数转换 (Log2 Transformation) 以处理偏态分布
    df_log2 = np.log2(df_filtered + 1)

    print(f"清洗后矩阵维度: {df_log2.shape}")
    return df_log2

# 示例调用
# processed_df = clean_expression_matrix("count_matrix.csv")
```
