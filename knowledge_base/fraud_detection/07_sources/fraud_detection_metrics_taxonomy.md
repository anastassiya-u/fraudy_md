---
title: Taxonomy of fraud detection metrics for business processes
doc_type: source_card
source_kind: risk_metrics
source_urls:
  - https://www.researchgate.net/publication/340625489_Taxonomy_of_Fraud_Detection_Metrics_for_Business_Processes
language: ru
safe_use: defensive_only
last_reviewed: 2026-05-07
---

# Taxonomy of fraud detection metrics for business processes

## Source URL

<https://www.researchgate.net/publication/340625489_Taxonomy_of_Fraud_Detection_Metrics_for_Business_Processes>

## RAG role

Risk and detection metric concepts for evaluating fraud classifiers and business-process detection.

## Suggested extraction targets

- Ключевые fraud indicators или benign indicators.
- Каналы атаки: SMS, email, call, messenger, website, marketplace, job platform.
- Requested action: click, login, pay, transfer, share OTP, install app, remote access, send documents.
- Sensitive asset: credentials, OTP, card, money, device access, identity documents, crypto keys.
- Safe user action, если источник содержит prevention guidance.

## Defensive-use constraints

- Суммаризировать и структурировать, не копировать большие фрагменты источника.
- Не использовать для генерации убедительных scam/phishing templates.
- Проверять license/terms перед использованием датасета для обучения или публикации.
- Для ResearchGate/Kaggle/Hugging Face/GitHub источников хранить дату выгрузки и версию snapshot при ingestion.
