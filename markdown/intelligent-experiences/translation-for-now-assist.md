---
title: Translation for Now Assist
description: There are two translation services available for user-generated content that you can use to speak to users in their preferred language in Now Assist applications.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-01-13"
reading_time_minutes: 2
keywords: [Translation, Now Assist, Generative AI, GenAI, Dynamic translation, Native translation]
breadcrumb: [Exploring Now Assist, Now Assist, Enable AI experiences]
---

# Translation for Now Assist

There are two translation services available for user-generated content that you can use to speak to users in their preferred language in Now Assist applications.

## Translation overview

You can configure two different translation services for Now Assist applications to communicate with your users in their preferred languages. Both translation services detect the language used based on the user's language choice in their Language &amp; Region preferences or the contents of the text, such as a conversation message.

For Dynamic Translation, once non-English content is detected, the translation service translates the content to English before sending the request to the large language model \(LLM\). After the LLM returns a response, the response is translated back into the user's preferred language for them to see. For example, with Dynamic Translation, a user enters a message in Spanish. Dynamic Translation translates the Spanish to English before giving the message to the LLM. The LLM generates a response in English, and then Dynamic Translation translates that response to Spanish to show to the user.

For native translation, text is sent as-is to the model and the model responds in the user's language. For example, if a user sends a message in Spanish, the multi-lingual LLM supports Spanish, so it receives the Spanish input directly from the user. It then generates a response in Spanish, regardless of the language used in the source material it uses to create that response.

If you have native translation enabled, then LLM requests that return outputs in the fallback language aren't translated by Dynamic Translation. They’re returned as-is to the user. This process helps increase skill performance and decrease latency.

## Dynamic Translation

Dynamic Translation for Now Assist uses the Microsoft Azure OEM translation service through ServiceNow. Every language available as a language pack on the ServiceNow platform is supported by the Microsoft Azure OEM. For more information, see [Microsoft Azure OEM for Dynamic Translation in Now Assist](../../now-assist-admin/concept/dynamic-translation-na-ms-azure-oem.md).

## Native Translation

Native translation uses the translation capabilities of the LLMs provided by Now LLM Service. Code generation, flow recommendation, flow generation, and skills that use Azure OpenAI aren’t supported.

The following languages are supported:

-   English
-   Spanish
-   Japanese
-   French
-   German
-   Italian
-   Brazilian Portuguese
-   Dutch
-   Canadian French

## Choosing a translation service

There are different factors that can go into your decision to use one translation service over the other, such as latency and quality of translation. Your entitlements determine what is available to you, and there are different costs associated with translation. For more information on tracking Now Assist usage, see [Monitoring Now Assist usage](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Enabling translation for Now Assist

For more information on turning on translation for Now Assist applications, see [Enable translation for Now Assist applications](../../now-assist-admin/task/enable-dynamic-translation-for-now-assist-applications.md).

If you enable both Dynamic Translation and native translation, native translation has preference and is used first.

