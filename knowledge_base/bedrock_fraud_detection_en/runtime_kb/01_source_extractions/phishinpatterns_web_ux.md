---
title: "PhishInPatterns: elicited user interactions on phishing websites"
doc_type: "source_extraction"
primary_channel: "web_page"
primary_risk_domain: "phishing"
language: "en"
region: "global"
runtime_use: true
safe_use: "defensive_only"
bedrock_ready: true
last_reviewed: "2026-05-07"
---

# PhishInPatterns: elicited user interactions on phishing websites

## What this source contributes to Fraudy

Use for webpage analysis. Extract page goal, requested fields, interaction sequence, anti-crawler/evasion clues, and brand/domain consistency.

## Key extracted facts

- The study analyzes modern phishing sites by UX/UI patterns and elicited user interactions.
- It used an intelligent crawler with browser automation and machine learning to explore more than 50,000 phishing websites.
- Modern phishing pages can look professional and do not always closely clone the legitimate site.
- Phishing pages often elicit personal information using multi-stage interactions and may include evasion features.

## Fraud detection indicators

- Multi-step credential, OTP, payment, or identity-data collection.
- Professional visual design combined with unofficial domain.
- CAPTCHA, anti-bot checks, fake loading screens, or interaction gates.
- Brand impersonation without exact visual clone.

## False-positive controls

- Professional design, HTTPS, or a lock icon does not prove safety.
- A visual mismatch alone is not enough; evaluate URL, source channel, and requested fields.

## Bedrock retrieval tags

```yaml
retrieval_tags:
  source_id: phishinpatterns_web_ux
  source_kind: research_paper
  risk_domains: ['phishing_pages', 'ux_ui']
  channels: ['web']
  safe_use: defensive_only
```

## Suggested structured extraction

```yaml
source_signal:
  source_id: phishinpatterns_web_ux
  observed_indicator: ""
  requested_action: ""
  sensitive_asset: ""
  risk_effect: raises|lowers|context_only
  explanation: ""
```
