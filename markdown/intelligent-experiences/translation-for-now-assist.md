---
title: Multilingual service for Now Assist
description: Now Assist applications use the multilingual capabilities of large language models \(LLMs\) to translate user-generated content.
locale: en-US
release: australia
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
keywords: [Translation, Now Assist, Generative AI, GenAI, Native translation]
breadcrumb: [Configure multilingual service for Now Assist applications, Now Assist Admin Settings, Exploring Now Assist Admin, Now Assist, Enable AI experiences]
---

# Multilingual service for Now Assist

Now Assist applications use the multilingual capabilities of large language models \(LLMs\) to translate user-generated content.

## Multilingual service overview

You can configure the multilingual services for Now Assist applications to communicate with your users in their preferred languages. The LLM detects the language used based on the user's language choice in their Language &amp; Region preferences or the contents of the text, such as a conversation message.

Multilingual support is enabled for multiple LLM providers, such as Now LLM Service, Microsoft Azure OpenAI, Anthropic Claude on AWS, and Google Gemini. Azure OpenAI offers the most language support on the ServiceNow AI Platform.

## How the different multilingual services work

The inherent multi-language capabilities of the LLM is called native translation. In native translation, text is sent as-is to the model and the model responds in the user's language. For example, if a user sends a message in Spanish, the multilingual LLM supports Spanish, so it receives the Spanish input directly from the user. It then generates a response in Spanish, regardless of the language used in the source material it uses to create that response.

For Dynamic Translation, once non-English content is detected, the translation service translates the content to English before sending the request to the large language model \(LLM\). After the LLM returns a response, the response is translated back into the user's preferred language for them to see. For example, a user enters a message in Slovenian. Dynamic Translation translates the Slovenian to English before giving the message to the LLM. The LLM generates a response in English, and then Dynamic Translation translates that response to Slovenian to show to the user.

If you enable both native translation and Dynamic Translation, native translation has preference and is used first.

If you have native translation enabled, the LLM checks the user's language to see if it is supported. If the language is supported, only native translation is used and no Dynamic Translation occurs. A small number of languages are not yet natively supported by all models. Now Assist Dynamic Translation is automatically applied to address this for unsupported languages. Additionally, if you have native translation enabled, then LLM requests that return outputs in the fallback language will not be translated by Dynamic Translation. Otherwise, they’ll be returned as-is to the user. This process helps increase skill performance and decrease latency.

**Note:** If you want to add a language that is not part of the regularly configured languages, you can do so. See the section below, Adding languages beyond the P1, P2, and P3 language groups.

## Native translation

Supported languages are categorized into three basic groups.

P1 languages have the strongest native support across most model providers, meaning high-quality translation and generative capabilities with fewer errors. Nuance, idioms, and context are usually handled well because these languages are deeply integrated into the models.

P2 languages are supported natively by smaller ServiceNow models and most external providers, but not always by every model \(e.g., some exceptions for Canadian French and Dutch\). Accuracy is good, but there may be occasional gaps in nuanced understanding compared to P1 languages.

P3 languages include a broader set of languages supported by major providers like Microsoft Azure OpenAI, Google Gemini, and Anthropic Claude on AWS, but not natively by ServiceNow’s own large models. While coverage is comprehensive, these languages generally have less training depth, so subtle tone or idiomatic expressions may be harder to capture perfectly.

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

Specific models vary in their support.

-   ServiceNow Large Language Model v1 \(Llama 3.3 70B\) only supports English natively.
-   ServiceNow Large Language Model v2 \(GPT-OSS\) supports English, French, German, Spanish, and Italian natively.
-   ServiceNow Small Language Model v1 \(Mistral Nemo 12B\) and v2 \(Apriel\) supports all P1 and P2 languages.
-   Microsoft Azure OpenAI GPT-4.1 and GPT-4.1-mini support more than 80 languages, including P1, P2, and P3.
-   Google Gemini 2.5 Flash/2.5 Pro currently does not support French Canadian natively.
-   Anthropic Claude 4.0 Sonnet currently does not support French Canadian or Dutch natively.

## Adding languages beyond the P1, P2, or P3 language groups

Some providers, such as Azure OpenAI, offer additional language support beyond the P1, P2, and P3 language groups previously described. You can configure your instance to include additional languages.

**Note:** Before adding a language that is not in the P1, P2, or P3 groups, you should confirm whether the language is supported by the provider. If you add a language that isn't supported, you may get unexpected results. The LLM could fail to detect the language, and/or it could not be able to translate effectively.

-   **Ensure the language is on the sys\_language table.**

    Create a record for the language if necessary. The record should include the language name and code. The **Active** field should be set to true.

-   **Enable the language for the Now Assist model.**
    -   Go to the sys\_generative\_ai\_model\_config table and open the record for the model you want to add the language to, such as gpt\_small by Azure OpenAI.

        **Note:** The model for AI Search is named E5FT. If you want to make changes to the language support for AI Search, you can configure that record. After, you need to reindex all sources in the new language.

    -   In the **Supported languages** list, add the language and save the record.
-   **Activate the language for Now Assist applications.**
    -   Go to **All** &gt; **Now Assist Admin** &gt; **Settings** and open the **Multilingual service** tab.
    -   Scroll to the provider you edited, then select the edit button.
    -   Select the language you added and save.

        **Note:** If you don't see your language as an option, ensure that the language is on the sys\_language table and **Active** is set to true.


**Note:** If semantic search is not working even after installing a language and enabling it for AI Search, you may need to clear the embedding model cache. To do so, run the following: `GlideCacheManager.flush("ais_semantic_embedding_model_cache");`.

## Dynamic Translation

Dynamic Translation for Now Assist uses the Microsoft Azure OEM translation service through ServiceNow. Every language available as a language pack on the ServiceNow platform is supported by Microsoft Azure OEM. These languages are:

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

For more information, see [Microsoft Azure OEM for Dynamic Translation in Now Assist](../../now-assist-admin/concept/dynamic-translation-na-ms-azure-oem.md).

## Choosing a translation service

There are different factors that can go into your decision to use one translation service over the other, such as latency and quality of translation. Your entitlements determine what is available to you, but there are no additional costs associated with native translation service.

**Note:** The native translation service is included in Pro Plus and Enterprise licenses, by default.

For more information on tracking Now Assist usage, see Monitoring Now Assist usage.

## Enabling translation for Now Assist

For more information on turning on multilingual services for Now Assist applications, see [Enable translation for Now Assist applications](../../now-assist-admin/task/enable-dynamic-translation-for-now-assist-applications.md).

**Parent Topic:**[Configure multilingual service for Now Assist applications](../../now-assist-admin/task/enable-dynamic-translation-for-now-assist-applications.md)

