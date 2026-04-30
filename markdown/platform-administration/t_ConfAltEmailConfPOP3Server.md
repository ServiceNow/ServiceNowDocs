---
title: Enable using your own POP3 server
description: You can use your own POP3 server to store and receive email for the instance.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Advanced email setup, Configure, Email Administration, Notifications, Configure core features, Administer]
---

# Enable using your own POP3 server

You can use your own POP3 server to store and receive email for the instance.

## Before you begin

-   Role required: admin
-   Email server required: POP3
-   [Basic email properties:](t_ConfiguringStandardEmail.md) enabled

## Procedure

1.  On your POP3 server, create a mailbox for your instance that has a custom email address. For example, create a mailbox for `service-desk@company.com`.

2.  Navigate to **System Mailboxes** &gt; **Administration** &gt; **Email Accounts**.

    The system displays the list of available email accounts.

3.  If you do not want to receive, email sent to the instance@service-now.com mailbox, locate the record for **ServiceNow POP3** and change **Active** to **false**.

    An instance can receive email from multiple POP3 accounts at the same time. Leaving the **ServiceNow POP3** account active permits the instance to receive email sent to the default email address.

4.  Click **New**.

    The system displays an empty email Account form.

5.  Create an email account record for your POP3 server where the **Type** is **POP3**.

6.  On the form, fill in the fields.

<table id="table_lwc_lrn_5sb"><thead><tr><th>

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
</table>7.  From **Related Links**, click **Test Connection**.

    If the email account is valid, the system returns a success message.

    ![Example successful Completion code status for testing POP3 connection](../../notification/image/test-pop3-connection.png)


## Example

![Flow diagram that shows the steps that show how email is received on your POP3 server](../image/AlternateEmailConfigurationUsingYourOwnPOP3Server.png "Receiving email using your own POP3 server")

**Parent Topic:**[Advanced email setup](../concept/c_AlternateEmailConfigurations.md)

