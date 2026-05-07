---
title: Short Message Service phishing attacks and defenses systematic review
doc_type: source_extraction
source_kind: systematic_review_pdf
language: en
safe_use: defensive_only
bedrock_ready: true
source_ids:
  - smishing_systematic_review
source_urls:
  - https://arxiv.org/pdf/2604.11429
risk_domains:
  - smishing
  - social_engineering
channels:
  - sms
  - messenger
last_reviewed: 2026-05-07
---

# Short Message Service phishing attacks and defenses systematic review

## What this source contributes to Fraudy

Use for SMS/messenger prompt analysis. Extract hook, authority, urgency, link risk, requested action, sensitive asset, and benign context.

## Key extracted facts

- Smishing attacks exploit psychological factors and techniques through short mobile messages.
- Relevant psychological factor categories include social, personality/individual differences, cognitive, emotional, and workplace factors.
- Smishing defenses require text, URL, sender, and requested-action analysis.

## Fraud detection indicators

- Fear/loss hooks: card blocked, account suspended, fine, suspicious transaction.
- Urgency hooks: act now, final notice, confirm today.
- Reward hooks: refund, subsidy, prize, bonus.
- Authority hooks: bank, telecom, delivery, government, employer.
- Shortened or lookalike URL, APK install, phone number, or credential/payment form.

## False-positive controls

- SMS delivery, marketing, and appointment reminders can be normal when no risky action is requested.
- Opening the official app manually is safer than tapping the SMS link.

## Bedrock retrieval tags

```yaml
retrieval_tags:
  source_id: smishing_systematic_review
  source_kind: systematic_review_pdf
  risk_domains: ['smishing', 'social_engineering']
  channels: ['sms', 'messenger']
  safe_use: defensive_only
```

## Suggested structured extraction

```yaml
source_signal:
  source_id: smishing_systematic_review
  observed_indicator: ""
  requested_action: ""
  sensitive_asset: ""
  risk_effect: raises|lowers|context_only
  explanation: ""
```
