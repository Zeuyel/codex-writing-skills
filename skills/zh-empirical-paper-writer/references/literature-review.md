# Literature Review

Use for `literature-review`: thematic grouping, method-family review, research
gap writing, and positioning transitions.

## Contents

1. Authority first
2. Review organization
3. Paragraph identities
4. Research gap and research value
5. Text-identification methods
6. Project boundaries
7. TeX handling

## 1. Authority First

Do not write novelty, gap, or contribution claims beyond the verified literature
base. Prefer project materials such as literature cards, exported references,
review notes, BibTeX/RIS/EndNote libraries, Scopus/WoS exports, and approved
chapter plans.

Claims requiring verification include:

- `现有研究多从……展开`
- `既有文献较少关注……`
- `鲜有研究讨论……`
- `本文的核心新意在于……`
- `据我们所知，尚无研究……`
- `该方向尚未被系统讨论`

If authority is incomplete, keep the claim provisional or leave it in TeX
comments rather than formal manuscript prose.

Use conservative alternatives such as:

- `本文的研究动机在于……`
- `从当前已整理文献看，……`
- `一个有待进一步核对的判断是……`

Only use the second form when a real curated base has been checked.

## 2. Review Organization

Organize by object, problem, method, mechanism, or viewpoint. Do not default to
article-by-article listing.

Default review unit order:

1. theme
2. representative viewpoints or findings
3. method or measurement evolution
4. what remains unresolved
5. research gap and research value

Preferred paragraph movement:

1. start from the concrete object, empirical difficulty, or measurement problem
2. show how existing studies handle that object
3. compress what has become relatively clear
4. identify the insufficiency that matters for this paper
5. bridge to the next block or this paper's question

Do not write `A文献发现... B文献发现... C文献发现...` unless the user explicitly
wants an annotated bibliography.

Avoid opening with `第一类文献`, `第二类文献`, `第三类文献`, or `研究线索` unless the
user explicitly requests that taxonomy.

## 3. Paragraph Identities

Plan these identities when relevant:

1. 本节首段: define the review object, bottleneck, and section order
2. 本小节首段: define the block object and why it matters
3. 证据铺陈段: place representative studies and compress a local consensus
4. 承上启下段: shift from one object to the next without changing the main question
5. 本小节末段: extract the insufficiency and hand off to the next block
6. 本节末段: unify the gap and hand off to the next chapter

For each identity, fix:

1. 段落身份
2. 段落职责
3. 段落套路
4. 句子序列
5. 当前义务

Do not draft review prose until fixed paragraph identities and sentence-role
sequences are known.

## 4. Research Gap And Research Value

Do not jump directly from a literature list to `研究缺口`. Insert an evolution
sentence first.

Useful movement:

1. `整体看，现有研究已经从……推进到……。`
2. `但在……这一层面，相关讨论仍然不够充分。`
3. `这意味着，后续研究需要进一步回答……。`

After the gap, move to value in two steps:

1. explain what the paper adds to the unresolved problem
2. explain why that addition matters for identification, mechanism, or
   interpretation

Avoid empty claims such as `具有重要理论意义和现实意义` unless followed by a
concrete statement.

## 5. Text-Identification Methods

When the task involves text identification, build a method-family map.

Method families:

1. dictionary or keyword matching
2. dictionary expansion with machine learning or external taxonomies
3. supervised classification
4. topic models or unsupervised discovery
5. pretrained language models and LLM-based semantic identification
6. information extraction and structured tagging

For each method family, compare:

- what the method identifies
- what data it requires
- where economics or management studies use it
- what validation it needs
- why it fits this paper's empirical object

For most empirical paper use cases, report:

- labeling protocol
- sampling strategy for validation set
- out-of-sample metrics
- confusion patterns or hard cases
- robustness to alternative dictionaries, thresholds, or model settings

Do not present a method as authoritative only because it is technically
available.

## 6. Project Boundaries

For `ai-innovation-lean`:

- the paper is a `理论驱动的实证研究`
- the theory section fixes research objects, mechanism chains, boundary
  conditions, and hypotheses for later empirical work
- Chapters 1 and 2 may be polished before later chapters are fixed
- Chapters 3 and later must not be written as formal manuscript text until
  literature, variables, data, and identification details are fixed by authority
  materials

Relevant local sources may include:

- `notes/literature_authority_checkpoint.md`
- `notes/literature_survey_report_2026-04-03.md`
- `notes/china_ai_innovation_literature_comparison.md`
- `notes/empirical_text_identification_review.md`
- `notes/empirical_master_plan.md`
- `archive/graduation-thesis/writing-history/docx_extracted.txt`
- `ref/`
- `notes/literature_cards/`

Do not write Lean4, compilation, workflow, or method-pipeline details into the
manuscript body unless they are direct contributions.

## 7. TeX Handling

Write approved review prose directly to the target `.tex` file. Keep provisional
gap claims, unresolved literature authority, and paragraph plans in TeX comments
unless the user asks to render them for PDF review.
