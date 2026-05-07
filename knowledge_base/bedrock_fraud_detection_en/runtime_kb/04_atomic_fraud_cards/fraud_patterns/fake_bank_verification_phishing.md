---
title: "Fake bank verification phishing"
doc_type: "fraud_pattern"
primary_channel: "phone_call"
primary_risk_domain: "phishing"
language: "en"
region: "global"
runtime_use: true
safe_use: "defensive_only"
bedrock_ready: true
last_reviewed: "2026-05-07"
---

# Fake bank verification phishing

## Pattern summary
An attacker impersonates a bank or bank security team and claims the account must be verified or protected.

## Core deception
The user is led to believe the caller/message is an official bank employee preventing loss or account takeover.

## Common channels
- phone_call
- sms
- email
- messenger

## Red flags
- Request for OTP, PIN, password, CVV, or card data
- Claim of suspicious transaction or account takeover
- Instruction to keep the call active while using banking app
- Request to transfer funds to a safe account

## Scam examples
- Bank security detected suspicious activity; verify your code now.
- Your card will be blocked unless you confirm details at [unknown-link].

## Legitimate contrast
Legitimate banks may alert users but do not ask customers to disclose OTP/PIN/CVV to a caller or move money to a safe account.

## What NOT to classify as fraud automatically
- User independently opened official bank app and sees a standard alert
- Bank notification asks only to contact official support and requests no secrets

## Safe user actions
- Hang up or stop replying
- Open official bank app or call number on card
- Never share OTP/PIN/CVV
- Contact bank immediately if data was shared

## Runtime model instruction
Use this card for bank impersonation. Classify as high or critical when secrets, transfer, loan, remote access, or safe-account language appears.
