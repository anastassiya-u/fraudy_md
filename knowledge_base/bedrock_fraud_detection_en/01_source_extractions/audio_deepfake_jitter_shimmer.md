---
title: Contributions of jitter and shimmer in voice for fake audio detection
doc_type: source_extraction
source_kind: research_article_pdf
language: en
safe_use: defensive_only
bedrock_ready: true
source_ids:
  - audio_deepfake_jitter_shimmer
source_urls:
  - https://www.nict.go.jp/en/asean_ivo/gden8c00000004el-att/pdnf1l00000004j7.pdf
risk_domains:
  - voice_deepfake
  - vishing
channels:
  - phone
  - voice_message
  - audio
last_reviewed: 2026-05-07
---

# Contributions of jitter and shimmer in voice for fake audio detection

## What this source contributes to Fraudy

Use for vishing and deepfake-call detection. Combine acoustic anomaly evidence with behavioral evidence and always recommend callback through an official channel.

## Key extracted facts

- Jitter captures frequency/period variation between glottal cycles; shimmer captures amplitude variation.
- The paper evaluates combining jitter/shimmer with spectrum-based features for fake audio detection.
- Accurate fundamental-frequency estimation affects the usefulness of jitter and shimmer features.
- Voice deepfake evidence should be treated as technical support evidence, not as the only fraud signal.

## Fraud detection indicators

- Unnatural timing, prosody, pauses, repeated phrases, or voice identity mismatch.
- Audio artifacts combined with social-engineering requests.
- Caller refuses verification through an official or known number.
- Caller asks for OTP, transfer, remote access, or secrecy.

## False-positive controls

- Call compression, background noise, and poor network quality can mimic artifacts.
- A familiar voice is not sufficient proof of safety when money or secrets are requested.

## Bedrock retrieval tags

```yaml
retrieval_tags:
  source_id: audio_deepfake_jitter_shimmer
  source_kind: research_article_pdf
  risk_domains: ['voice_deepfake', 'vishing']
  channels: ['phone', 'voice_message', 'audio']
  safe_use: defensive_only
```

## Suggested structured extraction

```yaml
source_signal:
  source_id: audio_deepfake_jitter_shimmer
  observed_indicator: ""
  requested_action: ""
  sensitive_asset: ""
  risk_effect: raises|lowers|context_only
  explanation: ""
```
