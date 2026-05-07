---
title: Smishing psychological patterns and text-message tactics
source_urls:
  - https://arxiv.org/pdf/2604.11429
doc_type: signal_rules
risk_domain: smishing
channels: [sms, messenger]
language: ru
safe_use: defensive_only
last_reviewed: 2026-05-07
---

# Smishing psychological patterns

## Common psychological tactics

| Tactic | Text pattern | Risk interpretation |
| --- | --- | --- |
| Fear/loss | card blocked, account suspended, fine, suspicious transaction | strong when link or OTP request follows |
| Urgency | confirm today, act now, final notice | medium alone; high with credential/payment request |
| Curiosity | missed delivery/photo/document | medium; high with APK or login form |
| Reward | bonus, refund, subsidy, prize | high if fee/card/login needed |
| Authority | bank, telecom, eGov, police, tax | high if channel cannot be verified |
| Convenience | one-click verification, quick courier payment | high if outside official app/platform |

## Smishing-specific indicators

- Shortened or masked URL.
- Sender name spoofing that looks like a bank/operator but arrives in a new thread.
- Request to install APK or mobile configuration profile.
- Link destination differs from displayed brand.
- Message asks user to solve a “problem” that the user did not initiate.

## Benign control

SMS notifications can be legitimate. Recommend opening the official app manually and checking the issue there instead of tapping the SMS link.
