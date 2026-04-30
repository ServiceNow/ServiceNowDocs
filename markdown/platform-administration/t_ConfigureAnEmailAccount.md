---
title: Create an email account
description: You can create email accounts in addition to the accounts provisioned for you.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Email accounts, Creating an email account, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Create an email account

You can create email accounts in addition to the accounts provisioned for you.

## Before you begin

-   Role required: admin
-   Email server: a compatible email server
    -   SMTP
    -   POP3
    -   IMAP

**Warning:** An SMTP server that uses a localhost or loopback \(127.0.0.1\) IP address is not accepted as a compatible email server. For more information, see [KB0724199](https://support.servicenow.com/kb_view.do?sysparm_article=KB0724199).

## Procedure

1.  Navigate to **All** &gt; **System Mailboxes** &gt; **Administration** &gt; **Email Accounts**, and then select **New**.

2.  On the form, fill in the fields.

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

Type of mail server. You can select one of the following:-   POP3
-   IMAP
-   SMTP
 **Note:** The system can use only one active SMTP account at a time.

</td></tr><tr><td>

Authentication

</td><td>

Type of authentication used for the email account to connect to the email server. You can select one of the following:-   –- None --
-   Password
-   OAUTH
-   OAUTH 2.0
The Email: OAUTH support for IMAP, Microsoft Graph \(Receiving\), and SMTP \(com.glide.email.oauth\) plugin must be active for the OAuth options to be visible.

</td></tr><tr><td>

OAuth Provider

</td><td>

OAuth application registry record for this account.

 This field appears if you selected **OAuth 2.0**.

</td></tr><tr><td>

Server

</td><td>

Remote server to which this account connects. To activate a server for an on-premise installation, enter the full address \(FQDN\) of the node \(for example, `node.customerdomain`\).

</td></tr><tr><td>

Active

</td><td>

Option to activate the email account.

</td></tr><tr><td>

ServiceNow Configured

</td><td>

Identifier of whether this account is provisioned by ServiceNow. If you create an account, this option is not selected.

</td></tr><tr><td>

Enable debug output

</td><td>

Option to create node logs for the raw data that is exchanged with the email server. You can review the node logs by navigating to **System Logs** &gt; **Utilities** &gt; **Node Log File Browser**.

 You can enable this field temporarily to diagnose issues related to receiving or sending email.

</td></tr><tr><td>

Email user label

</td><td>

Display value used for outgoing messages. This field is for SMTP type accounts only.

</td></tr><tr><td>

User name

</td><td>

User name or ID to authenticate an email address. The value in this field is also the **From** address when the instance sends email. If you are using SMTP, this must be a full email address. The value in the **From** field can override this \(for SMTP accounts\).**Note:** The address in the **From** field on the Notification \[sysevent\_email\_action\] form takes precedence over this field.

</td></tr><tr><td>

Password

</td><td>

Password when the **Authentication** type is **Password**.**Note:** You may need to increase the size of this field to accommodate longer passwords. By default, this field has a size of 40 characters.

</td></tr><tr><td>

From

</td><td>

\(SMTP only\) The From address used for notifications sent with this account. This address takes precedence over the **User name** field. If nothing is present in this field, the User name is used as the return address for notifications sent from the instance.

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

 For more information, see [System address filters](../concept/system-address-filters.md).

</td></tr></tbody>
</table>3.  Select **Submit**.

4.  Select the test connection link at the bottom to test the SMTP, POP3, or IMAP account.

    The system displays a pop-up window with the results of the connection test.

    ![Connection Test pop-up window displaying the results connection successful.](../image/connection-successful.png)

    If the test succeeds, select **Close** to return to the email account record. If the test fails, select **View Logs** to display more information about the test results.


## Result

The system uses the email account to send or receive email.

## What to do next

Enable the system to send or receive email.

**Parent Topic:**[Email accounts](../concept/c_EmailAccounts.md)

