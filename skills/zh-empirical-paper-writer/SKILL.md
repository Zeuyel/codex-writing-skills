---
name: zh-empirical-paper-writer
description: >-
  Orchestrate Chinese economics and management empirical paper writing directly
  in TeX/PDF. Use when planning, drafting, revising, auditing, compiling, or
  reviewing formal manuscript sections, especially for Chinese journal prose,
  paragraph and sentence obligations, literature reviews, theory/model logic,
  post-draft audits, or replacing a TeX paragraph. Enforces that active paper
  writing edits the target .tex file and compiled PDF rather than Markdown
  drafts, and dynamically loads only the reference rules needed for the current
  task mode.
---

# Zh Empirical Paper Writer

## Purpose

Use this as the top-level controller for formal Chinese empirical paper work.
First classify the task, then load only the matching reference file(s). Do not
load every writing skill or every reference by default.

This skill is the asset governor for active manuscript writing: the authoritative
assets are the target `.tex` manuscript source and the PDF generated from it.

## Hard Asset Rules

Read `references/asset-governance.md` before any task that may change manuscript
content, planning layers, or PDF review output.

- Do not create Markdown正文草稿 by default.
- Do not place paragraph obligations, sentence obligations, or formal prose in
  `research-notes/` by default.
- Write active drafting, replacement, revision, and approved planning directly
  into the target `.tex` file.
- Keep planning that should not appear in the PDF as TeX comments.
- Render planning as visible TeX content only when the user asks for PDF review.
- When replacing "one paragraph", keep one continuous Chinese paragraph in the
  TeX source; do not insert Markdown-style hard line breaks, bullets, or blank
  lines inside that paragraph.
- After changing formal manuscript prose, compile the relevant PDF when the
  project provides a viable TeX build path.

If the target `.tex` file cannot be identified, ask for it before editing. Do
not substitute a Markdown memo unless the user explicitly asks for a separate
memo.

## Task Router

Choose exactly one primary mode, then load the listed reference. Load a second
reference only when the task crosses modes.

| Mode | Use When | Load |
| --- | --- | --- |
| `container-planning` | Chapter slots, paragraph identity, paragraph obligations, sentence obligations, 套路 allocation | `references/assembly-workflow.md` |
| `prose-drafting` | Drafting approved paragraphs or sections as manuscript prose | `references/chinese-journal-style.md` |
| `prose-revision` | Rewriting Chinese journal prose, fixing translationese, transitions, openings, landings, terms, or collocations | `references/chinese-journal-style.md` |
| `literature-review` | Literature grouping, method families, research gap, review transitions, positioning claims | `references/literature-review.md` |
| `theory-audit` | Theory model, propositions, mechanism logic, variable setup, result-driven setup risk | `references/theory-audit.md` |
| `post-draft-audit` | A paragraph or section has already been drafted and needs final Chinese academic expression audit | `references/post-draft-audit.md` |
| `pdf-review` | Compile PDF, expose planning layer for PDF inspection, or verify TeX output | `references/asset-governance.md` |

For active prose drafting or revision, also load `references/post-draft-audit.md`
before presenting the final text or considering the edit complete.

## Default Workflow

1. Identify the target `.tex` file and the build command or compiled PDF path.
2. Classify the task mode using the router.
3. Load `references/asset-governance.md` if the task touches manuscript assets.
4. Load only the mode-specific reference file(s).
5. Edit the target `.tex` file using the project's existing macros and style.
6. Preserve TeX paragraph boundaries exactly when replacing a paragraph.
7. Compile or run the project's TeX smoke command when feasible.
8. Report the `.tex` file changed, the PDF/build result, and any remaining
   blocker.

## Failure Triggers

Stop and resolve the issue when any of these occur:

- The task is active manuscript writing but no target `.tex` file is known.
- The next action would create a Markdown正文草稿 for formal manuscript text.
- Planning content would appear in the PDF without an explicit PDF-review request.
- A paragraph replacement would become a list, table, or multiple TeX paragraphs.
- A literature or novelty claim is not supported by the project's verified
  literature base.
- A TeX compile fails after an edit; inspect the log and fix local causes before
  handing back the result when the fix is in scope.

## Specialized Skills

Use this skill first for formal paper projects. Existing specialized skills can
still be used when explicitly requested or when a local environment has them as
separate tools, but do not load all of them at once. Route through this skill's
references first, then load a specialized skill only for details that are not
covered by the selected reference.
