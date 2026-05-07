---
title: Audio fraud and voice deepfake research PDF
doc_type: source_card
source_kind: research_summary
source_urls:
  - https://www.nict.go.jp/en/asean_ivo/gden8c00000004el-att/pdnf1l00000004j7.pdf
language: ru
safe_use: defensive_only
last_reviewed: 2026-05-07
---

# Audio fraud and voice deepfake research PDF

## Source URL

<https://www.nict.go.jp/en/asean_ivo/gden8c00000004el-att/pdnf1l00000004j7.pdf>

## RAG role

Voice/deepfake detection source for vishing support signals.

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
