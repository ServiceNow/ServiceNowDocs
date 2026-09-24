---
title: Combined Authentication release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for Authentication from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-authentication-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Authentication release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for Authentication from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Authentication release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Authentication to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Authentication.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Authentication factors for AI voice service](https://www.servicenow.com/docs/access?context=authentication-factors&family=australia&ft:locale=en-US)**

Enable caller access to AI voice agents by configuring the required identification and authentication factors.

-   **[Web Embeddables](https://www.servicenow.com/docs/access?context=web-embeddables&family=australia&ft:locale=en-US)**

Secure the web embeddables feature for authenticating the ServiceNow®'s web components that are used in third-party portals.

-   **[Granular admin roles](https://www.servicenow.com/docs/access?context=granular-admin-roles&family=australia&ft:locale=en-US)**

The granular admin role enables developers and administrators to complete administrative configuration tasks for Authentication without requiring the full admin role.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Policy-based login experience](https://www.servicenow.com/docs/access?context=next-gen-login-experience&family=brazil&ft:locale=en-US)**

Use the Policy-based experience \(identifier-first login\) framework in the Authentication Console to craft login policies to simplify the login experience by presenting relevant login methods based on user context, such as username or email.

-   **[SAML certificate expiry notifications](https://www.servicenow.com/docs/access?context=c_SAML2.0WebBrowserSSOProfile&family=brazil&ft:locale=en-US)**

Receive banner alerts on the home page when SAML SP signing or encryption keystores are approaching or past their expiry date. The instance displays two separate banners — one for signing certificates and one for encryption certificates — each linking to a dedicated customer action in Security Center.

-   **[Email OTP as an authentication factor](https://www.servicenow.com/docs/access?context=email-otp-authentication&family=brazil&ft:locale=en-US)**

Use Email OTP as a standalone factor, a primary factor, or a secondary factor in AI voice agent authentication flows. When a caller reaches the voice agent, a one-time passcode is sent to their registered email address. The caller provides the passcode to complete authentication.

-   **Authenticate callers at the start of every call**

Prompt callers for authentication or identification details at the start of every call, before the voice-only assistant responds to any request, using the Authenticate at the start of the call option on the Assistant Designer's Caller verification page.

-   **[Workload Identity Federation for Microsoft Azure and Google Cloud Platform](https://www.servicenow.com/docs/access?context=workload-identity-federation&family=brazil&ft:locale=en-US)**

Authenticate outbound connections to Microsoft Azure and Google Cloud Platform using federated identity.

-   **[Domain-Level Certificate Validation Exclusion](https://www.servicenow.com/docs/access?context=outbound-certificate-policies&family=brazil&ft:locale=en-US)**

Configure SSL/TLS certificate validation for individual outbound endpoints by creating outbound certificate policies, so you can adjust hostname verification, certificate chain validation, and revocation checking for a specific host without changing the global validation policy for every other endpoint.

-   **Issue ID tokens signed with RS256**

Issue ID tokens signed with the RSA SHA-256 algorithm \(RS256\) from the OpenID Provider. Use the ID Tokens in OAuth client applications to verify end-user identity.

-   **[Restrict Basic Authentication access with the Basic Auth Restriction page](https://www.servicenow.com/docs/access?context=basic-auth-restriction&family=brazil&ft:locale=en-US)**

Use the Basic Auth Restriction page to strengthen instance security by limiting Basic Authentication access to a defined allowlist. Run the tracking period first to identify users currently relying on Basic Auth, then enable enforcement to block Basic Auth requests that don't match the allowlist. The allowlist covers Web Services Access Only \(WSAO\) users, SNC users, OAuth ROPC flow users, users presenting a valid OTP, and users granted the snc\_basic\_auth\_api\_access role.

-   **[Authenticate MCP clients with external authorization servers](https://www.servicenow.com/docs/access?context=mcp-3p-auth-concept&family=brazil&ft:locale=en-US)**

Register an external authorization server as a trusted token issuer for the MCP Server by creating an OIDC Provider Configuration that identifies the provider's issuer URI and metadata endpoint. The MCP Server validates a token from a registered provider locally — confirming the issuer is trusted, the signature is valid, the audience matches, and the token has not expired — without depending on the ServiceNow authorization server. Tokens from issuers that aren't registered and active are rejected.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Authentication features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[OAuth enhancements](https://www.servicenow.com/docs/access?context=api-inbound-and-outbound&family=australia&ft:locale=en-US)**

Following are the OAuth enhancements:

    -   Use **Opaque** or **JWT** token option for your inbound integration endpoints.
    -   Use the **Allow access only to APIs in selected scope** option to enable access to the APIs that are explicitly listed in the selected scopes for your inbound integrations.
    -   Use the OAuth Entity Resource tab for outbound integrations to configure resource parameters so they flow into the OAuth token request and are reflected in the token from your OAuth provider.

</td></tr><tr><td>

Brazil

</td><td>

-   **SAML certificate expiry notification**

Receive more timely alerts — the SAML certificate expiry notification triggers earlier and includes additional detail about affected keystores.

-   **Max age parameter handling**

Set the max\_age parameter in an authentication request to require that the end-user has authenticated within a specified number of seconds. When the elapsed time since the last authentication exceeds max\_age, the Authorization Server reauthenticates the end-user. The max\_age implementation has been refined to align with the OpenID Connect Core 1.0 specification.

-   **KBA for AI voice service**

Use the KBA setup to configure Knowledge-Based Authentication \(KBA\) for the voice channel. Choose from base system questions at both the identification level and the authentication level. AI voice service mappings are populated automatically from your Assistant Designer selection, so manually mapping voice services is no longer a mandatory step in the KBA setup.


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Authentication features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Authentication features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   Due to the launch of new simplified inbound integration configuration in Machine Identity Console, the following inbound integrations configurations in the Application registry page are deprecated:
    -   OAuth API endpoint for external clients
    -   OAuth JWT API endpoint for external clients
    -   OIDC provider to verify ID tokens
-   The \(`glide.login.no_blank_password`\) property is deprecated, since the property is no longer used and changing this property value doesn't effect login behavior.

 -   OAuth API endpoint for external clients
-   OAuth JWT API endpoint for external clients
-   OIDC provider to verify ID tokens

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Authentication.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Activation information**

Authentication is a ServiceNow AI Platform product that is active by default.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Authentication we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Authentication we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Authentication, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Accessibility information**
    -   **Coral theme**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Authentication we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Authentication we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

[Australia Patch 3](https://www.servicenow.com/docs/access?context=australia-patch-3&family=australia&ft:locale=en-US)

-   **[Authentication factors enhancement for AI voice service](https://www.servicenow.com/docs/access?context=explore-authentication-factors&family=australia&ft:locale=en-US)**

Following are the authentication factors enhancements:

    -   Email OTP as an authentication factor for AI voice service: Use Email OTP as a standalone factor, a primary factor, or a secondary factor in AI voice agent authentication flows. When a caller reaches the voice agent, a one-time password is sent to their registered email address. The caller provides the password to complete authentication.
    -   KBA for AI voice service: Use the KBA setup to configure Knowledge-Based Authentication \(KBA\) for the voice channel. Choose from base system questions at both the identification level and the authentication level. AI voice service mappings are populated automatically from your Assistant Designer selection, so manually mapping voice services is no longer a mandatory step in the KBA setup.
    -   Authenticate callers at the start of every call: Prompt callers for authentication or identification details at the start of every call, before the voice-only assistant responds to any request. Use the Authenticate at the start of the call option on the Assistant Designer's Caller verification page.

 [Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US)

-   **[Knowledge-based factor enhancement for AI voice service](https://www.servicenow.com/docs/access?context=knowledge-based-authentication&family=australia&ft:locale=en-US)**

Following are the knowledge-based authentication \(KBA\) enhancements:

    -   [Voice input support for KBA questions](https://www.servicenow.com/docs/access?context=create-knowledge-based-questions&family=australia&ft:locale=en-US): Configure KBA questions to support Voice as an input type, allowing users to provide spoken responses during identification and authentication. When Voice input is enabled, you can configure the expected format, provide examples, and optionally define a validation pattern using regular expressions.
    -   [Script-based validation for external systems](https://www.servicenow.com/docs/access?context=create-knowledge-based-answers&family=australia&ft:locale=en-US): Configure KBA answers to validate that are created against external systems using custom scripts through the Script Configuration field. When set to Identification mode, you can write scoped scripts that validate caller identity against external authentication systems instead of internal ServiceNow AI Platform tables.

 Australia

-   Enable caller access to AI voice agents by configuring the required identification and authentication factors.
-   Secure the web embeddables feature for authenticating the ServiceNow®'s web components that are used in third-party portals.
-   Use the granular roles to complete administrative configuration tasks for Authentication without requiring the full admin role.
-   Use the enhanced Auth Scope for your Inbound Integrations.

 See [Authentication](https://www.servicenow.com/docs/access?context=c_Authentication&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

