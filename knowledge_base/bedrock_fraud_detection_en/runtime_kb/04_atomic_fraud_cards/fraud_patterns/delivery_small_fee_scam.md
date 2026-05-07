---
title: "Delivery small-fee scam"
doc_type: "fraud_pattern"
primary_channel: "sms"
primary_risk_domain: "smishing"
language: "en"
region: "global"
runtime_use: true
safe_use: "defensive_only"
bedrock_ready: true
last_reviewed: "2026-05-07"
---

# Delivery small-fee scam

## Pattern summary
A delivery or customs message claims that a package is blocked and asks for a small fee through an unsolicited link.

## Core deception
The user is led to believe a real parcel will be lost unless they pay immediately or update card details.

## Common channels
- sms
- email
- messenger
- web_page

## Red flags
- Unexpected delivery problem message
- Small payment requested through [unknown-link]
- Card details requested to reschedule delivery
- Urgent deadline or package return threat

## Scam examples
- Package on hold; pay a small customs fee at [unknown-link].
- Delivery failed; confirm card for re-delivery at [suspicious-domain].

## Legitimate contrast
Legitimate couriers usually allow tracking in the official app/site and do not require card data from an unsolicited link to receive a parcel.

## What NOT to classify as fraud automatically
- User is expecting a parcel and checks tracking inside the official app
- Notification contains no payment, login, or card request

## Safe user actions
- Do not tap the unsolicited link
- Open the courier or marketplace app manually
- Do not enter card details to receive a package
- Report the message if the courier supports abuse reports

## Runtime model instruction
Use this card when a delivery-themed message requests payment, card data, or login through a link. Raise risk when urgency and payment/card collection appear together.
