---
title: Source inventory for Bedrock fraud detection knowledge base
doc_type: source_inventory
language: en
safe_use: defensive_only
bedrock_ready: true
last_reviewed: 2026-05-07
---

# Source inventory

| Source id | Kind | Domains | Channels | Extraction file |
| --- | --- | --- | --- | --- |
| fraud_typologies_uk_literature_review | research_report | general_fraud, mass_marketing, identity_fraud, small_business_fraud | email, phone, mail, web, in_person | `01_source_extractions/fraud_typologies_uk_literature_review.md` |
| phishing_classification_techniques_slr | systematic_review | phishing_classification, model_evaluation | email, sms, url, web | `01_source_extractions/phishing_classification_techniques_slr.md` |
| phishing_attack_techniques_future_internet | research_article | phishing, attack_techniques | email, sms, voice, web, social_media | `01_source_extractions/phishing_attack_techniques_future_internet.md` |
| email_based_phishing_attack_taxonomy | research_article | email_phishing, taxonomy | email | `01_source_extractions/email_based_phishing_attack_taxonomy.md` |
| audio_deepfake_jitter_shimmer | research_article_pdf | voice_deepfake, vishing | phone, voice_message, audio | `01_source_extractions/audio_deepfake_jitter_shimmer.md` |
| smishing_systematic_review | systematic_review_pdf | smishing, social_engineering | sms, messenger | `01_source_extractions/smishing_systematic_review.md` |
| uci_sms_spam_collection | dataset | sms_dataset, spam_ham | sms | `01_source_extractions/uci_sms_spam_collection.md` |
| mendeley_sms_phishing_dataset | dataset | smishing_dataset | sms | `01_source_extractions/mendeley_sms_phishing_dataset.md` |
| phishing_validation_emails_twente | dataset | email_dataset, phishing_validation | email | `01_source_extractions/phishing_validation_emails_twente.md` |
| phishtank_url_clearinghouse | threat_intel_service | url_reputation, phishing_urls | web, email, sms | `01_source_extractions/phishtank_url_clearinghouse.md` |
| phishinpatterns_web_ux | research_paper | phishing_pages, ux_ui | web | `01_source_extractions/phishinpatterns_web_ux.md` |
| fake_reviews_dataset_kaggle | dataset | marketplace, review_fraud | marketplace, web | `01_source_extractions/fake_reviews_dataset_kaggle.md` |
| amazon_reviews_unlocked_mobile_phones | dataset | marketplace, review_text | marketplace, web | `01_source_extractions/amazon_reviews_unlocked_mobile_phones.md` |
| multi_agent_scam_conversation_hf | dataset | phone_scam, conversation_detection | phone, conversation | `01_source_extractions/multi_agent_scam_conversation_hf.md` |
| scammer_conversation_hf | dataset | conversation_detection | phone, conversation | `01_source_extractions/scammer_conversation_hf.md` |
| linksec_phishing_templates | template_repository | security_awareness, template_indicators | email, web | `01_source_extractions/linksec_phishing_templates.md` |
| fake_job_posting_prediction_kaggle | dataset | employment_scam, job_posting | job_platform, email, messenger | `01_source_extractions/fake_job_posting_prediction_kaggle.md` |
| romance_emotion_scam_study | research_article_pdf | romance_scam, emotion_manipulation | dating_app, social_media, messenger | `01_source_extractions/romance_emotion_scam_study.md` |
| hailbytes_gophish_training_templates | template_repository | security_awareness, template_indicators | email, web | `01_source_extractions/hailbytes_gophish_training_templates.md` |
| mobile_fraud_prevention_actions | prevention_article | safe_actions, mobile_security | mobile, sms, app | `01_source_extractions/mobile_fraud_prevention_actions.md` |
| fraud_detection_metrics_taxonomy | research_article | risk_metrics, evaluation | all | `01_source_extractions/fraud_detection_metrics_taxonomy.md` |

## Normalized metadata fields

- `source_id`: stable slug for joins and citations.
- `source_kind`: research report, research article, dataset, threat-intelligence service, or template repository.
- `risk_domains`: fraud domains supported by the source.
- `channels`: communication channels covered by the source.
- `safe_use`: always `defensive_only`.
