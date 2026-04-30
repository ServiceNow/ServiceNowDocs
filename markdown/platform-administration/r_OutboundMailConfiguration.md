---
title: Outbound mail configuration
description: The Outbound Mail Configuration section of the Email Properties page contains properties for sending email.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Email properties, Configure email administration, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Outbound mail configuration

The **Outbound Mail Configuration** section of the Email Properties page contains properties for sending email.

![](../../notification/image/outbound_email_configuration.png "Outbound email configuration")

<table id="table_otj_3ly_bp"><thead><tr><th>

Property

</th><th>

Label

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**glide.email.smtp.active**

</td><td>

Email sending enabled

</td><td>

Specifies whether to enable or disable the outgoing mail server.-   Type: true \| false
-   Default value: true

</td></tr><tr><td>

**glide.email.test.user**

</td><td>

Send all email to this test email address \(non-production testing\)

</td><td>

Specifies the comma-separated list of email addresses to which the instance sends all email messages. Typically used in non-production instances for testing purposes.-   Type: string
-   Default value: none

</td></tr><tr><td>

**glide.email.append.timezone**

</td><td>

Append time zone to dates and times in sent mail

</td><td>

Specifies whether to append the system time zone to date and date/time values in outbound emails. For example, 2010-07-02 04:01:14 PST.-   Type: true \| false
-   Default value: true

</td></tr><tr><td>

**glide.email.watermark.visible**

</td><td>

Create visible watermark in sent mail. If false, create invisible watermark via hidden div tag.

</td><td>

Indicates whether the watermark in email notifications is visible \(true\) or wrapped in a hidden div tag \(false\).-   Type: true \| false
-   Default value: false

</td></tr><tr><td>

**glide.smtp.defer\_retry\_ids**

</td><td>

Resend email if server returns these SMTP error codes

</td><td>

Specifies the comma-separated list of SMTP error codes that force the instance to resend email.-   Type: string
-   Default value: 421,450,451,452

</td></tr><tr><td>

**glide.smtp.fail\_message\_ids**

</td><td>

Do not resend email if server returns these SMTP error codes

</td><td>

Specifies the comma-separated list of SMTP error codes that prevent the instance from resending email.-   Type: string
-   Default value: 500,501,502,503,504,550,551,552,553,554

</td></tr><tr><td>

**glide.smtp.default\_retry**

</td><td>

Resend email when server returns unknown SMTP error codes.

</td><td>

Enables \(true\) or disables \(false\) resending email when an unknown SMTP error code is encountered. The instance only recognizes the SMTP error codes defined in the **glide.smtp.defer\_retry\_ids** property.-   Type: true \| false
-   Default value: true

</td></tr><tr><td>

**glide.ui.activity.email\_roles**

</td><td>

Roles that can view email in the Activity formatter when including "Sent/Received Emails"

</td><td>

Specifies the comma-separated list of roles that can view email in the activity formatter.-   Type: string
-   Default value: itil

</td></tr><tr><td>

**glide.email.journal.lines**

</td><td>

Number of journal entries \(Additional comments, Work notes, etc.\) included in email notifications \(-1 means all\).

</td><td>

Specifies the number of entries from a journal field, such as Additional comments or Work notes, included in email notifications. A value of -1 includes all journal entries.-   Type: integer
-   Default value: 3
-   Learn More:Restrict the Number of Entries Sent in a Notification

</td></tr></tbody>
</table>**Parent Topic:**[Email properties](../concept/c_EmailProperties.md)

**Related topics**  


[Inbound mail configuration](r_InboundMailConfiguration.md)

[Email image filtering properties](../../notification/concept/email-image-filters.md)

[Email digest properties](../../notification/concept/email-digest-properties.md)

[Advanced email properties](r_AdditionalProperties.md)

