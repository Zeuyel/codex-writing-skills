# Adverb and Connector Library

## Purpose

This file stores a conservative adverb and connector inventory for Chinese journal prose.

Use it dynamically:
- choose according to rhetorical move, not stylistic variety for its own sake
- prefer forms observed in the designated reference article
- do not overload a paragraph with too many transition markers

Current default reference for `ai-innovation-lean`:
- `ref/人工智能技术应用如何影响企业创新_李玉花.pdf`

## A. Batch-validated core items

These items passed the current admission screen and are safe defaults when the rhetorical move matches:

- `然而`
- `例如`
- `进一步`
- `同时`
- `但是`
- `在此背景下`
- `基于此`
- `此外`
- `因此`
- `具体地`
- `显著`
- `充分`
- `深入`
- `迅速`
- `及时`
- `有效`
- `不断`
- `依然`
- `更好地`
- `更快`
- `更高效地`
- `基于以上分析`
- `为了弥补这一不足`

## B. Observation-layer only

These items remain usable, but should not automatically enter the core adverb inventory yet:

- `更精确地`
- `进一步分析发现`

Reason:
They are better handled as part of fixed collocations or still need broader support.

## C. Safe connectors observed in the default reference paper

- `然而`
- `为了弥补这一不足`
- `例如`
- `进一步`
- `同时`
- `但是`
- `在此背景下`
- `基于此`
- `此外`
- `因此`
- `具体地`
- `进一步分析发现`
- `基于以上分析`
- `余文安排如下`

## D. Use by rhetorical move

### 转折

Prefer:
- `然而`
- `但是`

### 举例

Prefer:
- `例如`

### 递进

Prefer:
- `进一步`
- `进一步分析发现`
- `此外`

### 并列补充

Prefer:
- `同时`

### 因果收束

Prefer:
- `因此`
- `基于此`
- `基于以上分析`

### 细化说明

Prefer:
- `具体地`

## E. High-risk adverbs and fillers

These often make the prose sound swollen or AI-generated when overused:

- `更加`
- `更为`
- `尤为`
- `显然`
- `实际上`
- `本质上`
- `某种程度上`
- `在很大程度上`
- `系统性地` when no system is shown
- `全面地` when no scope is specified

Use only when analytically necessary.

## F. Paragraph-level checking rule

Before finalizing a paragraph:
1. count the connectors
2. count the evaluative adverbs
3. remove decorative markers first
4. keep only the marker that matches the actual rhetorical move
