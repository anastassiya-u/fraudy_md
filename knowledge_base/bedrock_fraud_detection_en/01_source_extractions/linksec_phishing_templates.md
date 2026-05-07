---
title: LinkSec phishing templates repository
doc_type: source_extraction
source_kind: template_repository
language: en
safe_use: defensive_only
bedrock_ready: true
source_ids:
  - linksec_phishing_templates
source_urls:
  - https://github.com/LinkSec/phishing-templates
risk_domains:
  - security_awareness
  - template_indicators
channels:
  - email
  - web
last_reviewed: 2026-05-07
---

# LinkSec phishing templates repository

## What this source contributes to Fraudy

Use only for defensive indicator extraction and awareness-test coverage. Do not retrieve as operational template content in user-facing generation.

## Key extracted facts

- Repository contains over 50 GoPhish-oriented phishing templates, pages, and links.
- Repository legal disclaimer limits use to ethical cybersecurity awareness training with consent.
- Defensive extraction should store indicators, not reusable phishing copy.

## Fraud detection indicators

- Common impersonated brands and notification flows.
- Credential-collection forms and landing-page patterns.
- Security-awareness lure categories such as banking, cloud, meeting, and account alerts.

## False-positive controls

- Training templates are not evidence that a real user message is malicious unless observed indicators match a live artifact.

## Bedrock retrieval tags

```yaml
retrieval_tags:
  source_id: linksec_phishing_templates
  source_kind: template_repository
  risk_domains: ['security_awareness', 'template_indicators']
  channels: ['email', 'web']
  safe_use: defensive_only
```

## Suggested structured extraction

```yaml
source_signal:
  source_id: linksec_phishing_templates
  observed_indicator: ""
  requested_action: ""
  sensitive_asset: ""
  risk_effect: raises|lowers|context_only
  explanation: ""
```
