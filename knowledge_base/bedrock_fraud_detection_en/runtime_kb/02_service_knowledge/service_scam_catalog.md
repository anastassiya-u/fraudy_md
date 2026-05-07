---
title: "Service and scam-domain catalog for fraud detection"
doc_type: "service_knowledge"
primary_channel: "all"
primary_risk_domain: "general"
language: "en"
region: "global"
runtime_use: true
safe_use: "defensive_only"
bedrock_ready: true
last_reviewed: "2026-05-07"
---

# Service and scam-domain catalog

## Bank security / safe-account scam

```yaml
claimed_service: bank
channels: [phone, sms, messenger]
risk_floor: high
critical_when:
  - user is asked to share OTP/PIN/password/CVV
  - user is asked to transfer money to a safe account
  - user is instructed to install an app or keep the call open during banking actions
common_hooks:
  - suspicious transaction
  - account takeover attempt
  - money is at risk
  - loan or transfer must be blocked urgently
safe_response:
  - hang up
  - call the official bank number or open the official app manually
  - never share OTP or move money during an inbound call
```

## Telecom/operator discount or verification scam

```yaml
claimed_service: telecom_operator
channels: [phone, sms, messenger]
risk_floor: medium
high_when:
  - APK/profile/VPN/remote-access installation is requested
  - code sharing is requested
  - phone settings must be changed under caller instruction
common_hooks: [discount, bonus, SIM verification, account update]
safe_response: verify in the official operator app or storefront
```

## Delivery and courier phishing

```yaml
claimed_service: delivery_or_courier
channels: [sms, email, messenger, website]
risk_floor: medium
high_when:
  - user is asked to pay a small customs/delivery fee through an unsolicited link
  - card data is requested to receive a refund or delivery
  - courier verification occurs outside the marketplace platform
common_hooks: [failed delivery, address confirmation, customs fee, package on hold]
safe_response: track through the official courier or marketplace app
```

## Government portal / eGov / tax phishing

```yaml
claimed_service: government
channels: [sms, email, phone, website]
risk_floor: medium
high_when:
  - login credentials, identity documents, or payment are requested through an unsolicited link
  - threat of fine, account block, or legal consequence creates urgency
common_hooks: [fine, subsidy, refund, account verification, document notice]
safe_response: open the official government portal manually and verify there
```

## Marketplace and classifieds scam

```yaml
claimed_service: marketplace_or_courier_payment
channels: [marketplace_chat, messenger, sms, website]
risk_floor: medium
high_when:
  - payment moves outside the platform
  - card data is requested to receive money
  - buyer/seller sends a courier or payment verification link
common_hooks: [buyer already paid, courier pickup, confirm card, urgent reservation]
safe_response: keep payment and messaging inside the platform
```

## Technical support scam

```yaml
claimed_service: technical_support
channels: [phone, popup, search_ad, website]
risk_floor: high
critical_when:
  - remote access is requested
  - user is asked to pay to remove a fake infection
  - user is guided into banking or password screens while screen sharing
common_hooks: [device infected, account compromised, urgent repair, support number]
safe_response: close the page, do not grant access, contact official support independently
```

## Employment / fake job scam

```yaml
claimed_service: employer_or_recruiter
channels: [job_platform, email, messenger]
risk_floor: medium
high_when:
  - upfront fee, training fee, equipment fee, or task deposit is required
  - card/bank data is requested before a formal contract
  - salary is unrealistic and company identity is vague
common_hooks: [remote job, high pay, immediate hiring, easy tasks]
safe_response: do not pay to get a job; verify company domain and legal entity
```

## Investment and crypto scam

```yaml
claimed_service: investment_platform_or_broker
channels: [ads, social_media, messenger, website]
risk_floor: high
critical_when:
  - guaranteed returns are promised
  - withdrawal requires fee, tax, or additional deposit
  - private keys or seed phrases are requested
common_hooks: [exclusive opportunity, crypto profit, AI trading, fake dashboard profits]
safe_response: stop deposits and do not pay withdrawal fees
```

## Romance-investment hybrid

```yaml
claimed_service: romantic_contact
channels: [dating_app, social_media, messenger]
risk_floor: medium
critical_when:
  - romantic contact introduces investment/crypto opportunity
  - money, gift cards, crypto, or transfer help is requested
  - contact avoids identity verification while escalating intimacy
common_hooks: [fast emotional bond, crisis story, shared future, investment mentor]
safe_response: pause, consult a trusted person, and do not send money
```

## Recovery scam

```yaml
claimed_service: hacker_lawyer_investigator_recovery_service
channels: [messenger, social_media, forum, phone]
risk_floor: high
critical_when:
  - upfront recovery payment is required
  - guaranteed recovery is promised
  - wallet keys, bank access, or remote access are requested
common_hooks: [we can recover your funds, investigator, hacker, legal fee]
safe_response: do not pay; report through official bank/law-enforcement channels
```
