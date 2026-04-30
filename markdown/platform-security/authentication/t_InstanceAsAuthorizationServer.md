---
title: Authorization code flow example: ServiceNow instance as authorization server
description: You can use an instance as an authorization server to issue tokens to a client using authorization code flow.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [OAuth authorization code grant flow, OAuth Inbound, OAuth authentication, Authentication, Access Management]
---

# Authorization code flow example: ServiceNow instance as authorization server

You can use an instance as an authorization server to issue tokens to a client using authorization code flow.

## Before you begin

Role required: none.

This example uses two instances: one as the authorization server and the other as the client. One instance uses a REST call to request tokens from another instance.

You must [Activate OAuth](t_ActivateOAuth.md) on both instances.

## Procedure

1.  On the authorization server instance \(running the Istanbul or later release\), navigate to **System OAuth** &gt; **Application Registry** and then click **New**.

2.  Click **Create an OAuth API endpoint for external clients**.

3.  Fill out the form fields for the OAuth application record as described in [Create an endpoint for clients to access the instance](t_CreateEndpointforExternalClients.md).

    Completing these steps sets up an authorization server. Follow the next steps to set up the client server.

4.  On the client instance, navigate to **System OAuth** &gt; **Application Registry** and then click **New**.

5.  Click **Connect to a third party OAuth Provider**.

6.  Fill out the form fields for the OAuth application record as described in .

    Note the following field values:

    -   **Name**: A unique name that identifies the application that you require OAuth access for.
    -   **Client ID**: Client ID of the application registry record that you created for the authorization server.
    -   **Client Secret**: \[Read-Only\] The auto-generated unique ID of the application. The instance uses the client ID when requesting an access token.
    -   **Default Grant type**: Select **Authorization code**.
    -   **Authorization URL**: URL of the instance that is the authorization server. Remember to append `oauth_auth.do` at the end of the URL.
    -   **Logo URL**: The URL that contains an image to use as the application logo. The logo appears on the approval page when the user receives a request to grant a client application access to a restricted resource on the instance.
    -   **Token URL**: URL of the instance that is the authorization server. Remember to append `oauth_token.do` at the end of the URL.
    -   **Redirect URL**: URL of the instance: the client server instance. Remember to append `oauth_redirect.do` at the end of the URL.
7.  Create a profile for the record with the **Authorization code** grant type.

    The client server is setup. You can now create an outbound REST message and get an OAuth token.


