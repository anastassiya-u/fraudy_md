---
title: Amazon Bedrock ingestion manifest and retrieval plan
doc_type: bedrock_ingestion
language: en
safe_use: defensive_only
bedrock_ready: true
last_reviewed: 2026-05-07
---

# Amazon Bedrock ingestion manifest and retrieval plan

## Suggested S3 layout

```text
s3://<bucket>/fraudy/knowledge_base/bedrock_fraud_detection_en/00_manifest/
s3://<bucket>/fraudy/knowledge_base/bedrock_fraud_detection_en/01_source_extractions/
s3://<bucket>/fraudy/knowledge_base/bedrock_fraud_detection_en/02_service_knowledge/
s3://<bucket>/fraudy/knowledge_base/bedrock_fraud_detection_en/03_detection_policy/
s3://<bucket>/fraudy/knowledge_base/bedrock_fraud_detection_en/04_bedrock_ingestion/
```

## Metadata to preserve per chunk

```json
{
  "project": "fraudy",
  "language": "en",
  "safe_use": "defensive_only",
  "bedrock_ready": true,
  "doc_type": "source_extraction",
  "source_ids": ["smishing_systematic_review"],
  "risk_domains": ["smishing", "social_engineering"],
  "channels": ["sms", "messenger"],
  "last_reviewed": "2026-05-07"
}
```

## Retrieval recipes

| Input type | Retrieve first | Retrieve second | Retrieve third |
| --- | --- | --- | --- |
| Suspicious SMS | `02_service_knowledge/service_scam_catalog.md` | `01_source_extractions/smishing_systematic_review.md` | detection policy files |
| Suspicious phone call | `service_scam_catalog.md` | conversation and audio source extractions | detection policy files |
| Suspicious email | `email_based_phishing_attack_taxonomy.md` | notification template indicators | false-positive controls |
| Suspicious URL/page | `phishinpatterns_web_ux.md` and `phishtank_url_clearinghouse.md` | phishing techniques | risk scoring |
| Job offer | `fake_job_posting_prediction_kaggle.md` | service scam catalog | false-positive controls |
| Marketplace chat | service scam catalog | fake reviews/Amazon review context | risk scoring |
| User asks “what should I do?” | risk scoring and actions | relevant source extraction | false-positive controls |

## Chunking rules

- Use heading-aware chunking.
- Keep YAML blocks intact.
- Recommended chunk size: 500-900 tokens.
- Do not ingest raw phishing templates as retrievable generation examples.
- Keep source extraction files separately retrievable for audit and traceability.
