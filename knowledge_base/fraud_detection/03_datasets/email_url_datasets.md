---
title: Email and URL datasets for phishing validation
source_urls:
  - https://research.utwente.nl/en/datasets/phishing-validation-emails-dataset/
  - https://phishtank.org
doc_type: dataset_notes
risk_domain: email_url_phishing
language: ru
safe_use: defensive_only
last_reviewed: 2026-05-07
---

# Email and URL datasets

## Use cases

- Validate email phishing classifiers on safe and unsafe email examples.
- Build URL reputation and lexical-feature evaluation sets.
- Compare RAG explanations with dataset labels.

## Dataset notes

| Source | Best use | Cautions |
| --- | --- | --- |
| Phishing validation emails dataset | Email body/header examples for validation | Preserve privacy and licensing; avoid exposing real personal data |
| PhishTank | Community-verified phishing URLs | URLs age quickly; do not browse malicious links in production; store indicators safely |

## URL features for classifiers

- Domain mismatch with claimed brand.
- Use of IP address, punycode, excessive subdomains, typosquatting.
- Suspicious path keywords: login, verify, secure, update, payment, delivery, refund.
- Shortener or redirector usage.
- Recently observed phishing report or takedown signal.
