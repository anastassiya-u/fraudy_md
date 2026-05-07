---
title: E-mail-based phishing attack taxonomy phases
source_urls:
  - https://www.mdpi.com/2076-3417/10/7/2363
doc_type: typology
risk_domain: email_phishing
language: ru
safe_use: defensive_only
last_reviewed: 2026-05-07
---

# E-mail phishing taxonomy phases

## Six-phase defensive model

| Phase | Detection question | Risk evidence |
| --- | --- | --- |
| 1. Preparation | Is the sender/domain/brand context suspicious? | lookalike sender, compromised account, unusual template |
| 2. Delivery | How did the user receive it? | unexpected email, mass campaign, attachment/link |
| 3. Deception | What trust mechanism is used? | authority, urgency, fear, reward, brand mimicry |
| 4. Interaction | What action is requested? | click link, open attachment, scan QR, call number |
| 5. Exploitation | What sensitive asset is requested or exposed? | password, OTP, card, bank transfer, malware install |
| 6. Monetization/impact | What harm can happen? | account takeover, invoice diversion, card theft, identity theft |

## RAG extraction schema

```yaml
email_phishing_phase_evidence:
  preparation: []
  delivery: []
  deception: []
  interaction: []
  exploitation: []
  impact: []
```

Use this schema to explain decisions: “Risk is high because the message has evidence in phases 3, 4, and 5.”
