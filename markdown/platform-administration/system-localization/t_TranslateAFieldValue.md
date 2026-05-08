---
title: Translate a field value for the Classic Environment
description: Field values are the text entries that are used for fields with the type translated\_field, such as the Title or Hint field in the Module \[sys\_app\_module\] table.
locale: en-US
release: australia
product: System Localization
classification: system-localization
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Translating individual UI strings, Translating custom content, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Translate a field value for the Classic Environment

Field values are the text entries that are used for fields with the type translated\_field, such as the Title or Hint field in the Module \[sys\_app\_module\] table.

## Before you begin

Role required: admin

## About this task

The following procedure works best for translating values for individual fields, such as those added with a customization. To translate large numbers of field values, use the procedure described in [Export and edit translation records](t_TranslateTheInterface.md#).

## Procedure

1.  Use the language picker in the header bar to switch to the desired target language.

2.  Navigate to the field on the form.

3.  Update the field value with the text translated into the target language \(Spanish\).

    ![Translation field values.](../image/TranslationFieldValues.png)

4.  Select **Update**.

    This creates a new record in the Translated Name / Field \[sys\_translated\] table for the selected language or updates the existing record if a translation already exists. For more information about this table, see [Translated Name / Field table](../reference/r_TranslatedNameFieldTable.md).

    ![New record added to the Translated Name / Fields table for the field value translated into Spanish.](../image/translated-field-value.png "Translated field")


