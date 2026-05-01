---
title: Email image filtering properties
description: Use email image filtering properties to control how inbound email images attach to a target record.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-05-01"
reading_time_minutes: 2
breadcrumb: [Email properties, Configure, Email Administration, Notifications, Configure core features, Administer]
---

# Email image filtering properties

Use email image filtering properties to control how inbound email images attach to a target record.

When a user sends an email to the system, email images \(such as logos or email signatures\) attach to the target record by default. These images are also visible in the activity stream of the target record. The system then replicates these images, which can cause duplicate image attachments to the target record and also duplicate images in the activity stream.

To filter images from emails and reduce duplicate image attachments to target records, configure the following properties in the System Properties \[sys\_properties\] table. Use these properties to:

-   Specify the email image sizes eligible for filtering.
-   Choose an action that controls image attachment behavior and image visibility in the activity stream.

**Note:** These properties do not delete attachments. You can verify attachment records in the Attachments \[sys\_attachment\] table.

<table id="table_e2y_y43_mz"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**glide.email.inbound.image\_sys\_attachment.filter.minimum\_bytes**

</td><td>

Sets the minimum image size in bytes for inbound email images to attach to the target record. Any image that is below this size limit is subject to the image filtering behavior that you set in the **glide.email.inbound.image\_sys\_attachment.filter.action** property. To disable image filtering entirely and attach all email images to the target record, set the minimum byte size to `0`.-   Type: Integer
-   Default value: 0

</td></tr><tr><td>

**glide.email.inbound.image\_sys\_attachment.filter.action**

</td><td>

Specifies the image filtering behavior. **Note:** Regardless of the action you select, the image is visible when you choose to **Preview HTML Email** or **Show Email Details** in the activity formatter.

 -   Type: Choice list
    -   AttachTarget - Associate the image to the target record. The image is visible in the activity formatter and in the attachment to the target record.
    -   AttachEmail - Attach the image to the email record. The image is not visible in the activity formatter of the target record nor in the attachment to the target record.
    -   AttachNone - Do not attach the image to a record. You can select this option to attach the image manually at a later time.
-   Default value: AttachEmail

</td></tr></tbody>
</table>**Parent Topic:**[Email properties](../../reference-pages/concept/c_EmailProperties.md)

**Related topics**  


[Outbound email configuration](../../reference-pages/reference/r_OutboundMailConfiguration.md)

[Inbound email configuration](../../reference-pages/reference/r_InboundMailConfiguration.md)

[Email digest properties](email-digest-properties.md)

[Advanced email properties](../../reference-pages/reference/r_AdditionalProperties.md)

[Add a system property](../../reference-pages/reference/r_AvailableSystemProperties.md#)

