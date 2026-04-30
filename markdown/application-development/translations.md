---
title: Translations
description: When using one of the Internationalization plugins, most of the fields in the instance are automatically translated. However, customizations are not translated automatically, and need to be translated by hand. In this case, it is best to locate the individual untranslated strings, and insert those translations manually.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create design elements, Build your application, Exploring professional development, Building pro-code applications, Developing your application, Building applications]
---

# Translations

When using one of the Internationalization plugins, most of the fields in the instance are automatically translated. However, customizations are not translated automatically, and need to be translated by hand. In this case, it is best to locate the individual untranslated strings, and insert those translations manually.

To implement a new language, activate the plugin for the new language. Then export the existing values from any of the [Translation tables](https://servicenow.com/docs/bundle/paris-platform-administration/page/administer/localization/reference/r_TranslationTables.html).

For example, export all **sys\_choice** records. Provide the export to a translator to provide translations for the **Label** field in the provided file. The **Value** field should not change. Update the **Language** value to the new language. Then, upload the translated values back to the **sys\_choice** table.

**Note:** To insert values, make sure you are setting all the necessary fields; table, element, language, label, value, and sequence. Set the dependent value and hint where applicable. This logic is the same for all translation tables.

For more information, see [Language Internationalization Support](https://servicenow.com/docs/bundle/paris-platform-administration/page/administer/localization/concept/c_LangInternationalizationSupport.html)

**Parent Topic:**[Create design elements](create-design-elements.md)

