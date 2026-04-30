---
title: Email accounts
description: Email accounts store the connection details and credentials the system uses to access external email servers and services.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Creating an email account, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Email accounts

Email accounts store the connection details and credentials the system uses to access external email servers and services.

By default, instances come with email accounts for ServiceNow - managed SMTP and POP3 servers to send and receive email. These accounts cannot be modified, but can be deactivated if you do not want to use them. To connect to other email servers and services you must create email accounts for them. You can create email accounts for servers and services that use these protocols:

-   SMTP
-   POP3
-   IMAP

**Note:** The system only allows one SMTP email account to be active at a time and sends all email through this account. You can however receive email from multiple POP3 or IMAP accounts.

The system stores individual email accounts in the `sys_email_account` table. Create separate email accounts to send and receive email. Use [email properties](../../reference-pages/concept/c_EmailProperties.md) to define how the system processes email for all email accounts.

By default, the ServiceNow POP3 server provides each instance with its own mailbox at the address instance@service-now.com. Likewise, the ServiceNow SMTP server sends email from the address instance@service-now.com. To create another mailbox, provision your own POP3 or IMAP server and create an email account to the server on the instance. To change the sent from email address, update the address in the email account you use for sending email.

Emails received via a POP3 or IMAP server account are stored in the Email \[sys\_email\] table and then deleted from the account.

**Note:** ServiceNow has exclusive access to an account you configure. After a mail is read from a POP or IMAP account that you have configured, ServiceNow deletes the email from the server.

-   **[Create an email account](../task/t_ConfigureAnEmailAccount.md)**  
You can create email accounts in addition to the accounts provisioned for you.
-   **[Multiple email readers](email-account-groups.md)**  
Organize POP3/IMAP email accounts into email account groups \(subsets of email accounts\) that can be processed by multiple email reader jobs. To improve the performance of inbound email account processing, you can incrementally add email account groups and if needed, email reader jobs to process email account groups concurrently.

**Parent Topic:**[Creating an email account](using-email-admin.md)

