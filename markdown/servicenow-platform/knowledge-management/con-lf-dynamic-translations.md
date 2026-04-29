---
title: Add a custom Localization Framework setting to enable machine translation
description: Add a custom Localization Framework setting to enable machine translation for bulk translations of knowledge articles.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure translation management, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Add a custom Localization Framework setting to enable machine translation

Add a custom Localization Framework setting to enable machine translation for bulk translations of knowledge articles.

## Before you begin

-   [Activate the Knowledge Management Advanced plugin](../task/activate-knowledge-advanced-plugin.md).
-   [Activate Localization Framework](https://www.servicenow.com/docs/access?context=activate-lf-plugin&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   [Activate a language](https://www.servicenow.com/docs/access?context=t_ActivateALanguage&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   Bulk Translation is available with the base Australia release. If you are upgrading from a previous release, you must configure the following settings:
    -   Enable the Localization Framework by setting the **glide.knowman.translation.enable\_lf\_article\_translation** system property to true.
    -   Set the **glide.knowman.translation.enable\_translation\_task** system property to false.
    -   Set the **glide.knowman.translation.enable\_localization\_framework** system property to true.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Localization Framework** &gt; **Settings**.

2.  In the Setting list, select **New**.

3.  Enter a name for the setting.

4.  Select **Knowledge** from the **Artifact** list.

5.  Select the languages into which you want the articles translated.

6.  In the **Translation Preferences** tab, select the **Enable machine translate** check box to enable machine translation for knowledge articles.

7.  Select the desired translator in the **Translator** field.

8.  Select the **Workflow Preferences** tab.

9.  Select **Auto Translation** &gt; **Auto Publish** from the Workflow list.

10. Select the **Project Preferences** tab.

11. Enable the creation of bulk translation localization projects.

    -   To enable manual creation, select **Enable projects**. For more information, see [Create translation projects](https://www.servicenow.com/docs/access?context=projects-localization-framework&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
    -   To enable the auto-creation of the localization projects, select **Enable projects** and **Enable auto creation**.

        If auto creation is enabled, selected localization requested items \(LRITMs\) are automatically bundled into a single localization project.

12. Select the group that includes the localization\_manager role in the **Localization manager group** field.

    The **Localization manager group** field appears only when the **Enable projects** and the **Enable auto creation** options are selected.

13. Select **Update**.


## What to do next

[Translate knowledge articles using Dynamic Translation](dynamic-translation-translate-articles.md)

**Parent Topic:**[Configure translation management](configure-translation-management.md)

