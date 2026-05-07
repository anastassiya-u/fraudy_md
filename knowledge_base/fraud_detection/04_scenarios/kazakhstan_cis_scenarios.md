---
title: Kazakhstan and CIS local fraud scenarios for Fraudy MVP
doc_type: scenario_catalog
risk_domain: local_fraud
regions: [kazakhstan, cis]
language: ru
safe_use: defensive_only
last_reviewed: 2026-05-07
---

# Kazakhstan/CIS local fraud scenarios

## 1. Fake bank security call / “safe account” scam

```yaml
scenario: fake_bank_safe_account_call
channels: [call, sms, messenger]
intent: credential_theft_or_money_transfer
risk: critical
steps:
  - authority_impersonation_bank_security
  - suspicious_transaction_or_hack_claim
  - urgency_and_fear
  - request_otp_app_install_credit_or_transfer
signals:
  - "safe account"
  - "suspicious transaction"
  - "your money is at risk"
  - request for OTP/code
  - request to install remote app
outcomes:
  - money theft
  - loans issued on victim
recommended_action:
  - hang up
  - call official bank number from card/app/site
  - do not transfer money or share codes
```

## 2. SMS blaster fake operator/bank messages

```yaml
scenario: sms_blaster_fake_operator_bank
channels: [sms]
intent: credential_or_card_theft
risk: high
steps:
  - spoofed_sender_or_fake_base_station
  - bank_operator_delivery_problem_claim
  - urgent_link
  - fake_login_or_payment_page
signals:
  - "card is blocked"
  - "confirm account"
  - "package delivery failed"
  - suspicious link
  - fake telecom or bank branding
outcomes:
  - credential theft
  - card theft
recommended_action:
  - do not tap link
  - open official app manually
  - report SMS to operator/bank if possible
```

## 3. Telecom/service discount call scam

```yaml
scenario: telecom_service_discount_call
channels: [call, sms, messenger]
intent: device_compromise_or_bank_theft
risk: high
steps:
  - unsolicited_offer
  - discount_bonus_service_claim
  - phone_settings_or_app_install_instruction
  - access_to_device_or_banking
signals:
  - unsolicited telecom offer
  - remote instructions
  - code request
  - APK or configuration install
outcomes:
  - device compromise
  - banking theft
recommended_action:
  - refuse remote instructions
  - verify offer in official operator app
```

## 4. Fake investment / crypto platform

```yaml
scenario: fake_investment_crypto_platform
channels: [ads, social_media, messenger, website]
intent: investment_theft
risk: critical
steps:
  - profit_promise
  - fake_professional_platform
  - fake_dashboard_profits
  - pressure_for_more_deposits
  - withdrawal_blocked_with_fee_or_tax
signals:
  - guaranteed returns
  - pressure to deposit more
  - withdrawal fee or tax
  - fake dashboard profits
outcomes:
  - investment theft
recommended_action:
  - stop deposits
  - do not pay withdrawal fees
  - preserve evidence and contact bank/law enforcement
```

## 5. Romance + investment hybrid scam

```yaml
scenario: romance_investment_hybrid
channels: [dating_app, social_media, messenger]
intent: emotional_and_financial_exploitation
risk: critical
steps:
  - online_relationship
  - rapid_trust_and_emotional_attachment
  - investment_or_crypto_opportunity
  - deposits_and_escalation
signals:
  - fast emotional bonding
  - financial advice from stranger
  - crypto/investment recommendation
  - refusal to video meet or verify identity
outcomes:
  - emotional harm
  - investment theft
recommended_action:
  - stop payments
  - verify independently
  - talk to trusted person before acting
```

## 6. Fake marketplace / classifieds scam

```yaml
scenario: fake_marketplace_classifieds
channels: [marketplace_chat, messenger, sms]
intent: card_or_payment_theft
risk: high
steps:
  - product_listing_or_buyer_contact
  - fake_payment_or_delivery_link
  - card_details_or_login_requested
signals:
  - external payment link
  - courier payment verification
  - urgency to confirm
  - platform bypass
outcomes:
  - card theft
recommended_action:
  - keep payment in platform
  - do not enter card to receive money
```

## 7. Government services phishing (Gosuslugi/eGov style)

```yaml
scenario: government_services_phishing
channels: [sms, email, call, website]
intent: account_takeover_or_identity_theft
risk: high
steps:
  - government_impersonation
  - account_issue_fine_or_verification_claim
  - fake_login_page
signals:
  - credential request
  - urgency
  - domain spoofing
  - fake fine or verification
outcomes:
  - account takeover
  - identity theft
recommended_action:
  - open official government portal manually
  - do not log in via unsolicited link
```

## 8. Fake job / employment scam

```yaml
scenario: fake_job_employment_scam
channels: [job_platform, email, messenger]
intent: payment_or_data_theft
risk: high
steps:
  - attractive_remote_job_offer
  - high_pay_low_requirements
  - migration_to_private_messenger
  - registration_fee_training_fee_card_details_or_task_deposit
signals:
  - unrealistic salary
  - payment before employment
  - platform migration
  - vague employer identity
outcomes:
  - payment theft
  - data theft
recommended_action:
  - do not pay to get a job
  - verify company domain and legal entity
```

## 9. Technical support scam

```yaml
scenario: technical_support_scam
channels: [popup, call, search_ad, website]
intent: device_compromise_or_payment_theft
risk: critical
steps:
  - malware_warning_popup_or_call
  - fake_support_number
  - remote_control_request
  - payment_or_bank_access
signals:
  - malware warning popup
  - remote access request
  - payment for fixing issue
outcomes:
  - device compromise
  - banking theft
recommended_action:
  - close browser or disconnect internet if needed
  - do not grant remote access
  - contact official support independently
```

## 10. Recovery scam / second-order fraud

```yaml
scenario: recovery_scam_second_order_fraud
channels: [messenger, social_media, forum, call]
intent: second_financial_loss
risk: critical
steps:
  - victim_already_lost_money
  - fake_hacker_lawyer_investigator_or_recovery_service
  - guaranteed_recovery_claim
  - upfront_fee
signals:
  - upfront recovery payment
  - guaranteed recovery
  - request for wallet keys or bank access
outcomes:
  - victim scammed twice
recommended_action:
  - do not pay recovery fee
  - report through official law enforcement/bank channels
```
