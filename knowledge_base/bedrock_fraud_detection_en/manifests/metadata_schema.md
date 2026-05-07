---
title: "Fraudy Bedrock metadata sidecar schema"
doc_type: "metadata_schema"
language: "en"
safe_use: "defensive_only"
last_reviewed: "2026-05-07"
---

# Fraudy Bedrock metadata sidecar schema

Every runtime Markdown file under `runtime_kb/` has a sidecar file named `original_file.md.metadata.json` in the same folder.

## Required JSON wrapper

```json
{
  "metadataAttributes": {
    "project": "fraudy",
    "kb_version": "v1",
    "doc_type": "fraud_pattern",
    "primary_channel": "sms",
    "primary_risk_domain": "smishing",
    "language": "en",
    "region": "global",
    "source_kind": "curated_card",
    "source_reliability": "medium",
    "runtime_use": true,
    "safe_use": "defensive_only",
    "contains_examples": true,
    "contains_policy": false,
    "contains_legitimate_contrast": true,
    "last_reviewed": "2026-05-07"
  }
}
```

## Filtering guidance

Use `doc_type`, `primary_channel`, `primary_risk_domain`, `language`, `region`, `runtime_use`, and `safe_use` for Bedrock Knowledge Base metadata filtering. Metadata values are intentionally short strings/booleans to keep sidecars below 10 KB.
