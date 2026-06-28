# Asset Governance

## Authoritative Assets

For active formal paper writing, maintain only:

1. the target manuscript `.tex` source
2. the PDF compiled from that source

Do not create Markdown manuscript drafts by default. Do not move paragraph
obligations, sentence obligations, or draft prose into `research-notes/` unless
the user explicitly asks for a separate memo.

The known failure pattern is writing formal P2/P3 drafts to
`research-notes/writing/manuscript-structure/...` when the correct destination is
the target TeX file, such as
`tex/05_ai_org_high_grade_product_model/service_offering_upgrade_reduced_form_model.tex`.

## Selecting The Target TeX File

1. Use the file named by the user when provided.
2. If the user names a chapter, section, or PDF but not a source file, inspect
   the project's TeX tree, root files, `\input{}` and `\include{}` structure, and
   build files to identify the likely source.
3. If more than one plausible target remains, ask before editing.
4. If no TeX project exists, explain that active manuscript writing needs a
   target `.tex` file before formal prose can be installed.

## Planning Layer

Use TeX comments for planning that should not appear in the PDF.

Acceptable hidden planning:

```tex
% 段落身份：本节首段
% 段落职责：界定本节讨论对象并交代后续顺序
% 句子序列：S1 背景定位；S2 问题提出；S3 本节任务
```

Do not insert raw Markdown headings, bullets, or tables into TeX manuscript
content unless they are inside comments or the project already uses a compatible
macro for review notes.

## PDF Review Mode

Render planning as visible TeX content only when the user asks to inspect the
planning layer in PDF.

When doing so:

1. use existing project macros or plain TeX-compatible prose/list structures
2. make the review-only status clear in the visible text
3. keep formal manuscript prose separate from review-visible planning
4. remove or hide review-visible planning after the review if the user approves
   the prose-only version

## Paragraph Replacement Rule

When the user asks to replace one paragraph, the replacement must remain one
logical TeX paragraph.

- Use one continuous Chinese paragraph in the TeX source.
- Do not turn the replacement into bullets, numbered lists, Markdown headings, or
  sentence-per-line drafting.
- Do not insert a blank line inside the replacement.
- Preserve citations, labels, math, and macros that remain semantically needed.
- If the original paragraph contains TeX commands, preserve the surrounding
  command structure unless the prose change requires otherwise.

## Build And Smoke

After active manuscript edits:

1. find the project build command from `README`, `Makefile`, `justfile`,
   `latexmkrc`, CI config, or existing scripts
2. prefer the project's existing command over an invented command
3. if no command is documented, infer the root TeX file before trying `latexmk`
4. compile the PDF when the local toolchain is available
5. if compilation fails, inspect the log and fix local TeX errors caused by the
   edit before reporting back

Report the edited `.tex` path, the build command used, and the PDF path or
compile failure.
