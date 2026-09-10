---
title: Multilingual support for AI specialists
description: AI specialists can respond to users in multiple languages.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/lang-support-aiw.html
release: zurich
topic_type: concept
last_updated: "2026-09-01"
reading_time_minutes: 1
breadcrumb: [Explore, Autonomous Workforce, AI Agent Studio, Enable AI experiences]
---

# Multilingual support for AI specialists

AI specialists can respond to users in multiple languages.

The AI specialist can communicate with users in several languages, depending on their preference and language availability, using the built-in language capabilities of the large language model \(LLM\). The language that the AI specialist responds with is based on the language used for the majority of the activity and interactions for the record. Language detection is first done with an AI skill, then Dynamic Translation, then, as a fallback, it uses the user's language set in their user preferences.

For example, if a user leaves a comment in Spanish, the underlying LLM supports Spanish, so it reads the Spanish input directly. It then generates a response in Spanish, regardless of the language used in the source material it uses to create that response.

You can set the **glide.ais.translate.enable\_global\_language\_fallback** property to `true` to check for languages outside of the user's locale when no immediate language match is found.

Some content in response templates may not be translated.

Supported languages are categorized into three groups of fluency.

P1 languages have the strongest support, meaning generally high-quality translation and generative capabilities. Nuance, idioms, and context are usually handled well because these languages are deeply integrated into the models.

P2 languages are supported, and accuracy is good, but there may be occasional gaps in nuance compared to P1 languages.

P3 languages include a broader set of languages. While coverage can be comprehensive, these languages generally have less training depth, so subtle tone or idiomatic expressions may be harder to capture perfectly.

-   P1
    -   English
    -   French
    -   German
    -   Italian
    -   Spanish
    -   Brazilian Portuguese
-   P2
    -   Canadian French
    -   Japanese
    -   Dutch
-   P3
    -   Swedish
    -   Finnish
    -   Czech
    -   Hebrew
    -   Hungarian
    -   Korean
    -   Norwegian
    -   Polish
    -   Portuguese
    -   Russian
    -   Simplified Chinese
    -   Traditional Chinese
    -   Thai
    -   Turkish
    -   Arabic
    -   Danish

