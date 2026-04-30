---
title: Enable OAuth 2.0 for email
description: Setting up OAuth 2.0 for email requires you to obtain access and refresh tokens from your email provider.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [OAuth email authentication, Advanced email setup, Configure email administration, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Enable OAuth 2.0 for email

Setting up OAuth 2.0 for email requires you to obtain access and refresh tokens from your email provider.

## Before you begin

-   Role required: admin
-   Plugin required: Email - OAUTH support for IMAP and SMTP

## Procedure

1.  Log in to your third-party email account, such as Gmail, and enable OAuth 2.0.

2.  Obtain the following from your third-party email account:

    -   client ID
    -   client secret
    -   authorization URL
    -   token URL
    -   redirect URL
    -   token revocation URL
3.  Navigate to **System OAuth** &gt; **Application Registry**.

4.  Click **New**.

5.  Click **Connect to a third party OAuth Provider** to create an application registry record that email uses.

6.  Use the information you obtained from your third-party email account to fill in the fields on the form.

    See [Use a third-party OAuth provider](https://www.servicenow.com/docs/access?context=t_UseAThirdPartyOAuthProvider&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US) for instructions.

7.  Create the OAuth application registry record and its associated OAuth Entity Profile and OAuth Entity Scope records.

8.  Click **Submit**.

9.  Navigate to **System Mailboxes** &gt; **Administration** &gt; **Email Accounts**.

    **Note:** Port and Connection Security information is provided by the provider.

    The system displays the list of available email accounts.

10. If you do not want to receive email sent to the default instance email address, locate the record for **ServiceNow POP3** and change **Active** to **false**.

    The system can receive email from multiple POP3 and IMAP email accounts.

11. Locate the records for **ServiceNow SMTP** and change **Active** to **false**.

12. Click **New**.

13. Create an email account record for your OAuth 2.0 SMTP server where the **Type** is **SMTP**.

14. For **Authentication**, select **OAuth 2.0**.

15. For **OAuth Profile**, select the application registry record you created.

16. Click **Authorize Email Account Access** to obtain the access and refresh tokens.

    Another browser window opens asking you to authorize the account access on the third-party email account.

17. Authorize the access.

    After the authorization is successful and the tokens are saved to the instance, the **Authorize Email Account Access** button no longer appears on the Email Account form.

18. Click **New**.

19. Create an email account record for your OAuth 2.0 IMAP server where the **Type** is **IMAP**.

    Use the same **Authentication** and **OAuth profile** settings as the OAuth SMTP email account.


**Parent Topic:**[OAuth email authentication](../concept/c_OAuthEmailAuthentication.md)

