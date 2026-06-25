---
title: Translated text table
description: The Translated Text \[sys\_translated\_text\] table stores translations for fields with the field type translated\_text or translated\_html \(see the dictionary entry\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/system-localization/r\_TranslatedText.html
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

\[Omitted image "TranslatedTextList.png"\] Alt text: The list of records in the Translated Text table.

**Parent Topic:**[Translation tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/r_TranslationTables.md)

**Related topics**  


[Translating text fields]()

[Translating text fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/c_UseTranslatedText.md)

