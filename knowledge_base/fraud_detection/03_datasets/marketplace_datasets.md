---
title: Marketplace and review datasets
source_urls:
  - https://www.kaggle.com/datasets/muqaddasejaz/fake-reviews-dataset
  - https://www.kaggle.com/datasets/PromptCloudHQ/amazon-reviews-unlocked-mobile-phones
doc_type: dataset_notes
risk_domain: marketplace
language: ru
safe_use: defensive_only
last_reviewed: 2026-05-07
---

# Marketplace and review datasets

## Use cases

- Detect fake reviews, inflated seller trust, and suspicious marketplace profiles.
- Generate benign marketplace text examples to reduce false positives.
- Combine review signals with transaction-flow signals.

## Cautions

Fake review detection is not the same as payment fraud detection. A suspicious review profile should not automatically classify a buyer/seller message as fraud unless transaction red flags are present.

## Useful marketplace fraud indicators

- External payment or delivery link.
- Request for card details to “receive payment”.
- Courier verification flow outside platform.
- Buyer/seller pressure to leave the platform.
- Overpayment/refund request.
- Recently created account with repetitive reviews or unnatural rating distribution.
