---
title: Bedrock-ready English fraud detection knowledge base
doc_type: index
language: en
safe_use: defensive_only
bedrock_ready: true
last_reviewed: 2026-05-07
---

# Bedrock-ready English fraud detection knowledge base

This directory is an English, Amazon Bedrock/RAG-oriented knowledge base distilled from the source list stored in `knowledge_base/fraud_detection`. It is designed for the Fraudy AI service to compare user-submitted messages, calls, conversations, URLs, and pages against structured fraud knowledge.

## Directory layout

| Directory | Purpose |
| --- | --- |
| `00_manifest` | source inventory, document schema, and ingestion manifest |
| `01_source_extractions` | one markdown extraction per referenced source/document/service |
| `02_service_knowledge` | normalized fraud knowledge by impersonated service or scam domain |
| `03_detection_policy` | risk scoring, false-positive controls, and safe response policy |
| `04_bedrock_ingestion` | Amazon Bedrock chunking, metadata, and retrieval guidance |

## Retrieval rule of thumb

For every classification request, retrieve:

1. the relevant service/scenario document from `02_service_knowledge`,
2. `03_detection_policy/risk_scoring_and_actions.md`,
3. `03_detection_policy/false_positive_controls.md`, and
4. one or more source extraction files from `01_source_extractions`.

## Safety boundary

This knowledge base is defensive-only. Template repositories and scam conversations are summarized as indicators and evaluation material; they must not be used to generate operational phishing, scam, or social-engineering content.
