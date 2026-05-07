---
title: Fraudy fraud-detection knowledge base
doc_type: index
language: ru
audience: rag_ingestion
version: 0.1.0
last_reviewed: 2026-05-07
safe_use: defensive_only
---

# Fraudy fraud-detection knowledge base

Эта папка содержит RAG-ready markdown документы для базы знаний Fraudy: типологии мошенничества, признаки социальной инженерии, сценарии для Казахстана/СНГ, правила классификации риска, safe actions и список факторов, которые **не должны автоматически считаться мошенничеством**.

## Как использовать в RAG

1. Загружать документы как отдельные чанкуемые markdown-файлы.
2. Сохранять frontmatter как metadata: `doc_type`, `risk_domain`, `channels`, `regions`, `source_urls`, `safe_use`.
3. При ответе пользователю модель должна:
   - сравнить входящее сообщение/звонок/страницу с признаками и сценариями;
   - учитывать benign explanations и снижать false positives;
   - выдавать безопасную инструкцию без запроса секретов;
   - при высоком риске рекомендовать остановить действие и перейти в официальный канал.
4. Не использовать phishing templates для генерации новых фишинговых писем; они описаны только как defensive indicators.

## Структура

| Папка | Назначение |
| --- | --- |
| `00_overview` | карта источников и схема документов |
| `01_typologies` | типологии fraud/phishing/smishing/audio/deepfake |
| `02_signals` | red flags, social engineering, false-positive controls |
| `03_datasets` | наборы данных для scam/ham сообщений, URL, reviews, job scams |
| `04_scenarios` | сценарии: Казахстан/СНГ, marketplace, support, romance, investment, jobs |
| `05_actions` | безопасные инструкции пользователю |
| `06_risk` | правила risk classification и evidence scoring |
| `07_sources` | карточки источников по каждой ссылке |
| `08_ingestion` | рекомендации для AWS/RAG ingestion |

## Минимальный retrieval policy

- Для классификации всегда извлекать минимум: `risk_classification_rules.md`, `red_flags_social_engineering.md`, `not_automatically_fraud.md`, один или несколько документов сценариев по каналу.
- Для пользовательского совета всегда извлекать `safe_user_instructions.md`.
- Для обучения/оценки моделей извлекать соответствующий файл из `03_datasets` и карточку источника из `07_sources`.
