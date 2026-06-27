---
name: zh-journal-humanizer
description: >-
  Rewrite or review Chinese academic prose in a natural Chinese economics and
  management journal style when explicitly invoked for isolated prose work, or
  when zh-empirical-paper-writer has routed a prose-revision or post-draft wording
  task here. Use for 帽子段, paragraph transitions, openings and closings,
  sentence obligations, term and collocation discipline, and anti-translationese.
  For formal paper drafting in a project, use zh-empirical-paper-writer first so
  prose changes are written directly to TeX/PDF rather than Markdown drafts.
---

# Zh journal humanizer

## Overview

Edit Chinese academic writing so it reads like a polished economics or management journal manuscript, not a direct translation of English academic prose and not a generic AI rewrite.

Prioritize structure before wording:
1. Fix chapter or section task framing.
2. Repair paragraph-to-paragraph movement.
3. Repair sentence-to-sentence buildup and landing.
4. Enforce sentence roles and sentence obligations before surface rewriting.
5. Enforce verb-adverb discipline from the designated reference paper when one exists.
6. Run a final anti-AI pass on vocabulary, rhythm, and filler.

For manuscript drafting, do not jump directly to full freewriting. Treat chapters as fixed containers and complete them in staged order.

This skill governs the rhetorical discipline of the prose itself. If the task is chapter-by-chapter assembly, pair this skill with `paper-assembly-protocol`. If the task is literature review construction, pair this skill with `empirical-literature-builder`.

## Core rules

- Keep formal, neutral, and disciplined academic Chinese. Do not add colloquial personality, first-person commentary, chatty warmth, or motivational tone.
- Preserve the paper argument, variables, equations, and identification logic unless the user asks for substantive changes.
- Prefer Chinese academic rhetorical logic over literal English calques.
- In literature reviews, do not begin paragraphs with abstract meta-labels such as `研究线索`, `第一类文献`, `第二类文献`, or `第三类文献`.
- For Chinese-journal literature reviews, prefer this native sequence: discussion object or concrete problem -> representative prior handling -> local consensus -> specific insufficiency -> bridge to this paper.
- Do not stop at fixing paragraph identity. For any fixed paragraph such as 本节首段, 本节末段, 本小节首段, 本小节末段, or 承上启下段, also fix the sentence-role order sentence by sentence before any prose drafting.
- Avoid category-first sentence assembly copied from English academic prose. Let the sentence open from the current object, problem, or result under discussion, then advance to the author's judgment.
- Treat `empirical` as `实证上`, `实证层面`, or `实证部分` depending on context. Do not default to `经验上` when the meaning is empirical analysis.
- When a term has a more native Chinese-journal equivalent, prefer it. Examples: `regime` -> `区间`, `状态区间`, or `组织区间`; `theory-driven empirical paper` -> `理论驱动的实证研究`.
- Remove implementation details from the main text when they are not the direct contribution of the paper. Examples: Lean4 verification, compilation workflow, coding pipeline, data cleaning scripts, prompt engineering process.
- Do not inflate significance. Avoid slogan-like claims, broad era narratives, and empty high-level judgments that do not serve the paragraph task.
- Do not write literature-gap, novelty, or authority claims unless they have been checked against the user's curated literature base, preferably Scopus or WoS exports, EndNote libraries, BibTeX or RIS exports, or project review notes built from them.
- If literature review authority is incomplete, keep positioning language provisional and move speculative judgments to notes rather than the manuscript body.
- Do not generate full chapter prose in one pass unless the user explicitly asks for that. Default to staged planning first, paragraph execution second.
- When the user is currently reviewing `paragraph套路` or `sentence身份/义务`, do not turn those plans into prose. Keep the output at the planning layer, even if a prose draft seems easy to produce.
- If the user asks to inspect the planning layer in PDF, write the planning layer itself into the `.tex` manuscript as review-visible content rather than silently advancing to prose.
- Do not rely on generic “smooth” Chinese. When the user has designated a Chinese reference article, verb-adverb choices should be constrained by combinations actually used in that article.
- Sentence roles are not labels only. Each sentence role carries an obligation. A sentence that does not discharge its obligation should be deleted, merged, or reassigned.
- Prefer visible argument order. Do not bury the paragraph point in the middle.
- Prefer `old before new`: sentence openings should connect to what the reader already knows from the previous sentence or previous paragraph, then move to the new information.
- Prefer actions in verbs rather than hiding them in abstract nouns. Avoid over-nominalized phrases when a direct verb can carry the analysis more clearly.
- Enforce Chinese sentence-length discipline: prefer one sentence for one main obligation; when a sentence is carrying object definition, literature positioning, and gap extraction at the same time, split it.
- For chapter openings, section openings, and section closings, prefer 3-5 shorter sentences over one long sentence with multiple subordinate clauses.
- If a sentence has more than two layers of modification, repeated connectors such as `并` / `同时` / `而`, or multiple comma-separated tasks, rewrite it into shorter main-clause sentences.

## Sentence-role framework

Use `The Craft of Research` as the upper-level control rule for sentence movement.

### A. Three macro obligations

At the chapter opening, section opening, paragraph opening, or local argument turn, test whether the prose completes the following sequence when the context requires it:
1. `context`: give the reader the location of the discussion
2. `problem`: show what is missing, conflicting, difficult, or unresolved
3. `response`: state what this paper, this section, or this paragraph will do next

This does not mean every paragraph must mechanically contain all three. It means the local passage must not leave the reader without orientation, problem pressure, or response direction.

### B. Four argument obligations

When a sentence cluster is making an analytical claim, test whether the local argument eventually completes:
1. `claim`: what is being asserted here
2. `reason`: why this claim is plausible in the paper's logic
3. `evidence`: what literature fact, institutional fact, data fact, or model result supports it
4. `warrant`: why this evidence is relevant to that claim in this context

Do not assume the warrant is obvious. In Chinese journal prose, the warrant is often carried by a transition sentence, a narrowing sentence, or a landing sentence.

### C. Paragraph-point rule

- The paragraph point cannot be hidden in the middle behind two or three vague setup sentences.
- If a paragraph opens with background, the point must emerge early enough that the reader knows why the background is being given.
- If a paragraph ends with citations only, it usually has not landed.

## Sentence roles and obligations

Use the following sentence-role inventory. A sentence can have a dominant role and a secondary role, but never pile up unrelated tasks.

1. `权威启动句`
   Obligation: borrow externally recognized authority to secure the legitimacy of the discussion opening, such as policy text, institutional change, stylized fact, or high-confidence literature consensus.
   Constraint: authority must be relevant to the chapter task, not decorative.

2. `背景定位句`
   Obligation: tell the reader where the discussion is located and why this domain matters for the paper's object.
   Constraint: background is not a slogan zone. It must narrow, not sprawl.

3. `问题提出句`
   Obligation: identify the unresolved tension, inconsistency, omission, or difficulty that makes the next sentences necessary.
   Constraint: the problem must be concrete enough to generate a response.

4. `观点句`
   Obligation: give the paragraph's main point or the section's local conclusion.
   Constraint: do not bury it; do not make it verbally soft when the paragraph actually depends on it.

5. `承接句`
   Obligation: connect the new sentence or paragraph to the already established context.
   Constraint: it must carry forward a real old point, not just insert a habitual connector.

6. `展开句`
   Obligation: unpack the mechanism, distinction, or internal logic of the观点句.
   Constraint: each展开句 should advance one step, not reopen the whole paragraph.

7. `例证句`
   Obligation: provide a representative literature example, institutional fact, measurement fact, or model implication.
   Constraint: examples must support an already stated point; they should not substitute for the point.

8. `warrant句` or `解释关联句`
   Obligation: explain why the cited evidence or described mechanism is relevant to the point being argued.
   Constraint: if the reader could ask “这能说明什么”, the warrant is missing.

9. `收束句`
   Obligation: close the paragraph by extracting the local conclusion.
   Constraint: do not end with an empty significance sentence.

10. `过渡句`
    Obligation: hand off one unresolved aspect, one narrower question, or one next analytical step to the following paragraph or section.
    Constraint: transition must emerge from the current paragraph's landing, not be bolted on.

## Workflow

### Review-specific sequencing

For literature-review sections, paragraph openings should normally answer "现在讨论的对象是什么" before answering "这类文献叫什么".

Preferred opening moves:
1. the concrete phenomenon, empirical difficulty, or measurement problem under discussion
2. how existing studies have handled that object
3. what has become relatively clear
4. what remains insufficient for this paper
5. which bridge literature or transition leads to the next block

Disallowed default openings unless the user explicitly asks for them:
1. `现有文献可分为三类`
2. `第一类文献` / `第二类文献` / `第三类文献`
3. `围绕这一问题形成了三条研究线索`

Fixed paragraph identities that should usually be declared separately in review planning:
1. 本节首段
2. 本节末段
3. 本小节首段
4. 本小节末段
5. 承上启下段
6. 证据铺陈段

For each fixed paragraph identity, also fix a sentence-role sequence such as `S1-S5` before drafting prose.

Unified planning-layer template:
1. 段落身份
2. 段落职责
3. 段落套路
4. 句子序列
5. 当前义务

Do not change the field order across paragraphs within the same manuscript.

### 0. Use the fixed drafting sequence

For article drafting or restructuring, use this sequence unless the user overrides it:
1. fill the chapter or section slots first
2. draft only the first paragraph and the last paragraph of each chapter or section
3. decompose reference-paper paragraphs into reusable套路
4. assign套路 across the remaining paragraphs to avoid monotony
5. plan each paragraph sentence by sentence before writing prose

The key claim is that section types are relatively fixed. Quality mainly comes from the internal arrangement of paragraphs and sentences, not from improvising whole chapters at once.

### 1. Read by structural level

Inspect the text in this order:
1. chapter or section
2. paragraph
3. sentence

Do not start with wordsmithing. Start by locating where the structure breaks.

Before structural editing, check whether the passage contains literature-positioning or novelty claims. If it does, verify whether those claims are supported by a curated literature base. If not, mark them as provisional or remove them from the manuscript draft.

### 2. Fill chapter and section containers first

Before writing paragraphs, identify the fixed role of each chapter or section.

For a typical economics or management empirical paper, first decide:
1. what this chapter must do
2. what it should not do
3. how it connects from the previous chapter
4. what object it must hand over to the next chapter

Do not draft middle paragraphs before this container-level role is fixed.

### 3. Write the first and last paragraph first

For each chapter or section, write the opening and closing paragraphs before drafting the middle.

Opening paragraph usually has a fixed job:
1. state the task of this chapter or section
2. connect it to the previous chapter or section
3. narrow attention to the specific issue handled here
4. preview the order when useful

Closing paragraph usually has a fixed job:
1. summarize what this chapter or section has established
2. compress the unresolved part into one line
3. hand off naturally to the next chapter or section

These two paragraph types are relatively stable and should not be improvised each time.

Before surface drafting, first map the sentence obligations inside these opening and closing paragraphs.

### 4. Build a paragraph套路 inventory from reference papers

When a reference paper is available, do not merely imitate wording. Extract paragraph organization patterns.

Typical reusable套路 usually include only a limited number of types, for example:
1. problem-difficulty -> existing handling -> gap
2. grouped literature -> consensus -> specific insufficiency
3. mechanism split -> conditional distinction -> paragraph landing
4. concept definition -> boundary clarification -> why it matters here
5. empirical challenge -> measurement response -> handoff to method
6. section mini-summary -> transition to next block

For each reference paragraph, identify:
1. paragraph type
2. paragraph task
3. sentence order
4. opening move
5. landing move
6. sentence-role sequence
7. whether the paragraph completes `context -> problem -> response`
8. whether the argument completes `claim -> reason -> evidence -> warrant`

### 5. Assign remaining paragraph套路 statistically

After opening and closing paragraphs are fixed, do not let the middle paragraphs all use the same pattern.

Treat the remaining paragraphs as a distribution problem:
1. estimate how many paragraphs this chapter should have
2. choose which套路 each paragraph uses
3. avoid using the same opening move or landing move repeatedly in adjacent paragraphs
4. avoid repetitive rhythm such as every paragraph = topic sentence + two citations + gap sentence

The goal is not novelty for its own sake. The goal is to reduce reader fatigue while keeping the logic easy to track.

### 6. Plan each paragraph sentence by sentence

Before writing a paragraph, first assign sentence roles.

A paragraph usually needs some of these sentence functions:
1. 承接句
2. 主题句
3. 展开句
4. 文献例证句 or mechanism sentence
5. 收束句
6. 过渡句

Not every paragraph needs all six, but each sentence must have a job. Do not allow stacked sentences that perform multiple unrelated functions at once.

For each paragraph plan, also check:
1. whether the paragraph point appears early enough
2. whether sentence openings honor `old before new`
3. whether key actions are expressed in verbs rather than abstract nominal bundles
4. whether the paragraph has a real landing rather than a generic value claim

### 7. Enforce verb-adverb discipline

When a designated Chinese reference paper exists, do not stop at paragraph logic. Also control the micro-level wording.

Use this sequence:
1. extract the reference paper's actual connectors
2. extract the reference paper's actual adverb-verb and verb-object combinations
3. compare the target passage against this inventory
4. replace ungrounded writer-side meta verbs or inflated AI-style verb chains
5. keep the target prose inside the verified rhetorical register

Pay special attention to:
1. paragraph-opening verbs
2. transition phrases
3. adverb-verb pairs such as `进一步分析发现` and `显著促进`
4. verb-object pairs such as `提高效率`, `推动创新`, `打破惯例`, `开展行动`, `利用数据`

If a target passage uses verbs like `收束`, `压缩`, `固定`, `拉回`, `写成`, `锚定`, `统摄` in the manuscript body, check whether these are writer-side control words rather than article-side analysis words. Replace them unless they are unavoidable.

### 8. Repair paragraph transitions

Check whether each paragraph has a reason to come after the previous one.
- The first sentence should either 承接上文, 转入新问题, or explain why the next step is needed.
- The last sentence should 落到本段结论, or bridge to the next paragraph.
- If two adjacent paragraphs make similar points without movement, merge or differentiate them.

### 9. Repair sentence movement inside the paragraph

Treat each paragraph as a mini-argument.
- Give each sentence one main job.
- Use a natural order: set up the point, explain the mechanism or problem, narrow the implication, land the paragraph.
- Break long stacked sentences that simultaneously do background, literature, mechanism, contribution, and preview.
- Prefer explicit causal or rhetorical connectors when the logic may otherwise jump.
- If a sentence claims authority, ask what obligation that authority is serving.
- If a sentence provides evidence, ask whether the warrant is visible.

### 10. Decide what should not be written

Delete or compress material that does not belong in the manuscript main line.
- implementation details
- proof assistant or coding workflow details
- text that only repeats the previous paragraph in new words
- self-congratulatory contribution claims
- generic final sentences with no analytical landing
- empty phrases such as `具有重要意义` and `提供有益启示` unless followed by a concrete claim

### 11. Run a Chinese academic anti-AI pass

After structural repair, remove common AI tells:
- abstract nouns piled too densely
- inflated verbs such as `重塑`, `赋能`, `深化`, `激发` used without a concrete object
- translated-English contrasts like `不是……而是……` used mechanically
- symmetrical three-part lists everywhere
- repetitive `一方面/另一方面` with no real contrast
- repeated `这意味着`, `由此可见`, `需要指出的是` when not needed
- vague emphasis such as `更为关键`, `尤为重要`, `具有深远影响` with no analytic payoff
- smooth but ungrounded verb-adverb pairings that do not appear in the designated reference register

## Preferred writing moves

Prefer a conservative verb inventory when the reference paper supports it.

Examples of relatively safe verbs:
`考察`, `分析`, `发现`, `利用`, `提高`, `促进`, `推动`, `识别`, `衡量`, `表明`, `说明`, `探讨`, `开展`, `优化`

Use more abstract research verbs such as `界定`, `刻画`, `推导`, `构建`, `收束` only when the passage is genuinely methodological or theoretical and the wording does not pull the manuscript out of Chinese journal register.

Use connectors to make the logic visible, not decorative:
`基于此`, `进一步`, `进一步地`, `同时`, `例如`, `然而`, `因此`, `进而`, `具体地`

Do not force every paragraph to use the same connector. Vary only when the logic changes.

## Output pattern

When rewriting:
1. diagnose structural problems briefly
2. if drafting from scratch, start with chapter slots and paragraph plans rather than full prose
3. if a reference paper is designated, diagnose risky verb-adverb combinations before rewriting
4. if the task is to design prose, first produce a sentence-obligation table for the target paragraph
5. rewrite by section or paragraph only after the sentence obligations are fixed
6. keep terminology consistent across the whole text
7. if useful, note recurring issues such as `帽子段缺位`, `段间跳跃`, `句子堆叠`, `术语不统一`, `动词失真`, `副词过满`, `义务缺位`, `落点缺位`

When the user asks for direct editing, perform the edit rather than only describing it, but still respect the staged workflow unless the user explicitly requests full prose immediately.

## Resources

- For ready-to-use section-opening and transition templates, read `references/hat-and-transition-templates.md`.
- For terminology choices and a deletion checklist, read `references/term-and-deletion-rules.md`.
- For literature authority and anti-overreach rules, read `references/literature-authority-and-process.md`.
- For reference-constrained verb-adverb discipline, read `references/verb-adverb-discipline.md`.
- For dynamic lexical loading, read only the needed file among `references/verb-library.md`, `references/noun-library.md`, `references/adverb-library.md`, and `references/collocation-library.md`.
