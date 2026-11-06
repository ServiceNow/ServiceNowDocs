---
title: \(Legacy\) NLU Topic Languages tab
description: Use the Languages tab to view the topic's translation status for languages that have been activated in Virtual Agent. If NLU is enabled on your instance, you can also view model mappings for each language.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/vad-topic-languages-tab.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Virtual Agent Designer interface reference, NLU reference, \(Legacy\) Virtual Agent for NLU, Conversational Interfaces]
---

# \(Legacy\) NLU Topic Languages tab

Use the **Languages** tab to view the topic's translation status for languages that have been activated in Virtual Agent. If NLU is enabled on your instance, you can also view model mappings for each language.

Some features on the Languages tab require the appropriate localization roles. For more information, see [\(Legacy\) Localization roles for Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/localization-roles-va.md).

## Translations tab

\[Omitted image "vad-languages-translations-tab.png"\] Alt text: View the status and request translations. Some features vary with the localization role.

<table id="table_p3m_3vw_wqb"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Language

</td><td>

List of available languages in Virtual Agent.

 Only installed languages are displayed \(the language plugins are activated\). If a language appears as unavailable, it means the language plugin is installed, but it has not been activated in Virtual Agent settings or in the Localization Framework. For more information, see [\(Legacy\) Configure Natural Language Understanding in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-nlu-settings.md) and [Languages table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/r_LanguagesTable.md).

</td></tr><tr><td>

Topic translation status

</td><td>

Indicates translation status:-   **Complete**: Topic is completely translated
-   **Partial**: Topic is partially translated
-   **In progress**: Translation is in progress
-   **Not started**: Translation has not begun
-   **Needs publishing**: Topic is unpublished or in Draft state

 The ServiceNow platform provides translations for interface features and prebuilt topics, so languages may display as partially translated.

</td></tr><tr><td>

Topic translations

</td><td>

Depending on the state of the localization process and your role, you can either view the current content for the language, or you can edit the language content.Only users with the [Localization editor \[localization\_editor\] role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/localization-roles-va.md) can edit translated content.

</td></tr><tr><td>

Localization request

</td><td>

Click **Request translation** to create a Localization Framework task. Translation will begin depending on how the flow was set up in the Localization Framework.

 If translation has already begun and you have the [Localization fulfiller \[localization\_fulfiller\] role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/localization-roles-va.md), click **View requested item** to view the task.

</td></tr><tr><td>

Test

</td><td>

Click the link to test the topic in a particular language.

</td></tr></tbody>
</table>## NLU language mapping tab

If you've enabled NLU on your instance, you can view or modify the topic mappings on this tab. You can also map your entities and test the translated topic here.

**Note:** Unless you're using legacy, single-language models, all secondary languages in a topic must be mapped to the same model group. In most cases, changing the mapping for one secondary language will change the mappings for all secondary languages in the topic. For more information, see [\(Legacy\) NLU model mapping in Virtual Agent Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/nlu-model-binding-vad.md).

\[Omitted image "vad-languages-nlu-mapping-tab.png"\] Alt text: View NLU bindings and entity mapping.

**Parent Topic:**[\(Legacy\) Virtual Agent Designer interface reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/vad-reference-nlu.md)

