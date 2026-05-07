---
title: Scam conversation datasets
source_urls:
  - https://huggingface.co/datasets/BothBosu/multi-agent-scam-conversation
  - https://huggingface.co/datasets/BothBosu/Scammer-Conversation
doc_type: dataset_notes
risk_domain: conversational_scams
language: ru
safe_use: defensive_only
last_reviewed: 2026-05-07
---

# Scam conversation datasets

## Use cases

- Train conversation-level classifiers that detect scam progression across multiple turns.
- Extract stage patterns: setup, trust building, pressure, exploit request, persistence.
- Evaluate whether the model catches fraud before the final money/credential request.

## Conversation-stage schema

```yaml
conversation_stage:
  stage: introduction|trust_building|problem_or_opportunity|pressure|exploit_request|post_loss_recovery
  scammer_role: bank|support|romantic_partner|employer|investor|buyer|seller|government|unknown
  requested_action: none|click|share_code|install_app|transfer_money|pay_fee|deposit|remote_access
  risk: low|medium|high|critical
```

## Safety note

Do not use scam conversations to generate persuasive scam scripts. Use them to identify defensive indicators and safe interventions.
