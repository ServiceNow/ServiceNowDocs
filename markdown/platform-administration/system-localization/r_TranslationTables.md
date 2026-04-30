---
title: Translation tables
description: ServiceNow stores translation information in these tables.
locale: en-US
release: yokohama
product: System Localization
classification: system-localization
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [System Localization reference, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Translation tables

ServiceNow stores translation information in these tables.

-   Languages \[sys\_language\]
-   Translated Name / Field \[sys\_translated\]
-   Messages \[sys\_ui\_message\]
-   Field label \[sys\_documentation\]
-   Choice \[sys\_choice\]
-   Translated Text \[sys\_translated\_text\]

To see which table contains a specific translated label, enable the display of translation prefixes. For more information, see [Debug translations](../task/t_DisplayATranslationPrefix.md).

**Note:** The Languages table is available only after at least one I18N:Internationalization plugin has been activated.

-   **[Languages table](r_LanguagesTable.md)**  
The Languages \[sys\_language\] table contains a list of the languages for which translated text is available.
-   **[Choice table](r_ChoicesTable.md)**  
The Choice \[sys\_choice\] table contains translated text for options that appear in lists.
-   **[Translated Name / Field table](r_TranslatedNameFieldTable.md)**  
The Translated Name / Fields \[sys\_translated\] table stores translated values for text fields where the field type is translated\_field \(see the dictionary entry\).
-   **[Field Label table](r_FieldLabelTable.md)**  
The Field Label \[sys\_documentation\] table stores the text of table names along with the singular and plural labels for each field in the table.
-   **[Translated text table](r_TranslatedText.md)**  
The Translated Text \[sys\_translated\_text\] table stores translations for fields with the field type translated\_text or translated\_html \(see the dictionary entry\).
-   **[Message table](r_MessageTable.md)**  
The Message \[sys\_ui\_message\] table contains the translations for informational messages, confirmation messages, error messages, and other types of system messages across the platform.

**Parent Topic:**[System Localization reference](system-localization-reference.md)

**Related topics**  


[Activate a language](../task/t_ActivateALanguage.md)

