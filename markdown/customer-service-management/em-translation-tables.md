---
title: Engagement Messenger translation tables
description: Engagement Messenger uses the \[sys\_translated\_text\] and \[sys\_ui\_message\] tables to store translated text.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Customer Service Management]
---

# Engagement Messenger translation tables

Engagement Messenger uses the \[sys\_translated\_text\] and \[sys\_ui\_message\] tables to store translated text.

Each translated field on every row has one or more entries in the this table, one per language for which ServiceNow provides a translation.

<table id="table_c1f_l12_lpb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Translated Text \[sys\_translated\_text\]

</td><td>

Stores translations for configurable fields such as User Greeting and Search Message. These fields are configured in Engagement Messenger module configuration and have the field type `translated_text`.

 The main fields of this table are:

 -   **Document**: Internal identifier of the feature instance record this translation applies to.
-   **Field name**: Title or subtitle field from feature instance record.
-   **Language**: Language the text is translated into.
-   **Table Name**: Name of the feature instance.
-   **Value**: Translated text that the user sees.

 For details about translating text content into different languages, see [Translated text table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/r_TranslatedText.md) and [Translating text fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/c_UseTranslatedText.md).

</td></tr><tr><td>

Message \[sys\_ui\_message\]

</td><td>

Stores translations for static messages in Engagement Messenger.For more information about the Message table, see [Message table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/r_MessageTable.md).

</td></tr></tbody>
</table>**Note:** For information about Virtual Agent chat translation, see [Virtual Agent translation tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/va-translation-tables.md)

