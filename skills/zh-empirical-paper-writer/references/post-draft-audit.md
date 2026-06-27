# Post-Draft Audit

Use after manuscript prose has been drafted or revised.

This is not a first-drafting workflow. It checks whether the new prose is good
enough to remain in the TeX manuscript.

## Audit Order

1. Confirm the paragraph belongs in the current chapter or section container.
2. Check the paragraph identity and sentence-role sequence.
3. Check literature, novelty, method, or theory claims against verified project
   authority.
4. Check noun choice, verb-object collocation, aspect marking, and reference
   article register.
5. Check anti-translationese and sentence length.
6. Check TeX source integrity, especially paragraph boundaries.
7. Compile or smoke-test the PDF when feasible.

## Common Failures

Flag and repair:

1. smooth sentences that do not discharge their paragraph role
2. unsupported contribution or gap claims
3. generic shells such as `在此背景下`, `由此看`, or `更需要进一步讨论`
4. invented collocations such as `推进相关认识`
5. method-register nouns in problem-setting prose when object-language is needed
6. completed literature accumulation written without proper aspect marking
7. sentences that hide the actor behind abstract nouns
8. a requested one-paragraph replacement split into multiple TeX paragraphs

## Repair Rule

When the audit finds a problem, revise the TeX prose rather than only reporting
the issue, unless the user asked for review only.

Keep the final manuscript paragraph continuous in the TeX source when the user
asked for one paragraph. Report only the material audit findings and the build
result; do not create a separate Markdown change note.
