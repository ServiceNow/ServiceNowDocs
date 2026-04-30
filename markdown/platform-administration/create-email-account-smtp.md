---
title: Create an email account with SMTP OAuth2.0
description: Create an email account from Microsoft Exchange Online with SMTP OAuth2.0.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Send email using client credential flow, Advanced email setup, Configure email administration, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Create an email account with SMTP OAuth2.0

Create an email account from Microsoft Exchange Online with SMTP OAuth2.0.

## Before you begin

Role required: email\_account\_admin

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

SMTP

</td></tr><tr><td>

Authentication

</td><td>

Select **OAUTH 2.0**.Type of authentication used for the email account to connect to the email server.

</td></tr><tr><td>

Server

</td><td>

Server used for creating the email accounts.

</td></tr><tr><td>

Email user label

</td><td>

Display value used for outgoing messages. This field is for SMTP type accounts only.

</td></tr><tr><td>

User name

</td><td>

User name or ID to authenticate an email address. The value in this field is also the **From** address when the instance sends an email. If you're using SMTP, the value must be a full email address. The value in the **From** field can override this field for SMTP accounts.

</td></tr><tr><td>

From

</td><td>

The From email address used for notifications sent with this account. This address takes precedence over the **User name** field. If nothing is present in this field, the User name is used as the return address for notifications sent from the instance. **Note:** This value is for SMTP only.

</td></tr><tr><td>

OAuth Profile

</td><td>

OAuth profile configured during application registry.

</td></tr><tr><td>

Connection Security

</td><td>

If your email server supports TLS, an insecure connection is upgraded to a secure connection using the SSL/TLS encryption protocol.

</td></tr><tr><td>

Port

</td><td>

Connection TCP port.

</td></tr><tr><td>

Active

</td><td>

Option to activate the email account.

</td></tr><tr><td>

ServiceNow Configured

</td><td>

Identifier of whether this account is provisioned by ServiceNow. If you create an account, this option isn't selected.

</td></tr><tr><td>

Enable debug output

</td><td>

Option to create node logs for the raw data that is exchanged with the email server.

 You can enable this field temporarily to diagnose issues related to receiving or sending email.

</td></tr></tbody>
</table>4.  Select **Submit**.

5.  Test the connection by selecting the **Test Connection** link.


**Parent Topic:**[Send email using client credential flow](../concept/send-email-client-credential-flow.md)

