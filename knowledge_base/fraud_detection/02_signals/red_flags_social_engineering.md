---
title: Red flags and social-engineering indicators
source_urls:
  - https://www.mdpi.com/1999-5903/12/10/168
  - https://arxiv.org/pdf/2604.11429
  - https://www.mdpi.com/2076-3417/10/7/2363
doc_type: signal_rules
risk_domain: social_engineering
language: ru
safe_use: defensive_only
last_reviewed: 2026-05-07
---

# Red flags and social-engineering indicators

## Strong red flags

- Просьба сообщить OTP, password, PIN, CVV, private key, seed phrase или backup code.
- Просьба установить APK, remote access app, VPN/profile/configuration или отключить защиту.
- Просьба срочно перевести деньги, оформить кредит или отправить деньги на “safe account”.
- Ссылка на login/payment/KYC page, полученная из неожиданного SMS/email/chat.
- Давление временем: “сейчас”, “последний шанс”, “аккаунт будет заблокирован”, “операция уже идет”.
- Страх: “ваши деньги в опасности”, “попытка взлома”, “уголовная ответственность”, “штраф”.
- Нереалистичная выгода: guaranteed returns, high salary for low-skill work, prize without participation.
- Перевод общения за пределы официальной платформы: marketplace/job/dating chat → Telegram/WhatsApp.
- Запрет на проверку: “не кладите трубку”, “не говорите никому”, “банк не должен знать”.

## Medium red flags

- Unknown sender/number, especially with brand-like wording.
- Shortened, obfuscated, typo-squatted or newly registered-looking domain.
- Inconsistent language, formatting, logo quality, sender display name vs address.
- Attachment with macro/script/archive/password, especially if unexpected.
- Unusual payment method: gift cards, crypto, P2P transfer, courier cash, prepaid cards.

## Social-engineering levers

| Lever | How it appears | Detection cue |
| --- | --- | --- |
| Authority | bank, police, tax, eGov, employer, support agent | claimed role without verified channel |
| Urgency | immediate action required | deadline used to prevent verification |
| Fear | threat of loss, arrest, account block | emotional escalation before risky action |
| Scarcity/reward | prize, discount, job, investment | reward requires upfront fee/data |
| Reciprocity | “we helped you, now confirm” | user is asked to disclose secret |
| Trust/romance | emotional bonding | financial request from new relationship |
| Technical confusion | jargon about security/device infection | remote instructions or app install |

## Evidence scoring hint

A single medium red flag usually means `low` or `medium` risk. Any strong red flag involving credentials, money movement, remote access, or malware should move the case to `high` or `critical` depending on immediacy.
