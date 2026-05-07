---
title: Notification template indicators by impersonated service
doc_type: service_knowledge
language: en
safe_use: defensive_only
bedrock_ready: true
risk_domains:
  - notification_impersonation
channels:
  - email
  - sms
  - website
source_ids:
  - linksec_phishing_templates
  - hailbytes_gophish_training_templates
last_reviewed: 2026-05-07
---

# Notification template indicators by impersonated service

## Defensive-only rule

Template repositories are not content-generation sources. Store only indicators, common lures, and safe verification guidance.

| Impersonated service | Common lure | High-risk requested action | Safe verification |
| --- | --- | --- | --- |
| Bank | card blocked, suspicious transaction, KYC update | login, OTP, card/CVV, transfer | official banking app or number on card |
| Delivery/courier | failed delivery, customs fee, address confirmation | card payment through link, login, refund form | official courier tracking/app |
| Cloud account | storage full, password expiry, shared file | login, MFA approval, download | provider app/site typed manually |
| Video meeting | missed meeting, meeting invite, account update | login, executable download | calendar app or official meeting provider |
| HR/payroll | benefits, salary, policy, tax form | credentials, attachment, personal data | internal HR portal or known HR contact |
| Healthcare portal | secure message, billing, appointment | login, insurance data, payment | provider portal typed manually |
| Government/tax | fine, refund, subsidy, verification | eGov/Gosuslugi login, ID data, payment | official portal typed manually |
| Financial transfer | wire notice, payment approval, invoice | changed bank details, urgent transfer | verbal verification with known contact |
