---
title: "False-positive controls for fraud classification"
doc_type: "false_positive_policy"
primary_channel: "all"
primary_risk_domain: "general"
language: "en"
region: "global"
runtime_use: true
safe_use: "defensive_only"
bedrock_ready: true
last_reviewed: "2026-05-07"
---

# False-positive controls

## Do not classify as fraud automatically when only one weak signal is present

- A message contains a link.
- A sender is unknown.
- A service notification is urgent.
- A brand name appears in the message.
- A recruiter uses a messenger.
- A delivery notification arrives while the user expects a parcel.
- A bank alert asks the user to check the official app without requesting codes or card data.

## Benign context that can reduce risk

| Context | Risk reduction condition |
| --- | --- |
| User initiated reset/login/support | Domain/app is official and no person asks for secrets |
| Expected delivery | Tracking can be verified in official app and no card-to-receive-money request appears |
| Known appointment reminder | No payment, credential, or identity-document request appears |
| Formal recruitment process | No upfront fees and company identity/domain are verifiable |
| Marketplace transaction inside platform | No external payment/courier link or card request |

## Explanation requirement

Fraudy must explain both sides:

```yaml
verdict_explanation:
  risk_evidence: []
  benign_indicators: []
  uncertainty: ""
  safest_next_step: ""
```
