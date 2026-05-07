---
title: Real or Fake fake jobposting prediction dataset
doc_type: source_card
source_kind: dataset
source_urls:
  - https://www.kaggle.com/datasets/shivamb/real-or-fake-fake-jobposting-prediction
language: ru
safe_use: defensive_only
last_reviewed: 2026-05-07
---

# Real or Fake fake jobposting prediction dataset

## Source URL

<https://www.kaggle.com/datasets/shivamb/real-or-fake-fake-jobposting-prediction>

## RAG role

Job posting dataset for employment-scam features and benign recruitment controls.

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
