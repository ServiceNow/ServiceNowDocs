---
title: Language support for NLU services
description: Entity extraction is supported on ServiceNow NLU models for specific languages only. The remaining languages support intent matching only. If you are using IBM Watson Assistant, supported languages vary.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Localizing Virtual Agent conversations, Localization options for Virtual Agent, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Language support for NLU services

Entity extraction is supported on ServiceNow® NLU models for specific languages only. The remaining languages support intent matching only. If you are using IBM Watson Assistant, supported languages vary.

You can see the list of currently supported languages in the Open NLU Driver Languages \[open\_nlu\_driver\_language\] table.

The VA NLU Languages \[sys\_cs\_nlu\_language\] table lists the languages that are currently enabled in Virtual Agent.

**Note:** If you choose a language that doesn't support full entity extraction, an error message appears.

For unsupported language codes, you can specify a fallback language for NLU prediction. For example, if a user's language detected language is Mexican Spanish \(es-mx\), you can specify Spanish \(es\) as the fallback language, if it is enabled on your instance. For more information, see [Specify a fallback language for locale-specific languages and NLU prediction](../task/specify-fallback-language-nlu-prediction.md). You can also enable Dynamic Translation for Virtual Agent. For details, see [Using language detection and dynamic machine translation in Virtual Agent enhanced chat conversations](../concept/dynamic-lang-detection-translation-enhanced-chat.md).

**Note:** This content focuses specifically on NLU language support. For more information on LLM language support for Now Assist in Virtual Agent, see [Multilingual service for Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/translation-for-now-assist.md).

<table id="table_tkk_ymg_fpb"><thead><tr><th>

Service

</th><th>

Supported languages

</th></tr></thead><tbody><tr><td>

ServiceNow NLU

</td><td>

For intent matching and entity recognition:-   English
-   French
-   German
-   Japanese
-   Spanish

 For intent matching only:

 -   English
-   Chinese \(Simplified\)
-   Danish
-   Dutch
-   Finnish
-   French
-   French \(Canadian\)
-   German
-   Italian
-   Japanese
-   Korean
-   Norwegian
-   Polish
-   Portuguese \(Brazilian\)
-   Spanish
-   Swedish

</td></tr><tr><td>

IBM Watson Assistant

</td><td>

-   English
-   Chinese \(Simplified\)
-   Dutch
-   French
-   German
-   Italian
-   Japanese
-   Korean
-   Portuguese
-   Spanish

</td></tr><tr><td>

Google Dialogflow ES

</td><td>

-   English
-   Chinese \(Simplified\)
-   Chinese \(Traditional\)
-   Dutch
-   Finnish
-   French
-   French \(Canadian\)
-   German
-   Italian
-   Japanese
-   Korean
-   Norwegian
-   Polish
-   Portuguese
-   Portuguese \(Brazilian\)
-   Russian
-   Spanish
-   Swedish
-   Thai
-   Turkish

</td></tr></tbody>
</table>**Parent Topic:**[Localizing Virtual Agent conversations](../concept/localize-va-topic.md)

