---
title: Outbound email
description: Use outbound email accounts to send emails.
locale: en-US
release: australia
topic_type: reference
last_updated: "2025-12-05"
reading_time_minutes: 2
breadcrumb: [Platform module configuration, Configure, Now Assist for Setup, Get started, Administer the ServiceNow AI Platform]
---

# Outbound email

Use outbound email accounts to send emails.

## Accounts

Use Accounts to process the outbound emails. On selecting Accounts under Outbound email, a list of existing accounts shows up. Select **Add an account** to create a new account.

![Image showing outbound accounts](../image/ia-outbound-accounts.png)

<table id="table_scf_btj_nhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the account

</td></tr><tr><td>

Type

</td><td>

States the type of account. It can either be POP3 or IMAP.

</td></tr><tr><td>

Authentication

</td><td>

States the authentication method of the account**Note:** Authentication is a mandatory field

</td></tr><tr><td>

Server

</td><td>

Remote server to which this account connects. To activate a server for an on-premises installation, enter the full address \(FQDN\) of the node \(for example, `node.customerdomain`\).**Note:** Server is a mandatory field

</td></tr><tr><td>

Username

</td><td>

Username used to create the account**Note:** Username is a mandatory field

</td></tr><tr><td>

Password

</td><td>

Password used to set up the account**Note:** Password is a mandatory field

</td></tr><tr><td>

Connection Security

</td><td>

Type of secure connection. Choose a setting:-   None: No secure protocol is used.
-   STARTTLS: Upgrades an insecure connection to a secure connection using the SSL/TLS encryption protocol, if your email server supports TLS.
-   SSL/TLS: Connect to an SSL/TLS encrypted port to secure the connection. Email is encrypted between the ServiceNow instance and your mail server.

**Warning:**

Selecting a less secure protocol like STARTTLS or None may expose your data. To better ensure the security of data in your email server, select SSL/TLS.


</td></tr><tr><td>

Port

</td><td>

Connection TCP port.

</td></tr><tr><td>

Active

</td><td>

Optional checkbox to create an active account

</td></tr><tr><td>

Enable Debug Logging

</td><td>

Option to create node logs for the raw data that is exchanged with the email server. You can review the node logs by navigating to **System Logs** &gt; **Utilities** &gt; **Node Log File Browser**.

</td></tr></tbody>
</table>Select **Export** to export the accounts on to an Excel, CSV, JSON or PDF. You can then select the delivery type either through download or email.

## Properties

Manage the behavior of outgoing emails with Properties.

![Image showing outbound properties](../image/ia-outbound-properties.png)

-   Outbound sending and delivery options: You can either enable or disable the following options:
    -   Enable sending emails
    -   Include timezone in the email
    -   Include visible watermark in the outbound emails
    -   Retry sending email on unknown SMTP error codes
    -   Enable internationalization of email address
-   Outbound debugging and access: You can configure the following:
    -   Email address to be used to send all test emails
    -   Number of journal entries to be included in email notifications
    -   Roles that can view email in the Activity formatter

**Note:** Select **Save** to save the recent property settings. You can also undo the most recent change by selecting **Undo**. By selecting **Undo**, the values are reverted back to the most recent saved values.

See [Outbound email configuration](../../reference-pages/reference/r_OutboundMailConfiguration.md) for more information.

**Parent Topic:**[Platform module configuration in Now Assist for Setup](ia-config-platform-il.md)

