---
title: Localize Virtual Agent topics that use keyword topic discovery
description: Use the ServiceNow Localization Framework to manage the process of localizing Virtual Agent conversations and keywords.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Localizing Virtual Agent conversations, Localization options for Virtual Agent, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Localize Virtual Agent topics that use keyword topic discovery

Use the ServiceNow Localization Framework to manage the process of localizing Virtual Agent conversations and keywords.

## Before you begin

Check the prerequisites for translating Virtual Agent components. For more information, see [Localizing Virtual Agent conversations](../concept/localize-va-topic.md).

Make sure that your Virtual Agent topics are published and performing the way you want them to. Make any adjustments before you send them to localization.

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  Select the **NLU** toggle, and open the topic that you want to translate.

3.  Select the **Languages** tab.

    Only languages that are installed and activated are displayed. To learn how to activate localization plugins, see [Activate a language](https://www.servicenow.com/docs/access?context=t_ActivateALanguage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

    **Note:** The ServiceNow AI Platform provides translations for interface features and pre-built topics. So in some topics, languages may display as partially translated.

    ![The Languages tab displays English as the primary language, with Brazilian Portuguese and Simplified Chinese languages available for translation.](../images/va-languages-tab-no-nlu.png)

4.  Do one of the following:

    -   Request translation:
        1.  Select the applicable check boxes, and then click **Request translations**.
        2.  When prompted, confirm your choice.

            A translation record is created, and the translation status changes to **In progress**. The translation task is assigned to a user with the localization fulfiller role. For information about the fulfillment process in the Localization Framework, see [Fulfill a localization task](https://www.servicenow.com/docs/access?context=fulfill-localization-task&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

    -   [Edit translations directly in Virtual Agent Designer](edit-translations-va-topics.md).

## Result

When translations are complete, Virtual Agent admins can view, unlock, or edit them from the topic Languages tab or the Manage languages page.

Once translations are published, they are made available to Virtual Agent topics that use keywords dynamically.

**Parent Topic:**[Localizing Virtual Agent conversations](../concept/localize-va-topic.md)

