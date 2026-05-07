---
title: "Risk scoring and safe user actions"
doc_type: "safe_response_policy"
primary_channel: "all"
primary_risk_domain: "general"
language: "en"
region: "global"
runtime_use: true
safe_use: "defensive_only"
bedrock_ready: true
last_reviewed: "2026-05-07"
---

# Risk scoring and safe user actions

## Risk levels

| Risk | Definition | Evidence examples | User action |
| --- | --- | --- | --- |
| low | No clear fraud intent; benign context likely | expected message, no risky requested action, official app context | verify normally; stay cautious |
| medium | Suspicious context but no direct exploit request | unknown sender, urgency, link, odd branding | do not click; verify via official channel |
| high | Direct request can expose credentials, card, identity, or account | login/payment link, OTP request, APK install, platform bypass | stop; do not disclose data; verify independently |
| critical | Immediate money loss, account takeover, or device compromise likely | safe-account transfer, remote access, private key request, withdrawal fee, recovery fee | stop immediately; contact bank/official support; preserve evidence |

## Deterministic escalation rules

```yaml
rules:
  - if requested_action in [share_otp, install_app, remote_access, transfer_money, share_crypto_key]: risk_at_least: high
  - if requested_action == transfer_money and claimed_service == bank and hook contains safe_account: risk: critical
  - if requested_action == share_crypto_key: risk: critical
  - if upfront_fee_required_for in [job, prize, refund, withdrawal, recovery]: risk_at_least: high
  - if suspicious_link and no credential_payment_install_request: usual_risk: medium
  - if benign_context in [user_initiated, official_app] and no person requests secrets: lower_risk_by_one_level: true
```

## Safe response policy

- Never ask the user to provide OTP, PIN, password, CVV, seed phrase, or private documents in chat.
- Prefer official-channel verification over definitive accusations when evidence is incomplete.
- If money/card/banking data was exposed, advise immediate bank contact and evidence preservation.
- If suspicious software was installed, advise disconnecting internet if needed, uninstalling suspicious apps, reviewing permissions, updating OS/security tools, and seeking official support.
