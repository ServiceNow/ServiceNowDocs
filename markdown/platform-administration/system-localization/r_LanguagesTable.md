---
title: Languages table
description: The Languages \[sys\_language\] table contains a list of the languages for which translated text is available.
locale: en-US
release: australia
product: System Localization
classification: system-localization
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Translation tables, System Localization reference, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Languages table

The Languages \[sys\_language\] table contains a list of the languages for which translated text is available.

To enable translation to a new language, add a record to the Languages table. The main fields for this table are:

-   Name: Language name
-   ID: [BCP 47](http://www.iana.org/assignments/language-subtag-registry/language-subtag-registry) code for the language
-   Text Direction: Direction of text in this language
-   Active: Indicator that shows whether the language has been activated \(true\) for this instance or not \(false\)
-   Fallback: Name of the language that the instance uses if a translation is not available

**Parent Topic:**[Translation tables](r_TranslationTables.md)

**Related topics**  


[Activate a language](../task/t_ActivateALanguage.md)

[Create a language record](../task/t_CreateANewLanguageRecord.md)

[Ensure that translated choices appear for applications added by plugins](../task/activate-translated-choices-plugins.md)

