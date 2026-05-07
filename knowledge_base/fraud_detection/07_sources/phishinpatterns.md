---
title: PhishInPatterns phishing website UX/UI study
doc_type: source_card
source_kind: research_summary
source_urls:
  - https://www.researchgate.net/publication/364718137_PhishInPatterns_measuring_elicited_user_interactions_at_scale_on_phishing_websites
language: ru
safe_use: defensive_only
last_reviewed: 2026-05-07
---

# PhishInPatterns phishing website UX/UI study

## Source URL

<https://www.researchgate.net/publication/364718137_PhishInPatterns_measuring_elicited_user_interactions_at_scale_on_phishing_websites>

## RAG role

Study of elicited user interactions, legitimacy mimicry, and crawler-evasion-oriented web design patterns.

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
