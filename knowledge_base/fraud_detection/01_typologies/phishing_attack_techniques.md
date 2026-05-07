---
title: Classic, modern, and cutting-edge phishing attack techniques
source_urls:
  - https://www.mdpi.com/1999-5903/12/10/168
doc_type: typology
risk_domain: phishing
language: ru
safe_use: defensive_only
last_reviewed: 2026-05-07
---

# Phishing attack techniques

## Technique families

| Family | Description for detection | Indicators |
| --- | --- | --- |
| Classic email phishing | Массовые email с имитацией бренда и ссылкой на credential page | generic greeting, spoofed domain, login urgency |
| Spear phishing | Персонализированная атака на конкретного человека/организацию | internal context, executive/vendor impersonation, payment change |
| Smishing | SMS/messenger phishing with short messages and links | shortened URL, delivery/bank hook, urgent action |
| Vishing | Voice call impersonation | caller authority, fear, OTP request, safe-account script |
| Clone phishing | Legitimate-looking copy of prior communication with modified link/attachment | повтор темы, but changed link or attachment |
| Credential harvesting page | Fake login/payment/KYC page | brand mimicry, password/OTP/card fields, domain mismatch |
| MFA/OTP interception | Convincing user to disclose one-time code or approve push | "read the code", "confirm push", live pressure |
| QR phishing | QR code hides destination URL | QR in email/poster, payment or login destination not visible |
| Ad/search phishing | Fake support or bank result in ads/search | sponsored result, fake phone number, remote access request |

## Defensive use

The model should map an observed artifact to one or more technique families, then retrieve the appropriate scenario document. A message can be both smishing and bank impersonation, or both romance scam and investment fraud.
