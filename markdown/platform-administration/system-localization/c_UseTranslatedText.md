---
title: Translating text fields
description: Translate long pieces of text into the language of the user.Translate the content of translated text and HTML fields directly in the form where the content is specified.
locale: en-US
release: australia
product: System Localization
classification: system-localization
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Translating individual UI strings, Translating custom content, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Translating text fields

Translate long pieces of text into the language of the user.

Translated text fields allow the same field to display different content based on the language of the user.

There are two different translated text fields:

-   Translated Text: Stores long text values in plain text.
-   Translated HTML: Store long text values in HTML.

These fields operate the same as normal text and HTML fields respectively, except that they can store multiple inputs in multiple languages. The most frequent use of translated text fields is Service Catalog names, descriptions, or variables.

**Note:** There is a slight performance penalty associated with changing a normal HTML or text field into a translated HTML or text field. It is best only to use translated fields if the translated capability is required.

For translated text and HTML fields, the English language text is stored in the main table, but the values of other languages are stored in the Translated Text \[sys\_translated\_text\] table. Each translated field on every row has one or more entries in the Translated Text table: one per language for which ServiceNow provides a translation. For more information, see [Translated text table](../reference/r_TranslatedText.md).

**Note:** Knowledge article translation uses a separate system that relies on the I18N: Knowledge Management Internationalization Plugin. If this plugin is not activated, knowledge article translation falls back on the system described here, with translations kept in the Translated Text \[sys\_translated\_text\] table. For more information about Knowledge Management internationalization, see Translation management in the Knowledge Management documentation.

## Translate long text content

Translate the content of translated text and HTML fields directly in the form where the content is specified.

### Before you begin

Role required: admin

### About this task

Use the following procedure to translate the content for customer-created text fields. To edit existing text translations, export the records from the Translated Text table and follow the procedure in [Export and edit translation records](../task/t_TranslateTheInterface.md#).

### Procedure

1.  Open the record with the field that you want to translate.

2.  Verify that the field whose content you want to translate is a translated\_text or translated\_html field.

    The following steps are one possible way to verify a field type:

    1.  Right-click the label of the field and select **Configure dictionary**.

        In this example, the context menu has been opened for the **Name** field for a record in the Record Producer \[sc\_cat\_item\_producer\] table.

        ![The context menu from clicking on the label of the Name field, with the Configure Dictionary option highlighted.](../image/field-label-context-menu.png "Context menu for field")

    2.  In the **Dictionary Entry** record that opens, confirm that the **Type** field is **Translated Text** or **Translated HTML**.

        In this example, you see that the **Name** field is of the type **Translated Text**.

        ![Dictionary entry for the Name field, with the Type highlighted.](../image/field-type-dictionary-entry.png "Dictionary entry for field")

    3.  Navigate back to the form.

3.  Use the language picker to switch to the desired language.

4.  In the relevant field, replace the English text with the text of the target language.

5.  Select **Submit**.

    A new record in the Translated Text \[sys\_translated\_text\] table for the active language is added. For more information about this table, see [Translated text table](../reference/r_TranslatedText.md).


