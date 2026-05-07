---
title: Phishing classification techniques and evaluation dimensions
source_urls:
  - https://www.researchgate.net/publication/359884880_Phishing_Classification_Techniques_A_Systematic_Literature_Review
doc_type: typology
risk_domain: phishing_detection
language: ru
safe_use: defensive_only
last_reviewed: 2026-05-07
---

# Phishing classification techniques

## Source summary

Систематические обзоры phishing classification обычно группируют проблему по четырем осям: techniques, datasets, performance evaluation и phishing types. Для Fraudy это полезно как схема оценки качества классификатора, а не как единственный набор правил.

## Classification dimensions

| Dimension | Examples | RAG metadata to keep |
| --- | --- | --- |
| Techniques | rule-based features, lexical URL features, content features, ML classifiers, deep learning, hybrid systems | `technique_family`, `features_used`, `model_type` |
| Datasets | emails, SMS, URLs, webpages, conversations, screenshots | `dataset_name`, `label_schema`, `license`, `collection_period` |
| Performance evaluation | precision, recall, F1, ROC-AUC, false-positive rate, false-negative rate | `metric`, `threshold`, `test_split` |
| Phishing types | email phishing, spear phishing, smishing, vishing, clone phishing, credential-harvesting pages | `phishing_type`, `channel`, `target_asset` |

## Practical rules for Fraudy

- Optimize for **low false negatives** when the requested action exposes money, credentials, OTP, private keys, or remote device access.
- Optimize for **low false positives** when the input is a benign notification without a risky requested action.
- Use datasets only as evidence of patterns; do not assume labels transfer perfectly across languages, regions, or years.
