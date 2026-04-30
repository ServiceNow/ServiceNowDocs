---
title: List untranslated items
description: Get a list of all custom UI strings that have not been translated into any language \(English only\) to provide your own translations.
locale: en-US
release: xanadu
product: System Localization
classification: system-localization
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Locating translatable UI strings, Translating custom content, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
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

    ![Non-translated localization modules.](../image/LocalizationModulesTrue.png)

    **Note:** Instead of **Customizations**, your list might show a record titled **Non-translated Items**. When you activate the **Customizations** module, the title changes to **Non-translated Items**.

    After the application navigator refreshes, the modules appear in the filter navigator beneath **Non-translated Items**.

    ![Filter navigator showing non-translated items per translation table.](../image/non-translated-items-nav.png)

4.  From the application menu, open each module and export their lists to any supported format, such as Microsoft Excel.

    For example, select **Non-translated Items** &gt; **Translated Name/Fields**, right click any column, and export the list.

    ![List of non-translated Translated Name/Fields.](../image/non-translated-name-fields.png)


## What to do next

You can translate the fields in an external application and reload the translations as an update set. For more information see, [Export and edit translation records](t_TranslateTheInterface.md#). If you have a small number of strings to translate, you can translate them individually. For more information, see [Translating individual UI strings](../concept/c_TranslateIndFieldLabelsAndValues.md).

