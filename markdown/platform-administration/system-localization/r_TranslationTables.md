---
title: Translation tables
description: ServiceNow stores translation information in these tables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/system-localization/r\_TranslationTables.html
release: australia
product: System Localization
classification: system-localization
topic_type: reference
last_updated: "2026-03-12"
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

To see which table contains a specific translated label, enable the display of translation prefixes. For more information, see [Debug translations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/t_DisplayATranslationPrefix.md).

**Note:** The Languages table is available only after at least one I18N:Internationalization plugin has been activated.

-   **[Languages table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/r_LanguagesTable.md)**  
The Languages \[sys\_language\] table contains a list of the languages for which translated text is available.
-   **[Choice table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/r_ChoicesTable.md)**  
The Choice \[sys\_choice\] table contains translated text for options that appear in lists.
-   **[Translated Name / Field table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/r_TranslatedNameFieldTable.md)**  
The Translated Name / Fields \[sys\_translated\] table stores translated values for text fields where the field type is translated\_field \(see the dictionary entry\).
-   **[Field Label table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/r_FieldLabelTable.md)**  
The Field Label \[sys\_documentation\] table stores the text of table names along with the singular and plural labels for each field in the table.
-   **[Translated text table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/r_TranslatedText.md)**  
The Translated Text \[sys\_translated\_text\] table stores translations for fields with the field type translated\_text or translated\_html \(see the dictionary entry\).
-   **[Message table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/r_MessageTable.md)**  
The Message \[sys\_ui\_message\] table contains the translations for informational messages, confirmation messages, error messages, and other types of system messages across the platform.

**Parent Topic:**[System Localization reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/system-localization-reference.md)

**Related topics**  


[Activate a language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/t_ActivateALanguage.md)

