---
title: "Professional appearance impersonation"
doc_type: "fraud_technique"
primary_channel: "web_page"
primary_risk_domain: "phishing"
language: "en"
region: "global"
runtime_use: true
safe_use: "defensive_only"
bedrock_ready: true
last_reviewed: "2026-05-07"
---

# Professional appearance impersonation

## Pattern summary
Fraud pages and messages may use polished branding, logos, HTTPS, and professional layouts to appear legitimate.

## Core deception
The user is led to trust visual quality instead of verifying domain, channel, and requested fields.

## Common channels
- web_page
- email
- sms
- messenger

## Red flags
- Professional page reached from unsolicited link
- Branding looks right but domain is unofficial
- Multi-step form requests credentials/card/OTP/ID
- Security badges or lock icons inside page content

## Scam examples
- A polished login page asks for card and OTP after an SMS link.
- A branded delivery page asks for payment at [suspicious-domain].

## Legitimate contrast
Legitimate services can look professional too; appearance is not enough either way. Domain, app context, and requested action matter.

## What NOT to classify as fraud automatically
- User typed official domain or used official app
- No sensitive data requested after unsolicited contact

## Safe user actions
- Check domain carefully
- Open service manually
- Do not trust logos or HTTPS alone
- Stop if OTP/card/ID collection follows unsolicited link

## Runtime model instruction
Use this technique card when the user says a page “looks real.” Explain that visual polish does not prove safety and evaluate requested fields.
