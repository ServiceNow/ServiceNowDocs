---
title: Multilingual support for AI specialists
description: AI specialists can respond to users in multiple languages.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/lang-support-aiw.html
release: australia
topic_type: concept
last_updated: "2026-10-13"
reading_time_minutes: 1
keywords: [language support ai specialists, multilingual support ai specialists, language support ai workforce, multilingual support ai workforce, language support autonomous workforce, multilingual support autonomous workforce, translation ai specialists, translation ai workforce, translation autonomous workforce]
breadcrumb: [Explore, Autonomous Workforce, AI Agent Studio \(legacy\), AI agents and agentic workflows, Enable AI Experiences]
---

# Multilingual support for AI specialists

AI specialists can respond to users in multiple languages.

The AI specialist can communicate with users in several languages, depending on their preference and language availability, using the built-in language capabilities of the large language model \(LLM\). It responds in the language used for most of the activity and interactions on the record.

To detect that language, the AI specialist checks the following sources in order:

1.  An AI skill that detects the language of the record's activity
2.  Dynamic Translation
3.  The language set in the user's preferences

For example, if a user leaves a comment in Spanish, the underlying LLM supports Spanish, so it reads the Spanish input directly. It then generates a response in Spanish, regardless of the language used in the source material it uses to create that response.

You can set the **glide.ais.translate.enable\_global\_language\_fallback** property to `true` to check for languages outside of the user's locale when no immediate language match is found.

Some content in response templates may not be translated.

Supported languages are categorized into three groups of fluency.

|Tier|Support level|Languages|
|----|-------------|---------|
|P1|Strongest support. Nuance, idioms, and context are usually handled well.|Brazilian Portuguese, English, French, German, Italian, Spanish|
|P2|Good accuracy, with occasional gaps in nuance compared to P1.|Canadian French, Dutch, Japanese|
|P3|Broad coverage with less training depth. Subtle tone and idioms may be harder to capture.|Arabic, Czech, Danish, Finnish, Hebrew, Hungarian, Korean, Norwegian, Polish, Portuguese, Russian, Simplified Chinese, Swedish, Thai, Traditional Chinese, Turkish|

