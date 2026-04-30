---
title: OAuth Inbound
description: Inbound authentication allows trusted external applications to securely access ServiceNow APIs, ensuring controlled and authorized connections.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [OAuth authentication, Authentication, Access Management]
---

# OAuth Inbound

Inbound authentication allows trusted external applications to securely access ServiceNow APIs, ensuring controlled and authorized connections.

You must have the `security_admin` role to manage the OAuth integration.

You can configure **OAuth external client scenario** \(Inbound\) integration, when your want your instance to provide an endpoint for third-party clients to pull data from the instance.

**Note:** You must user authenticate for the first time to fetch the token post which, you don't need to authenticate using a user account before the token expiry.

You can perform the OAuth inbound configuration, depending on the following type of grant type:

-   **Authorization code grant flow**: For a user initiated grant flow, where the user without requiring to enter username or password, but through the access token can configure an authorized URL for authentication. For more information, see [OAuth authorization code grant flow](../../../administer/security/concept/c_OAuthAuthorizationCodeFlow.md).
-   **Password grant flow**: For a user initiated grant flow, where a user interaction is required for authentication. For more information, see [Password grant](../../../administer/security/task/t_AuthorizeAccessEndpiont.md) flow configuration.

    **Note:** For authorization code flow, user needs to complete the Authentication by local login, SSO or MFA and then provide consent.

-   **JWT bearer grant flow**: For a system to system integration, where a user intervention is not required. For more information, see [JWT bearer grant flow](../../../administer/security/task/create-jwt-endpoint.md) configuration.
-   **ID token flow**: For using a ID token issued by 3rd party OIDC providers such as Okta, Azure. For more information, see [ID token flow](../../../administer/security/task/add-OIDC-entity.md) for authentication.
-   **OAuth implicit grants**: For allowing the access token to be given directly to the client application through the user agent, which is typically the web browser or mobile device. For more information, see [OAuth implicit grants](../../../administer/security/concept/c_OAuthImplicitGrants.md).
-   **Client credentials**: For using the OAuth client credentials grant type for Inbound Integrations from a third party OAuth client to the ServiceNow® platform. For more information, see [Client Credentials](client-credentials.md).

## OAuth Scopes

You can scope the OAuth authentication scope support for REST API. OAuth Scope provides access to only the particular REST APIs. For more information, see [REST API Auth Scope](../../../administer/security/concept/rest-api-auth-scope.md).

