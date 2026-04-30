---
title: Advanced email setup
description: With an advanced email setup, you can use your own SMTP server, POP3 server, or both.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Email Administration, Notifications, Configure core features, Administer]
---

# Advanced email setup

With an advanced email setup, you can use your own SMTP server, POP3 server, or both.

Setting up your own email environment can be useful if you want to use existing filtering, retention, or compliance aspects of your internal email architecture. You can set up email in several ways:

-   Use your own SMTP server to forward email to ServiceNow servers.
-   Use your own SMTP server to send email.
-   Use your own POP3 server to receive email.
-   Use your own SMTP and POP3 servers to send and receive email.
-   Use an OAuth 2.0-enabled SMTP server to send email from a third-party service.
-   Use an OAuth 2.0-enabled IMAP server to receive email from a third-party service.

The following procedures assume that you [enabled basic email properties](../task/t_ConfiguringStandardEmail.md).

-   **[Enable using your own SMTP server](../task/t_ConfAltEmailUsgOwnSMTP.md)**  
Enable using your own SMTP server so that you can leverage the existing filtering, retention, or compliance aspects of your own SMTP server while also using the ServiceNow POP3 server.
-   **[Enable using your own POP3 server](../task/t_ConfAltEmailConfPOP3Server.md)**  
You can use your own POP3 server to store and receive email for the instance.
-   **[Enable using your own SMTP and POP3 servers](../task/t_ConfAltEmailConfServers.md)**  
You can use your own SMTP and POP3 servers to send email from the instance and to store and receive email for the instance.
-   **[Email bounce management](../../notification/concept/email-bounce.md)**  
Help prevent sending emails to addresses that are known to generate bounces by monitoring and filtering them out while sending emails.
-   **[OAuth email authentication](../../notification/concept/c_OAuthEmailAuthentication.md)**  
OAuth enables your instance to receive and send email through a third-party email account.
-   **[System address filters](../../notification/concept/system-address-filters.md)**  
Prevent your system from communicating with untrusted domains and email addresses.
-   **[Reading email using Microsoft Graph](../../notification/concept/read-email-using-ms-graph.md)**  
Use Microsoft Graph endpoints to read emails from Microsoft Exchange Online.
-   **[Sending email using client credential flow](../../notification/concept/send-email-client-credential-flow.md)**  
Use the client credential flow to send emails from Microsoft Exchange Online.

**Parent Topic:**[Configure email administration](../../notification/concept/configuring-email-admin.md)

