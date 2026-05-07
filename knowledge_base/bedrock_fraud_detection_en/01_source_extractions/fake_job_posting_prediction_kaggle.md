---
title: Real / Fake Job Posting Prediction dataset
doc_type: source_extraction
source_kind: dataset
language: en
safe_use: defensive_only
bedrock_ready: true
source_ids:
  - fake_job_posting_prediction_kaggle
source_urls:
  - https://www.kaggle.com/datasets/shivamb/real-or-fake-fake-jobposting-prediction
risk_domains:
  - employment_scam
  - job_posting
channels:
  - job_platform
  - email
  - messenger
last_reviewed: 2026-05-07
---

# Real / Fake Job Posting Prediction dataset

## What this source contributes to Fraudy

Use for employment scam features and class imbalance-aware evaluation. Monitor precision/recall because fake postings are minority class.

## Key extracted facts

- Dataset contains about 18K job descriptions, with about 800 fake postings.
- It includes textual information and meta-information about jobs.
- It can support models that classify fraudulent versus real job descriptions and identify fraudulent traits.
- License is CC0 Public Domain on Kaggle.

## Fraud detection indicators

- High salary with vague requirements.
- Upfront registration, training, equipment, or task deposit fee.
- Vague company profile, non-corporate email domain, or missing company website.
- Request for bank/card data before formal employment.

## False-positive controls

- Real recruiters may ask for documents later in a formal process.
- Remote work, high salary, or messenger contact alone is not enough without payment/data-risk evidence.

## Bedrock retrieval tags

```yaml
retrieval_tags:
  source_id: fake_job_posting_prediction_kaggle
  source_kind: dataset
  risk_domains: ['employment_scam', 'job_posting']
  channels: ['job_platform', 'email', 'messenger']
  safe_use: defensive_only
```

## Suggested structured extraction

```yaml
source_signal:
  source_id: fake_job_posting_prediction_kaggle
  observed_indicator: ""
  requested_action: ""
  sensitive_asset: ""
  risk_effect: raises|lowers|context_only
  explanation: ""
```
