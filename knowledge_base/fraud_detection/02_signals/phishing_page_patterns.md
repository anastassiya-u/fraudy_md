---
title: Phishing website UX/UI patterns
source_urls:
  - https://www.researchgate.net/publication/364718137_PhishInPatterns_measuring_elicited_user_interactions_at_scale_on_phishing_websites
doc_type: signal_rules
risk_domain: phishing_pages
language: ru
safe_use: defensive_only
last_reviewed: 2026-05-07
---

# Phishing website UX/UI patterns

## Purpose

Modern phishing pages can look professional. Fraudy should inspect requested interactions, page context, and URL/domain evidence rather than visual polish alone.

## Interaction patterns that raise risk

- Login form reached from unsolicited SMS/email/chat.
- Payment/card form for delivery, marketplace payout, refund, fee, tax, or verification.
- OTP entry screen after password/card entry.
- Multi-step flow that collects progressively more sensitive data.
- Fake loading/progress screens that keep the user engaged while attackers attempt live login.
- Chat/support widget that pressures user to continue.
- CAPTCHA or bot checks used to block automated security crawlers.
- Browser notification, file download, APK, or configuration profile prompt.

## Legitimacy mimicry patterns

- Brand logo, color palette, footer links, fake copyright.
- Security badges and lock icons inside page content.
- Domain that visually resembles the brand but is not official.
- Language localized to the user’s country/telecom/bank.

## Detection rule

Visual professionalism is not evidence of safety. If a page asks for credentials, card data, OTP, or installation and was reached through an unsolicited link, classify as at least `high` risk.
