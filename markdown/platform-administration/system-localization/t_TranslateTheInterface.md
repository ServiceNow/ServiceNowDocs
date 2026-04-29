---
title: Export and edit translation records
description: Export translation records to translate to additional languages in your preferred translation environment and import the new or edited translation records through import sets.The System Import Sets application contains import tables and corresponding transform maps to assist with importing translations from an Excel spreadsheet.
locale: en-US
release: australia
product: System Localization
classification: system-localization
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Translating custom content, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Export and edit translation records

Export translation records to translate to additional languages in your preferred translation environment and import the new or edited translation records through import sets.

## Before you begin

**Note:** Using the Localization Framework application is recommend for translating to an unsupported language or translating large amounts of custom UI string content in a supported language. For more information, see [Localization Framework](../../localization-framework/concept/localization-framework-landing.md).

Role required: admin

## About this task

In the following cases, translate strings in the UI outside of the ServiceNow AI Platform and import them through import sets:

-   You have a significant amount of customer-created UI components and you want to translate these components into other languages.
-   You want to modify translations that ServiceNow provides in internationalization plugins.
-   You want to translate an instance into a language that ServiceNow does not support with internationalization plugins. For more information, see [Translating to an unsupported language](self-localize.md).

All translatable UI strings items are stored in translation table records. The only time you would translate UI directly in translation records is when you have a small amount of customer-created UI components and you know exactly where they are. For more information about translation tables, see [Translation tables](../reference/r_TranslationTables.md) and [Translating individual UI strings](../concept/c_TranslateIndFieldLabelsAndValues.md).

## Procedure

1.  If you are translating customer-created UI components, locate the translatable strings.

    For more information, [Locating translatable UI strings](../concept/c_TranslateNewCustomizations.md).

2.  Export the relevant translation table records into a format \(such as Excel\) that can be easily manipulated.

    For more information about exporting a list of records, see [Export data from a list](../../exporting-data/task/export-list-data.md).

3.  Within the exported document, translate the following fields in each row, depending on the translation table:

    |Translation table|Fields to translate|
    |-----------------|-------------------|
    |Field Labels|Label, Plural, Hint|
    |Translated Name/Field|Label \(translate\)|
    |Message|Message|
    |Choices|Label|
    |Translated Text|Value|

4.  Within each row, change the "Language" column to the [BCP 47](http://www.iana.org/assignments/language-subtag-registry/language-subtag-registry) code of the new language.

    In Translated Text and Message records, type the full name of the language instead of the BCP 47 code.

5.  Save your changes.


## What to do next

Import the translated document back into the instance as an import set.

**Parent Topic:**[Translating custom content](../concept/translating-applications.md)

## Import a translation from an Excel spreadsheet

The System Import Sets application contains import tables and corresponding transform maps to assist with importing translations from an Excel spreadsheet.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Load Data**.

2.  Select **Use Existing** and the **Table name** that matches the type of data being imported, as follows.

    -   For choices, select the `[u_sys_choice]` table.
    -   For field labels, select the `[u_sys_documentation]` table.
    -   For translated names and fields, select the `[u_sys_translated]` table.
    -   For messages, select the `[u_sys_ui_message]` table.
    -   For translated text, select the `[u_sys_translated_text]` table.
3.  Select **Upload an Excel file**, and then click **Browse** to select the source Excel spreadsheet.

4.  If appropriate, specify the Work sheet and Header row number.

5.  Select **Go**.

    The translations are now available in the appropriate Import Set Table.

6.  Navigate to **All** &gt; **System Import Sets** &gt; **Table Name** and review the imported information to verify that the import was successful.

7.  To transform the imported data into the corresponding table, navigate to **All** &gt; **System Import Sets** &gt; **Run Transform**.

8.  Select the appropriate transform map, as follows.

    **Note:** Make sure you choose a transform map that has the **Run Business Rule** option selected. If the transform map does not have this option selected, any customized translations you have may be overwritten during the next upgrade.

    -   For choices, select the **Sys Choice Translation Map**.
    -   For field labels, select the **Sys Documentation Translation Map**.
    -   For translated names and fields, select the **Sys Translated Translation Map**.
    -   For messages, select the **Sys UI Message Translation Map**.
    -   For translated text, select the **Sys Translated Text Translation Map**.
9.  Select **Transform**.


