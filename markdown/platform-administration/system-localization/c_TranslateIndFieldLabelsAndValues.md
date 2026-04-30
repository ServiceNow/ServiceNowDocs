---
title: Translating individual UI strings
description: When translating just a few UI strings, such as when you add customizations to a translated instance, use the procedure that applies to the type of text being translated.
locale: en-US
release: yokohama
product: System Localization
classification: system-localization
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Translating custom content, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Translating individual UI strings

When translating just a few UI strings, such as when you add customizations to a translated instance, use the procedure that applies to the type of text being translated.

UI strings include field names and values, related list names, and messages.

## Fields and related lists

Three types of fields support translated strings for fields and related list names:

-   **Translated\_field**

    Stores field labels, related list names, and certain field values. The value of the translated\_field replaces the label, list name, or field value when the user selects the matching language. Translated\_field values have a one-to-many relationship with their associated keys. As a result, multiple records can reference one translated\_field value. For more information, see the following topics:

    -   [Translate a field label](../task/t_TranslateAFieldLabel.md)
    -   [Translate a related list name](../task/t_TranslateARelatedListName.md)
    -   [Translate a field value for the Classic Environment](../task/t_TranslateAFieldValue.md)
-   **Translated\_text**

    Stores long text values in plain text. The value of the translated\_text replaces the plain text when the user selects the matching language. Translated\_text values have a one-to-one relationship with their associated keys. As a result, only one record can reference a translated\_text value. For more information, see [Translating text fields](c_UseTranslatedText.md#).

-   **Translated\_html**

    Stores long text values in HTML. The value of the translated\_html replaces the HTML when the user selects the matching language. Translated\_html values have a one-to-one relationship with their associated keys. As a result, only one record can reference a translated\_html value. For more information, see [Translating text fields](c_UseTranslatedText.md#).


The translated values are stored as separate records and display the proper value according to the end user’s language. To determine the field type, right-click the field on the form, select **Configure Dictionary**, and check the **Type** field.

## Messages

Informational messages, confirmation messages, error messages, and other types of system messages across the platform can be translated. Messages that support translation come from HTML in a UI page in a customer-created application or Service Portal widget messages when these texts are wrapped correctly. When a client script contains a getMessage call or a server script contains a `gs.getMessage` call, the system checks the Messages \[sys\_ui\_message\] table for a translation. Fore more information, see [Translate a client script message](../task/t_TranslateAClientScriptMessage.md).

