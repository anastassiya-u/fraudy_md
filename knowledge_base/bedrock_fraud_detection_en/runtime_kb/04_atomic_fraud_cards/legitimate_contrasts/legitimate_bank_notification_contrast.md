---
title: "Legitimate bank notification contrast"
doc_type: "legitimate_contrast"
primary_channel: "all"
primary_risk_domain: "phishing"
language: "en"
region: "global"
runtime_use: true
safe_use: "defensive_only"
bedrock_ready: true
last_reviewed: "2026-05-07"
---

# Legitimate bank notification contrast

## Pattern summary
This contrast helps avoid false positives for real bank alerts while still protecting users from bank impersonation.

## Core deception
Fraudulent alerts try to move the user into secret disclosure, transfer, remote access, or unofficial links.

## Common channels
- sms
- email
- phone_call
- mobile_app

## Red flags
- Legitimate bank alerts usually direct users to the official app or published support number
- Legitimate staff should not ask for OTP/PIN/CVV/password
- Legitimate security teams do not ask users to transfer funds to a safe account

## Scam examples
- Possible scam: caller asks for OTP to cancel transaction.
- Possible scam: SMS link asks for full card details.

## Legitimate contrast
A legitimate alert may say a transaction was blocked and ask the user to review it in the official app without sharing secrets.

## What NOT to classify as fraud automatically
- Do not mark every bank alert as fraud
- Do not mark official-app notifications as fraud when no secrets or transfers are requested

## Safe user actions
- Open the bank app manually
- Call the number on the card if concerned
- Do not share codes
- Freeze card/contact bank if data was exposed

## Runtime model instruction
Use this contrast whenever a bank-themed message has mixed evidence. Lower risk when user initiated official-app action and no human requests secrets.
