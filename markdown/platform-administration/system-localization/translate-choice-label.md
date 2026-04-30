---
title: Translate a choice label
description: Translate the labels of choices in a list.
locale: en-US
release: xanadu
product: System Localization
classification: system-localization
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Translating individual UI strings, Translating custom content, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Translate a choice label

Translate the labels of choices in a list.

## Before you begin

Role required: admin

## About this task

To translate a choice in a list, you must create a choice record for each language that you want to support in the Choice \[sys\_choice\] table. For more information about this table, see [Choice table](../reference/r_ChoicesTable.md).

## Procedure

1.  Navigate to **All** &gt; **System Localization** &gt; **Choices**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Table|The name of the table that contains the choice.|
    |Element|The column name for the field that contains the choice.|
    |Language|The [BCP 47](http://www.iana.org/assignments/language-subtag-registry/language-subtag-registry) code of the language for the translated choice. The identifier can contain a language code or language code followed by a country or region code. For example, tr for Turkish or es-MX for Spanish Mexico.|
    |Label|The label for the choice in the specified language.|
    |Value|A key that is the same for the choice in each language. For example, you could use the English label or the sequence number as the value for all languages to map them to each other.|
    |Sequence|A number that determines in what order the option appears in the list if you don’t want to list choices alphabetically.|

    The following record translates the "Email" choice in the subcategory field on the Incident table into Spanish.

    -   **Table**: Incident \[incident\]
    -   **Element**: subcategory
    -   **Language**: es
    -   **Label**: Correo electrónico
    -   **Value**: email
4.  Select **Submit**.

5.  From the context menu, select **Insert and Stay** and update the form to translate the choice into another language.


