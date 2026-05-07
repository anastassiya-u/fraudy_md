---
title: Fraud typologies and victims of fraud literature review
doc_type: source_extraction
source_kind: research_report
language: en
safe_use: defensive_only
bedrock_ready: true
source_ids:
  - fraud_typologies_uk_literature_review
source_urls:
  - https://assets.publishing.service.gov.uk/media/5a7ad8c2ed915d670dd7efad/fraud-typologies.pdf
risk_domains:
  - general_fraud
  - mass_marketing
  - identity_fraud
  - small_business_fraud
channels:
  - email
  - phone
  - mail
  - web
  - in_person
last_reviewed: 2026-05-07
---

# Fraud typologies and victims of fraud literature review

## What this source contributes to Fraudy

Use as the top-level fraud taxonomy. Map user reports into mass-marketing, investment, identity, small-business, payment-card, loan, career-opportunity, romance, or technology-trick fraud. Preserve victim-impact context so the assistant gives supportive and non-blaming guidance.

## Key extracted facts

- Fraud is broad deception for gain and includes false representation, failure to disclose information, and abuse of position.
- The review focuses on mass marketing scams, investment fraud, identity fraud, and fraud affecting small businesses.
- Mass-marketing scams often start from unsolicited contact and false promises to obtain money.
- Fraudster techniques can be grouped as victim selection, perpetration strategies, detection avoidance, and securing gains.
- Victims may under-report because of shame, ambiguity, low loss, confusion, or not realizing they were defrauded.

## Fraud detection indicators

- Unsolicited offer or contact with a promised benefit.
- Advance administrative, insurance, tax, premium-rate, or setup fee before the claimed benefit.
- Professional-looking materials used to create trust.
- Targeting of prior victims or vulnerable user segments.
- Requests for personal data that enable identity fraud.

## False-positive controls

- Not every unsolicited commercial message is fraud; risk increases when payment, secrets, or identity data are requested.
- Low-value purchases can be legitimate; risk depends on deception, non-delivery, or pressure.

## Bedrock retrieval tags

```yaml
retrieval_tags:
  source_id: fraud_typologies_uk_literature_review
  source_kind: research_report
  risk_domains: ['general_fraud', 'mass_marketing', 'identity_fraud', 'small_business_fraud']
  channels: ['email', 'phone', 'mail', 'web', 'in_person']
  safe_use: defensive_only
```

## Suggested structured extraction

```yaml
source_signal:
  source_id: fraud_typologies_uk_literature_review
  observed_indicator: ""
  requested_action: ""
  sensitive_asset: ""
  risk_effect: raises|lowers|context_only
  explanation: ""
```
