# Collocation Library

## Purpose

This file stores fixed or semi-fixed collocations that survived the current admission screen.

Use it dynamically:
- prefer these when a sentence needs a stable Chinese-journal combination
- use collocations before inventing new verb-adverb pairs
- avoid table-driven statistical phrases unless the sentence is truly reporting regression output

Current default reference for `ai-innovation-lean`:
- `ref/人工智能技术应用如何影响企业创新_李玉花.pdf`

## A. Core admitted collocations

- `显著提高`
- `推动创新`
- `深入分析`
- `显著促进`
- `促进创新`
- `深入考察`
- `尝试利用`
- `有效识别`
- `不断增强`
- `提高效率`
- `利用数据`
- `开始借助`
- `进一步指出`
- `进一步分析`
- `显著影响`
- `显著提升`
- `进一步发现`
- `深入剖析`

## B. Best use by chapter type

### 引言

Prefer:
- `深入分析`
- `尝试利用`
- `有效识别`
- `显著促进`
- `推动创新`

### 文献综述

Prefer:
- `开始借助`
- `尝试利用`
- `进一步指出`
- `进一步发现`
- `有效识别`

### 理论分析

Prefer:
- `深入分析`
- `显著影响`
- `不断增强`
- `推动创新`
- `提高效率`

### 实证设计和结果

Prefer:
- `显著提高`
- `显著促进`
- `显著提升`
- `利用数据`
- `有效识别`

## C. Excluded technical-statistical phrases

Do not treat these as style-building collocations for general prose:

- `显著为正`
- `显著为负`
- `显著性水平`
- `显著正相关`
- `显著差异`

These belong to regression reporting, not to general rhetorical style.

## D. Checking rule

Before introducing a new collocation:
1. check whether an admitted collocation already serves the sentence
2. if not, check whether the new one appears in multiple Chinese papers
3. if it only appears in tables or OCR noise, reject it
