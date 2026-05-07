---
title: Sorting according to the session language
description: Order string values according to the user's session language when sorting a column in a list.Enable sorting string values in columns according to the user's session language.Configure whether the values in columns are sorted according to the user's session language.
locale: en-US
release: australia
product: System Localization
classification: system-localization
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 3
breadcrumb: [Configuring System Localization, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Sorting according to the session language

Order string values according to the user's session language when sorting a column in a list.

By default, when sorting columns in lists, string values are ordered according to the English alphabet. To support sorting a column according to the user's session language, you can configure the instance behavior and the behavior of individual columns.

In the following example, the user's session language is Swedish. The Example string field column is sorted in descending order with the values ordered from Ö to A according to the Swedish alphabet.

![Column sorted according to the session language](../image/sort-session-lang.png)

**Note:** This column attribute can't be used with the following column attribute: Locale text match. For more information see [Set case and accent sensitivity on a per-column basis](../concept/sl-locale-text-match.md).

The availability of this functionality for a supported language depends on the availability of a collation in the underlying Relational Database Management System \(RDBMS\) used in the instance. For a list of available collations for each language and RDBMS, navigate to the DB Collation Info \[sys\_db\_collation\_info\] table. To add a collation for an unsupported language, see [Add collation information for an unsupported language](add-collation-unsupported-language.md).

## Enable sorting according to the session language

Enable sorting string values in columns according to the user's session language.

### Before you begin

Role required: admin

### About this task

**Note:** Sorting lists when the user's session language isn’t English might take longer than with English, particularly for tables with large amounts of records \(100,000 or greater\).

### Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **System Localization**.

2.  Select the **Enable sorting \(for lists\) in the user's session language when the language is other than English** option.

3.  Select **Save**.


### Result

When sorting a column in a list, the string values are ordered according to the user's session language. If needed, you can turn off this behavior for individual columns.

## Configure sorting for a column

Configure whether the values in columns are sorted according to the user's session language.

### Before you begin

Enable sorting according to the user's session language for the instance.

This column attribute can't be used with locale text match. For more information see [Set case and accent sensitivity on a per-column basis](../concept/sl-locale-text-match.md).

Role required: admin

### Procedure

1.  Navigate to a field on a form, select and hold \(or right-click\) the field, and select **Configure Dictionary**.

    The field must be a string field.

2.  From the Related Links, select **Advanced view**.

3.  In the Attributes field, add the `i18n_session_language_sortable` attribute and specify a value of true or false.

    -   Enter `i18n_session_language_sortable=false` to turn off sorting the column by the user's session language. The column is sorted according to the English alphabet instead.
    -   Enter `i18n_session_language_sortable=true` to enable sorting the column by the user's session language. To turn off sorting according to the user's session language for all other columns, see the following step.
4.  If you added the `i18n_session_language_sortable=true` attribute for one or more columns and want to change the default behavior of all other columns to sort according to the English alphabet, complete the following steps.

    1.  In the navigation filter, enter `sys_properties.list`.

    2.  Select **New**.

    3.  On the form, fill in the fields.

        |Field|Value|
        |-----|-----|
        |Name|com.glide.db.i18n\_session\_language\_sortable\_default|
        |Type|true\|false|
        |Value|false|

    4.  Select **Submit**.


### What to do next

Configure the sorting behavior for any additional columns as needed.

