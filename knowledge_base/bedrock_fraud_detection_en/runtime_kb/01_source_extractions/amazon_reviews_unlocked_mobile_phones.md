---
title: "Amazon reviews unlocked mobile phones dataset"
doc_type: "source_extraction"
primary_channel: "web_page"
primary_risk_domain: "fake_review"
language: "en"
region: "global"
runtime_use: true
safe_use: "defensive_only"
bedrock_ready: true
last_reviewed: "2026-05-07"
---

# Amazon reviews unlocked mobile phones dataset

## What this source contributes to Fraudy

Use mostly as benign review-language data and marketplace context, not as a direct scam-scenario source.

## Key extracted facts

- Dataset contains Amazon mobile-phone review text and metadata.
- Useful for benign marketplace/review language baselines and review-text modeling.

## Fraud detection indicators

- Product-review language can train normal marketplace context.
- Review metadata can support anomaly analysis when combined with marketplace behavior.

## False-positive controls

- Ordinary product reviews and complaints are not fraud indicators by themselves.

## Bedrock retrieval tags

```yaml
retrieval_tags:
  source_id: amazon_reviews_unlocked_mobile_phones
  source_kind: dataset
  risk_domains: ['marketplace', 'review_text']
  channels: ['marketplace', 'web']
  safe_use: defensive_only
```

## Suggested structured extraction

```yaml
source_signal:
  source_id: amazon_reviews_unlocked_mobile_phones
  observed_indicator: ""
  requested_action: ""
  sensitive_asset: ""
  risk_effect: raises|lowers|context_only
  explanation: ""
```
