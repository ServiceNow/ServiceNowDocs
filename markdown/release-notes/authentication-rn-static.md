---
title: Authentication release notes
description: The ServiceNow Authentication application supports many authentication mechanisms that enable you to authenticate the users. See the following sections for release notes by version.The Brazil Early Availability release adds security features for Authentication.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/authentication-rn-static.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [ServiceNow AI Platform security release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Authentication release notes

The ServiceNow® Authentication application supports many authentication mechanisms that enable you to authenticate the users. See the following sections for release notes by version.

## About Authentication

-   Simplify the login experience by crafting login policies that present relevant methods based on user context with the Policy-based experience - Identifier-first login experience.
-   Act before SSO is disrupted with home page banner alerts when SAML SP signing or encryption keystores are nearing or past expiry.
-   Authenticate callers in AI voice agent sessions using a one-time passcode delivered to a registered email address, as a standalone, primary, or secondary factor.
-   Connect ServiceNow to Microsoft Azure and Google Cloud Platform without storing or rotating client secrets, using federated identity based on signed JWTs.
-   Issue ID Tokens signed with RS256 from the ServiceNow OpenID Provider to give OAuth client applications a way to verify end-user identity.
-   Restrict Basic Authentication access on the instance to a defined set of trusted scenarios, with a tracking period to identify legitimate users before enforcement begins.
-   Configure SSL/TLS certificate validation for individual outbound endpoints by creating outbound certificate policies, so you can adjust hostname verification, certificate chain validation, and revocation checking for a specific host without changing the global validation policy for every other endpoint.
-   Register an external authorization server — such as Microsoft Entra ID or Okta — as a trusted token issuer for the MCP Server, so MCP clients can authenticate using tokens from your enterprise identity provider.

See [Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/c_Authentication.md) for more information.

## Activation and other requirements

-   **Activation information**

    Authentication is a ServiceNow AI Platform product that is active by default.


## Accessibility and localization

-   **Accessibility information**
    -   **Coral theme**

        Coral is the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme uses brand-neutral illustrations. A dark theme option is available for web and mobile experiences.


## Brazil Early Availability

The Brazil Early Availability release adds security features for Authentication.

### What's new

-   **[Policy-based login experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/next-gen-login-experience.md)**

    Use the Policy-based experience \(identifier-first login\) framework in the Authentication Console to craft login policies to simplify the login experience by presenting relevant login methods based on user context, such as username or email.

-   **[SAML certificate expiry notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/c_SAML2.0WebBrowserSSOProfile.md)**

    Receive banner alerts on the home page when SAML SP signing or encryption keystores are approaching or past their expiry date. The instance displays two separate banners — one for signing certificates and one for encryption certificates — each linking to a dedicated customer action in Security Center.

-   **[Email OTP as an authentication factor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/email-otp-authentication.md)**

    Use Email OTP as a standalone factor, a primary factor, or a secondary factor in AI voice agent authentication flows. When a caller reaches the voice agent, a one-time passcode is sent to their registered email address. The caller provides the passcode to complete authentication.

-   **Authenticate callers at the start of every call**

    Prompt callers for authentication or identification details at the start of every call, before the voice-only assistant responds to any request, using the Authenticate at the start of the call option on the Assistant Designer's Caller verification page.

-   **[Workload Identity Federation for Microsoft Azure and Google Cloud Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/workload-identity-federation.md)**

    Authenticate outbound connections to Microsoft Azure and Google Cloud Platform using federated identity.

-   **[Domain-Level Certificate Validation Exclusion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/outbound-certificate-policies.md)**

    Configure SSL/TLS certificate validation for individual outbound endpoints by creating outbound certificate policies, so you can adjust hostname verification, certificate chain validation, and revocation checking for a specific host without changing the global validation policy for every other endpoint.

-   **Issue ID tokens signed with RS256**

    Issue ID tokens signed with the RSA SHA-256 algorithm \(RS256\) from the OpenID Provider. Use the ID Tokens in OAuth client applications to verify end-user identity.

-   **[Restrict Basic Authentication access with the Basic Auth Restriction page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/basic-auth-restriction.md)**

    Use the Basic Auth Restriction page to strengthen instance security by limiting Basic Authentication access to a defined allowlist. Run the tracking period first to identify users currently relying on Basic Auth, then enable enforcement to block Basic Auth requests that don't match the allowlist. The allowlist covers Web Services Access Only \(WSAO\) users, SNC users, OAuth ROPC flow users, users presenting a valid OTP, and users granted the snc\_basic\_auth\_api\_access role.

-   **[Authenticate MCP clients with external authorization servers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/mcp-3p-auth-concept.md)**

    Register an external authorization server as a trusted token issuer for the MCP Server by creating an OIDC Provider Configuration that identifies the provider's issuer URI and metadata endpoint. The MCP Server validates a token from a registered provider locally — confirming the issuer is trusted, the signature is valid, the audience matches, and the token has not expired — without depending on the ServiceNow authorization server. Tokens from issuers that aren't registered and active are rejected.


### What's changed

-   **SAML certificate expiry notification**

    Receive more timely alerts — the SAML certificate expiry notification triggers earlier and includes additional detail about affected keystores.

-   **Max age parameter handling**

    Set the max\_age parameter in an authentication request to require that the end-user has authenticated within a specified number of seconds. When the elapsed time since the last authentication exceeds max\_age, the Authorization Server reauthenticates the end-user. The max\_age implementation has been refined to align with the OpenID Connect Core 1.0 specification.

-   **KBA for AI voice service**

    Use the KBA setup to configure Knowledge-Based Authentication \(KBA\) for the voice channel. Choose from base system questions at both the identification level and the authentication level. AI voice service mappings are populated automatically from your Assistant Designer selection, so manually mapping voice services is no longer a mandatory step in the KBA setup.


