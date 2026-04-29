---
title: Language internationalization support
description: The ServiceNow platform supports multiple languages.
locale: en-US
release: australia
product: System Localization
classification: system-localization
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exploring System Localization, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Language internationalization support

The ServiceNow platform supports multiple languages.

Language support is available when at least one language plugin has been activated, as described in [Activate a language](../task/t_ActivateALanguage.md).

When a user logs in, the language for the instance session is determined by the following logic:

1.  If the language selection at login is enabled, that language is used.
2.  If not, the language preference selected using the language picker in the header bar is used.
3.  If not, the language setting in the User \[sys\_user\] table is used.
4.  If none of the above are true, the system default language is used.

You can also enable a fallback language to use if a translation isn’t available in the preferred language, as described in [Set a fallback language](../task/set-fallback-language.md).

Some parts of the system aren’t translated and remain in the language used to create them:

-   Journal fields
-   Report titles
-   Any field that stores free-form text

Additionally, plugin names and spoke names aren’t translated. The English version of plugins and spoke names is always kept, even when they’re used in other contexts. Feature names are translated, however.

Beginning in the Washington DC release, new product and application names are localized in all supported languages. Existing product and application names are being localized incrementally.

|Question|Answer|
|--------|------|
|Will fields that I created or edited myself be translated?|The ServiceNow AI Platform does not perform translations. ServiceNow only provides translations of strings that the company itself has created. When you create a field, a message, or other textual UI content, translate this content manually.|
|I am not seeing journal fields translated.|Translation tables are not provided for user-defined string fields, such as short description, additional comments, and report titles. These fields can appear only in the language they were created in.|

**Related topics**  


[Locating translatable UI strings](c_TranslateNewCustomizations.md)

