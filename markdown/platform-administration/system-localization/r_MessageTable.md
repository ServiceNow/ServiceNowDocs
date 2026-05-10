---
title: Message table
description: The Message \[sys\_ui\_message\] table contains the translations for informational messages, confirmation messages, error messages, and other types of system messages across the platform.The name of this table appears as "Messages" in the list view but technically the table name is "Message" in the system definition.
locale: en-US
release: australia
product: System Localization
classification: system-localization
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Translation tables, System Localization reference, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Message table

The Message \[sys\_ui\_message\] table contains the translations for informational messages, confirmation messages, error messages, and other types of system messages across the platform.

The Message table contains custom translatable text from the following sources when these texts are wrapped correctly:

-   HTML in a UI page in a customer-created application
-   Service Portal widget messages \(including in surveys\)
-   Playbook text:
    -   Playbook Label
    -   Stage Label
    -   Activity Label
    -   Activity Description
    -   HTML and string Activity UI Layout properties

ServiceNow checks this table for translated text when a client script contains a getMessage call or a server script contains a `gs.getMessage` call. The main fields for this table are:

-   Key: internal, case-insensitive, unique identifier of this message.
-   Language: language the message is translated into.
-   Message: translated text that users see.

**Note:** If you create a record in the Message \[sys\_ui\_message\] table that uses an existing key and the same language, the message for existing references using the key can change. For example, if a record exists with "Refresh" for the key, English for the language, and "Refresh" for the message, and you create another record with the same key and language but a different message of "Refresh the screen", existing UI strings using the "Refresh" key will display the new "Refresh the screen" message. Records in this table are created in the global scope and aren’t scope-restricted.

For more information about translatable custom content in the Message table, see [Translating custom content](../concept/translating-applications.md).



![The Messages list showing messages translated into Spanish.](../image/MessageList.png)

![The message that "The following mandatory fields are not filled: Name", translated into Spanish.](../image/TranslatedMessage.png "Translated message")

**Parent Topic:**[Translation tables](r_TranslationTables.md)

**Related topics**  


[Translate a client script message](../task/t_TranslateAClientScriptMessage.md)

[Translating Service Catalog cart labels](r_ServiceCatalogButtons.md)

