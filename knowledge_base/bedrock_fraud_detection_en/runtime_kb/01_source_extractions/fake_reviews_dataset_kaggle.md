---
title: "Fake reviews dataset"
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

# Fake reviews dataset

## What this source contributes to Fraudy

Use as marketplace trust context. Combine with external payment links, courier verification forms, card-to-receive-money requests, and platform-bypass behavior.

## Key extracted facts

- Dataset is intended for fake review detection in e-commerce/review contexts.
- Fake reviews are an auxiliary trust-manipulation signal, not a direct payment-fraud verdict.

## Fraud detection indicators

- Repetitive or unnatural review language.
- Suspicious rating distribution or review bursts.
- Seller trust boosted by low-quality or coordinated-looking reviews.

## False-positive controls

- A suspicious review profile does not automatically mean the seller is running payment fraud.
- Use transaction-flow evidence before warning the user about payment/card theft.

## Bedrock retrieval tags

```yaml
retrieval_tags:
  source_id: fake_reviews_dataset_kaggle
  source_kind: dataset
  risk_domains: ['marketplace', 'review_fraud']
  channels: ['marketplace', 'web']
  safe_use: defensive_only
```

## Suggested structured extraction

```yaml
source_signal:
  source_id: fake_reviews_dataset_kaggle
  observed_indicator: ""
  requested_action: ""
  sensitive_asset: ""
  risk_effect: raises|lowers|context_only
  explanation: ""
```
