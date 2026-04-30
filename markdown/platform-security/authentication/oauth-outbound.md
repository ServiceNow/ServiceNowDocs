---
title: OAuth outbound
description: OAuth outbound enables you to pull data from a third-party provider to your instance.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [OAuth authentication, Authentication, Access Management]
---

# OAuth outbound

OAuth outbound enables you to pull data from a third-party provider to your instance.

You must have the security\_admin role to manage the OAuth integration.

You can configure outbound OAuth 2.0 for the following grant types:

-   **Connect to third-party provider**: Use the client ID and secret to send it to the OAuth provider. For more information, see [Connect to a third-party OAuth provider](../../../administer/security/task/connect-3rd-party-oauth-provider.md).
-   **JWT Bearer**: An authorization server validates a JWT token which enables identity and security information to be shared across security domains. For more information, see [Set up OAuth provider with JWT Bearer grant type](../../../administer/security/task/JWT-Bearer-token-support.md#).
-   **SAML2 Bearer**: Generates the SAML2 assertion and then exchanges the assertion for the access tokens wit the provider.

    **Note:** For outbound request to SuccessFactors use the **SAML2 Bearer** as the Default Grant Type. To know more about how to configure **SAML2 Bearer**, refer the example in [Set up the v4.x.x](https://www.servicenow.com/docs/access?context=setup-successfactors&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).

-   **Authorization code**: The code that is granted to the client to obtain an access token, which is then used to obtain access to the resource. If you select this option, then you need an authorization URL \(the URL of the authorization server\).
-   **Resource owner password credentials**: The user name and password of the user that is trying to obtain access to the resource.
-   **Client Credentials**: The client ID and client secret, which are both used to get the access token. This method does not provide refresh tokens.
-   **MID Server**: The MID Servers facilitate communication and data movement between a single ServiceNow® instance and external applications, data sources, and services. Use the Authorization code, resource owner password credential, SAML bearer, and JWT bearer OAuth grant types of OAuth for outbound integration requests through the MID Server. Personal Auth is also supported through the MID server.

You can configure **OAuth provider scenario** \(Outbound\): Your instance pulls data from a third-party provider.

**Note:** You must user authenticate for the first time to fetch the token post which, you don't need to authenticate using a user account before the token expiry.

