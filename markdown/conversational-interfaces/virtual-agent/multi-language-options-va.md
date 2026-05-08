---
title: Localization options for Virtual Agent
description: The ServiceNow platform provides several methods for serving your international Virtual Agent users, regardless of their language and locale. Professionally localize your conversations, use dynamic machine translation, or a combination of the two.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Localization options for Virtual Agent

The ServiceNow platform provides several methods for serving your international Virtual Agent users, regardless of their language and locale. Professionally localize your conversations, use dynamic machine translation, or a combination of the two.

## Direct and dynamic language support

If your chat audience is diverse, you want to support them in their own language whenever possible. One option is to localize everything professionally using linguists who can translate your topics into the desired languages. While this option produces the best user outcomes, it is often the most expensive. Another option available to you is language detection combined with dynamic machine translation. Instead of using translated topics and models, dynamic translation connects to a third-party machine translator. During the conversation, user utterances and responses are translated into the primary language on the instance, and all results are translated back into the user's language for the session. There are benefits and drawbacks for all options, as described in the following list. Before activating machine translations, you should carefully weigh the costs and benefits and set proper expectations for your deployment objectives.

-   **[Direct language support \(professional localization\)](localize-va-topic.md)**

    A direct language strategy employs an expert linguist to configure entities, intents, strings, keywords, and vocabulary, which are then used to match user utterances with configured content. Since an expert provides translations that directly match the conversation's content, the accuracy of the translated content will be high. In addition to the translations themselves, experts can use the NLU vocabulary feature to further define words and phrases that it may encounter from your users. For example, a user may enter an acronym such as `MS`, which you can define as the vocabulary item `Microsoft`.

    Professional translations are implemented directly in Virtual Agent Designer. For details, see [Localizing Virtual Agent conversations](localize-va-topic.md).

<table id="table_a4p_whg_jtb"><thead><tr><th>

Benefits

</th><th>

Constraints

</th></tr></thead><tbody><tr><td>

-   More accurate translations
-   For supported languages, NLU intents and entities are localized


</td><td>

-   Requires more resources to build and maintain
-   Longer completion time
-   Higher implementation costs
-   5 languages have NLU intent and entity support
-   12 languages have NLU intent support only
-   Increased coverage is not typically scalable
-   Not easily extensible
 For more information, see [Language support for NLU services](../reference/language-support-nlu-services.md).

</td></tr></tbody>
</table>-   **[Dynamic language detection and machine translation](multi-language-options-va.md)**

    Dynamic machine translation relies on the translation service to translate all content in real time. The accuracy of the translations is dependent on the translation service. Although translation services typically leverage algorithms to translate words based on the context of the conversation or sentence, there may be times when there is minimal context for the algorithm to leverage. Accuracy may be diminished in this situation. Check with your translation service provider about the ability to exclude words from translation or associate vocabulary with specific synonyms.

<table id="table_bw2_f3g_jtb"><thead><tr><th>

Benefits

</th><th>

Constraints

</th></tr></thead><tbody><tr><td>

-   Lower implementation costs
-   Faster completion time
-   Less human maintenance
-   ServiceNow provides 22 language plugins with basic translations


</td><td>

-   Limited scalability
-   Limited extensibility
-   5 languages have NLU intent and entity support
-   12 languages have NLU intent support only
 For more information, see [Language support for NLU services](../reference/language-support-nlu-services.md).

</td></tr></tbody>
</table>    Dynamic machine translation for languages that are not supported on the ServiceNow platform provides coverage, but the quality of the user experience may be lower.

<table id="table_yjl_3jg_jtb"><thead><tr><th>

Benefits

</th><th>

Constraints

</th></tr></thead><tbody><tr><td>

-   Lower implementation costs
-   Faster completion time
-   Less human maintenance
-   Support for many languages
-   Highly scalable
-   Highly extensible


</td><td>

-   User experience may vary
-   Potential for mistranslation may reduce user outcomes


</td></tr></tbody>
</table>
## Multi-language deployment strategies

Depending on the needs of your user base, you may want a mix of solutions to maximize both user experience and access. For example, you may choose to professionally localize prioritized languages and dynamically translate others. For example, if 95% of your users speak six languages, you may decide to use a linguist to translate your topics into those six. You might then use Dynamic Translation for the remaining five percent.

You can also enable locale support by [designating translated languages as fallback languages](../task/specify-fallback-language-nlu-prediction.md). For example, you can support Mexican Spanish users by designating Spanish as the fallback language for that locale.

In the following example, French, German, and Spanish are professionally localized, including the NLU models, intents, and entities. This localized content provides the best user experience. Polish is supported as a language on the ServiceNow platform, and when the plugin is installed and activated, it includes some translated content. In this imaginary scenario, the business decision was made to dynamically translate Polish content because it accounts for a smaller percentage of users. The quality of this experience may vary since NLU models are not localized. Instead, utterances are dynamically translated to English, and NLU topic discovery is run through the English model. Since Czech is currently not a supported language on the ServiceNow platform, dynamic machine translation is the only option. Admins can add Czech as a language and enable Dynamic Translation for the language in Virtual Agent.

![A language support strategy in which French, German, and Spanish are fully localized with NLU and are designated as fallback languages for regional dialects. Polish and Czech are dynamically translated.](../images/multi-lang-va-environment.png "Example language support strategy")

## Localization insights

You can view dynamic translation and localization insights from the Virtual Agent Designer page. Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**, and select **Localization Insights**from the list of links in the side panel.

For more information, see Localization Insights dashboard.

-   **[Using language detection and dynamic machine translation in Virtual Agent enhanced chat conversations](dynamic-lang-detection-translation-enhanced-chat.md)**  
Enable a combination of language detection and machine translation for Virtual Agent to improve the chat experience for diverse users. You can designate fallback languages for locales or dynamically translate languages that are not professionally localized or are not supported in topic discovery.
-   **[Using language detection and dynamic machine translation in Virtual Agent NLU and LLM standard chat conversations](dynamic-lang-detection-translation-standard-chat-nlu.md)**  
Enable a combination of language detection and machine translation for Virtual Agent to improve the chat experience for diverse users. You can designate fallback languages for locales or dynamically translate languages that are not professionally localized or are not supported in topic discovery.
-   **[Prerequisites for using Dynamic Translation in Virtual Agent](prereq-using-dt-va.md)**  
To enable dynamic machine translation, install ServiceNow® language plugins and Dynamic Translation plugins. Then configure Dynamic Translation for your instance.
-   **[Configure Dynamic Translation service integration credentials](../task/configure-translation-srvc-integration-credentials.md)**  
Configure the credential and connection for your translation service.
-   **[Activate your translation service in Dynamic Translation](../task/activate-dt-translation-service.md)**  
Activate your preferred Dynamic Translation provider and mark it as the default service for both translation and language detection.
-   **[Enable Dynamic Translation for languages in Virtual Agent](../task/enable-dynamic-lang-detection.md)**  
Enable Dynamic Translation for one or more languages in Chat Settings for Virtual Agent.
-   **[Configure multilingual service for Now Assist applications](../../now-assist-admin/task/enable-dynamic-translation-for-now-assist-applications.md)**  
Turn on multilingual service for user-entered text with native translation or Dynamic Translation in Now Assist applications.
-   **[Enable Dynamic Translation for an unsupported language](../task/enable-dt-unsupported-language.md)**  
The ServiceNow® platform supports several languages, but you can enable dynamic machine translation for additional languages in Virtual Agent.
-   **[Specify a fallback language for locale-specific languages and NLU prediction](../task/specify-fallback-language-nlu-prediction.md)**  
Provide language locale support by specifying a fallback language for Virtual Agent to use for topics, keywords, and NLU prediction. For example, the ServiceNow® platform doesn't support Mexican Spanish \(mx-es\), but it does support Spanish \(es\), which you can designate as the fallback language for a better user experience.
-   **[Localizing Virtual Agent conversations](localize-va-topic.md)**  
The ServiceNow platform provides several methods for localizing Virtual Agent conversations, depending on your needs. Use the Localization Framework to manage all aspects of the translation process, whether you are using machine translation, a third-party provider, or both.

**Parent Topic:**[Building and deploying Virtual Agent](using-virtual-agent.md)

