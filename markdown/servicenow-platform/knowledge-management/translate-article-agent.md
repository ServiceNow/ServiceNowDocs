---
title: Translate a knowledge article from a translation task in Agent Workspace
description: Translate a published knowledge article for which you have been assigned a translation task.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Authoring a knowledge article in Agent Workspace, Creating and maintaining articles, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Translate a knowledge article from a translation task in Agent Workspace

Translate a published knowledge article for which you have been assigned a translation task.

## Before you begin

You must have contribute access to the knowledge base that stores the knowledge article.

Ensure that the system administrator verifies the following settings:

-   Knowledge Management Advanced plugin \(com.snc.knowledge\_advanced\) is activated.
-   I18N: Knowledge Management Internationalization Plugin v2 plugin \(com.glideapp.knowledge.i18n2\) is activated.

    **Note:** The 18N: Internationalization plugin \(com.glide.i18n\) activates the I18N: Knowledge Management Internationalization Plugin v2 plugin.

-   The **glide.knowman.translation.enable\_translation\_task** property is set to `true` in the ServiceNow AI Platform interface. For more information, see [Knowledge Management properties](../reference/r_KnowledgeProperties.md#).

Role required: agent\_workspace\_user

## About this task

A translation task is created for a knowledge article when a request for translation is submitted or its knowledge base is configured to automatically create translation tasks. For more information, see [Request translations for missing languages in Agent Workspace](request-translations-agent.md) and [Create a knowledge base](create-a-knowledgebase.md).

**Note:** The translation management feature isn't available for knowledge blocks in Agent Workspace.

## Procedure

1.  Navigate to **All** &gt; **Agent Workspace** &gt; **Agent Workspace Home**.

2.  Click **Lists** &gt; **Knowledge** &gt; **My Tasks - Translation**.

3.  In the **Number** column, click the link to a translation task.

4.  Click **Translate**.

    **Note:** The **Translate** button is not available if the **glide.knowman.translation.enable\_translation\_task** property is disabled, translations of the knowledge article are available in all available languages, or a translation task has already been created for all the available languages.

    The Original language and Translated language sections appear side by side for easy viewing, as shown in the following figure. By default, the Translated language section includes the original language content.

    ![Translate knowledge article](../image/translate-to-from-agent.png)

5.  Provide the translation in the Translated language section.

    -   If dynamic translation is enabled, click **Machine translate** to automatically replace the draft content in the Translated language section with machine-translated content in the targeted language.

        **Note:** A default translator configuration should be available. For configuring the translation API, see [Dynamic translation](https://www.servicenow.com/docs/access?context=dynamic-translation&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

        When you click **Machine translate**, any draft content in the Translated language section is automatically replaced with the machine-translated content.

    -   If dynamic translation is not available, replace the draft content in the Translated language section with your translated text.
6.  Click **Create draft article** to create a draft version of the translated article.

7.  Click **Publish**.


## Result

When the translated version of the knowledge article is published, a new knowledge number is assigned to the translated version. The translated version is available in the All Articles list in Agent Workspace. Also, the Translated Versions related list on the Knowledge form of the original and translated knowledge article is updated with all the translated versions.

**Related topics**  


[Request translations for missing languages in Agent Workspace](request-translations-agent.md)

[Translation management](../concept/translation-management.md)

