---
title: Enable using your own SMTP and POP3 servers
description: You can use your own SMTP and POP3 servers to send email from the instance and to store and receive email for the instance.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Advanced email setup, Configure email administration, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Enable using your own SMTP and POP3 servers

You can use your own SMTP and POP3 servers to send email from the instance and to store and receive email for the instance.

## Before you begin

-   Role required: admin
-   Email servers required:
    -   SMTP
    -   POP3
-   [Basic email properties:](t_ConfiguringStandardEmail.md) enabled

## Procedure

1.  On your POP3 server, create a mailbox for your instance.

    For example, create a mailbox for `service-desk@company.com`.

2.  Navigate to **System Mailboxes** &gt; **Administration** &gt; **Email Accounts**.

    The system displays the list of available email accounts.

3.  Locate the record for **ServiceNow SMTP** and change **Active** to **false**.

4.  If you do not want to receive email sent to the instance@service-now.com mailbox, locate the record for **ServiceNow POP3** and change **Active** to **false**.

    An instance can receive email from multiple POP3 accounts at the same time. Leaving the**ServiceNow POP3** account active means that the instance receives email sent to its default email address.

5.  Click **New**.

    The system displays a blank Email Account form.

6.  Create an email account record for your SMTP server where the **Type** is **SMTP**.

7.  On the form, fill in the fields.

<table id="table_k3r_tlt_rsb"><thead><tr><th>

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

Type of mail server.

</td></tr><tr><td>

Authentication

</td><td>

Type of authentication used for the email account to connect to the email server. You can select one of the following:-   –- None --
-   Password
-   OAUTH
-   OAUTH 2.0


</td></tr><tr><td>

Server

</td><td>

Remote server to which this account connects. To activate a server for an on-premise installation, enter the full address \(FQDN\) of the node \(for example, `node.customerdomain`\).

</td></tr><tr><td>

User Name

</td><td>

Username or ID to authenticate an email address.

</td></tr><tr><td>

Password

</td><td>

Password when the **Authentication** type is **Password**.

</td></tr><tr><td>

Connection Security

</td><td>

Type of secure connection. Choose a setting:-   **__None__**

No secure protocol is used.

-   **__STARTTLS__**

Upgrades an insecure connection to a secure connection using the SSL/TLS encryption protocol, if your email server supports TLS.

-   **__SSL/TLS__**

Connect to an SSL/TLS encrypted port to secure the connection. Email is encrypted between the ServiceNow instance and your mail server.

 **Warning:** Selecting a less secure protocol like **STARTTLS** or **None** may expose your data. To better ensure the security of data in your email server, select **SSL/TLS**.

</td></tr><tr><td>

Port

</td><td>

Connection TCP port.

</td></tr><tr><td>

System Address Filter

</td><td>

System address filter to apply to the email account. If left blank, the system uses the default system address filter for inbound or outbound email.

 For more information, see [System address filters](../../notification/concept/system-address-filters.md).

</td></tr><tr><td>

Active

</td><td>

Option to activate the email account.

</td></tr><tr><td>

ServiceNow Configured

</td><td>

Identifier of whether this account is provisioned by ServiceNow. If you create an account, this option is not selected.

</td></tr><tr><td>

Enable Debug Logging

</td><td>

Option to create node logs for the raw data that is exchanged with the email server. You can review the node logs by navigating to **System Logs** &gt; **Utilities** &gt; **Node Log File Browser**.

 You can enable this field temporarily to diagnose issues related to receiving or sending email.

</td></tr></tbody>
</table>8.  From **Related Links**, click **Test Connection**.

    If the email account is valid, the system returns a success message.

    ![Test SMTP connection](../../notification/image/test-smtp-connection.png)

9.  Click **New**.

    The system displays a blank Email Account form.

10. Create an email account record for your POP3 server where the **Type** is **POP3**.

11. From **Related Links**, click **Test Connection**.

    If the email account is valid, the system returns a success message.

    ![Test POP3 connection](../../notification/image/test-pop3-connection.png)


## Example

![Using your own SMTP and POP3 servers](../image/AlternateEmailConfigurationUsingYourOwnSMTPAndPOP3Servers.png "Using your own SMTP and POP3 servers")

**Parent Topic:**[Advanced email setup](../concept/c_AlternateEmailConfigurations.md)

