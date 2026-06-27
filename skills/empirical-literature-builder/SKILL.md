---
name: empirical-literature-builder
description: >-
  Build or revise literature-review logic for economics and management empirical
  papers when explicitly invoked, or when zh-empirical-paper-writer has routed a
  literature-review task here. Use for theme, viewpoint, method, or mechanism
  grouping, text-identification method review, research-gap transitions, and
  ai-innovation-lean boundaries. For active manuscript writing, use
  zh-empirical-paper-writer first so review prose and planning are applied to the
  target TeX/PDF assets.
---

# Empirical Literature Builder

## When to use

Use this skill when the task is to:

- write or revise a literature review for an empirical paper
- collect and compare text-identification methods used in economics or management empirical work
- organize prior literature by `主题 / 观点 / 方法 / 机制`
- transition from literature evolution to `研究缺口` and `研究价值`
- continue the `ai-innovation-lean` project without overrunning the literature or method authority already fixed

## Workflow

### 1. Start from authority, not from freewriting

Before writing, check whether the project already has curated literature materials.

For `ai-innovation-lean`, start with:

- `notes/literature_authority_checkpoint.md`
- `archive/graduation-thesis/writing-history/docx_extracted.txt`
- `notes/literature_survey_report_2026-04-03.md`
- `notes/china_ai_innovation_literature_comparison.md`
- `notes/empirical_text_identification_review.md`
- `notes/empirical_master_plan.md`
- `ref/` and `notes/literature_cards/`

Do not write novelty or gap claims beyond what these materials support.

### 2. Do not freewrite the whole review at once

Default staged order:
1. fix the chapter or section containers
2. write only the opening and closing paragraphs first
3. extract reusable paragraph套路 from reference papers
4. allocate paragraph套路 across the remaining middle paragraphs
5. plan sentence functions inside each paragraph
6. only then draft prose

For this project, the literature review should be built slowly and structurally, not generated as one full block.

### 3. Organize the review by unit, not by article sequence

Do not default to abstract grouping labels such as `第一类文献` or `研究线索`. In Chinese economics and management journals, the review usually starts from the object, difficulty, or measurement issue itself, then moves to representative studies and only afterwards compresses them into the author's judgment.

Default review unit order:
1. theme
2. representative viewpoints or findings
3. method or measurement evolution
4. what remains unresolved
5. research gap and research value

Do not write `A文献发现... B文献发现... C文献发现...` unless the user explicitly wants an annotated bibliography.

### 4. Use a fixed paragraph logic

Preferred Chinese-journal paragraph order:
1. start from the concrete object, empirical difficulty, or mechanism at stake
2. show how existing studies handle that object
3. compress what is already relatively clear
4. identify the insufficiency that matters for this paper
5. bridge to the next block or to the paper

Avoid English-style category-first review prose such as "the first stream" or "the second line of research" unless the user explicitly requests that style.

Fixed review-paragraph identities should be planned separately:
1. 本节首段: define the review object, the bottleneck, and the section order
2. 本小节首段: define the block object and why this block matters
3. 证据铺陈段: place representative studies and compress a local consensus
4. 承上启下段: shift from one object to the next without changing the paper's main question
5. 本小节末段: extract the insufficiency and hand off to the next block
6. 本节末段: unify the gap and hand off to the next chapter

For each fixed paragraph identity, also set a sentence-role sequence, not only a paragraph label.

Use the same planning template throughout the review section:
1. 段落身份
2. 段落职责
3. 段落套路
4. 句子序列
5. 当前义务

Preferred Chinese-journal paragraph order:
1. start from the concrete object, empirical difficulty, or mechanism at stake
2. show how existing studies handle that object
3. compress what is already relatively clear
4. identify the insufficiency that matters for this paper
5. bridge to the next block or to the paper

Avoid English-style category-first review prose such as "the first stream" or "the second line of research" unless the user explicitly requests that style.


For each literature block:
1. open with the problem this block addresses
2. summarize the main findings or viewpoints
3. explain the dominant methods or measurement approaches
4. point out the unresolved issue that matters for this paper
5. land on why the next block or the paper's question follows naturally

### 5. Learn paragraph套路 from high-quality references

When the user provides a Chinese reference article, decompose each paragraph into:
1. paragraph role
2. opening move
3. sentence-function sequence
4. landing move
5. reusable套路 label

Assume that academic paragraph organization uses a small number of recurring套路. Reuse those套路 deliberately instead of improvising every paragraph from scratch.

### 6. Treat the remaining paragraph plan as a distribution problem

After the chapter and section opening/closing paragraphs are fixed, decide how many remaining paragraphs are needed and assign套路 with variation.

Control for repetition:
1. avoid identical opening moves in adjacent paragraphs
2. avoid identical landing moves in adjacent paragraphs
3. avoid turning every paragraph into `topic sentence + literature list + gap`
4. keep the rhetorical rhythm varied but the logic stable

### 7. For text-identification methods, always build a method family map

Default method families are in `references/text-identification-methods.md`.
Use those families to compare:

- what the method identifies
- where it is commonly used
- why it is useful here
- what validation it requires

### 8. Keep project positioning stable

For `ai-innovation-lean`:

- the paper is a `理论驱动的实证文章`
- Chapters 1 and 2 may be polished before later chapters are fixed
- Chapters 3+ must not be written as formal manuscript text until literature, variables, data, and identification have been fixed by authority materials

Read `references/ai-innovation-lean-boundaries.md` when working on this project.

## Output pattern

When asked to help with a literature review, usually produce:

1. a thematic map
2. a paragraph套路 map when a reference article is available
3. a sentence-function plan for key paragraphs
4. a gap statement that stays within the verified evidence
5. if useful, a draft paragraph or section that follows the project's journal style

## References

- For review structure and transitions: read `references/review-architecture.md`
- For text-identification methods: read `references/text-identification-methods.md`
- For this project's boundaries: read `references/ai-innovation-lean-boundaries.md`
