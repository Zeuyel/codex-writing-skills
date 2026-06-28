# Assembly Workflow

Use for `container-planning`: chapter containers, paragraph identities,
paragraph obligations, sentence obligations, and paragraph-pattern allocation.

## Contents

1. Core constraints
2. Fixed staged workflow
3. Chapter and section containers
4. First and last paragraphs
5. Reference-paragraph pattern inventory
6. Paragraph allocation
7. Sentence-role planning
8. Output discipline

## 1. Core Constraints

Planning is not a Markdown deliverable during active manuscript work. When a
target `.tex` file exists, install approved planning in TeX comments near the
affected passage. Keep it hidden from the PDF unless the user requests PDF
review.

- Do not freewrite a whole chapter by default.
- Do not jump directly from an outline to polished prose.
- Treat chapter, section, and subsection types as fixed containers before
  writing.
- Fix the target section or subsection before planning individual paragraphs.
  A paragraph cannot be drafted only from a loose topic; it must belong to a
  named or working-titled section container.
- Quality comes mainly from paragraph arrangement and sentence roles inside
  containers, not from one-pass generation.
- Every staged planning step is gated by user review unless the user explicitly
  asks for direct execution.
- If the current step is `paragraph套路` or `sentence身份/义务`, do not generate
  chapter prose. Keep output at the planning layer.
- Use one planning template in fixed order:
  `段落身份 -> 段落职责 -> 段落套路 -> 句子序列 -> 当前义务`.

If wording becomes in scope, load `chinese-journal-style.md`. If the chapter is
a literature review, load `literature-review.md`.

## 2. Fixed Staged Workflow

Follow this order unless the user explicitly overrides it:

1. fill the chapter slots
2. fix target section or subsection slots, including titles or working titles
3. define each section's task, boundary, and handoff
4. map sentence obligations for first and last paragraphs
5. write first and last paragraphs as manuscript prose
6. decompose reference-paper paragraphs into reusable套路
7. allocate套路 across the remaining paragraphs
8. assign sentence roles inside each remaining paragraph
9. render the planning layer into TeX only if PDF review is requested
10. draft or revise remaining prose after the planning layer is approved

If prose was written too early, roll back conceptually to the last approved
planning layer and continue from there.

## 3. Chapter And Section Containers

For each chapter, section, or subsection, decide before drafting:

1. what this unit must do
2. what it should not do
3. how it connects from the previous unit
4. what object it hands to the next unit
5. what title or working title identifies this unit in the manuscript
6. which paragraphs belong inside this unit

Minimum deliverables:

- chapter or section container map
- section/subsection slot map with titles or working titles
- section-level task, boundary, and handoff statement
- paragraph inventory for each section before prose
- fixed paragraph identity map
- local handoff between adjacent units

If the section is not fixed, stop at container planning. Do not draft a paragraph
and decide later which section it belongs to.

Common paragraph identities:

- 本章首段
- 本章末段
- 本节首段
- 本节末段
- 本小节首段
- 本小节末段
- 承上启下段
- 证据铺陈段
- 机制展开段
- 研究设计交代段

Do not draft middle paragraphs before fixed paragraph identities are known.

## 4. First And Last Paragraphs

Opening paragraphs usually need:

1. authority, context, or previous-unit connection
2. unit task
3. problem narrowing
4. response or roadmap when useful

Closing paragraphs usually need:

1. local finding or section summary
2. unresolved-point compression
3. handoff to the next unit

Before writing either paragraph, map the sentence obligations. The default macro
sequence is `context -> problem -> response`. For local arguments, check
`claim -> reason -> evidence -> warrant`.

## 5. Reference-Paragraph Pattern Inventory

When a Chinese reference paper is provided, extract organization patterns rather
than imitating wording.

For each reference paragraph, record:

1. paragraph role
2. paragraph task
3. opening move
4. sentence-function sequence
5. landing move
6. reusable套路 label
7. whether it completes `context -> problem -> response`
8. whether it completes `claim -> reason -> evidence -> warrant`

Typical reusable patterns:

- problem difficulty -> existing handling -> gap
- grouped literature -> consensus -> specific insufficiency
- mechanism split -> conditional distinction -> landing
- concept definition -> boundary clarification -> why it matters here
- empirical challenge -> measurement response -> handoff to method
- section mini-summary -> transition to next block

## 6. Paragraph Allocation

Treat remaining paragraphs as a distribution problem.

For the current chapter or section:

1. estimate how many middle paragraphs are needed
2. assign one primary套路 to each paragraph
3. avoid identical opening moves in adjacent paragraphs
4. avoid identical landing moves in adjacent paragraphs
5. avoid turning every paragraph into `topic sentence + literature list + gap`

Variation serves readability; it must not break the paper's logic.

## 7. Sentence-Role Planning

Before writing a paragraph, assign one dominant job to each sentence.

Common roles:

1. `权威启动句`
2. `背景定位句`
3. `问题提出句`
4. `观点句`
5. `承接句`
6. `展开句`
7. `例证句` or mechanism sentence
8. `warrant句` or `解释关联句`
9. `收束句`
10. `过渡句`

Check every sentence-role plan:

- The paragraph point appears early enough.
- Sentence openings follow old information before new information.
- Key actions are carried by verbs rather than abstract nouns.
- Evidence is followed by a visible warrant.
- The paragraph lands rather than ending with citations or generic value.

## 8. Output Discipline

For active manuscript work, the durable output is the target `.tex` file.

When the user is reviewing planning, output the planning layer only. When the
user approves drafting, write prose into TeX and then run `post-draft-audit.md`.
