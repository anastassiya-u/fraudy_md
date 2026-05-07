---
title: Source map for fraud-detection RAG knowledge base
doc_type: source_map
language: ru
audience: rag_ingestion
last_reviewed: 2026-05-07
safe_use: defensive_only
---

# Source map

Этот документ нормализует исходный список ресурсов в набор тем и RAG-файлов.

## Source-to-topic mapping

| Topic | Source URL | Recommended markdown file |
| --- | --- | --- |
| Fraud typologies | https://assets.publishing.service.gov.uk/media/5a7ad8c2ed915d670dd7efad/fraud-typologies.pdf | `01_typologies/fraud_typologies.md` |
| Phishing classification techniques | https://www.researchgate.net/publication/359884880_Phishing_Classification_Techniques_A_Systematic_Literature_Review | `01_typologies/phishing_classification_techniques.md` |
| Classic/modern/cutting-edge phishing | https://www.mdpi.com/1999-5903/12/10/168 | `01_typologies/phishing_attack_techniques.md` |
| Audio fraud and voice deepfake detection | https://www.nict.go.jp/en/asean_ivo/gden8c00000004el-att/pdnf1l00000004j7.pdf | `02_signals/audio_voice_deepfake_signals.md` |
| Smishing psychology/taxonomy | https://arxiv.org/pdf/2604.11429 | `02_signals/smishing_psychological_patterns.md` |
| E-mail phishing taxonomy phases | https://www.mdpi.com/2076-3417/10/7/2363 | `01_typologies/email_phishing_taxonomy.md` |
| SMS spam collection | https://archive.ics.uci.edu/dataset/228/sms+spam+collection | `03_datasets/message_datasets.md` |
| Smishing/ham dataset | https://data.mendeley.com/datasets/f45bkkt8pr/1 | `03_datasets/message_datasets.md` |
| Phishing validation emails | https://research.utwente.nl/en/datasets/phishing-validation-emails-dataset/ | `03_datasets/email_url_datasets.md` |
| PhishTank URLs | https://phishtank.org | `03_datasets/email_url_datasets.md` |
| Phishing page UX/UI patterns | https://www.researchgate.net/publication/364718137_PhishInPatterns_measuring_elicited_user_interactions_at_scale_on_phishing_websites | `02_signals/phishing_page_patterns.md` |
| Fake marketplace reviews | https://www.kaggle.com/datasets/muqaddasejaz/fake-reviews-dataset | `03_datasets/marketplace_datasets.md` |
| Amazon reviews | https://www.kaggle.com/datasets/PromptCloudHQ/amazon-reviews-unlocked-mobile-phones | `03_datasets/marketplace_datasets.md` |
| Multi-agent scam conversation | https://huggingface.co/datasets/BothBosu/multi-agent-scam-conversation | `03_datasets/conversation_scam_datasets.md` |
| Scammer conversation | https://huggingface.co/datasets/BothBosu/Scammer-Conversation | `03_datasets/conversation_scam_datasets.md` |
| LinkSec phishing templates | https://github.com/LinkSec/phishing-templates | `04_scenarios/bank_delivery_government_templates.md` |
| Fake job postings | https://www.kaggle.com/datasets/shivamb/real-or-fake-fake-jobposting-prediction | `03_datasets/job_scam_datasets.md` |
| Romance/emotion scam study | https://rsisinternational.org/journals/ijriss/uploads/vol9-iss12-pg3719-3732-202601_pdf.pdf | `04_scenarios/romance_investment_job_scenarios.md` |
| Gophish training templates | https://github.com/HailBytes/gophish-training-templates | `04_scenarios/bank_delivery_government_templates.md` |
| Mobile fraud prevention actions | https://ejournal.unsrat.ac.id/v3/index.php/icon-smart/article/view/57220/47177 | `05_actions/safe_user_instructions.md` |
| Fraud metrics taxonomy | https://www.researchgate.net/publication/340625489_Taxonomy_of_Fraud_Detection_Metrics_for_Business_Processes | `06_risk/risk_classification_rules.md` |

## Normalized evidence labels

- `source_summary`: paraphrased notes from the source.
- `fraud_indicator`: signal that raises risk.
- `benign_indicator`: signal that can reduce risk or require more evidence.
- `safe_action`: instruction that protects the user and does not disclose secrets.
- `dataset_note`: training/evaluation data note, not a production rule.
