---
title: Translating custom content
description: Translate content you create or modify to a supported language or add an unsupported language.
locale: en-US
release: zurich
product: System Localization
classification: system-localization
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [System Localization, Translation and localization, Configure core features, Administer]
---

# Translating custom content

Translate content you create or modify to a supported language or add an unsupported language.

**Note:** Using the Localization Framework application is recommend for translating to an unsupported language or translating large amounts of custom UI string content in a supported language. For more information, see [Localization Framework](../../localization-framework/concept/localization-framework-landing.md).

ServiceNow provides translations of the base system UI strings in supported languages through the internationalization \(I18N\) language plugins. For applications you create and modifications you make to the ServiceNow AI Platform® content, you must provide your own translations. You can also provide any translations to unsupported languages that ServiceNow does not provide translations for. The ServiceNow AI Platform does not provide any automatic translation capability.

The translation method depends on the material that you are translating. Repeat the translation process whenever you edit or update content.

<table id="table_xfh_rgr_f3b"><thead><tr><th>

What needs translation

</th><th>

Approach to take

</th><th>

Resources

</th></tr></thead><tbody><tr><td>

Field labels in a table for a customer-created application

</td><td>

1.  Create English versions for all fields in the table.
2.  Locate the records for the table in the application.
3.  Open the Field Labels translation table.
4.  Export the records, translate the appropriate fields, set the language field, and reimport through an import set.

</td><td>

-   [Export and edit translation records](../task/t_TranslateTheInterface.md#)
-   Alternatively, follow the procedure for translating individual labels in [Translate a field label](../task/t_TranslateAFieldLabel.md).

</td></tr><tr><td>

HTML in a UI page in a customer-created application

</td><td>

1.  Create the English version. When creating the HTML in the UI Page form, wrap any translatable text in `gs.getMessage` calls.
2.  Create a Message \[sys\_ui\_message\] record for each English message with a corresponding key/value pair.
3.  Create additional Message records for each message for each other language.

</td><td>

[Translate a client script message](../task/t_TranslateAClientScriptMessage.md)

</td></tr><tr><td>

Service Catalog items

</td><td>

1.  Navigate to **All** &gt; **System Properties** &gt; **System Localization** and set **Display translation prefix on translatable strings** to **Yes**.
2.  Create the item in English.
3.  Change the preferred language to a different language.
4.  Translate all the translatable items, now identified by translation prefix.
5.  Save the record.

</td><td>

-   To activate translation prefixes, see [Debug translations](../task/t_DisplayATranslationPrefix.md).
-   For translatable text fields, which are common in Service Catalog items, see [Translating text fields](c_UseTranslatedText.md#).

</td></tr><tr><td>

Service Portal widget

</td><td>

1.  Create the English version. Externalize any translatable text by surrounding the text with`${}` wrappers.
2.  Create a Message \[sys\_ui\_message\] record for each English translatable text with a corresponding key/value pair.
3.  Create additional Message records for each piece of translatable text for each other language.

</td><td>

-   [Translate a client script message](../task/t_TranslateAClientScriptMessage.md)
-   [Internationalize a widget](https://www.servicenow.com/docs/access?context=c_WidgetLocalization&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) in Service Portal documentation
-   For unofficial advice, see [Building multi-lingual service portals](https://www.dylanlindgren.com/2018/11/07/building-multilingual-service-portals/)

</td></tr><tr><td>

Playbooks

</td><td>

1.  Activate any playbook that you want to translate.
2.  Create translations for each translatable text in a playbook's process definition \[sys\_pd\_process\_definition\].

</td><td>

[Add translations for playbooks](https://www.servicenow.com/docs/access?context=add-translations-playbooks&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)

</td></tr><tr><td>

Edit a translation provided in a plugin

</td><td>

1.  Export the records from the translation table.
2.  Edit them outside the translation table and reimport them.

 Do not edit the records directly, because your changes could be overwritten when you upgrade or zBoot your instance.

</td><td>

[Export and edit translation records](../task/t_TranslateTheInterface.md#)

</td></tr><tr><td>

Translate an instance to an unsupported language

</td><td>

1.  Create a Choice \[sys\_choice\] record for that language.
2.  Add other translation records through the Export and import set approach.

</td><td>

[Translating to an unsupported language](../task/self-localize.md)

</td></tr><tr><td>

Support Chat texts

</td><td>

Support Chat is mostly translated through the I18N language plugins. If you customize any Support Chat texts, follow the procedure for Service Portal widgets.

</td><td>

[Internationalize a widget](https://www.servicenow.com/docs/access?context=c_WidgetLocalization&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) in Service Portal documentation

</td></tr><tr><td>

Notifications and surveys

</td><td>

System Localization does not cover platform notifications or surveys. The usual approach is to create a separate version of each survey or notification in each language and use business rules to send the right language version to the right end user.

</td><td>

—

</td></tr></tbody>
</table>-   **[Export and edit translation records](../task/t_TranslateTheInterface.md#)**  
Export translation records to translate to additional languages in your preferred translation environment and import the new or edited translation records through import sets.

**Parent Topic:**[System Localization](system-localization-landing.md)

