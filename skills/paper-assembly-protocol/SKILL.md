---
name: paper-assembly-protocol
description: >-
  Run the staged assembly protocol for Chinese economics or management journal
  papers when explicitly invoked, or when zh-empirical-paper-writer has routed a
  container-planning task here. Use for chapter-container definition, paragraph
  identity, sentence-obligation planning, reference-paragraph pattern extraction,
  and paragraph allocation. For active formal manuscript writing, use
  zh-empirical-paper-writer first so the target .tex file and compiled PDF remain
  the authoritative assets.
---

# Paper Assembly Protocol

## Purpose

Use this skill when the task is not merely to rewrite text, but to assemble a paper in a controlled order.

This skill is for situations where the user wants the paper built slowly, structurally, and reproducibly, not generated in one pass.

This skill does not define Chinese journal rhetoric by itself. It orchestrates the assembly order. For sentence obligations, rhetorical register, paragraph landing, and verb-adverb discipline, load `zh-journal-humanizer`. For literature-review construction and research-gap organization, load `empirical-literature-builder`.

## Non-negotiable rules

- Do not freewrite a whole chapter by default.
- Do not jump directly from an outline to polished prose.
- Treat chapter types as relatively fixed containers.
- Quality comes mainly from paragraph arrangement and sentence roles inside those containers.
- The rhetorical constraints of each sentence are governed by `zh-journal-humanizer`, not improvised inside this skill.
- Literature-review authority, topic clustering, and gap wording should follow `empirical-literature-builder` when the chapter involves review writing.
- When a reference paper is designated, prefer the adverb-verb and connector patterns that actually appear in that paper.
- Avoid introducing meta-writing verbs or inflated verbs that the reference paper does not use unless there is a clear reason.
- Every step is gated by user review. Do not move to the next step until the user has reviewed and approved the current step.
- When the user asks to review a planning layer in the manuscript or PDF, write that layer directly into the working `.tex` file as review-visible content instead of skipping ahead to prose.
- If the required current step is `paragraph套路` or `sentence身份/义务`, do not generate chapter prose, even partially. Output only the current planning layer.
- In planning layers, do not stop at naming the paragraph type. Fix both the paragraph identity and the sentence-role sequence inside that paragraph before any prose is written.
- Use one unified planning template in fixed order: `段落身份 -> 段落职责 -> 段落套路 -> 句子序列 -> 当前义务`. Do not drift between templates within one manuscript.
- If you accidentally skip a step and write prose too early, immediately roll back conceptually to the last approved step and continue from there.

## Fixed workflow

Follow this order unless the user explicitly overrides it:

1. fill the chapter or section slots
2. map the sentence obligations of the first paragraph and the last paragraph of each chapter or section
3. write the first paragraph and the last paragraph of each chapter or section as actual manuscript prose
4. decompose the reference paper's paragraphs into reusable套路
5. plan the remaining paragraphs as a套路 distribution problem
6. assign sentence roles inside each paragraph
7. if the user wants PDF review, render the current planning layer into the manuscript source for inspection
8. only then draft or revise the remaining prose

At the end of each step, stop and wait for user review before continuing.

## Step 1: Fill the chapter or section slots

For each chapter or section, first decide:
1. what this unit must do
2. what it should not do
3. how it connects from the previous unit
4. what object it hands to the next unit

Deliverable:
- a chapter or section container map
- a fixed-paragraph identity map, at minimum marking whether a paragraph is 本章首段, 本章末段, 本节首段, 本节末段, 承上启下段, or 证据铺陈段

Do not draft middle paragraphs before this is fixed.

## Step 2: Map sentence obligations for the first and last paragraph

Before writing prose, map the sentence obligations of the opening and closing paragraphs.

Opening paragraph usually needs a controlled sequence such as:
1. authority-launch or context sentence
2. chapter-task sentence
3. problem-narrowing sentence
4. response or roadmap sentence when needed

Closing paragraph usually needs a controlled sequence such as:
1. local finding or section-summary sentence
2. unresolved-point compression sentence
3. handoff sentence to the next unit

For this step, rely on `zh-journal-humanizer` for sentence-role obligations:
- `context -> problem -> response`
- `claim -> reason -> evidence -> warrant`
- point not buried in the middle
- `old before new`
- actions carried by verbs

Deliverable:
- a sentence-obligation table for the first paragraph
- a sentence-obligation table for the last paragraph
- when relevant, an `S1-S5` sentence-role sequence for each fixed paragraph identity that is already in scope

After delivering these tables, stop and wait for user review.

## Step 3: Write the first and last paragraph first

For each chapter or section, write the opening and closing paragraphs as actual manuscript text, not merely as a function list.

Opening paragraph should usually do four things:
1. state the unit task
2. connect to the previous unit
3. narrow the problem handled here
4. preview the order when useful

Closing paragraph should usually do three things:
1. summarize what has been established
2. compress the unresolved issue into one line
3. hand off naturally to the next unit

Deliverable:
- the full text of the first paragraph
- the full text of the last paragraph

After delivering these two paragraphs, stop and wait for user review. Do not write the middle paragraphs yet.

## Step 4: Decompose reference-paper paragraphs into套路

Do not imitate wording line by line. Extract organization patterns.

For each reference paragraph, identify:
1. paragraph role
2. opening move
3. sentence-function sequence
4. landing move
5. reusable套路 label
6. sentence-obligation pattern when relevant

Assume the paragraph inventory is small. Most paragraphs in a journal article are variants of a few stable types.

Deliverable:
- a paragraph套路 inventory for the designated reference paper

## Step 5: Allocate套路 across remaining paragraphs

Treat the remaining paragraphs as a distribution problem.

For the chapter under construction, decide:
1. how many middle paragraphs are needed
2. which套路 each paragraph uses
3. where repetition would fatigue the reader
4. how to vary opening and landing moves without breaking logic

Avoid repetitive rhythm such as every paragraph being `topic sentence + literature list + gap`.

Deliverable:
- a paragraph allocation table for the remaining paragraphs

## Step 6: Plan sentence roles before prose

Before writing a paragraph, label the sentence functions first.

Common sentence roles:
1. 承接句
2. 主题句
3. 展开句
4. 例证句 or mechanism sentence
5. 收束句
6. 过渡句

Each sentence should have one main job.

Also check:
1. whether the paragraph point appears early enough
2. whether the paragraph completes its local obligation
3. whether sentence openings connect old information to new information
4. whether the paragraph lands rather than drifts away

Deliverable:
- a sentence-role plan for each remaining paragraph

## Step 7: Draft or revise the remaining prose

Only after Steps 1 to 6 have been reviewed and approved should the remaining paragraphs be drafted or revised.

Deliverable:
- the remaining chapter prose

## Reference-constrained wording rule

When the user requires stylistic discipline from a designated Chinese reference paper:

1. extract the paper's actual connectors, adverb-verb pairs, and paragraph-opening verbs
2. prefer those observed combinations when revising the target manuscript
3. flag verbs that sound like writer-side meta-control rather than article-side analysis, such as overly procedural verbs if the reference paper does not use them
4. avoid inflated or AI-like verb chains even if they sound smooth

Examples of what to inspect in the reference paper:
1. `进一步分析发现`
2. `显著促进`
3. `有效提高`
4. `开始借助`
5. `尝试利用`
6. `基于此`
7. `进而`

The point is not blind imitation. The point is to keep the manuscript inside a verified rhetorical register.

## Output pattern

When using this skill, default output should be:
1. chapter container map
2. sentence-obligation table for the first and last paragraph
3. first/last paragraph manuscript text
4. paragraph套路 inventory
5. 套路 allocation table for the current chapter
6. sentence-role plan for the next paragraph to be drafted

Only produce full chapter prose after these layers are fixed and approved by the user.
