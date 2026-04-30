---
title: Topic Languages tab
description: Use the Languages tab to view the topic's translation status for languages that have been activated in Virtual Agent. If NLU is enabled on your instance, you can also view model mappings for each language.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Virtual Agent Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Topic Languages tab

Use the **Languages** tab to view the topic's translation status for languages that have been activated in Virtual Agent. If NLU is enabled on your instance, you can also view model mappings for each language.

Some features on the Languages tab require the appropriate localization roles. For more information, see [Localization roles for Virtual Agent](localization-roles-va.md#).

## Translations tab

![View the status and request translations. Some features vary with the localization role.](../images/vad-languages-translations-tab.png "Example Translations tab")

<table id="table_p3m_3vw_wqb"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Language

</td><td>

List of available languages in Virtual Agent.

 Only installed languages are displayed \(the language plugins are activated\). If a language appears as unavailable, it means the language plugin is installed, but it has not been activated in Virtual Agent settings or in the Localization Framework. For more information, see [Configure Natural Language Understanding in Virtual Agent](../task/configure-nlu-settings.md) and [Languages table](https://www.servicenow.com/docs/access?context=r_LanguagesTable&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Topic translation status

</td><td>

Indicates translation status:-   **Complete**: Topic is completely translated
-   **Partial**: Topic is partially translated
-   **In progress**: Translation is in progress
-   **Not started**: Translation has not begun
-   **Needs publishing**: Topic is unpublished or in Draft state

 The ServiceNow platform provides translations for interface features and pre-built topics, so languages may display as partially translated.

</td></tr><tr><td>

Topic translations

</td><td>

Depending on the state of the localization process and your role, you can either view the current content for the language, or you can edit the language content.Only users with the [Localization editor \[localization\_editor\] role](localization-roles-va.md#) can edit translated content.

</td></tr><tr><td>

Localization request

</td><td>

Click **Request translation** to create a Localization Framework task. Translation will begin depending on how the flow was set up in the Localization Framework.

 If translation has already begun and you have the [Localization fulfiller \[localization\_fulfiller\] role](localization-roles-va.md#), click **View requested item** to view the task.

</td></tr><tr><td>

Test

</td><td>

Click the link to test the topic in a particular language.

</td></tr></tbody>
</table>## NLU language mapping tab

If you've enabled NLU on your instance, you can view or modify the topic mappings on this tab. You can also map your entities and test the translated topic here.

**Note:** Unless you're using legacy, single-language models, all secondary languages in a topic must be mapped to the same model group. In most cases, changing the mapping for one secondary language will change the mappings for all secondary languages in the topic. For more information, see [NLU model mapping in Virtual Agent Designer](../concept/nlu-model-binding-vad.md).

![View NLU bindings and entity mapping.](../images/vad-languages-nlu-mapping-tab.png "Example NLU language mapping tab")

**Parent Topic:**[Virtual Agent Designer interface reference](../concept/vad-reference.md)

