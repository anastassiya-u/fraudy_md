---
title: "Scammer Conversation dataset"
doc_type: "source_extraction"
primary_channel: "phone_call"
primary_risk_domain: "general"
language: "en"
region: "global"
runtime_use: true
safe_use: "defensive_only"
bedrock_ready: true
last_reviewed: "2026-05-07"
---

# Scammer Conversation dataset

## What this source contributes to Fraudy

Use as simple conversation classification baseline. Prefer the larger multi-agent dataset for richer scam-type metadata.

## Key extracted facts

- Dataset has about 1,000 CSV rows, English text, and Apache 2.0 license.
- Rows include conversation text and binary labels.
- Examples include bank or credit-card verification calls contrasted with ordinary conversations.

## Fraud detection indicators

- Unexpected call from bank/credit-card company asking to verify details.
- Claim of unusual or unauthorized activity followed by account/card verification request.
- User asks for employee ID or reason; inability to verify can raise risk.

## False-positive controls

- Ordinary friendly conversation is label 0 and helps prevent overclassification.

## Bedrock retrieval tags

```yaml
retrieval_tags:
  source_id: scammer_conversation_hf
  source_kind: dataset
  risk_domains: ['conversation_detection']
  channels: ['phone', 'conversation']
  safe_use: defensive_only
```

## Suggested structured extraction

```yaml
source_signal:
  source_id: scammer_conversation_hf
  observed_indicator: ""
  requested_action: ""
  sensitive_asset: ""
  risk_effect: raises|lowers|context_only
  explanation: ""
```
