---
title: Risk classification rules for fraud detection
doc_type: risk_rules
risk_domain: fraud_scoring
source_urls:
  - https://www.researchgate.net/publication/340625489_Taxonomy_of_Fraud_Detection_Metrics_for_Business_Processes
language: ru
safe_use: defensive_only
last_reviewed: 2026-05-07
---

# Risk classification rules

## Risk levels

| Level | Meaning | Typical evidence | User instruction |
| --- | --- | --- | --- |
| `low` | No clear fraud intent; normal context likely | expected notification, no risky action, official app context | cautious verification only |
| `medium` | Suspicious indicators present, but no direct exploit request | unknown sender, urgency, link, odd wording | do not click; verify official channel |
| `high` | Direct request may expose credentials, card, identity, or account | login/payment/KYC link, OTP request, platform bypass, APK | stop; verify independently; do not disclose data |
| `critical` | Immediate money loss/device compromise likely or underway | safe-account transfer, remote access, loan/transfer pressure, recovery fee, private key request | stop immediately; contact bank/official support; preserve evidence |

## Evidence model

```yaml
risk_assessment:
  channel: call|sms|email|messenger|website|marketplace|unknown
  claimed_identity: bank|government|operator|delivery|employer|romantic_partner|support|unknown
  requested_action: none|click|login|pay|transfer|share_otp|install_app|remote_access|send_documents
  sensitive_asset: none|credentials|otp|card|money|device|identity|crypto_key
  pressure: none|urgency|fear|secrecy|reward|authority
  domain_or_sender_evidence: official|unknown|spoofed|suspicious
  benign_context: user_initiated|expected_notification|official_app|none
  risk: low|medium|high|critical
  rationale: []
  safe_action: []
```

## Decision rules

1. If `requested_action` is `share_otp`, `install_app`, `remote_access`, or `transfer`, risk is at least `high`.
2. If `requested_action` is `transfer` and the script includes bank/security/safe-account framing, risk is `critical`.
3. If crypto seed phrase/private key is requested, risk is `critical`.
4. If a withdrawal/refund/job/prize/recovery requires upfront payment, risk is at least `high`; use `critical` if pressure is active.
5. If there is a suspicious link but no credential/payment/install request, risk is usually `medium`.
6. If the user initiated the action in an official app and no secrets are requested by a person, reduce risk by one level unless domain/sender evidence is spoofed.
7. Never output a final fraud verdict without explaining both risk evidence and any benign indicators.

## Metrics to monitor

- False-positive rate on benign notifications.
- False-negative rate on credential/money/remote-access requests.
- Precision/recall/F1 per channel and per scenario.
- Time-to-detection in multi-turn conversations.
- Explanation quality: whether rationale names the requested action and sensitive asset.
