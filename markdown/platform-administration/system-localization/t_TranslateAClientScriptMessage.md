---
title: Translate a client script message
description: Translate the messages used by client scripts.
locale: en-US
release: australia
product: System Localization
classification: system-localization
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Translating individual UI strings, Translating custom content, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Translate a client script message

Translate the messages used by client scripts.

## Before you begin

Create a client script that contains messages. For information about creating client scripts, see [Client scripts](https://www.servicenow.com/docs/access?context=client-scripts&version=australia&pubname=australia-api-reference&ft:locale=en-US).

Role required: admin

## About this task

Client scripts include a multi-line Messages field, which is for message strings that the client script can use as a key to look up a localized message alternative from the Message \[sys\_ui\_message\] table. Each message key in a client script is on a separate line in the Messages field. The instance looks for a localized message string anytime the client script makes a getMessage\(msg\) call where the msg string matches a key in the Messages field in the client script.

![A client script form with message key strings in the Messages field and getMessage calls in the script field.](../image/client-script-messages.png)

For example, if you add the string `Please populate the Reason` field to the Messages field in the client script, then the instance will look for a localized string from the Message `[sys_ui_message]` table any time the client script calls:

`getMessage("Please populate the Reason field")`

**Note:** If you create a record in the Message \[sys\_ui\_message\] table that uses an existing key and the same language, the message for existing references using the key can change. For example, if a record exists with "Refresh" for the key, English for the language, and "Refresh" for the message, and you create another record with the same key and language but a different message of "Refresh the screen", existing UI strings using the "Refresh" key will display the new "Refresh the screen" message. Records in this table are created in the global scope and aren’t scope-restricted.

## Procedure

1.  Navigate to **All** &gt; **System Localization** &gt; **Messages**.

2.  Select **New**.

3.  On the form, fill in the required fields.

    |Field|Description|
    |-----|-----------|
    |Key|The internal unique identifier for this message.|
    |Language|The language the message is translated into.|
    |Message|The translated text that users see.|

    ![A message form with a message key translated into Spanish.](../image/translated-message.png)

4.  Select **Submit**.

    A new record is added to the Message `[sys_ui_message]` table for the localized message key string. For more information about this table, see [Message table](../reference/r_MessageTable.md).


