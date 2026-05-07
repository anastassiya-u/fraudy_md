---
title: Fraud typologies for Fraudy MVP
source_urls:
  - https://assets.publishing.service.gov.uk/media/5a7ad8c2ed915d670dd7efad/fraud-typologies.pdf
doc_type: typology
risk_domain: fraud_general
language: ru
regions: [global, kazakhstan, cis]
safe_use: defensive_only
last_reviewed: 2026-05-07
---

# Fraud typologies

## Purpose

Использовать как верхнеуровневую карту мошенничества. Документ помогает RAG-классификатору определить, к какой семье относится подозрительный кейс, и выбрать более детальный сценарий.

## High-level taxonomy

| Typology | Core pattern | Common channels | Primary harm | Typical red flags |
| --- | --- | --- | --- | --- |
| Identity theft | Получение персональных данных для доступа к аккаунтам или кредитам | SMS, email, call, fake forms | Account takeover, credit fraud | request for ID, OTP, password, KYC upload через неизвестную ссылку |
| Payment diversion | Перенаправление платежа на счет мошенника | email, invoice, messenger | direct transfer loss | changed bank details, urgent invoice, refusal to verify by official channel |
| Advance-fee fraud | Обещание выгоды после предоплаты | messenger, marketplace, job, romance | upfront fee loss | fee before reward, tax/clearance fee, guaranteed payout |
| Investment fraud | Обещание высокой доходности или fake trading dashboard | ads, social media, messenger | investment theft | guaranteed returns, withdrawal blocked, pressure to deposit more |
| Impersonation fraud | Имитация банка, госоргана, доставки, работодателя, службы поддержки | call, SMS, email, website | credentials, money transfer | authority claim, urgency, spoofed branding, unofficial link |
| Marketplace fraud | Обман покупателя/продавца через fake payment/delivery flow | classifieds, marketplace chat, courier link | card theft, goods theft | external payment link, courier verification, platform bypass |
| Romance/social trust fraud | Доверительные отношения с последующим финансовым запросом | dating apps, social media, messenger | emotional and financial exploitation | fast intimacy, crisis story, investment advice from stranger |
| Tech support fraud | Fake alert/call and remote access request | pop-up, call, search ads | device compromise, payment theft | malware warning, support number, remote-control app |
| Recovery fraud | Повторное мошенничество после уже случившейся потери | messenger, social media, forums | second loss | guaranteed recovery, upfront fee, fake investigator/hacker |

## RAG usage notes

- Не классифицировать только по одному слабому признаку. Использовать комбинацию: intent + requested action + channel + urgency + asset at risk.
- Если обнаружен запрос на OTP, password, card details, remote access или перевод денег на неизвестный счет, повышать риск минимум до `high`.
- Если пользователь уже инициировал контакт с официальной организацией и нет запроса секретов/денег/remote access, не считать мошенничеством автоматически.
