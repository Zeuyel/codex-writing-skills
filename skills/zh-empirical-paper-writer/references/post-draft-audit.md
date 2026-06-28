# Post-Draft Audit

Use after any manuscript prose has been drafted or revised. This is a mandatory
post-writing layer, not a separate optional skill and not a first-drafting
workflow.

Any step that produces actual prose must end with this audit. Planning layers do
not require it. First paragraphs, last paragraphs, contribution paragraphs,
literature-review hats, section closings, paragraph replacements, and theory
prose always require it before the work is treated as complete.

## Contents

1. Mandatory integration
2. Audit order
3. Genre and paragraph-pattern audit
4. Claim, term, and source-grounding audit
5. Noun, verb, and anti-translationese audit
6. Sentence-role and sentence-chain audit
7. Empirical-register timing audit
8. Paragraph closing, aspect, and contribution audit
9. Repair and output rule

## 1. Mandatory Integration

After drafting or revising manuscript prose:

1. run this audit before presenting the text as acceptable
2. revise the TeX candidate when problems are found
3. only then report the audit result and build status

Do not stop at “looks smoother”. A sentence can have the right role and still
fail if its wording is source-free, its noun choice is unsupported, or its
paragraph landing is empty.

Audit against:

- the verified literature base
- the designated Chinese reference paper's register
- the project material bank, usually
  `research-notes/writing/material-banks/project_material_bank.md`
- the sentence-role plan and paragraph identity fixed earlier

## 2. Audit Order

1. Confirm the passage belongs in the current chapter or section container.
2. Check genre, paragraph identity, paragraph套路, and sentence-role sequence.
3. Check literature, novelty, contribution, method, and theory claims against
   verified project authority.
4. Check specialized terms and project-defined concepts for explicit source and
   local meaning.
5. Check noun choice, noun provenance, verb-object collocation, aspect marking,
   and reference-article register.
6. Check anti-translationese, sentence length, and sentence-to-sentence logic.
7. Check TeX source integrity, especially paragraph boundaries.
8. Compile or smoke-test the PDF when feasible.

If genre or paragraph套路 is wrong, stop sentence-level polishing and rebuild the
paragraph plan first.

## 3. Genre And Paragraph-Pattern Audit

Before sentence-level auditing, ask:

- What container is this passage in: 摘要, 引言, 理论设定, 命题, 机制讨论,
  实证设计, 结果, or 结论?
- What macro sequence should this container follow?
- What is this paragraph's identity and local job?
- What paragraph套路 is it using, and is that套路 appropriate here?
- Does each sentence serve that套路, or is the paragraph only a chain of smooth
  sentences?

Failure triggers:

- an abstract starts with broad background, technology scenery, or model
  description before the research problem
- an introduction paragraph starts with category labels before fixing the object
  and tension
- a theory paragraph states equations before the economic object and decision
  problem are fixed
- a proposition paragraph gives a result before stating the condition and
  mechanism
- a mechanism paragraph lists examples without extracting the mechanism
- a closing paragraph floats upward into significance language without landing
  the local result

For abstracts in theory, economics, and management manuscripts, default to:

```text
研究问题/理论张力 -> 现有解释不足 -> 本文对象与方法 -> 核心机制 -> 主要结论 -> 理论含义
```

## 4. Claim, Term, And Source-Grounding Audit

Flag unsupported high-level claims, including:

- broad novelty claims without verified review support
- `研究位置`
- `处理意义`
- `经验入口`
- `一般性平均效应`
- `现有研究尚未……`
- `鲜有研究讨论……`

Specialized terms are allowed only when traceable. At first use, the prose or
nearby literature setup must state:

1. which article, theory stream, or project theorem supports the term
2. what the term means in plain firm-level behavior
3. what this manuscript observes in data for that term

If no source can be named, replace the term with ordinary object-language. Do
not leave an abstract term in the manuscript just because it sounds theoretically
useful.

Flag source-free template sentences, including:

- `在……场景下讨论……问题`
- `不能只停留在……这一层面`
- `更需要进一步讨论……`
- `形成了何种组织选择`
- `在此背景下`
- `由此可见`
- `从现实情况看`
- `为了把上述……进一步落实到可观测层面`
- `要把上述……转化为可检验的经验分析`
- `经验变量`
- `释放……信号`
- `不是……而是……`
- `并不表示……`
- `这里所说的……`

If a sentence head can be deleted and the sentence becomes clearer, the original
head is probably filler rather than sourced prose.

## 5. Noun, Verb, And Anti-Translationese Audit

Check whether core nouns are grounded in the project's verified material bank and
belong to the right chapter register.

- In introduction, literature review, theory framing, and hats, prefer object
  nouns and judgment nouns already admitted by the project.
- Be cautious with method-register nouns such as `窗口`, `识别口径`, `事件窗口`,
  `估计式`, and `工具变量` unless the passage is actually discussing empirical
  design or identification.
- Replace vague landing nouns such as `相关行为`.

Check verb-object stability. Flag by default:

- `推进相关认识`
- `回顾三支文献`
- `沿着这一定位`
- `重新界定这一问题`

Apply anti-translationese repair to every manuscript passage:

1. flag abstract nouns doing verb work, such as `……的提高`, `……的实现`, or
   `……的转化`
2. replace weak-verb compounds, such as `进行研究`, `产生影响`, `发挥作用`
3. delete prepositional scaffolding such as `对于……而言`, `关于……的问题`,
   `有关……`, or `通过……来` unless it prevents ambiguity
4. replace English-style nominal subjects with event clauses when possible
5. avoid passive or causative shells that hide the actor
6. split overloaded sentences; one sentence should carry one main obligation

## 6. Sentence-Role And Sentence-Chain Audit

Each sentence must have one lawful dominant identity:

- `context`
- `problem`
- `response`
- `claim`
- `reason`
- `evidence`
- `warrant`
- `权威启动句`
- `背景定位句`
- `问题提出句`
- `观点句`
- `承接句`
- `展开句`
- `例证句`
- `warrant句`
- `收束句`
- `过渡句`

Flag by default:

- explanation-first openings such as `之所以……是因为……` when the sentence
  should open with a claim
- grouping-first literature sentences such as `主要集中在三个方面` or `可分为三类`
  when they replace a real point sentence
- pronoun-first openings such as `这一问题` before the discussion object is fixed
- meta-literature openings that announce scope but do not state a substantive
  point
- writer-side control verbs in manuscript prose such as `收束`, `压缩`, `拉回`,
  or `锚定`
- level jumps without aggregation bridges, such as `工作包 -> 问题层净收益`,
  `岗位选择 -> 企业层路径`, or `任务环节 -> 创新结果`

For adjacent sentences, check:

1. Does sentence 2 answer why sentence 1 was written?
2. Does each sentence inherit one old point and add one new point?
3. If a paragraph ends in a claim, did the previous sentence prepare it?
4. Can the paragraph be reduced to a visible chain such as
   `权威/背景 -> 现实展开 -> 问题提出` or `观点 -> 展开 -> 收束`?

If two adjacent sentences do not stand in a clear relation, rewrite, merge, or
reorder them.

## 7. Empirical-Register Timing Audit

Check whether the sentence uses method-stage diction too early.

In introduction, literature review, theory framing, chapter hats, and
problem-setting paragraphs, usually prefer:

- `关注`
- `回答`
- `讨论`
- `说明`
- `解释`
- `刻画`
- `考察`
- `提出`

Reserve these for research design, identification strategy, empirical model,
results, mechanism tests, robustness, and appendices:

- `识别`
- `估计`
- `检验`
- `因果识别`
- `工具变量`
- `DID`

Flag by default:

- `本文真正希望识别……`
- `本文识别……`
- `本文估计……`
- `本文检验……`
- `本文的贡献在于识别……`

If the sentence is setting up the question or contribution, replace empirical
verbs with framing verbs. If it is really about later empirical work, rewrite it
as a handoff.

## 8. Paragraph Closing, Aspect, And Contribution Audit

A valid closing sentence should compress the local literature or mechanism,
sharpen the gap, or hand the object to the next section with a substantive
landing.

Flag procedural endings:

- `在此基础上，进一步提出本文需要回应的核心问题`
- `下文将对上述问题展开分析`
- `以下分别讨论……`
- `由此引出下文……`

For literature-review endings, prefer:

```text
已有研究分别说明了什么 -> 尚缺什么 -> 本文转向何对象
```

Check aspect marking for prior literature. Use completed forms when the sentence
expresses completed accumulation, shift, consensus, or prior handling, such as
`展开了讨论`, `积累了成果`, `形成了共识`, or `转向了机制分析`.

For contribution paragraphs, enforce:

1. existing studies usually do X
2. this paper instead does Y
3. therefore this paper can answer Z

Do not allow contribution prose to praise itself before naming the actual move.

## 9. Repair And Output Rule

When the audit finds problems, revise the TeX prose rather than only reporting
the issue, unless the user asked for review only.

Repair in this order:

1. remove unsupported abstractions
2. fix genre and paragraph-pattern failures
3. fix sentence-identity violations
4. fix empirical-register timing violations
5. fix noun provenance and chapter-register mismatches
6. fix noun choice and verb-object collocation
7. repair sentence-to-sentence logic
8. shorten overloaded sentences
9. restore paragraph landing
10. re-check contribution wording against verified literature support

Keep the final manuscript paragraph continuous in the TeX source when the user
asked for one paragraph. Report:

1. `审计结论`
2. concrete high-risk expressions found and repaired
3. the revised TeX location or revised paragraph
4. residual risks needing user or literature confirmation

Do not create a separate Markdown change note for formal manuscript writing.
