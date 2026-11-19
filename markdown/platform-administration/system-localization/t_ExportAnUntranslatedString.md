---
title: List untranslated items
description: Get a list of all custom UI strings that have not been translated into any language \(English only\) to provide your own translations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/system-localization/t\_ExportAnUntranslatedString.html
release: zurich
product: System Localization
classification: system-localization
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Locating translatable UI strings, Translating custom content, System Localization, Translation and localization, Configure core features, Administer]
---

# List untranslated items

Get a list of all custom UI strings that have not been translated into any language \(English only\) to provide your own translations.

## Before you begin

Role required: admin

## About this task

This procedure activates modules corresponding to the following translation tables that list records with only an English version.

-   Translated Name / Fields
-   Messages
-   Field Labels
-   Choices

This method of listing untranslated items does not identify strings that have been translated into at least one non-English language but are missing translations in other languages.

**Note:** This process works best with a small number of untranslated items. For information about a workaround for large numbers of untranslated items, see the [Inefficient load of customizations for System Localization -&gt; Non-Translated Items \[KB0813304\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0813304) article in the Now Support Knowledge Base.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Application Menus**.

2.  Select the **System Localization** application menu.

3.  From the **Modules** list in the **System Localization** record, update the **Customizations**, **Translated Name/Fields**, **Messages**, **Field Labels**, and **Choice** modules to set the **Active** field to **True** using the list editor.

    When the list is sorted by **Order**, the modules appear in order from 500 to 900.

    \[Omitted image "LocalizationModulesTrue.png"\] Alt text: Non-translated localization modules.

    **Note:** Instead of **Customizations**, your list might show a record titled **Non-translated Items**. When you activate the **Customizations** module, the title changes to **Non-translated Items**.

    After the application navigator refreshes, the modules appear in the filter navigator beneath **Non-translated Items**.

    \[Omitted image "non-translated-items-nav.png"\] Alt text: Filter navigator showing non-translated items per translation table.

4.  From the application menu, open each module and export their lists to any supported format, such as Microsoft Excel.

    For example, select **Non-translated Items** &gt; **Translated Name/Fields**, right click any column, and export the list.

    \[Omitted image "non-translated-name-fields.png"\] Alt text: List of non-translated Translated Name/Fields.


## What to do next

You can translate the fields in an external application and reload the translations as an update set. For more information see, [Export and edit translation records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/system-localization/t_TranslateTheInterface.md). If you have a small number of strings to translate, you can translate them individually. For more information, see [Translating individual UI strings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/system-localization/c_TranslateIndFieldLabelsAndValues.md).

