# Chinese Journal Style

Use for `prose-drafting` and `prose-revision`.

## Drafting Into TeX

Draft or revise directly in the target `.tex` file when the task is formal
manuscript writing. Do not prepare a Markdown正文草稿 first.

For a paragraph replacement, keep the result as one continuous Chinese paragraph
in TeX source. Do not split the paragraph into sentence-per-line drafts.

## Register

Keep the prose formal, neutral, and disciplined. Prefer Chinese economics and
management journal logic over literal English academic syntax.

Default movement:

1. locate the object or problem under discussion
2. state the local claim or task early enough
3. unfold the mechanism, evidence, or literature handling
4. land on a concrete implication or handoff

Avoid slogan-like significance, broad era narration, and empty upward floating.

## Anti-Translationese Checks

Repair these before accepting a sentence:

1. abstract nouns doing verb work, such as `……的提高`, `……的实现`, or `……的转化`
2. weak verb shells, such as `进行研究`, `产生影响`, `发挥作用`
3. prepositional scaffolding that delays the object, such as `对于……而言` or
   `关于……的问题`
4. English-style category-first openings, such as `第一类文献` or `三条研究线索`
5. passive or causative shells that hide the actual actor
6. overlong sentences carrying more than one main obligation

Prefer direct subjects, visible verbs, and shorter sentences when the sentence
is doing too much.

## Collocation Discipline

Before keeping a low-frequency noun, verb-object pair, or adverb-verb pair:

1. check the project's material bank if one exists, usually
   `notes/material_banks/project_material_bank.md`
2. check designated Chinese reference articles when provided
3. otherwise use a simpler high-frequency academic expression

Stable defaults include:

- `展开了讨论`
- `积累了成果`
- `形成了共识`
- `揭示了机制`
- `提供了证据`
- `纳入统一框架`
- `进一步分析`
- `较为系统地讨论`

Avoid unsupported defaults such as `推进相关认识`, `相关行为`, `新证据`, and
category labels that substitute for argument.

## After Drafting

After drafting or revising manuscript prose, load `post-draft-audit.md` and run
an audit pass before treating the text as final.
