---
title: Field Label table
description: The Field Label \[sys\_documentation\] table stores the text of table names along with the singular and plural labels for each field in the table.
locale: en-US
release: australia
product: System Localization
classification: system-localization
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Translation tables, System Localization reference, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Field Label table

The Field Label \[sys\_documentation\] table stores the text of table names along with the singular and plural labels for each field in the table.

For each table name and field label, the Field Label table contains a record for each installed language. ServiceNow uses the table and field names from this table to display lists and forms in the proper language. The main fields for this table are:

-   Table: name of the table this translation applies to.
-   Element: name of the field this translation applies to.
-   Language: [BCP 47](http://www.iana.org/assignments/language-subtag-registry/language-subtag-registry) code of the language for the translated text.
-   Label: translated text that users see.
-   Plural: plural of the label.
-   Help: reserved for future use. A question mark \(?\) icon appears next to hint labels when accessibility mode is enabled.
-   Hint: text that pops up when the cursor rests on the field.
-   URL: URL for a web page that provides information about the field. When a URL is provided, the text appears blue and underlined to indicate the label is clickable.

![List of Field labels showing field names in the element column and label translations in English and Spanish.](../image/FieldLabel.png "Field label")

![An Incident record with field labels translated into Spanish.](../image/TranslatedField.png "Translated field")

**Parent Topic:**[Translation tables](r_TranslationTables.md)

**Related topics**  


[Translate a field label](../task/t_TranslateAFieldLabel.md)

