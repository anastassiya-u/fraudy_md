---
title: Phishing Classification Techniques: systematic literature review
doc_type: source_extraction
source_kind: systematic_review
language: en
safe_use: defensive_only
bedrock_ready: true
source_ids:
  - phishing_classification_techniques_slr
source_urls:
  - https://www.researchgate.net/publication/359884880_Phishing_Classification_Techniques_A_Systematic_Literature_Review
risk_domains:
  - phishing_classification
  - model_evaluation
channels:
  - email
  - sms
  - url
  - web
last_reviewed: 2026-05-07
---

# Phishing Classification Techniques: systematic literature review

## What this source contributes to Fraudy

Use as methodology guidance for Fraudy evaluation. Retrieval should surface this source when building model-evaluation prompts, choosing datasets, or explaining why precision, recall, F1, false-positive rate, and false-negative rate must be monitored per channel.

## Key extracted facts

- The review organizes phishing classification work by techniques, datasets, performance evaluation, and phishing types.
- Useful detection systems should choose features and metrics according to the phishing type and channel.
- Dataset selection strongly affects evaluation quality and generalization.

## Fraud detection indicators

- Mismatch between classifier training data and production channel/language/region.
- High accuracy without false-positive and false-negative analysis is insufficient for fraud safety.
- Need to track URLs, message text, page content, and requested action separately.

## False-positive controls

- A model score alone should not be the final user-facing verdict.
- Classifier outputs should be combined with rule evidence and benign-context checks.

## Bedrock retrieval tags

```yaml
retrieval_tags:
  source_id: phishing_classification_techniques_slr
  source_kind: systematic_review
  risk_domains: ['phishing_classification', 'model_evaluation']
  channels: ['email', 'sms', 'url', 'web']
  safe_use: defensive_only
```

## Suggested structured extraction

```yaml
source_signal:
  source_id: phishing_classification_techniques_slr
  observed_indicator: ""
  requested_action: ""
  sensitive_asset: ""
  risk_effect: raises|lowers|context_only
  explanation: ""
```
