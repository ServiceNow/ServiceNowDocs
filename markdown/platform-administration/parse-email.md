---
title: Parse an email thread
description: When an email is received, parse the most recent message in an email thread by creating Email Reply Separators using specified string or regular expressions.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Email and SMS notifications, System notifications, Notifications, Configure core features, Administer]
---

# Parse an email thread

When an email is received, parse the most recent message in an email thread by creating **Email Reply Separators** using specified string or regular expressions.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Policy** &gt; **Email** &gt; **Email Reply Separators**.

    A list of email reply separators shows up.

2.  Click **New** to create a new email reply separator.

3.  On the **Email Reply Separator** form, fill in the fields.

<table id="table_vvk_jdc_3nb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the separator.

</td></tr><tr><td>

Application

</td><td>

Scope of the separator.

</td></tr><tr><td>

Active

</td><td>

Option to activate the separator.

</td></tr><tr><td>

Type

</td><td>

Type of separator.-   String: Searches for the specified string to parse out an email thread.
-   Regex: Searches for the specified regular expression to parse out an email thread.
 **Note:** Complex regular expressions may take time to evaluate the email thread. In such cases, the regular expression evaluation is timed out after 10 seconds and skipped for that regular expression and the email processing is continued.

</td></tr><tr><td>

Order

</td><td>

Priority of the separator.

</td></tr><tr><td>

Separator

</td><td>

Separator value based on the selection of the **Type**.

</td></tr><tr><td>

Short description

</td><td>

Description about the separator.

</td></tr><tr><td>

Language

</td><td>

Language of the reply separator.**Note:** All email clients don't indicate a language, so all active reply separators are applied to locate a separator in the email message.

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Email and SMS notifications](../concept/c_EmailNotifications.md)

**Related topics**  


[Create notification categories](create-notification-categories.md)

[Create an email notification](t_CreateANotification.md)

[Email notifications dashboard](../concept/email-notifications-dashboard.md)

[Email diagnostics dashboard](../concept/email-diagnostics-dashboard.md)

[Email templates](../concept/c_EmailTemplates.md)

[Email layouts](../concept/email-layouts.md)

[Email retention](../concept/email-retention.md)

[Watermarks on notification emails](../concept/c_WorkingWithWatermarks.md)

[Email digests](../concept/email-digests.md)

[Domain separation and Notifications](../concept/domain-separation-notifications.md)

[Email FAQs and troubleshooting notification emails](../concept/troubleshooting-notification-emails.md)

