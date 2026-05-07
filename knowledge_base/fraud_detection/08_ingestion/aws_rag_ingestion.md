---
title: AWS RAG ingestion guidance for Fraudy knowledge base
doc_type: ingestion_guide
language: ru
audience: aws_rag_pipeline
safe_use: defensive_only
last_reviewed: 2026-05-07
---

# AWS RAG ingestion guidance

## Recommended metadata

```json
{
  "project": "fraudy",
  "language": "ru",
  "doc_type": "signal_rules",
  "risk_domain": "smishing",
  "regions": ["kazakhstan", "cis"],
  "channels": ["sms", "messenger"],
  "safe_use": "defensive_only",
  "source_urls": ["https://example.com/source"]
}
```

## Chunking recommendations

- Chunk by heading, preserving frontmatter metadata in every chunk.
- Target 500-900 tokens per chunk for scenario/rules documents.
- Keep YAML scenario blocks intact; do not split inside a single scenario.
- Store `source_urls` and `last_reviewed` for auditability.
- Deduplicate repeated source URLs before embedding.

## Retrieval recipes

| User input type | Retrieve first | Retrieve second |
| --- | --- | --- |
| Suspicious SMS | `02_signals/smishing_psychological_patterns.md` | `06_risk/risk_classification_rules.md`, relevant scenario |
| Suspicious call | `02_signals/audio_voice_deepfake_signals.md` | `04_scenarios/kazakhstan_cis_scenarios.md` |
| Marketplace chat | `04_scenarios/kazakhstan_cis_scenarios.md` | `03_datasets/marketplace_datasets.md` |
| Website/login page | `02_signals/phishing_page_patterns.md` | `01_typologies/phishing_attack_techniques.md` |
| Job offer | `03_datasets/job_scam_datasets.md` | `04_scenarios/romance_investment_job_scenarios.md` |
| Model risk explanation | `06_risk/risk_classification_rules.md` | `02_signals/not_automatically_fraud.md` |

## Guardrails

- The assistant must not generate operational phishing templates or instructions to deceive users.
- When examples are needed, use short sanitized snippets and label them as examples.
- For uncertain cases, prefer safe verification steps over definitive accusations.
