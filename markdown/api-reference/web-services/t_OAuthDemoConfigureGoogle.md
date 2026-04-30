---
title: OAuth 2.0 tutorial - configure the Google service as an OAuth provider
description: Use the Google Developer Console to set up an OAuth 2.0 provider.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [OAuth 2.0 profile tutorial: integrating with Google Contacts, Configure a message with OAuth, Outbound REST authentication, REST, Outbound, Web services, API implementation, API implementation and reference]
---

# OAuth 2.0 tutorial - configure the Google service as an OAuth provider

Use the Google Developer Console to set up an OAuth 2.0 provider.

## Before you begin

This procedure is performed within the Google Developer Console. You must have a Google account to access this console.

Role required: None

## About this task

Configure the Google service in order to obtain a client ID and client secret, and specify your ServiceNow instance URL as the OAuth redirect URL.

**Note:** This information describes the state of the Google Developer Console and Contacts API as of July 22, 2015. Changes made after that date may not be included in this document.

## Procedure

1.  Navigate to the Google Developer Console \(`https://console.developers.google.com`\).

2.  Log in using your Google credentials.

3.  Click **Create a project**.

4.  Enter a **Project name**.

5.  Click **Create**.

    After Google creates the project, the project dashboard appears.

6.  Navigate to **APIs &amp; Services** &gt; **Enable APIs &amp; Services**.

7.  Click the **Enable APIs and Services** button.

8.  Enter Contacts API in the search bar.

9.  Click on **Contacts API** and then click **Enable API**.

10. Return to the **APIs &amp; Services** homepage from the hamburger menu and navigate to **APIs &amp; Services** &gt; **OAuth consent screen**.

11. Click **Configure consent screen** and complete the app registration wizard according to your business needs.

12. Navigate to **APIs &amp; Services** &gt; **Credentials** and click **Create Credentials** &gt; **Oauth client ID**.

13. Select **Web application** from the drop down.

14. Enter a descriptive OAuth 2.0 client in the **Name**.

    This name appears when you authorize the OAuth token in your instance.

15. In the **Create Client ID** window, add the OAuth redirect URI for your instance to the **Authorized redirect URIs** field.

    This URI follows the format `https://<instance>.service-now.com/oauth_redirect.do`

16. Click **Create**.

    The client ID information appears.

17. Record the **Client ID** and **Client secret** values.

    You use these values to configure the Google service as an OAuth provider in your instance.


**Parent Topic:**[Outbound REST with OAuth 2.0 profile tutorial - integrating with Google Contacts API](../concept/c_OAuth2ProfileTutorialGoogle.md)

**Previous topic:**[Outbound REST with OAuth 2.0 profile tutorial - integrating with Google Contacts API](../concept/c_OAuth2ProfileTutorialGoogle.md)

**Next topic:**[OAuth 2.0 tutorial - create an OAuth provider and profile](t_OAuthDemoCreateProvider.md)

