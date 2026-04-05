# Text Identification Methods In Economics And Management Empirics

## Purpose

This reference gives a compact method-family map for text identification tasks in empirical work.

## Method families

### 1. Dictionary or keyword matching

Use when:

- the target concept is lexically stable
- interpretability matters
- you need transparent robustness checks

Typical outputs:

- term counts
- term ratios
- binary hit indicators
- layered dictionary scores

Risks:

- false positives and false negatives
- poor semantic boundary detection

### 2. Dictionary expansion with machine learning or external taxonomies

Use when:

- a manual dictionary is too narrow
- you still want an interpretable measure

Typical outputs:

- expanded keyword lists
- layered technical vocabularies
- weighted concept lexicons

Risks:

- expansion logic must be documented
- still weaker than semantic classification for task-boundary problems

### 3. Supervised classification

Use when:

- the task is to assign documents or snippets into known labels
- you can build a labeled sample

Typical outputs:

- class labels
- class probabilities
- out-of-sample precision, recall, F1, Kappa

Typical models:

- SVM
- XGBoost
- Naive Bayes
- BERT-style fine-tuned classifiers

Risks:

- label quality dominates model quality
- requires explicit validation reporting

### 4. Topic models or unsupervised discovery

Use when:

- you need to explore corpus structure before fixing labels
- you need descriptive theme discovery rather than final classification

Typical outputs:

- latent topics
- topic shares
- theme clusters

Risks:

- interpretation is subjective
- usually not enough as the final core identification method by itself

### 5. Pretrained language models and LLM-based semantic identification

Use when:

- lexical matching is too crude
- semantic boundary matters
- short texts still carry clear task meaning, such as job postings

Typical outputs:

- semantic labels
- exposure scores
- task or skill classifications
- hard-case triage for human review

Risks:

- stability and reproducibility must be addressed
- should be paired with human validation and error analysis

### 6. Information extraction and structured tagging

Use when:

- you need to extract tasks, skills, tools, levels, functions, or entities
- the final empirical variables are structured features rather than a single score

Typical outputs:

- skill tags
- task tags
- job-level features
- cross-functional indicators

Risks:

- schema design matters as much as model choice
- extraction quality must be validated at field level

## Validation checklist

For most empirical paper use cases, report at least:

- labeling protocol
- sampling strategy for validation set
- out-of-sample metrics
- confusion patterns or hard cases
- robustness to alternative dictionaries, thresholds, or model settings
