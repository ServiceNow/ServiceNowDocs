---
title: Email diagnostics
description: The Diagnostics and Connection page provides information on the current state of your email configuration. This page includes status on email properties, scheduled jobs, and email account connections that affect how your instance receives and sends email.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Email FAQs and troubleshooting, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Email diagnostics

The Diagnostics and Connection page provides information on the current state of your email configuration. This page includes status on email properties, scheduled jobs, and email account connections that affect how your instance receives and sends email.

Email diagnostic information can help you identify problems with inbound or outbound email. The following video shows different steps to determine why your instance is not receiving inbound emails. One of the steps uses email diagnostics to check the email connection status and email reader scheduled job.

Navigate to the Diagnostics and Connection page from either of these modules:

-   **System Mailboxes** &gt; **Email Diagnostics**
-   **System Diagnostics** &gt; **Email Diagnostics**

![Diagnostics and Connection page that shows email receiving as non-operational](../../notification/image/EmailDiagnosticsPage.png "Email Diagnostics and Connection page")

For quick status on a field, point to the green check mark or red X icon. The check mark icon indicates that the item is operational or healthy, while the X icon indicates that the item is not operational or within the expected range.

<table id="table_z4v_pfy_bp"><thead><tr><th>

Diagnostic

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

**Email Sending is \[Status\]**

</td></tr><tr><td>

Email Sending

</td><td>

Status of outbound email as either **Enabled** or **Disabled**.To change the status, click the **Modify Email Sending/Receiving** related link, and in the Email Properties form, update the **Email sending enabled** property.

</td></tr><tr><td>

Email in Queue

</td><td>

Number of email messages that are ready to be sent.

</td></tr><tr><td>

Last Sent Mail

</td><td>

Date and time the last email message was sent.

</td></tr><tr><td>

SMTP Sender State

</td><td>

Current state of the SMTP Sender job, which sends email on a recurring schedule. By default, this job runs every minute.To update the SMTP Sender state, click the **SMTP Sender Job** related link, and in the Schedule table, open the SMTP Sender record to be changed.

</td></tr><tr><td>

SMTP Processing Time

</td><td>

Duration of the last SMTP Sender job run. This value should be shorter than the SMTP Sender interval.

</td></tr><tr><td>

SMTP Job Last Run

</td><td>

Date and time when the SMTP Sender job last ran.

</td></tr><tr><td>

Default SMTP Status

</td><td>

Indication of whether the SMTP connection was successful, shown only if the email accounts feature is active. Click **Default SMTP** to change your SMTP account settings.

</td></tr><tr><td>

SMS Sender State

</td><td>

Current state of the **SMS Sender** job, which sends SMS notifications on a recurring schedule. By default, this job runs every minute.To update the SMS Sender job, click the **SMS Sender Job** related link, and in the Schedule table, open the SMS sender record to be changed.

</td></tr><tr><td>

SMS Sender Processing Time

</td><td>

Duration of the last **SMS Sender** job run. This value should be shorter than the **SMS Sender** interval.

</td></tr><tr><td>

SMS Sender Job Last Run

</td><td>

Date and time when the **SMS Sender** job last ran.

</td></tr><tr><td class="sub-head" colspan="2">

**Email Receiving is \[Status\]**

</td></tr><tr><td>

Email Receiving

</td><td>

Status of inbound email as either **Enabled** or **Disabled**. To change the status for email receiving, click the **Modify Email Sending/Receiving** related link, and in the Email Properties form, update the **Email receiving enabled** property.

</td></tr><tr><td>

Last Received Email

</td><td>

Date and time the last email message was received.

</td></tr><tr><td>

Email Reader Status

</td><td>

Current state of the email reader job, which downloads any email waiting on the mail server and creates email.read events.To update the Email Reader Status job, click the **Email Reader Job** related link, and in the Schedule table, open the email reader record to be changed.

</td></tr><tr><td>

Email Reader Processing Time

</td><td>

Duration of the last reader job run. This value should be shorter than the reader interval.

</td></tr><tr><td>

Job Last Run

</td><td>

Date and time when the reader job last ran.

</td></tr><tr><td class="sub-head" colspan="2">

**Connection Status**

</td></tr><tr><td>

\{Accounts\}

</td><td>

The result of the test connection to the accounts. The connection is tested every time you load the page.

</td></tr></tbody>
</table>**Parent Topic:**[Email FAQs and troubleshooting notification emails](../../notification/concept/troubleshooting-notification-emails.md)

**Related topics**  


[Scheduled jobs](../concept/c_ScheduledJobs.md)

