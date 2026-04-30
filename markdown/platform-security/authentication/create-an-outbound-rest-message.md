---
title: Create an outbound REST message
description: Create outbound rest message to authorize instance as authorization server.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [OAuth outbound, OAuth authentication, Authentication, Access Management]
---

# Create an outbound REST message

Create outbound rest message to authorize instance as authorization server.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **System Web Services** &gt; **Outbound** &gt; **REST Message** and then click **New**.

2.  Fill out the form fields for the OAuth application record as described in .

    Note the following field values:

    -   **Endpoint**: URL of the instance that is the authorization server.
    -   **Authentication type**: **OAuth 2.0**.
    -   **OAuth profile**: OAuth profile that you created for the client server.
3.  On the REST message record, click **Get OAuth Token**.

4.  Authenticate with the instance that provides the token—the method depends on the single-sign on integration.

    You might use:

    -   Your username and password that you use to authenticate to the instance.
    -   The username and password for the IdP if is enabled. Click **Use External Login** to access the IdP login screen.

        **Note:** In order to automatically get redirected to the IdP login page, you must set the glide.authenticate.external system property.

    -   Your code, if MFA is enabled.
5.  Click **Allow** or **Deny** to complete the authorization and issue the tokens.

    The process that follows is outlined in [OAuth authorization code grant flow](../concept/c_OAuthAuthorizationCodeFlow.md).


