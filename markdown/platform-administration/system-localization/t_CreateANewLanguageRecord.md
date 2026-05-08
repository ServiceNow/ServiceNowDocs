---
title: Create a language record
description: Add a record for a language not provided by an internationalization \(I18N\) plugin to associate new translations with.
locale: en-US
release: australia
product: System Localization
classification: system-localization
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Translating to an unsupported language, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a language record

Add a record for a language not provided by an internationalization \(I18N\) plugin to associate new translations with.

## Before you begin

Role required: admin

## About this task

To translate the interface of an instance to a language for which ServiceNow does not provide an internationalization plugin, you must create a language record for a new translation in the Languages \[sys\_language\] table. For more information about this table, see [Languages table](../reference/r_LanguagesTable.md).

## Procedure

1.  Navigate to **All** &gt; **System Localization** &gt; **Languages**.

2.  Select **New**.

3.  Provide the language information.

    -   **Name**: The name of the language, for example, Turkish.
    -   **ID**: The [BCP 47](http://www.iana.org/assignments/language-subtag-registry/language-subtag-registry) code for the language, for example, tr.
    -   **Text Direction**: The direction that the instance should use to display the language: Left-to-Right or Right-to-Left.
    -   **Active**: Option to activate the language for the instance.
    -   **Fallback**: The name of another active language to use as a fallback language. For more information about fallback languages, see [Set a fallback language](set-fallback-language.md).
4.  Select **Submit**.


**Related topics**  


[Languages table](../reference/r_LanguagesTable.md)

