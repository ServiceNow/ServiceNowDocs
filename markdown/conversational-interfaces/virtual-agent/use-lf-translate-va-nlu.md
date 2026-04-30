---
title: Localize Virtual Agent topics that use NLU topic discovery
description: Use the ServiceNow Localization Framework to manage the process of localizing Virtual Agent conversations that use Natural Language Understanding \(NLU\).
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Localizing Virtual Agent conversations, Localization options for Virtual Agent, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Localize Virtual Agent topics that use NLU topic discovery

Use the ServiceNow Localization Framework to manage the process of localizing Virtual Agent conversations that use Natural Language Understanding \(NLU\).

## Before you begin

Check the prerequisites for translating Virtual Agent components. For more information, see [Localizing Virtual Agent conversations](../concept/localize-va-topic.md).

Make sure that your Virtual Agent topics are published and performing the way you want them to. Make any adjustments before you send them to localization.

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  Slide the disovery type toggle switch to **NLU/Keyword**, then select **Manage Languages**

3.  In the **Select NLU Model** list, select the model group you want to manage.

    Intents that are mapped to a topic display on the page.

4.  In the **View language** list, select a language.

    The translation status of each topic in the chosen language displays on the page. Select a topic name to open the topic in Virtual Agent Designer, view or edit translations, or test translated content. The **Topic translation status** column shows the current status of the topic in the localization process.

    ![The Manage languages page displaying the topic and their associated NLU models with topic translation status, translations, test, and NLU intent.](../images/va-loc-manage-languages-page.png "Manage languages page")

    If the **Topic translation status** column shows **Needs publishing**, you must publish the topic before you can submit it for translation.

    **Note:** The ServiceNow AI Platform provides translations for interface features and pre-built topics. So in some topics, languages may display as partially translated.

5.  Do one of the following:

    -   Select the check boxes for the topics you want to translate, and then click **Request topic translations**. When prompted, confirm your choice.

        A translation record is created, and the translation status changes to **In progress**. The translation task is assigned to a user with the localization fulfiller role. For information about the fulfillment process in the Localization Framework, see [Fulfill a localization task](https://www.servicenow.com/docs/access?context=fulfill-localization-task&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

        **Note:** If a topic is already in localization, the corresponding check box is not available.

    -   [Edit translations directly.](edit-translations-va-topics.md)
6.  Click **Manage NLU translations**.

    The model opens in NLU Workbench. Request translations for your model group. For more information, see [Translate a multilingual model](https://www.servicenow.com/docs/access?context=translate-multilingual-model&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).


## Result

When translations are complete, Virtual Agent admins can view, unlock, or edit them from the topic Languages tab or the Manage languages page.

Once translations are published, they are made available to Virtual Agent topics that use keywords dynamically. However, language-specific intent matching is not available until model groups are also translated and published.

## What to do next

You may need to [map a topic to secondary models or a language-specific model](map-nlu-language-model.md).

When translations are done, you can [test localized NLU models](test-nlu-language-model.md).

-   **[Map a topic to a secondary NLU model](map-nlu-language-model.md)**  
Map a Virtual Agent topic to a secondary model in the model group or to a standalone, single-language NLU model for each supported language.
-   **[Test topic and NLU model translations](test-nlu-language-model.md)**  
Test a translated Virtual Agent topic and the localized NLU model to ensure that it works as expected in a conversation.

**Parent Topic:**[Localizing Virtual Agent conversations](../concept/localize-va-topic.md)

