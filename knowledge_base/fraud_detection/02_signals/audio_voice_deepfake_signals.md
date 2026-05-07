---
title: Audio fraud and voice deepfake signals
doc_type: signal_rules
risk_domain: vishing_audio_deepfake
source_urls:
  - https://www.nict.go.jp/en/asean_ivo/gden8c00000004el-att/pdnf1l00000004j7.pdf
language: ru
safe_use: defensive_only
last_reviewed: 2026-05-07
---

# Audio fraud and voice deepfake signals

## Scope

Использовать для vishing, fake bank/security calls, fake family emergency calls и voice deepfake подозрений. Технические аудио-признаки должны дополнять поведенческие признаки, а не заменять их.

## Behavioral call red flags

- Caller claims authority or close relationship but refuses callback via official/known number.
- Caller creates panic and prevents verification.
- Caller requests OTP, transfer, credit application, remote app install, or card details.
- Caller asks to keep the call open while the user acts in banking app.
- Caller gives instructions that contradict official bank/government safety advice.

## Audio-quality indicators to treat as supporting evidence

- Unnatural pauses, timing, or turn-taking.
- Flat prosody, inconsistent emotion, robotic artifacts, or repeated phrases.
- Background noise that does not match caller story.
- Voice identity mismatch noticed by the user.
- Compression/call artifacts alone are weak evidence and should not be decisive.

## Safe response

- Hang up or pause the call.
- Call back using the official bank number, government hotline, or known family contact.
- Never disclose one-time codes or move money during an inbound call.
