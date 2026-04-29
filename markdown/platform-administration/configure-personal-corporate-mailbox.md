---
title: Configure templates for personal corporate mailboxes
description: Configure personal corporate mailboxes in the ServiceNow platform to enable users and agents to send and receive emails.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Personal corporate mailbox, Advanced email setup, Configure, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure templates for personal corporate mailboxes

Configure personal corporate mailboxes in the ServiceNow platform to enable users and agents to send and receive emails.

## Before you begin

The email account should be created and connected. For more information, see [Create an email account](t_ConfigureAnEmailAccount.md).

The User Mailbox Integration \(com.glide.email.user\_mailbox.integration\) plugin must be installed.

Role required: admin

## Procedure

1.  Create an email client template.

    To configure an email client template, see [Create an email client template](t_CreateAnEmailClientTemplate.md#).

    1.  On the **Sender Configuration** tab, for the **From Generation Type** select **User Email Addresses**.

    2.  To include shared email address, select the **Include Shared Email Address** check box.

    3.  Select **Submit**.

2.  [Apply an email client template](t_CreateAnEmailClientTemplate.md#).

3.  Navigate to **All** &gt; **User Mailboxes** &gt; **Administration** &gt; **Server Configuration**.

4.  Select **New**.

5.  On the form, fill in the fields.

<table id="table_pkj_z3t_m3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Name**

</td><td>

Name of the email account.

</td></tr><tr><td>

**Server**

</td><td>

Remote server to which this account connects.

</td></tr><tr><td>

**Type**

</td><td>

Type of mail server. Select **SMTP**.**Note:** The system can use only one active SMTP account at a time.

</td></tr><tr><td>

**Port**

</td><td>

Connection TCP port.

</td></tr><tr><td>

**Connection Security**

</td><td>

Type of secure connection. Choose a setting:-   **None**

No secure protocol is used.

-   **__STARTTLS__**

Upgrades an insecure connection to a secure connection using the SSL/TLS encryption protocol, if your email server supports TLS.

-   **__SSL/TLS__**

Connect to an SSL/TLS encrypted port to secure the connection. Email is encrypted between the ServiceNow instance and your mail server.

**Warning:** Selecting a less secure protocol like **STARTTLS** or **None** may expose your data. To better ensure the security of data in your email server, select **SSL/TLS**.

</td></tr></tbody>
</table>6.  Select **Submit**.

7.  Navigate to **All** &gt; **User Mailboxes** &gt; **Administration** &gt; **Template Configuration**.

8.  Select **New**.

9.  On the form, fill in the fields.

<table id="table_yh3_44t_m3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Name**

</td><td>

Name of the email account.

</td></tr><tr><td>

**Authentication Type**

</td><td>

Type of authentication used for the email account to connect to the email server. You can select one of the following:-   –- None --
-   Password
-   OAUTH
-   OAUTH 2.0
The Email: OAUTH support for IMAP, Microsoft Graph \(Receiving\), and SMTP \(com.glide.email.oauth\) plugin must be active for the OAuth options to be visible.

</td></tr><tr><td>

**Mail Server**

</td><td>

Remote server to which this account connects.

</td></tr><tr><td>

**OAuth profile**

</td><td>

OAuth application registry record for this account.

 This field appears if you select **OAuth 2.0** as the authentication type.

</td></tr><tr><td>

**Domain**

</td><td>

Enter a domain name to identify your email service \(for example gmail.com\).

</td></tr></tbody>
</table>10. Select **Submit**.


**Parent Topic:**[Personal corporate mailbox](../concept/personal-corporate-mailbox.md)

