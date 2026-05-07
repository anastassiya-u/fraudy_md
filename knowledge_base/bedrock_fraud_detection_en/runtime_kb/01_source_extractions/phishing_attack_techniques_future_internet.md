---
title: "Classic, modern, and emerging phishing attack techniques"
doc_type: "source_extraction"
primary_channel: "all"
primary_risk_domain: "phishing"
language: "en"
region: "global"
runtime_use: true
safe_use: "defensive_only"
bedrock_ready: true
last_reviewed: "2026-05-07"
---

# Classic, modern, and emerging phishing attack techniques

## What this source contributes to Fraudy

Use as a channel/technique taxonomy. The assistant should identify technique family first, then retrieve scenario-specific rules for requested action and asset at risk.

## Key extracted facts

- Phishing has evolved from classic email campaigns to modern multi-channel techniques.
- Detection must handle email phishing, spear phishing, smishing, vishing, clone phishing, credential-harvesting pages, and technical subterfuge.
- Modern attacks combine social engineering with technical evasion and brand impersonation.

## Fraud detection indicators

- Brand impersonation plus credential or payment request.
- Clone or lookalike communication with changed link or attachment.
- Authority, urgency, fear, reward, or account-suspension framing.
- Multi-channel escalation from email/SMS to phone or messenger.

## False-positive controls

- Brand names and links are common in legitimate notifications; risk depends on sender/domain, context, and requested action.

## Bedrock retrieval tags

```yaml
retrieval_tags:
  source_id: phishing_attack_techniques_future_internet
  source_kind: research_article
  risk_domains: ['phishing', 'attack_techniques']
  channels: ['email', 'sms', 'voice', 'web', 'social_media']
  safe_use: defensive_only
```

## Suggested structured extraction

```yaml
source_signal:
  source_id: phishing_attack_techniques_future_internet
  observed_indicator: ""
  requested_action: ""
  sensitive_asset: ""
  risk_effect: raises|lowers|context_only
  explanation: ""
```
