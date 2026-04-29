---
title: OAuth email authentication
description: OAuth enables your instance to receive and send email through a third-party email account.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Advanced email setup, Configure, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# OAuth email authentication

OAuth enables your instance to receive and send email through a third-party email account.

Open Authentication \(OAuth\) is an open standard for authorization that provides administrators with an authorization method when connecting to incoming IMAP and outgoing SMTP servers. OAuth enables an instance to receive and send email from a third-party account, such as Gmail, without having to enter the credentials for that account.

The OAuth 2.0 implementation requires you to obtain an access and refresh token from your third-party email provider for each third-party email account. The tokens are automatically saved to the instance database. They provide authorization for all email communication between the instance and the authorized third-party account. A scheduled job regularly checks to see if email access tokens are valid. If the access token is not valid, but the refresh token is, the instance automatically regenerates a new access token.

OAuth 2.0 support is available starting with the Geneva release. The OAuth implementation supports IMAP and SMTP accounts only. POP3 is not supported. OAuth 1.0 is no longer supported.

**Note:** Customer email accounts configured to use OAuth 1.0 authentication with Gmail cease to function as of April 20, 2015. See [KB0546976](https://support.servicenow.com/kb_view.do?sysparm_article=KB0546976) for more information.

Activating the Email - OAuth support for IMAP and SMTP plugin allows you to use OAuth with email. If you upgrade to Geneva or later instances and are already using OAuth 1.0, activate the plugin again.

**Note:** For configuring SMTP and IMAP email accounts with Microsoft Office 365 using OAuth 2.0, see [KB0816072](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sysparm_article%3DKB0816072).

See [Outbound REST with OAuth 2.0 profile tutorial - integrating with Google Contacts API](https://www.servicenow.com/docs/access?context=c_OAuth2ProfileTutorialGoogle&version=australia&pubname=australia-api-reference&ft:locale=en-US) for an example of using an OAuth 2.0 profile to authenticate an outbound REST message with Google to retrieve contact information. Also see [OAuth 2.0](https://www.servicenow.com/docs/access?context=c_OAuthApplications&version=australia&pubname=australia-platform-security&ft:locale=en-US) for more information on OAuth 2.0 support in the instance.

-   **[Activate OAuth email authentication](../task/t_ActOAuthEmailAuthPlugin.md)**  
You can activate the Email:OAUTH support for IMAP, Microsoft Graph \(Receiving\), and SMTP plugin \(com.glide.email.oauth\) for Notifications if you have the admin role.
-   **[Enable OAuth 2.0 for email](../task/t_SetUpOAuth2ForEmail.md)**  
Setting up OAuth 2.0 for email requires you to obtain access and refresh tokens from your email provider.

**Parent Topic:**[Advanced email setup](../../reference-pages/concept/c_AlternateEmailConfigurations.md)

