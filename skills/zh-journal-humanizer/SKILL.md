---
name: zh-journal-humanizer
description: >-
  Compatibility wrapper for legacy $zh-journal-humanizer invocations only. Do
  not use as a default entry point for formal Chinese empirical paper writing;
  use zh-empirical-paper-writer instead, which owns TeX/PDF asset governance and
  routes prose-drafting, prose-revision, and post-draft wording tasks to
  references/chinese-journal-style.md and references/post-draft-audit.md.
---

# Zh Journal Humanizer

This legacy skill is kept only for explicit user invocations and backward
compatibility.

For formal manuscript prose, use `zh-empirical-paper-writer` and route the task
to `references/chinese-journal-style.md`. Do not run an independent humanizing
workflow here, and do not create Markdown manuscript drafts from this wrapper.

If the user explicitly invoked this legacy name, state that the active rules now
live under `zh-empirical-paper-writer`, then continue through that skill's
`prose-revision` or `post-draft-audit` route.
