---
title: E-mail-Based Phishing Attack Taxonomy
doc_type: source_extraction
source_kind: research_article
language: en
safe_use: defensive_only
bedrock_ready: true
source_ids:
  - email_based_phishing_attack_taxonomy
source_urls:
  - https://www.mdpi.com/2076-3417/10/7/2363
risk_domains:
  - email_phishing
  - taxonomy
channels:
  - email
last_reviewed: 2026-05-07
---

# E-mail-Based Phishing Attack Taxonomy

## What this source contributes to Fraudy

Use for email incident decomposition. Store evidence under phases: address_selection, content_generation, sending, waiting_actions, data_gathering, data_usage.

## Key extracted facts

- The paper proposes an e-mail-focused taxonomy with six attack phases.
- The taxonomy covers e-mail address selection, e-mail text generation, e-mail sending, waiting for response, data gathering, and data usage.
- The taxonomy improves incident notation by replacing free-form descriptions with structured criteria and classes.

## Fraud detection indicators

- Generated or harvested recipient address lists.
- Human- or computer-created text that presents benefit, legitimate request, important information, possible failure, or other lures.
- Spoofed sender, systemic follow-up, repeated messages, or contact through other channels.
- Data gathering via forms, replies, malware, or credentials followed by data usage.

## False-positive controls

- Legitimate email can be personalized and urgent; classify based on exploit request and sender/domain evidence, not style alone.

## Bedrock retrieval tags

```yaml
retrieval_tags:
  source_id: email_based_phishing_attack_taxonomy
  source_kind: research_article
  risk_domains: ['email_phishing', 'taxonomy']
  channels: ['email']
  safe_use: defensive_only
```

## Suggested structured extraction

```yaml
source_signal:
  source_id: email_based_phishing_attack_taxonomy
  observed_indicator: ""
  requested_action: ""
  sensitive_asset: ""
  risk_effect: raises|lowers|context_only
  explanation: ""
```
