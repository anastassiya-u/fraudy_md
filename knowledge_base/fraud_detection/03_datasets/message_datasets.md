---
title: SMS, smishing, spam, and ham message datasets
source_urls:
  - https://archive.ics.uci.edu/dataset/228/sms+spam+collection
  - https://data.mendeley.com/datasets/f45bkkt8pr/1
doc_type: dataset_notes
risk_domain: sms_smishing
language: ru
safe_use: defensive_only
last_reviewed: 2026-05-07
---

# SMS and smishing datasets

## Use cases

- Train or evaluate text classifiers for spam/scam/ham separation.
- Build examples of risky vs normal short messages.
- Test false-positive controls for normal notifications and marketing messages.

## Dataset notes

| Dataset | Useful labels | Best use | Cautions |
| --- | --- | --- | --- |
| UCI SMS Spam Collection | ham/spam | baseline SMS spam classification | Older English dataset; spam is not always fraud; not Kazakhstan/CIS-localized |
| Mendeley smishing/spam/ham dataset | smishing/spam/ham | distinguish scam-intent SMS from generic spam and normal messages | Check license, collection period, duplicates, language distribution |

## RAG fields to extract

```yaml
dataset_record:
  message_text: "..."
  label: ham|spam|smishing|unknown
  channel: sms
  language: en|ru|kk|other
  contains_url: true|false
  requested_action: none|click|login|pay|install|reply|call
  sensitive_asset: none|credentials|otp|card|money|device_access
```
