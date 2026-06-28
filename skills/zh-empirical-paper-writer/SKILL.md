---
name: zh-empirical-paper-writer
description: >-
  Primary and only default entry point for Chinese economics and management
  empirical paper writing in TeX/PDF. Use when planning, drafting, revising,
  auditing, compiling, or reviewing formal manuscript sections, including
  paragraph and sentence obligations, Chinese journal prose, literature reviews,
  theory/model logic, post-draft audits, PDF review, or replacing a TeX
  paragraph. Enforces that active manuscript work edits the target .tex source
  and compiled PDF instead of Markdown drafts, and dynamically loads only the
  needed reference rules.
---

# Zh Empirical Paper Writer

## Purpose

Use this as the single default controller for formal Chinese empirical paper
work. First classify the task, then load only the matching reference file. Do not
load legacy writing skills as separate default entry points.

This skill owns the asset rule for active manuscript writing: the authoritative
assets are the target `.tex` manuscript source and the PDF generated from it.

## Hard Asset Rules

Read `references/asset-governance.md` before any task that may change manuscript
content, planning layers, or PDF review output.

- Edit the target `.tex` file by default for active paper writing.
- Treat the PDF as the review asset compiled from that `.tex` file.
- Do not create Markdown正文草稿 by default.
- Do not place paragraph obligations, sentence obligations, or formal prose in
  `research-notes/` by default.
- Keep hidden planning in TeX comments.
- Render planning as visible TeX content only when the user asks for PDF review.
- When replacing "one paragraph", keep one continuous Chinese paragraph in the
  TeX source; do not insert Markdown-style hard line breaks, bullets, or blank
  lines inside that paragraph.

If the target `.tex` file cannot be identified, ask for it before editing. Do
not substitute a Markdown memo unless the user explicitly asks for a separate
memo.

## Task Router

Choose exactly one primary mode. Load a second reference only when the task
crosses modes.

| Mode | Use When | Load |
| --- | --- | --- |
| `container-planning` | Chapter slots, paragraph identity, paragraph obligations, sentence obligations, 套路 allocation | `references/assembly-workflow.md` |
| `prose-drafting` | Drafting approved paragraphs or sections as manuscript prose | `references/chinese-journal-style.md` |
| `prose-revision` | Rewriting Chinese journal prose, fixing translationese, transitions, openings, landings, terms, or collocations | `references/chinese-journal-style.md` |
| `literature-review` | Literature grouping, method families, research gap, review transitions, positioning claims | `references/literature-review.md` |
| `theory-audit` | Theory model, propositions, mechanism logic, variable setup, result-driven setup risk | `references/theory-audit.md` |
| `post-draft-audit` | A paragraph or section has already been drafted and needs final Chinese academic expression audit | `references/post-draft-audit.md` |
| `pdf-review` | Compile PDF, expose planning layer for PDF inspection, or verify TeX output | `references/asset-governance.md` |

For active prose drafting or revision, load `references/post-draft-audit.md`
before presenting the final text or considering the edit complete.

## Default Workflow

1. Identify the target `.tex` file and the build command or compiled PDF path.
2. Classify the task mode using the router.
3. Load `references/asset-governance.md` if the task touches manuscript assets.
4. Load only the mode-specific reference file.
5. Edit the target `.tex` file using the project's existing macros and style.
6. Preserve TeX paragraph boundaries exactly when replacing a paragraph.
7. Compile or run the project's TeX smoke command when feasible.
8. Report the `.tex` file changed, the PDF/build result, and any blocker.

## Failure Triggers

Stop and resolve the issue when any of these occur:

- Active manuscript writing has no known target `.tex` file.
- The next action would create a Markdown正文草稿 for formal manuscript text.
- Planning content would appear in the PDF without an explicit PDF-review request.
- A paragraph replacement would become a list, table, or multiple TeX paragraphs.
- A literature, novelty, or contribution claim is unsupported by the verified
  literature base.
- A TeX compile fails after an edit; inspect the log and fix local causes before
  handing back the result when the fix is in scope.

## Legacy Skills

Legacy skill folders for `paper-assembly-protocol`, `zh-journal-humanizer`, and
`empirical-literature-builder` are compatibility wrappers only. Do not load them
as default writing entry points. Their core rules live in this skill's
`references/` files.
