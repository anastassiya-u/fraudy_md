---
title: "Fraudy Bedrock KB validation report"
doc_type: "validation_report"
language: "en"
safe_use: "defensive_only"
last_reviewed: "2026-05-07"
---

# Fraudy Bedrock KB validation report

## Summary

- Total files scanned: 106
- Runtime Markdown files included: 41
- Internal Markdown files excluded from runtime: 8
- Metadata sidecars created: 41
- YAML/frontmatter files normalized or fixed: 41
- Missing metadata sidecars: 0
- Invalid runtime YAML/frontmatter files: 0

## Internal files excluded from runtime

- knowledge_base/bedrock_fraud_detection_en/internal_docs/00_manifest/document_schema.md
- knowledge_base/bedrock_fraud_detection_en/internal_docs/00_manifest/source_inventory.md
- knowledge_base/bedrock_fraud_detection_en/internal_docs/04_bedrock_ingestion/bedrock_guardrails.md
- knowledge_base/bedrock_fraud_detection_en/internal_docs/04_bedrock_ingestion/bedrock_ingestion_manifest.md
- knowledge_base/bedrock_fraud_detection_en/internal_docs/README.md
- knowledge_base/bedrock_fraud_detection_en/internal_docs/document_schema.md
- knowledge_base/bedrock_fraud_detection_en/internal_docs/source_extraction_index.md
- knowledge_base/bedrock_fraud_detection_en/internal_docs/source_inventory.md

## Files that need human review

- Source reliability for community/template repositories should be reviewed before using strict trust filters.
- Dataset licenses and snapshots should be reviewed before model training or public redistribution.
- ResearchGate-hosted papers should be replaced with publisher/preprint URLs where available for stronger provenance.

## Sources with weak or medium reliability

- knowledge_base/bedrock_fraud_detection_en/runtime_kb/01_source_extractions/amazon_reviews_unlocked_mobile_phones.md
- knowledge_base/bedrock_fraud_detection_en/runtime_kb/01_source_extractions/fake_job_posting_prediction_kaggle.md
- knowledge_base/bedrock_fraud_detection_en/runtime_kb/01_source_extractions/fake_reviews_dataset_kaggle.md
- knowledge_base/bedrock_fraud_detection_en/runtime_kb/01_source_extractions/hailbytes_gophish_training_templates.md
- knowledge_base/bedrock_fraud_detection_en/runtime_kb/01_source_extractions/linksec_phishing_templates.md
- knowledge_base/bedrock_fraud_detection_en/runtime_kb/01_source_extractions/mendeley_sms_phishing_dataset.md
- knowledge_base/bedrock_fraud_detection_en/runtime_kb/01_source_extractions/multi_agent_scam_conversation_hf.md
- knowledge_base/bedrock_fraud_detection_en/runtime_kb/01_source_extractions/phishing_validation_emails_twente.md
- knowledge_base/bedrock_fraud_detection_en/runtime_kb/01_source_extractions/scammer_conversation_hf.md
- knowledge_base/bedrock_fraud_detection_en/runtime_kb/01_source_extractions/smishing_systematic_review.md
- knowledge_base/bedrock_fraud_detection_en/runtime_kb/01_source_extractions/uci_sms_spam_collection.md

## YAML fixes made

- Runtime frontmatter was shortened to scalar fields only.
- Titles are quoted.
- Long arrays were removed from runtime frontmatter and represented in Bedrock sidecar metadata instead.
- Every runtime Markdown file starts and ends its frontmatter with `---`.

## Recommended next steps before Bedrock ingestion

1. Upload only `knowledge_base/bedrock_fraud_detection_en/runtime_kb/` to `s3://<bucket-name>/fraudy-kb/v1/runtime_kb/`.
2. Include every `.md.metadata.json` sidecar next to its `.md` file in S3.
3. Configure Bedrock Knowledge Bases metadata filtering on `runtime_use`, `safe_use`, `doc_type`, `primary_channel`, and `primary_risk_domain`.
4. Run a small retrieval QA set for SMS, phone call, email, web page, marketplace, and job-scam inputs.
5. Review weak/community sources and replace or supplement them with primary sources when possible.
