---
title: Message body size limit properties
description: Add properties to control the maximum email body size allowed for inbound and outbound email messages.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Email size limits, Reference, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Message body size limit properties

Add properties to control the maximum email body size allowed for inbound and outbound email messages.

## Properties

By default, the system processes up to 524,000 characters in the email **body** and **body\_text** fields.

You can add and configure system properties **glide.email.inbound.max\_body\_chars** and **glide.email.outbound.max\_body\_chars** to increase or decrease the email body size limits. The system truncates the email body when it exceeds the configured limit. For example, if you configure the body size limit of **glide.email.inbound.max\_body\_chars** to 1,000 characters but receive an inbound email that is 2,000 characters, then the system truncates the email body at 1,000 characters.

<table id="table_lft_wmt_gr"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**glide.email.inbound.max\_body\_chars**

</td><td>

Sets the maximum body size in characters allowed per inbound email.

-   Type: integer
-   Default value: 524288

</td></tr><tr><td>

**glide.email.outbound.max\_body\_chars**

</td><td>

Sets the maximum body size in characters allowed per outbound email.

-   Type: integer
-   Default value: 524288

</td></tr></tbody>
</table>**Note:** A different property, **com.glide.attachment.max\_size**, sets the maximum file size allowed for any attachment in the system and overrides any larger values of **glide.email.inbound.max\_total\_attachment\_size\_bytes** and **glide.email.outbound.max\_total\_attachment\_size\_bytes**.

## Inbound email body processing

For inbound emails, the system enforces the maximum body size as set by the **glide.email.inbound.max\_body\_chars** property. When the body size exceeds the configured value:

-   The system does not run inbound email actions that would otherwise be triggered by the email.
-   The system truncates the Body text on the Email form.
-   The system logs a warning and sets the Error string field on the Email form. The log message for such an email might look like this: `Email set to receive-ignored because its size exceeds the value set in **glide.email.inbound.max\_body\_chars**.`

## Outbound email body processing

For outbound emails, the system enforces the maximum body size as set by the **glide.email.outbound.max\_body\_chars** property. When the body size exceeds the configured value:

-   The system does not send the email.
-   The system truncates the Body text on the Email form.
-   The system logs a warning and sets the Error string field on the Email form. The log message for such an email might look like this: `Email set to send-ignored because its size exceeds the value set in **glide.email.outbound.max\_body\_chars**. 1337 character(s) were truncated from the body field.`

**Parent Topic:**[Email size limits](../concept/c_EmailAttachmentLimits.md)

**Related topics**  


[Advanced email properties](../../reference-pages/reference/r_AdditionalProperties.md)

