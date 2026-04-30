---
title: Old inbound integrations experience
description: Old experience - Inbound integrations.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [OAuth inbound, OAuth authentication, Authentication, Access Management]
---

# Old inbound integrations experience

Old experience - Inbound integrations.

**Note:**

You can perform the OAuth inbound configuration, depending on the following type of grant type:

-   [OAuth authorization code grant flow](../../../administer/security/concept/c_OAuthAuthorizationCodeFlow.md)

    **Note:** For authorization code flow, user needs to complete the Authentication by local login, SSO or MFA and then provide consent.

-   [Password grant](../../../administer/security/task/t_AuthorizeAccessEndpiont.md)
-   [JWT bearer grant flow](../../../administer/security/task/create-jwt-endpoint.md)
-   [ID token flow](../../../administer/security/task/add-OIDC-entity.md)
-   [OAuth implicit grants](../../../administer/security/concept/c_OAuthImplicitGrants.md)
-   [Client Credentials](client-credentials.md)

Configure OAuth integration that includes the following enhancements from Zurich release:

-   Increase client secret length up-to 4096 characters to meet security requirements of third-party systems.
-   Provide a JSON Web Key Set \(JWKS\) URL to automatically manage and update the public key for JSON Web Tokens \(JWT\) signature validation.
-   Request OAuth tokens using the JWT grant type signed with Elliptic Curve Digital Signature Algorithm \(ES\) signing algorithms, including ES256, ES384, and ES512, for inbound JSON Web Tokens \(JWT\).
-   Customize the JWT ID \(JTI\) claim name in both inbound OpenID Connect \(OIDC\) and JWT Bearer flows.

