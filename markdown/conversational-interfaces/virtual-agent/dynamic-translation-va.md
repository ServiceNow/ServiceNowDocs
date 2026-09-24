---
title: Dynamic Translation in Virtual Agent
description: If your chat audience is diverse, you want to support them in their own language whenever possible. Use language detection combined with dynamic machine translation to meet that need.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/dynamic-translation-va.html
release: brazil
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Virtual Agent, Conversational Interfaces]
---

# Dynamic Translation in Virtual Agent

If your chat audience is diverse, you want to support them in their own language whenever possible. Use language detection combined with dynamic machine translation to meet that need.

## Dynamic language support

The Dynamic Translation application connects to a third-party machine translator. During the conversation, user inputs and responses are translated into the primary language on the instance, and all results are translated back into the user's language for the session. There are benefits and drawbacks for all options, as described in the following list. Before activating machine translations, you should carefully weigh the costs and benefits and set proper expectations for your deployment objectives.

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

</td></tr></tbody>
</table>## Dynamic language detection and machine translation

Dynamic machine translation for languages that are not supported on the ServiceNow platform provides coverage, but the quality of the user experience may be lower.

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
</table>## Multi-language deployment strategies

Depending on the needs of your user base, you may want a mix of solutions to maximize both user experience and access. You can enable locale support by [designating translated languages as fallback languages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/specify-fallback-language-nlu-prediction.md). For example, you can support Mexican Spanish users by designating Spanish as the fallback language for that locale.

In the following example, French, Spanish, and Polish are dynamically translated and supported as a language on the ServiceNow platform. When the language plugins are installed and activated, it includes some translated content. Since Czech is currently not a supported language on the ServiceNow platform, admins can add Czech as a language and enable Dynamic Translation for the language in Virtual Agent.

\[Omitted image "multi-lang-va-environment.png"\] Alt text: A language support strategy in which French, Spanish, and Polish are dynamically translated, and Czech was manually enabled for Dynamic Translation. French and Spanish are fallback languages for regional dialects.

## Localization insights

You can view dynamic translation and localization insights from the Assistant Designer page. Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer**, and select **Localization Insights**from the list of links in the side panel.

For more information, see [Localization Insights dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/localization-insights-dashboard.md).

