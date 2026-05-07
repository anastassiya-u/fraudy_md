---
title: "Synthetic multi-turn scam and non-scam phone dialogue dataset"
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

# Synthetic multi-turn scam and non-scam phone dialogue dataset

## What this source contributes to Fraudy

Use for multi-turn call-stage detection and false-positive tests. Extract stage, claimed identity, requested action, sensitive asset, pressure tactic, and user vulnerability context.

## Key extracted facts

- Dataset has 1,600 synthetic phone dialogues with scam and non-scam labels.
- Columns include dialogue, receiver personality, interaction type, and binary label.
- Scam types include SSN, refund, support, and reward scams.
- Non-scam types include delivery confirmation, insurance sales, appointment reminders, and wrong-number calls.
- License is Apache 2.0; generated dialogues may not capture all real-world nuances.

## Fraud detection indicators

- Caller role marked as Suspect and receiver as Innocent.
- Scam dialogue often progresses from authority/reason to personal data, refund, reward, or support access.
- Receiver personality affects vulnerability and response style.

## False-positive controls

- Legitimate appointment, delivery, insurance, and wrong-number calls must be represented to reduce false positives.
- Synthetic data should not be the only production evidence source.

## Bedrock retrieval tags

```yaml
retrieval_tags:
  source_id: multi_agent_scam_conversation_hf
  source_kind: dataset
  risk_domains: ['phone_scam', 'conversation_detection']
  channels: ['phone', 'conversation']
  safe_use: defensive_only
```

## Suggested structured extraction

```yaml
source_signal:
  source_id: multi_agent_scam_conversation_hf
  observed_indicator: ""
  requested_action: ""
  sensitive_asset: ""
  risk_effect: raises|lowers|context_only
  explanation: ""
```
