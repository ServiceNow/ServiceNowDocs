---
title: Ensure that translated choices appear for applications added by plugins
description: Ensure that translated choices appear for applications by activating translated choice records after corresponding English choice records have been added by plugins.
locale: en-US
release: australia
product: System Localization
classification: system-localization
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring System Localization, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Ensure that translated choices appear for applications added by plugins

Ensure that translated choices appear for applications by activating translated choice records after corresponding English choice records have been added by plugins.

## Before you begin

You must have activated a language and then activated a plugin that includes the corresponding English choice records. For more information, see [Activate a language](t_ActivateALanguage.md) and [Activate a plugin](../../plugins/task/t_ActivateAPlugin.md).

Role required: admin

## About this task

When you activate plugins after having activated languages, translated choices in lists might not appear for applications or features installed by the plugins. Translated choice records installed by a language plugin that don’t already have corresponding English records in the Choices \[sys\_choice\] table are set to **Inactive** by default. If you activate plugins that include those corresponding English choice records later, you need to make these records active to display translated choices for any applications or features installed with the plugin.

## Procedure

1.  Navigate to **All** &gt; **System Localization** &gt; **Languages**.

2.  In the Languages \[sys\_language\] table, select the name of any active language.

    You can select any language because this process updates choice records for all languages.

3.  In the Related Links section, select **Repair non-english sys\_choice records**.

4.  In the Repair Non-English Choices? dialog box, select **Yes**.

    A job that makes the **Inactive** field for all translated choice records match their corresponding English choice records runs 15 minutes after you make this choice.


## Result

Translations for all choices with corresponding English choice records appear for applications or features installed with plugins.

**Related topics**  


[Choice table](../reference/r_ChoicesTable.md)

[Languages table](../reference/r_LanguagesTable.md)

