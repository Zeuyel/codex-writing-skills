# Theory Audit

Use for `theory-audit`: formal model, mechanism, proposition, hypothesis, and
theory chapter review.

## Default Stance

Audit before polishing. A model or mechanism should not pass because the prose is
smooth. It must start from a non-obvious organizational or economic problem and
derive implications from that object rather than from convenient variables.

## Hard Gates

Flag high risk when:

1. the model cannot state a non-obvious problem before notation
2. variables appear before the organizational process is clear
3. one state variable improves too many margins at once
4. thresholds or regions carry the story without a prior process
5. empirical measurement categories are promoted into theory primitives too soon
6. propositions only restate monotonicity
7. the same concept appears under multiple variable names
8. dynamic claims lack a stable state vector or transition process

When two or more hard gates fail, treat the theory object as not ready for
manuscript polishing.

## Review Workflow

1. Name the review target: model, proposition set, mechanism subsection, or
   theory chapter.
2. Reconstruct the non-obvious problem in plain language.
3. Identify the organizational object before variables.
4. Separate state variables, parameters, controls, and empirical proxies.
5. Check whether each assumption is needed or merely convenient.
6. Rank findings by severity before suggesting wording improvements.

## Output

Use findings-first output:

1. hard-gate verdict
2. findings ordered by severity
3. variable disposition: keep, demote, merge, delete
4. open questions
5. next fixes limited to the binding issues

If the audit leads to prose edits, install only approved wording in the target
`.tex` file and keep audit notes in TeX comments unless the user asks for a memo.
