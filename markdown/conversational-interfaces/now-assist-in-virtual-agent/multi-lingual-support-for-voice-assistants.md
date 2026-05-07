---
title: Multilingual support for voice assistants
description: Voice assistants support multiple languages to enable users to interact in their preferred language. This topic lists the languages available for voice interactions and linguistic capabilities of the voice assistant.
locale: en-US
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: reference
last_updated: "2026-01-11"
reading_time_minutes: 1
breadcrumb: [Now Assist in Virtual Agent reference, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Multilingual support for voice assistants

Voice assistants support multiple languages to enable users to interact in their preferred language. This topic lists the languages available for voice interactions and linguistic capabilities of the voice assistant.

## Supported languages for voice assistants

Voice assistants support the following languages for user interactions:

-   English
-   German
-   Spanish
-   Japanese
-   Korean
-   Dutch
-   Brazilian Portuguese
-   Italian
-   Mandarin Simplified
-   French
-   Canadian French
-   British English
-   Mexican Spanish
-   Thai
-   Hindi

## Japanese language considerations

Japanese language support for voice assistants enables Japanese-speaking users to experience natural, culturally appropriate interactions with AI voice agents.

-   **Key considerations**

    Formality and honorifics: Voice assistants use appropriate levels of formal Japanese speech \(keigo\) correctly and consistently throughout interactions.

    User addressing: Voice agents address users according to Japanese cultural and linguistic norms.

    Natural expressions: Responses sound more natural to native speakers while remaining concise, avoiding overly literal translations.

    Support for Kanji, Kana, and Furigana in transcriptions.

-   **Alphanumeric content processing**

    To ensure accurate pronunciation in Japanese text-to-speech \(TTS\), alphanumeric expressions in tool call results are pre-processed as follows:

    **Alphabet classification**

    Alphabetic characters are classified to determine whether they should be:

    -   Read as a word \(for example, "OK" read as "オーケー"\)
    -   Read letter-by-letter \(for example, "ID" read as "アイディー"\)
    **Number classification**

    Numeric values are classified by type to ensure correct pronunciation:

    -   Dates and times
    -   Durations
    -   Currency amounts
    -   Measurements
    -   Record numbers
    -   Phone numbers
    -   Other numeric values
    **Kana transliteration**

    After classification, all alphanumeric expressions are transliterated into kana \(Japanese phonetic characters\) for accurate TTS pronunciation.


