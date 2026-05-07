---
title: HailBytes Gophish training templates
doc_type: source_extraction
source_kind: template_repository
language: en
safe_use: defensive_only
bedrock_ready: true
source_ids:
  - hailbytes_gophish_training_templates
source_urls:
  - https://github.com/HailBytes/gophish-training-templates
risk_domains:
  - security_awareness
  - template_indicators
channels:
  - email
  - web
last_reviewed: 2026-05-07
---

# HailBytes Gophish training templates

## What this source contributes to Fraudy

Use as defensive taxonomy of impersonated business services. Do not generate full phishing emails from this source.

## Key extracted facts

- Repository provides phishing-training templates for awareness campaigns.
- Categories can cover business, healthcare, finance, HR, cloud, and transfer notifications.
- Use only as defensive awareness and detector-coverage knowledge.

## Fraud detection indicators

- HR/payroll notice asking for login.
- Healthcare portal or billing message asking for credentials/payment.
- Financial transfer or document-review lure.
- Cloud storage, password expiry, or shared-file lure.

## False-positive controls

- Templates are simulated; do not use them as proof that a brand notification is malicious.

## Bedrock retrieval tags

```yaml
retrieval_tags:
  source_id: hailbytes_gophish_training_templates
  source_kind: template_repository
  risk_domains: ['security_awareness', 'template_indicators']
  channels: ['email', 'web']
  safe_use: defensive_only
```

## Suggested structured extraction

```yaml
source_signal:
  source_id: hailbytes_gophish_training_templates
  observed_indicator: ""
  requested_action: ""
  sensitive_asset: ""
  risk_effect: raises|lowers|context_only
  explanation: ""
```
