---
title: Attachment limit properties
description: Several properties control email attachment limits.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Email size limits, Reference, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Attachment limit properties

Several properties control email attachment limits.

To see the status of all email attachments, go to the Email Attachments \[sys\_email\_attachment\] table.

## Properties

All the properties are located in the System Property \[sys\_properties\] table. Setting any of the following properties to an excessively large value may cause performance issues.

<table id="table_lft_wmt_gr"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**glide.email.inbound.max\_attachment\_count**

</td><td>

Sets the maximum number of attachments allowed per inbound email.-   Type: integer
-   Default value: 30
-   Learn more: Inbound Email Attachment Processing

</td></tr><tr><td>

**glide.email.inbound.max\_total\_attachment\_size\_bytes**

</td><td>

Sets the maximum total attachment size in bytes allowed per inbound email.-   Type: integer
-   Default value: 18874368
-   Learn more: Inbound Email Attachment Processing

</td></tr><tr><td>

**glide.email.outbound.max\_attachment\_count**

</td><td>

Sets the maximum number of attachments allowed per outbound email.-   Type: integer
-   Default value: 30
-   Learn more: Outbound Email Attachment Processing

</td></tr><tr><td>

**glide.email.outbound.max\_total\_attachment\_size\_bytes**

</td><td>

Sets the maximum total attachment size in bytes allowed per outbound email. To send an email, the system must encode the contents of the email. This process may significantly increase the size of the email, including any attachments. It is best to set this property to a value well below the maximum email size.-   Type: integer
-   Default value: 18874368
-   Learn more: Outbound Email Attachment Processing

</td></tr></tbody>
</table>**Note:** A different property, **com.glide.attachment.max\_size**, sets the maximum file size allowed for any attachment in the system and overrides any larger values of **glide.email.inbound.max\_total\_attachment\_size\_bytes** and **glide.email.outbound.max\_total\_attachment\_size\_bytes**.

## Inbound email attachment processing

For inbound emails, the system enforces the maximum number and size of attachments as set by the **glide.email.inbound.max\_attachment\_count** and **glide.email.inbound.max\_total\_attachment\_size\_bytes** properties. When an attachment for an inbound email exceeds either value, the attachment is discarded. A record is created in the Email Attachments \[sys\_email\_attachment\] table containing the discarded file name and the reason it was discarded. The discarded file remains in the Email \[sys\_email\] record. The order in which the system processes the attachments determines which attachments are discarded. This order may not be consistent from email to email.

When an inbound email attachment is discarded, the system also fires the **inbound.email\_attachments.discarded** event. You can use the event to trigger a notification that alerts the email sender. For an example of a notification that can be triggered by the event, see the inactive "Demo Email Attachment\(s\) Discarded" notification.

Inbound email attachments are prevented from attaching to the target record if an identical attachment exists.

## Outbound email attachment processing

For outbound emails, the system enforces the maximum number and size of attachments as set by the **glide.email.outbound.max\_attachment\_count** and **glide.email.outbound.max\_total\_attachment\_size\_bytes** properties. Email records are created from various sources and may exceed the configured attachment limits.

Emails that are ready to be sent from the Email \[sys\_email\] table are subject to the outbound attachment limits. Emails that exceed either limit trigger a warning in the email system log and are sent with attachments up to the maximum number or total file size.

The log message for such an email might look like this: `Maximum combined attachment size exceeded. (max:15728640 bytes). One or more attachment records ignored.`

## Emails for notifications, scheduled reports, and exported tables

Notifications can be set to include all the attachments from the record that triggers the notification. If the attachments exceed either of the outbound email attachment limits, the system excludes the excess attachments from the email and logs a warning message.

Reports can be scheduled for email distribution as attachments. Large reports may exceed the outbound attachment size limit. In this case, the system sends the scheduled report email without the report attached and logs a warning message. To avoid the issue, send links to large reports instead of sending the reports as attachments.

If a user attempts to export numerous records from a list that exceeds a configured warning threshold, a dialog box offers the option to email the exported records as an attachment. If the attachment exceeds the outbound attachment size limit, the system sends the email without the exported record list attached and logs a warning message.

**Parent Topic:**[Email size limits](../concept/c_EmailAttachmentLimits.md)

