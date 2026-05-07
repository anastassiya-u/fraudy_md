---
title: Bedrock markdown document schema
doc_type: schema
language: en
safe_use: defensive_only
bedrock_ready: true
last_reviewed: 2026-05-07
---

# Bedrock markdown document schema

## Required frontmatter

```yaml
title: Human-readable document title
doc_type: source_extraction|service_knowledge|detection_policy|bedrock_ingestion|source_inventory|schema
language: en
safe_use: defensive_only
bedrock_ready: true
risk_domains: []
channels: []
source_ids: []
source_urls: []
last_reviewed: 2026-05-07
```

## Recommended chunk boundaries

- Keep one source extraction as one or more chunks split by headings.
- Do not split YAML detection blocks in the middle.
- Preserve frontmatter metadata in every chunk during ingestion.
- Prefer 500-900 token chunks for service knowledge and policy documents.

## Canonical evidence fields

```yaml
evidence:
  channel: sms|email|phone|messenger|website|marketplace|job_platform|unknown
  claimed_service: bank|telecom|delivery|government|marketplace|support|employer|investment|romance|recovery|unknown
  requested_action: none|click_link|login|pay_fee|transfer_money|share_otp|install_app|remote_access|send_documents|share_crypto_key
  sensitive_asset: none|credentials|otp|card|money|identity|device|crypto_key
  pressure_tactic: none|urgency|fear|authority|reward|secrecy|emotional_trust
  benign_context: none|user_initiated|expected_notification|official_app|known_contact
  risk: low|medium|high|critical
```
