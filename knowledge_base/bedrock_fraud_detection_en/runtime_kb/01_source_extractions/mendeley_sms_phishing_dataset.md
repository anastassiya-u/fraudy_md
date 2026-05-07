---
title: "SMS phishing dataset for machine learning and pattern recognition"
doc_type: "source_extraction"
primary_channel: "sms"
primary_risk_domain: "smishing"
language: "en"
region: "global"
runtime_use: true
safe_use: "defensive_only"
bedrock_ready: true
last_reviewed: "2026-05-07"
---

# SMS phishing dataset for machine learning and pattern recognition

## What this source contributes to Fraudy

Use for smishing/ham/spam supervised evaluation. Suggested fields: label, text, has_url, has_email, has_phone, requested_action, sensitive_asset.

## Key extracted facts

- Dataset has 5,971 labeled text messages.
- Labels include 4,844 ham, 489 spam, and 638 smishing messages.
- Attributes include raw text plus URL, EMAIL, and PHONE indicators.
- Published as Mendeley Data Version 1 with CC BY 4.0 license.

## Fraud detection indicators

- Presence of URL, email address, or phone number in malicious SMS.
- Raw text can be used for content analysis and feature extraction.
- Smishing label is more fraud-specific than generic spam label.

## False-positive controls

- Presence of a URL or phone number is not sufficient by itself; combine with requested action.

## Bedrock retrieval tags

```yaml
retrieval_tags:
  source_id: mendeley_sms_phishing_dataset
  source_kind: dataset
  risk_domains: ['smishing_dataset']
  channels: ['sms']
  safe_use: defensive_only
```

## Suggested structured extraction

```yaml
source_signal:
  source_id: mendeley_sms_phishing_dataset
  observed_indicator: ""
  requested_action: ""
  sensitive_asset: ""
  risk_effect: raises|lowers|context_only
  explanation: ""
```
