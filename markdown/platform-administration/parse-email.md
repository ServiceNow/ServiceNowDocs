---
title: Parse an email thread
description: When an email is received, parse the most recent message in an email thread by creating Email Reply Separators using specified string or regular expressions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/parse-email.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
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


**Parent Topic:**[Email and SMS notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_EmailNotifications.md)

**Related topics**  


[Create notification categories]()

[Create an email notification]()

[Email notifications dashboard]()

[Email diagnostics dashboard]()

[Email templates]()

[Email layouts]()

[Email retention]()

[Watermarks on notification emails]()

[Email digests]()

[Domain separation and Notifications]()

[Email FAQs and troubleshooting notification emails]()

