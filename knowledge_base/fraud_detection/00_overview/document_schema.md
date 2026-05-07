---
title: Markdown document schema for Fraudy RAG files
doc_type: schema
language: ru
audience: rag_ingestion
last_reviewed: 2026-05-07
safe_use: defensive_only
---

# Markdown document schema

## Required frontmatter

```yaml
title: Human-readable title
doc_type: typology|signal_rules|dataset_notes|scenario_catalog|scenario_patterns|safe_actions|risk_rules|source_card|ingestion_guide
risk_domain: phishing|smishing|vishing_audio_deepfake|marketplace|employment_scams|fraud_scoring
source_urls:
  - https://example.com/source
language: ru
safe_use: defensive_only
last_reviewed: 2026-05-07
```

## Recommended body sections

1. `Purpose` or `RAG role`.
2. Normalized tables for indicators, scenarios, datasets, or actions.
3. `Benign controls` where applicable.
4. `Safe response` for user-facing action.
5. YAML/JSON-like extraction schema for machine-friendly retrieval.

## Label vocabulary

- `fraud_indicator`: raises risk.
- `benign_indicator`: lowers risk or prevents overclassification.
- `requested_action`: what the attacker asks user to do.
- `sensitive_asset`: what can be lost or exposed.
- `safe_action`: recommended non-harmful user action.
- `risk`: low, medium, high, critical.
