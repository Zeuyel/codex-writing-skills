---
name: paper-assembly-protocol
description: >-
  Compatibility wrapper for legacy $paper-assembly-protocol invocations only.
  Do not use as a default entry point for formal Chinese empirical paper writing;
  use zh-empirical-paper-writer instead, which owns TeX/PDF asset governance and
  routes container-planning tasks to references/assembly-workflow.md.
---

# Paper Assembly Protocol

This legacy skill is kept only for explicit user invocations and backward
compatibility.

For any formal manuscript planning, use `zh-empirical-paper-writer` and route the
task to `references/assembly-workflow.md`. Do not run an independent assembly
workflow here, and do not create Markdown manuscript drafts from this wrapper.

If the user explicitly invoked this legacy name, state that the active rules now
live under `zh-empirical-paper-writer`, then continue through that skill's
`container-planning` route.
