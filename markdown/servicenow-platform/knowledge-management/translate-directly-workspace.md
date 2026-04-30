---
title: Translate a knowledge article in Agent Workspace
description: Translate published knowledge articles to make them available in other languages.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Authoring a knowledge article in Agent Workspace, Creating and maintaining articles, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Translate a knowledge article in Agent Workspace

Translate published knowledge articles to make them available in other languages.

## Before you begin

You must have contribute access to the knowledge base that stores the knowledge article.

Ensure that the system administrator verifies the following settings:

-   Knowledge Management Advanced plugin \(com.snc.knowledge\_advanced\) is activated.
-   I18N: Knowledge Management Internationalization Plugin v2 plugin \(com.glideapp.knowledge.i18n2\) is activated.

    **Note:** The 18N: Internationalization plugin \(com.glide.i18n\) activates the I18N: Knowledge Management Internationalization Plugin v2 plugin.

-   The **glide.knowman.translation.enable\_translation\_task** property is set to `true` in the ServiceNow AI Platform interface. For more information, see [Knowledge Management properties](../reference/r_KnowledgeProperties.md#).

    **Note:** When the **glide.knowman.translation.enable\_translation\_task** property is set to `false`, translate the knowledge article by clicking **New** in the Translated version related list of a Knowledge form. The Knowledge form that is displayed to translate the article is based on the article template of the source knowledge article. You can enter your translation content in the Knowledge form. For more information about the Knowledge form, see [Create a knowledge article in Agent Workspace](create-article-workspace.md).


Role required: agent\_workspace\_user

## About this task

If you have contribute access to a knowledge article, you can translate a knowledge article directly from the knowledge form.

If your system administrator has configured languages for the knowledge base, you can translate into those languages only. For more information, see [Create a knowledge base](create-a-knowledgebase.md).

**Note:** The translation management feature isn't available for knowledge blocks in Agent Workspace.

## Procedure

1.  Navigate to **All** &gt; **Agent Workspace** &gt; **Agent Workspace Home**.

2.  Click **Lists** &gt; **Knowledge** &gt; **All Articles**.

3.  In the **Number** column, click the link to a knowledge article that you want to translate.

4.  Click **Edit**.

5.  Click **Translate**.

    **Note:** The **Translate** button is not available if the **glide.knowman.translation.enable\_translation\_task** property is disabled, translations of the knowledge article are available in all available languages, or a translation task has already been created for all the available languages.

    The Original language and Translated language sections appear side by side for easy viewing, as shown in the following figure. The text in the Translated language section still appears in the original language content.

    ![Translate Article display.](../image/translate-to-from-agent.png)

6.  Provide the translation in the Translated language section.

    -   If dynamic translation is enabled, click **Machine translate** to automatically replace the draft content in the Translated language section with machine-translated content in the targeted language.

        **Note:** A default translator configuration should be available. For configuring the translation API, see [Dynamic translation](https://www.servicenow.com/docs/access?context=dynamic-translation&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

        When you click **Machine translate**, any draft content in the Translated language section is automatically replaced with the machine-translated content.

    -   If dynamic translation is not available, replace the draft content in the Translated language section with your translated text.
7.  Click **Create draft article** to create a draft version of the translated article.

8.  Click **Publish**.


## Result

When the translated version of the knowledge article is published, a new knowledge number is assigned to the translated version. The translated version is available in the All Articles list in Agent Workspace. Also, the Translated Versions related list on the Knowledge form of the original and translated knowledge article is updated with all the translated versions.

**Related topics**  


[Request translations for missing languages in Agent Workspace](request-translations-agent.md)

[Translation management](../concept/translation-management.md)

