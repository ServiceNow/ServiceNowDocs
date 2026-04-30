---
title: Set a fallback language
description: Set a fallback language to be used when user interface text is not translated in the user's preferred language to accommodate the language needs of your users.
locale: en-US
release: zurich
product: System Localization
classification: system-localization
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring System Localization, System Localization, Translation and localization, Configure core features, Administer]
---

# Set a fallback language

Set a fallback language to be used when user interface text is not translated in the user's preferred language to accommodate the language needs of your users.

## Before you begin

Activate the languages that your users need. For more information, see [Activate a language](t_ActivateALanguage.md) for supported languages or [Translating to an unsupported language](self-localize.md) for custom translations.

Role required: admin

## About this task

By default, if a UI string is not translated in the preferred language of an instance session, it displays in English. Setting fallback languages creates a three-level hierarchy in which an intermediate language is used before defaulting to English. Setting a fallback language also means you don't need to add custom translations for UI strings that are suitable in the fallback language and users get UI strings in the languages most appropriate for them.

For example, you could set the fallback language for Mexican Spanish to Spanish. If a UI string is not translated in Mexican Spanish, it displays in Spanish instead. If a Spanish translation is not available either, the UI string displays in English. As an admin, you would need to provide custom translations of UI strings in Mexican Spanish only when the translation differs from the Spanish translation.

**Note:** To turn off fallback languages and always fall back to English, add the **glide\_i18n.language\_fallback\_enabled** property to the System Properties \[sys\_properties\] table and set the value to `false` .

## Procedure

1.  Navigate to **All** &gt; **System Localization** &gt; **Languages**.

2.  In the Languages \[sys\_language\] table, select the name of an active language.

3.  In the **Fallback** field of the language record, select the name of the fallback language.

    You can select only an active language as the fallback language. You cannot set English as the fallback language because it is the default fallback language.

4.  Select **Update**.


