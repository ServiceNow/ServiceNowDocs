---
title: Translated text table
description: The Translated Text \[sys\_translated\_text\] table stores translations for fields with the field type translated\_text or translated\_html \(see the dictionary entry\).
locale: en-US
release: australia
product: System Localization
classification: system-localization
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Translation tables, System Localization reference, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Translated text table

The Translated Text \[sys\_translated\_text\] table stores translations for fields with the field type translated\_text or translated\_html \(see the dictionary entry\).

This field type is typically used for long text fields, up to 65,000 characters in length, such as survey name and introduction. The main fields for this table are:

-   Document: internal identifier of the record this translation applies to.
-   Field name: field this translated text appears in, for example, Close notes.
-   Language: language the text is translated into.
-   Table Name: table this translation applies to.
-   Value: translated text that the user sees.

![The list of records in the Translated Text table.](../image/TranslatedTextList.png "Translated text list")

**Parent Topic:**[Translation tables](r_TranslationTables.md)

**Related topics**  


[Translating text fields](../concept/c_UseTranslatedText.md#)

[Translating text fields](../concept/c_UseTranslatedText.md#)

