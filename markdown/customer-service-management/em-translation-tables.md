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

 For details about translating text content into different languages, see [Translated text table](https://www.servicenow.com/docs/access?context=r_TranslatedText&version=australia&pubname=australia-platform-administration&ft:locale=en-US) and [Translating text fields](https://www.servicenow.com/docs/access?context=c_UseTranslatedText&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Message \[sys\_ui\_message\]

</td><td>

Stores translations for static messages in Engagement Messenger.For more information about the Message table, see [Message table](https://www.servicenow.com/docs/access?context=r_MessageTable&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr></tbody>
</table>**Note:** For information about Virtual Agent chat translation, see [Virtual Agent translation tables](https://www.servicenow.com/docs/access?context=va-translation-tables&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US)

