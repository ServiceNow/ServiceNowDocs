---
title: OAuth 2.0 tutorial - create a REST message
description: Create a REST message and associated HTTP method to contact the Google service using the OAuth 2.0 profile.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [OAuth 2.0 profile tutorial: integrating with Google Contacts, Configure a message with OAuth, Outbound REST authentication, REST, Outbound, Web services, API implementation, API implementation and reference]
---

# OAuth 2.0 tutorial - create a REST message

Create a REST message and associated HTTP method to contact the Google service using the OAuth 2.0 profile.

## Before you begin

Role required: web\_service\_admin and oauth\_admin

You must have configured an OAuth provider and profile using the Google API information and your OAuth credentials.

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **REST Message**.

2.  Click **New**.

3.  Enter a descriptive **Name**.

4.  In the **Endpoint** field, enter `https://www.google.com/m8/feeds/contacts/default/full`.

    By using default instead of a specific username, the Google API uses the OAuth credentials to determine which account to get information from.

5.  In the **Authentication** tab, set the **Authentication type** to **OAuth 2.0**.

6.  In the **OAuth profile** field, select the Google contacts OAuth profile.

7.  Right-click the form header and select **Save**.

8.  Click the **Get OAuth Token** related link to request an authorization token from Google using the configured client ID and secret.

9.  In the Request for Permission window that appears, click **Accept** to grant access to your Google contacts.

    The token aquired is not directly accessible in your instance.

10. In the **HTTP Methods** related list, select the **GET** method.

11. Leave the HTTP method **Authentication type** as **-- None --** to use the OAuth profile from the parent REST message record.

12. On the **HTTP Request** tab, add a new row to the **HTTP Headers** related list with a **Name** of `GData - Version` and a **Value** of `3.0`.

13. Right-click the form header and select **Save**.

14. Click the **Test** related link.

    The test result should display an **HTTP Status** of 200, and the result of the contacts API call.


**Parent Topic:**[Outbound REST with OAuth 2.0 profile tutorial - integrating with Google Contacts API](../concept/c_OAuth2ProfileTutorialGoogle.md)

**Previous topic:**[OAuth 2.0 tutorial - create an OAuth provider and profile](t_OAuthDemoCreateProvider.md)

**Next topic:**[Outbound REST mutual authentication](../concept/c_OutboundRESTMutualAuthentication.md)

