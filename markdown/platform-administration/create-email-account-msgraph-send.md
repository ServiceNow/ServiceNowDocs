---
title: Create an email account for Microsoft Graph \(send\)
description: Create an email account for sending emails from Microsoft Exchange Online using Microsoft Graph Endpoints.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Send email using Microsoft Graph, Read or send emails using Microsoft Graph, Advanced email setup, Configure, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Create an email account for Microsoft Graph \(send\)

Create an email account for sending emails from Microsoft Exchange Online using Microsoft Graph Endpoints.

## Before you begin

Role required: admin

## About this task

Antispam and malware scanning are managed by Microsoft Graph account and not ServiceNow

## Procedure

1.  Navigate to **All** &gt; **System Mailboxes** &gt; **Administration** &gt; **Email Accounts**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_tpm_kwl_x4"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the email account.

</td></tr><tr><td>

Type

</td><td>

Microsoft Graph \(Send\)

</td></tr><tr><td>

Authentication

</td><td>

OAUTH 2.0 - Type of authentication used for the email account to connect to the email server.

</td></tr><tr><td>

Email user label

</td><td>

Name of the sender.

</td></tr><tr><td>

OAuth Profile

</td><td>

OAuth profile configured during application registry.

</td></tr><tr><td>

Active

</td><td>

Option to activate the email account.

</td></tr><tr><td>

Enable debug output

</td><td>

Option to create node logs for the raw data that is exchanged with the email server.

 You can enable this field temporarily to diagnose issues related to receiving or sending email.

</td></tr></tbody>
</table>4.  Select **Submit**.

5.  Select the test connection link at the bottom to test the account.


**Parent Topic:**[Sending email using Microsoft Graph](../concept/send-email-using-ms-graph.md)

