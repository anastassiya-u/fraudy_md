---
title: Bank, delivery, cloud, HR, and government notification template patterns
doc_type: scenario_patterns
risk_domain: notification_impersonation
source_urls:
  - https://github.com/LinkSec/phishing-templates
  - https://github.com/HailBytes/gophish-training-templates
language: ru
safe_use: defensive_only
last_reviewed: 2026-05-07
---

# Notification template patterns

## Defensive-only handling

Template repositories can be useful for awareness training and detector testing. Do not store or retrieve them as ready-to-send phishing copy. Store only indicators and safe examples.

## Common impersonated notification types

| Template family | Hook | Risky requested action |
| --- | --- | --- |
| Bank alert | card blocked, suspicious transaction, KYC update | login, OTP, card/CVV, transfer |
| Delivery notice | failed delivery, customs fee, address confirmation | small payment, card entry, login |
| Cloud account | storage full, password expiring, file shared | login, MFA approval |
| Video conference | missed meeting, Zoom invite, account update | login, download |
| HR/payroll | benefits update, salary document, policy acknowledgement | credentials, attachment, personal data |
| Healthcare/portal | secure message, HIPAA portal, appointment billing | login, insurance/payment data |
| Government/tax | fine, subsidy, refund, verification | eGov/Gosuslugi login, ID data, payment |

## Safe retrieval snippets

- “A legitimate notification should not require sharing OTP with a caller.”
- “Open the official app/site manually instead of using a link from an unsolicited message.”
- “Payment to receive money is a high-risk pattern in marketplace and delivery scams.”
