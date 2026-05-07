---
title: Taxonomy of fraud detection metrics for business processes
doc_type: source_extraction
source_kind: research_article
language: en
safe_use: defensive_only
bedrock_ready: true
source_ids:
  - fraud_detection_metrics_taxonomy
source_urls:
  - https://www.researchgate.net/publication/340625489_Taxonomy_of_Fraud_Detection_Metrics_for_Business_Processes
risk_domains:
  - risk_metrics
  - evaluation
channels:
  - all
last_reviewed: 2026-05-07
---

# Taxonomy of fraud detection metrics for business processes

## What this source contributes to Fraudy

Use to define risk-scoring metrics and threshold governance. Track precision, recall, F1, false-positive rate, false-negative rate, time-to-detection, and harm-weighted miss cost.

## Key extracted facts

- Fraud-detection systems need metrics that reflect business-process risk, not only generic classification accuracy.
- Operational evaluation should include false positives, false negatives, timeliness, and impact.

## Fraud detection indicators

- Model reports accuracy without cost/impact metrics.
- Thresholds not separated by channel, requested action, or asset at risk.
- No monitoring of false positives on legitimate notifications.

## False-positive controls

- A low-risk model warning can still be useful if phrased as verification guidance rather than accusation.

## Bedrock retrieval tags

```yaml
retrieval_tags:
  source_id: fraud_detection_metrics_taxonomy
  source_kind: research_article
  risk_domains: ['risk_metrics', 'evaluation']
  channels: ['all']
  safe_use: defensive_only
```

## Suggested structured extraction

```yaml
source_signal:
  source_id: fraud_detection_metrics_taxonomy
  observed_indicator: ""
  requested_action: ""
  sensitive_asset: ""
  risk_effect: raises|lowers|context_only
  explanation: ""
```
