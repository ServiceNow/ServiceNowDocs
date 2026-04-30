---
title: Private Key JWT Support for OAuth 2.0 Client Authentication
description: Support JWT Support for OAuth 2.0 Client Authentication.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [OAuth Outbound, OAuth Inbound and Outbound authentication, Authentication, Access Management]
---

# Private Key JWT Support for OAuth 2.0 Client Authentication

Support JWT Support for OAuth 2.0 Client Authentication.

Private Key JWT Client Authentication is an authentication method that can be used by clients to authenticate to the authorization server when using the token endpoint.

In this authentication mechanism, only the clients that have registered a public key and signed a JWT using that key can authenticate.

The JWT must contain REQUIRED claim values and may contain OPTIONAL claim values. To know more about the claim values needed for the JWT for `private_key_jwt` authentication, refer the Client Authentication section in the [OpenID Connect core](https://openid.net/specs/openid-connect-core-1_0.html#ClientAuthentication) documentation.

**Note:** The authentication token must be sent as the value of the client\_assertion parameter. The value of the  **client\_assertion\_type ** parameter must be  `urn:ietf:params:oauth:client-assertion-type:jwt-bearer`.

Plugins required for OAuth 2.0 Client Authentication using JWT token:

-   **OAuth 2.0 \(com.snc.platform.security.oauth\)**: This plugin is active on new and upgraded instances. If the plugin is not active on your instance, you can activate it.
-   **Integration - Multiple Provider Single Sign-On Installer \(com.snc.integration.sso.multi.installer\)**: For OIDC based single sign-on use case.

You can use the OAuth 2.0 Client Authentication using Private Key JWT for the following:

-   [OIDC based single sign-on](../task/config-private-key-jwt-oidc-sso.md)
-   [Outbound OAuth integrations](../task/config-private-key-jwt-outbound-oauth.md)

