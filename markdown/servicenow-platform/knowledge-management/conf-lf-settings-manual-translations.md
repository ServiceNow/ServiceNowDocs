---
title: Add a custom Localization Framework setting to enable bulk translations
description: Add a custom Localization Framework setting to translate multiple knowledge articles manually.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure translation management, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Add a custom Localization Framework setting to enable bulk translations

Add a custom Localization Framework setting to translate multiple knowledge articles manually.

## Before you begin

-   [Activate the Knowledge Management Advanced plugin](../task/activate-knowledge-advanced-plugin.md).
-   Activate Localization Framework.
-   Activate a language.
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

6.  Select the **Workflow Preferences** tab.

7.  Select **Translation -&gt; Publish** from the **Workflow** list.

8.  Select the **Project Preferences** tab.

9.  Enable the creation of bulk translation localization projects.

    -   To enable manual creation, select **Enable projects**. For more information, see Create translation projects.
    -   To enable the auto-creation of the localization projects, select **Enable projects** and **Enable auto creation**.

        If auto creation is enabled, selected localization requested items \(LRITMs\) are automatically bundled into a single localization project.

10. Select **Update**.


## What to do next

[Request bulk translations for multiple knowledge articles](bulk-translations-step.md).

**Parent Topic:**[Configure translation management](configure-translation-management.md)

