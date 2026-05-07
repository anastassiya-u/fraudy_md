---
title: What not to classify as fraud automatically
source_urls:
  - https://www.researchgate.net/publication/359884880_Phishing_Classification_Techniques_A_Systematic_Literature_Review
doc_type: false_positive_control
risk_domain: classification_quality
language: ru
safe_use: defensive_only
last_reviewed: 2026-05-07
---

# What not to classify as fraud automatically

## Purpose

Этот документ снижает false positives. Fraudy должен объяснять риск, но не должен объявлять мошенничеством каждое сообщение с брендом, ссылкой или срочным текстом.

## Benign indicators

| Situation | Why it may be normal | Required caution |
| --- | --- | --- |
| User initiated the action | Пользователь сам вошел в приложение/сайт или запросил reset | Verify domain/app, do not share OTP with people |
| Official app notification | Push inside installed bank/operator/government app can be legitimate | Open app directly, not via SMS link |
| Expected delivery update | Пользователь реально ждет доставку | Track through official app/site; beware payment/card requests |
| Password reset email requested by user | Reset links can be normal | Check sender/domain; never share code with caller |
| Bank fraud alert that asks only to confirm yes/no in app | Some banks send alerts | Use official app/phone number; no OTP/card/CVV disclosure |
| Marketing discount | Promotions are common | Risk rises if APK, card details, or unofficial payment are requested |
| Job offer after formal application | Recruiters may contact candidates | No upfront fees, no task deposits, verify company domain |
| Marketplace negotiation | Buyers/sellers negotiate price and shipping | Keep payment inside platform; avoid external payment forms |

## False-positive reduction rules

- Do not classify as fraud solely because a message contains a link.
- Do not classify as fraud solely because the sender is unknown; combine with requested action and asset risk.
- Do not classify as fraud solely because the text has urgency; legitimate security notifications can be urgent.
- Escalate only when urgency is paired with secret disclosure, money transfer, remote access, APK/install, or unofficial payment/login page.
- If uncertain, recommend verification via official channel rather than declaring fraud.
