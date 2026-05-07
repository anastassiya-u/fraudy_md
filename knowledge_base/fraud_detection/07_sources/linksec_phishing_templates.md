---
title: LinkSec phishing templates
doc_type: source_card
source_kind: template_indicators
source_urls:
  - https://github.com/LinkSec/phishing-templates
language: ru
safe_use: defensive_only
last_reviewed: 2026-05-07
---

# LinkSec phishing templates

## Source URL

<https://github.com/LinkSec/phishing-templates>

## RAG role

Defensive indicators from brand-impersonation templates; do not use for generating phishing content.

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
