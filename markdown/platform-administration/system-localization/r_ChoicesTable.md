---
title: Choice table
description: The Choice \[sys\_choice\] table contains translated text for options that appear in lists.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/system-localization/r\_ChoicesTable.html
release: australia
product: System Localization
classification: system-localization
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Translation tables, System Localization reference, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Choice table

The Choice \[sys\_choice\] table contains translated text for options that appear in lists.

The main fields for this table are:

-   Table: The name of the table this translation applies to.
-   Element: The name of the field this translation is used for.
-   Language: The [BCP 47](http://www.iana.org/assignments/language-subtag-registry/language-subtag-registry) code of the language for the translated choice.
-   Value: A key that is the same for the choice in each language. For example, you could use the English label or the sequence number as the value for all languages to map them to each other.
-   Label: The label for the choice in the specified language.
-   Sequence: A number that determines in what order the option appears in the list if you don’t want to list choices alphabetically.

\[Omitted image "ChoiceList.png"\] Alt text: The list of records in the Choices table with choice labels in English and Spanish.

\[Omitted image "TranslatedChoiceList.png"\] Alt text: A Choice record translated into Spanish.

**Parent Topic:**[Translation tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/r_TranslationTables.md)

**Related topics**  


[Create a language choice for users]()

[Ensure that translated choices appear for applications added by plugins]()

