---
name: empirical-literature-builder
description: >-
  Compatibility wrapper for legacy $empirical-literature-builder invocations
  only. Do not use as a default entry point for formal Chinese empirical paper
  writing; use zh-empirical-paper-writer instead, which owns TeX/PDF asset
  governance and routes literature-review tasks to references/literature-review.md.
---

# Empirical Literature Builder

This legacy skill is kept only for explicit user invocations and backward
compatibility.

For formal manuscript literature-review work, use `zh-empirical-paper-writer` and
route the task to `references/literature-review.md`. Do not run an independent
review-writing workflow here, and do not create Markdown manuscript drafts from
this wrapper.

If the user explicitly invoked this legacy name, state that the active rules now
live under `zh-empirical-paper-writer`, then continue through that skill's
`literature-review` route.
