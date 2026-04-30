---
title: Using language detection and dynamic machine translation in Virtual Agent enhanced chat conversations
description: Enable a combination of language detection and machine translation for Virtual Agent to improve the chat experience for diverse users. You can designate fallback languages for locales or dynamically translate languages that are not professionally localized or are not supported in topic discovery.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [Localization options for Virtual Agent, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Using language detection and dynamic machine translation in Virtual Agent enhanced chat conversations

Enable a combination of language detection and machine translation for Virtual Agent to improve the chat experience for diverse users. You can designate fallback languages for locales or dynamically translate languages that are not professionally localized or are not supported in topic discovery.

Chat users are more comfortable having conversations in their preferred language. Their preferred language is set in the user's profile language preference. For example, Virtual Agent greets users in the preferred language specified in their user profile. But if a user responds in another language, Virtual Agent can detect the change. Depending on your user experience, users either receive a prompt regarding whether they'd like to switch the conversational language to the detected language or the conversational language updates automatically to the detected language. After the language is switched to the detected language, that language becomes the conversation's language for the remainder of the conversation. But in many cases users don't have control over their preferred language, particularly if they are guest users.

Guest conversations do not support language detection if resumable guest sessions are not enabled. This is why language detection and dynamic machine translation can improve the chat experience, particularly if you have conversations that have not been localized in some languages. For example, your organization may routinely localize into Spanish and French, but you may also want to support Dutch and Danish. You can enable Dynamic Translation on your ServiceNow® instance for those languages.

You can use language detection to support custom or locale-specific language codes as well. For example, you could designate Spanish \(es\) as the fallback language for Mexican Spanish \(es-mx\) to ensure that those users have a good customer experience.

Virtual Agent conversations can be dynamically translated. Virtual Agent uses platform translations and if no platform translations are found, then Dynamic Translation is used instead. If some conversations have been professionally translated, you should disable dynamic translation for those specific languages. Expert translations may be more accurate and of higher quality than machine translations. Prior to making a dynamic translation call, the Text Translations for Dynamic Translation \[sys\_cs\_dynamic\_translation\_text\] and Message \[sys\_ui\_message\] tables are checked to see if the text has been previously translated or already has a localization record. A dynamic translation call is only made if no translation exists in either table. After a dynamic translation call is made and that text is translated, that translated text is stored in the Text Translations for Dynamic Translation \[sys\_cs\_dynamic\_translation\_text\] table for future use. This table is cleared every 24 hours to ensure that the most up-to-date translations stored in the Message \[sys\_ui\_message\] table are being referenced. Storing previously translated text results in fewer dynamic translation calls to third-party translation services. For more information about localizing Virtual Agent conversations, see [Localizing Virtual Agent conversations](localize-va-topic.md).

You can use Dynamic Translation during the localization process as well. If you are localizing conversations with professional linguists, you can enable Dynamic Translation while some topics and strings remain untranslated. When your deployment in that language is complete, you can disable Dynamic Translation, since professional translations are likely more accurate.

![Video link](../../conversational-interfaces/image/icon-video-link.png) [Virtual Agent Academy: Dynamically translate languages in Virtual Agent](https://www.youtube.com/watch?v=QiwwPii5rq4&list=PLkGSnjw5y2U79gjQuQW-2GBqzEccwFkWH&index=5) Watch this video for a demonstration of using Virtual Agent with Dynamic Translation.

**Note:** You can use language detection independently of Dynamic Translation. Language detection only occurs at the beginning of the conversation, while a Topic Picker is present. It doesn't apply when a user tries to switch the language in the middle of a topic.

## Language detection and Dynamic Translation process in Virtual Agent enhanced chat conversations

When you enable language detection and Dynamic Translation for Virtual Agent for other languages, a variety of diverse users gain access to your Virtual Agent chat environment.

For more information on enabling language detection, see [Enable Dynamic Translation for languages in Virtual Agent](../task/enable-dynamic-lang-detection.md). For more information on enabling dynamic translation, see [Configure multilingual service for Now Assist applications](../../now-assist-admin/task/enable-dynamic-translation-for-now-assist-applications.md).

Language detection is only applicable to the first utterance entered into the conversation. Conversational language switching cannot occur mid-conversation. During LLM enhanced chat conversations, the conversational language automatically switches to the user's detected language. This automatic switch can occur when a user enters an utterance at the start of a new conversation or within the home page’s search field. If the conversational language does not automatically switch to the detected language, the preferred conversational language continues. The following list details the few exceptions in an enhanced chat conversation that would not automatically switch the conversational language:

-   The language plugin for the user's detected language is not installed.
-   The language plugin for the user's detected language was not installed and dynamic translation wasn't turned on.
-   The confidence level of the detected language didn't meet the threshold.

    **Note:** If the conversational language does not automatically switch to the detected language, restart the conversation and try entering a more specific utterance. Entering a more specific utterance may improve the confidence score and lead to an automatic switch to the user’s detected language.


When language detection is turned off, no conversational language switching can occur.

The default system language sets all users’ default session language. That user's default session language is what sets the conversational language. When a user types an utterance that is not recognized as the system language, the results depend upon your configuration for that language.

The following examples show how a conversational language can be impacted depending upon the language detection and dynamic translation settings:

**Note:** If you create exclusion rules for Dynamic Translation, those excluded terms are honored during Dynamic Translation. For more information about the Exclusion Framework, see [Exclusion Framework in Dynamic Translation](https://www.servicenow.com/docs/access?context=dyn-translation-exclusion-framework&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

<table id="table_r24_xr4_ftb"><thead><tr><th>

Language configuration

</th><th>

Results in Virtual Agent LLM enhanced chat conversations

</th></tr></thead><tbody><tr><td>

Language detection is enabled, but not Dynamic Translation

</td><td>

Language responses can show up differently depending on whether localization was done or not for those topics. The conversation language may continue in the detected language based on whether localization records for those topics were previously included. If localization records are not provided, the conversation language would continue in the preferred conversational language.

 If the detected language is a locale or other language code that has been configured with a fallback language, the conversational language would either switch to a previously localized language, or the conversation would continue in the preferred conversational language.

</td></tr><tr><td>

Language detection and Dynamic Translation are enabled

</td><td>

If the detected language is enabled for dynamic translation in Virtual Agent Chat Settings and the confidence level is met, the conversation automatically switches to the detected language.

 For example, the preferred conversational language is in English but the user types an utterance in Spanish. The conversation language automatically switches to Spanish. The user sees the whole conversation in Spanish even though only the Virtual Agent response is dynamically translated and not the user's utterance. When the user starts a new chat, the preferred conversational language resumes. In this example, English would be the conversational language and the user must enter an initial utterance in Spanish to trigger language detection so that they can have another conversation in Spanish.

</td></tr></tbody>
</table>The language detection and dynamic machine translation process operates according to the following principles:

-   Language detection occurs only once per conversation, at the initial utterance.

    If a user tries to change the language in the middle of a conversation, Virtual Agent returns an `I didn't understand` message.

-   When the conversation has closed and restarted, the language used in the next conversation is the preferred conversational language.
-   If a user's detected language is the same as the preferred language, the user does not switch languages.
-   If a user's detected language has no fallback language specified and dynamic translation is not enabled for it, the conversation continues in the preferred language.
-   If a user's detected language is not activated on the instance, the conversation continues in the preferred language. For more information, see [Activate a language](https://www.servicenow.com/docs/access?context=t_ActivateALanguage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

**Note:** AI Search results are not translated.

## Dynamic Translation and Agent Chat

If Dynamic Translation is enabled on Virtual Agent but turned off for Agent Chat, the live agent will see what the user sees. If the user started the conversation in another language and the conversational language switches, then the live agent will see the conversation in the user's detected language. This may cause some confusion for both the agent and the customer. To resolve this issue, consider turning on Dynamic Translation for Agent Chat as well. For details, see [Configuring Dynamic Translation for Agent Chat](../../conversational-interfaces/concept/configure-dtac.md).

## Supported languages

For better results, install the ServiceNow language plugins for each language that uses dynamic translation. For a detailed list of language plugins, see [Activate a language](https://www.servicenow.com/docs/access?context=t_ActivateALanguage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

You can enable dynamic translation for languages that are not currently supported on the ServiceNow platform. For details, see [Enable Dynamic Translation for an unsupported language](../task/enable-dt-unsupported-language.md).

## Supported channels

Dynamic Translation for Virtual Agent is currently supported in the following channels:

-   ServiceNow chat widget
-   Microsoft Teams
-   Slack
-   Workplace from Facebook
-   Facebook Messenger

**Note:** The Virtual Agent topic test window may identify user utterances from Microsoft Teams or other adapters as `sysparm_search_text`. Dynamic Translation will translate this content as well.

The following channels do not support Dynamic Translation for Virtual Agent:

-   ServiceNow mobile client
-   WhatsApp
-   LINE
-   Twilio SMS
-   Alexa
-   Google Assistant
-   Siri

**Parent Topic:**[Localization options for Virtual Agent](multi-language-options-va.md)

