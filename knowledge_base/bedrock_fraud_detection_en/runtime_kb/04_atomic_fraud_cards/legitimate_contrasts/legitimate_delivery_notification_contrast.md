---
title: "Legitimate delivery notification contrast"
doc_type: "legitimate_contrast"
primary_channel: "sms"
primary_risk_domain: "smishing"
language: "en"
region: "global"
runtime_use: true
safe_use: "defensive_only"
bedrock_ready: true
last_reviewed: "2026-05-07"
---

# Legitimate delivery notification contrast

## Pattern summary
This contrast helps distinguish normal parcel tracking messages from delivery phishing.

## Core deception
Delivery scams use parcel urgency to collect card data, fees, credentials, or identity information through unsolicited links.

## Common channels
- sms
- email
- messenger
- mobile_app

## Red flags
- Legitimate tracking can be checked in the courier or marketplace app
- Legitimate messages may contain tracking numbers but should not require card data to receive money
- Unexpected customs/payment links require verification

## Scam examples
- Possible scam: pay redelivery fee at [unknown-link].
- Possible scam: enter card to confirm package refund.

## Legitimate contrast
A legitimate delivery notification may simply provide status or tell the user to check the official app.

## What NOT to classify as fraud automatically
- Do not mark expected parcel status updates as fraud if no risky action is requested
- Do not classify a tracking number alone as suspicious

## Safe user actions
- Track through official app/site
- Avoid payment links from SMS
- Contact courier support through official channel
- Do not enter card data from unsolicited link

## Runtime model instruction
Use this contrast when a delivery message lacks payment, login, or card requests. Keep risk lower but recommend official tracking.
