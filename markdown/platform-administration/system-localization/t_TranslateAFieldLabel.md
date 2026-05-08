---
title: Translate a field label
description: Field labels are the names that appear on forms and lists to describe the type of information the field contains.
locale: en-US
release: australia
product: System Localization
classification: system-localization
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Translating individual UI strings, Translating custom content, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Translate a field label

Field labels are the names that appear on forms and lists to describe the type of information the field contains.

## Before you begin

Role required: admin

## About this task

The following procedure works best for translating individual field labels, such as those added with a customization. To translate large numbers of field labels, use the procedure described in [Export and edit translation records](t_TranslateTheInterface.md#).

## Procedure

1.  Navigate to the field on the form.

2.  Right-click the field label and select **Configure Label**.

3.  In the Field Label form, replace the English text with the text of the target language in the Label, Plural, and Hint fields.

4.  Enter the [BCP 47](http://www.iana.org/assignments/language-subtag-registry/language-subtag-registry) code of the target language.

5.  Right-click the header bar and select **Insert**.

    Selecting **Insert** creates a new record in the Field Label \[sys\_documentation\] table for this field label in the selected language. For more information about this table, see [Field Label table](../reference/r_FieldLabelTable.md).


