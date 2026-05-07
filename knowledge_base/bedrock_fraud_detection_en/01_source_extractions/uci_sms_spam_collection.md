---
title: UCI SMS Spam Collection
doc_type: source_extraction
source_kind: dataset
language: en
safe_use: defensive_only
bedrock_ready: true
source_ids:
  - uci_sms_spam_collection
source_urls:
  - https://archive.ics.uci.edu/dataset/228/sms+spam+collection
risk_domains:
  - sms_dataset
  - spam_ham
channels:
  - sms
last_reviewed: 2026-05-07
---

# UCI SMS Spam Collection

## What this source contributes to Fraudy

Use for baseline SMS text examples, not as a direct high-risk fraud rule source. Keep dataset provenance and label mapping in metadata.

## Key extracted facts

- Dataset contains 5,574 SMS instances.
- Labels are ham and spam, making it useful for baseline short-message classification.
- It is older and English-oriented, so it should not be treated as complete coverage for modern CIS/Kazakhstan scams.

## Fraud detection indicators

- Spam-like promotional language.
- Unexpected message asking user to reply, click, or claim a prize.
- Useful as negative/positive baseline for short-text model behavior.

## False-positive controls

- Spam is not always fraud.
- Ham examples help reduce false positives on normal personal and service messages.

## Bedrock retrieval tags

```yaml
retrieval_tags:
  source_id: uci_sms_spam_collection
  source_kind: dataset
  risk_domains: ['sms_dataset', 'spam_ham']
  channels: ['sms']
  safe_use: defensive_only
```

## Suggested structured extraction

```yaml
source_signal:
  source_id: uci_sms_spam_collection
  observed_indicator: ""
  requested_action: ""
  sensitive_asset: ""
  risk_effect: raises|lowers|context_only
  explanation: ""
```
