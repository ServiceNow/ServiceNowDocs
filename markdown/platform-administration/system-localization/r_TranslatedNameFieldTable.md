---
title: Translated Name / Field table
description: The Translated Name / Fields \[sys\_translated\] table stores translated values for text fields where the field type is translated\_field \(see the dictionary entry\).
locale: en-US
release: australia
product: System Localization
classification: system-localization
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Translation tables, System Localization reference, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Translated Name / Field table

The Translated Name / Fields \[sys\_translated\] table stores translated values for text fields where the field type is translated\_field \(see the dictionary entry\).

This option is available for text fields up to 255 characters in length. Some examples are names, titles, and short descriptions. The main fields for this table are:

-   Table: name of the table this translation applies to.
-   Element: name of the field this translation applies to.
-   Label \(translate\): translated text that users see on forms and lists.
-   Language: [BCP 47](http://www.iana.org/assignments/language-subtag-registry/language-subtag-registry) code of the language for this translated text.
-   Value: English value that causes this translated text to be displayed.

![The Translated Name/Fields table with Spanish translations for name and field values.](../image/FieldList.png "Translated Name/Fields table")

**Parent Topic:**[Translation tables](r_TranslationTables.md)

**Related topics**  


[Translate a field value for the Classic Environment](../task/t_TranslateAFieldValue.md)

[Translate a related list name](../task/t_TranslateARelatedListName.md)

