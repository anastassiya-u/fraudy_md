---
title: "PhishTank phishing URL clearing house"
doc_type: "source_extraction"
primary_channel: "web_page"
primary_risk_domain: "phishing"
language: "en"
region: "global"
runtime_use: true
safe_use: "defensive_only"
bedrock_ready: true
last_reviewed: "2026-05-07"
---

# PhishTank phishing URL clearing house

## What this source contributes to Fraudy

Use as URL reputation enrichment. Store lookup timestamp, normalized URL, domain, verdict, and confidence source.

## Key extracted facts

- PhishTank is a collaborative clearing house for phishing data and information.
- It provides an open API for developers and researchers to integrate anti-phishing data at no charge.
- The service is operated by Cisco Talos Intelligence Group.

## Fraud detection indicators

- URL reported or verified as phishing.
- Domain/path associated with credential theft or brand impersonation.
- Useful external reputation signal for suspicious links.

## False-positive controls

- No match in a URL feed does not prove safety.
- Old feed entries can be stale; phishing URLs are short-lived.

## Bedrock retrieval tags

```yaml
retrieval_tags:
  source_id: phishtank_url_clearinghouse
  source_kind: threat_intel_service
  risk_domains: ['url_reputation', 'phishing_urls']
  channels: ['web', 'email', 'sms']
  safe_use: defensive_only
```

## Suggested structured extraction

```yaml
source_signal:
  source_id: phishtank_url_clearinghouse
  observed_indicator: ""
  requested_action: ""
  sensitive_asset: ""
  risk_effect: raises|lowers|context_only
  explanation: ""
```
