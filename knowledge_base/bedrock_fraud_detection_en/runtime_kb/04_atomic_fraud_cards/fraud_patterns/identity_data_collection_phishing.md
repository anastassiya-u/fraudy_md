---
title: "Identity data collection phishing"
doc_type: "fraud_pattern"
primary_channel: "web_page"
primary_risk_domain: "identity_fraud"
language: "en"
region: "global"
runtime_use: true
safe_use: "defensive_only"
bedrock_ready: true
last_reviewed: "2026-05-07"
---

# Identity data collection phishing

## Pattern summary
A fake form requests identity documents, personal data, card data, or account credentials under verification/KYC/update framing.

## Core deception
The user is led to believe identity submission is required to keep access, receive funds, or comply with rules.

## Common channels
- web_page
- email
- sms
- messenger
- document

## Red flags
- Unsolicited KYC or verification link
- Requests ID scans, selfie, card, login, OTP, or personal identifiers
- Domain does not match official service
- Urgency or account restriction pressure

## Scam examples
- Verify your identity at [unknown-link] to avoid account suspension.
- Upload ID and card details to receive refund.

## Legitimate contrast
Legitimate KYC usually occurs inside the official app or secure portal reached manually, not through unexpected links.

## What NOT to classify as fraud automatically
- User initiated verification inside official app
- Request is expected and domain/app is verified

## Safe user actions
- Do not upload documents from unsolicited links
- Open official app/site manually
- Contact official support
- Monitor accounts if data was submitted

## Runtime model instruction
Use this card when identity data is requested. Increase risk with unofficial domain, urgency, or paired OTP/card collection.
