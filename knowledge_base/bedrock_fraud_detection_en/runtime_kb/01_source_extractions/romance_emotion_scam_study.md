---
title: "Romance and emotion-based scam study"
doc_type: "source_extraction"
primary_channel: "messenger"
primary_risk_domain: "investment_scam"
language: "en"
region: "global"
runtime_use: true
safe_use: "defensive_only"
bedrock_ready: true
last_reviewed: "2026-05-07"
---

# Romance and emotion-based scam study

## What this source contributes to Fraudy

Use to detect trust-building and delayed exploit requests across multi-turn chats. Retrieval should consider conversation history, not only the latest message.

## Key extracted facts

- Romance scams rely on emotional attachment, trust building, and gradual escalation to financial exploitation.
- Investment hybrids introduce a financial opportunity after relationship trust is established.

## Fraud detection indicators

- Fast emotional intimacy with a new online contact.
- Avoidance of in-person or video verification.
- Crisis story, travel issue, medical need, customs fee, or investment opportunity.
- Request for crypto, transfer, gift cards, or receiving/transferring funds.

## False-positive controls

- Online relationships are not scams by default; risk rises when money, secrecy, or investment advice appears.

## Bedrock retrieval tags

```yaml
retrieval_tags:
  source_id: romance_emotion_scam_study
  source_kind: research_article_pdf
  risk_domains: ['romance_scam', 'emotion_manipulation']
  channels: ['dating_app', 'social_media', 'messenger']
  safe_use: defensive_only
```

## Suggested structured extraction

```yaml
source_signal:
  source_id: romance_emotion_scam_study
  observed_indicator: ""
  requested_action: ""
  sensitive_asset: ""
  risk_effect: raises|lowers|context_only
  explanation: ""
```
