---
title: "Phishing validation emails dataset"
doc_type: "source_extraction"
primary_channel: "email"
primary_risk_domain: "phishing"
language: "en"
region: "EU"
runtime_use: true
safe_use: "defensive_only"
bedrock_ready: true
last_reviewed: "2026-05-07"
---

# Phishing validation emails dataset

## What this source contributes to Fraudy

Use for email validation and calibration, especially to test explanations and false-positive behavior before deployment.

## Key extracted facts

- Dataset contains 2,000 emails curated to validate machine-learning models.
- Labels distinguish Safe Email and Phishing Email.
- Records include full email text and corresponding label.
- The dataset mixes real-world and artificially generated emails and was made available on 29 Aug 2024 through Zenodo.

## Fraud detection indicators

- Gift-card/prize and credential-harvesting examples.
- Safe email examples for false-positive testing.
- Full-body email text for model validation after training.

## False-positive controls

- Artificially generated examples may not fully represent production language and regional patterns.

## Bedrock retrieval tags

```yaml
retrieval_tags:
  source_id: phishing_validation_emails_twente
  source_kind: dataset
  risk_domains: ['email_dataset', 'phishing_validation']
  channels: ['email']
  safe_use: defensive_only
```

## Suggested structured extraction

```yaml
source_signal:
  source_id: phishing_validation_emails_twente
  observed_indicator: ""
  requested_action: ""
  sensitive_asset: ""
  risk_effect: raises|lowers|context_only
  explanation: ""
```
