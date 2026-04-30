---
title: OAuth 2.0 tutorial - create an OAuth provider and profile
description: Set up the Google service as an OAuth provider in ServiceNow by entering your client information, Google API URLs, and configuring the OAuth profile.
locale: en-US
release: xanadu
product: Web Services
classification: web-services
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Outbound REST with OAuth 2.0 profile tutorial - integrating with Google Contacts API, Configure a REST message with OAuth, Outbound REST authentication, Outbound REST web service, Outbound web services, Web services, API implementation, API implementation and reference]
---

# OAuth 2.0 tutorial - create an OAuth provider and profile

Set up the Google service as an OAuth provider in ServiceNow by entering your client information, Google API URLs, and configuring the OAuth profile.

## Before you begin

You must have configured the Google service as an OAuth provider and recorded your **Client ID** and **Client Secret** values.

Role required: oauth\_admin

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Click **New**.

3.  Select **Connect to a third party OAuth Provider**.

4.  Enter a **Name** for the OAuth provider.

    For this example, use `Google`.

5.  Enter the **Client ID** and **Client Secret** that you obtained from Google.

6.  Set the **Default Grant type** to **Authorization Code**.

7.  In the **Authorization URL** field, enter `https://accounts.google.com/o/oauth2/auth`.

8.  In the **Token URL** field, enter `https://www.googleapis.com/oauth2/v3/token`.

9.  In the **Redirect URL** field, enter `https://<instance>.service-now.com/oauth_redirect.do`.

    This URL must match the redirect URL provided to Google.

10. In the **Token Revocation URL** field, enter `https://accounts.google.com/o/oauth2/revoke`.

11. Right-click the form header and select **Save**.

    A new OAuth Entity Profile record is created.

12. In the **OAuth Entity Scopes** embedded list, add a new row with the **Name** and **OAuth scope** values set to `https://www.googleapis.com/auth/contacts.readonly`.

13. Right-click the form header and select **Save**.

14. In the **OAuth Entity Profiles** embedded list, select the automatically-created profile.

15. In the **OAuth Entity Profile Scopes** embedded list, add a new row and select the Google contacts API read-only scope.

16. Click **Update**.


**Parent Topic:**[Outbound REST with OAuth 2.0 profile tutorial - integrating with Google Contacts API](../concept/c_OAuth2ProfileTutorialGoogle.md)

**Previous topic:**[OAuth 2.0 tutorial - configure the Google service as an OAuth provider](t_OAuthDemoConfigureGoogle.md)

**Next topic:**[OAuth 2.0 tutorial - create a REST message](t_OAuthDemoCreateRESTMessage.md)

