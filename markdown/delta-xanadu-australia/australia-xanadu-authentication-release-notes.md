---
title: Combined Authentication release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for Authentication from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-authentication-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-21"
reading_time_minutes: 13
breadcrumb: [Products combined by family]
---

# Combined Authentication release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for Authentication from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Authentication release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Authentication to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Authentication.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Continuous Authentication](https://www.servicenow.com/docs/access?context=ca-homepage&family=yokohama&ft:locale=en-US)**

Use Continuous Authentication to require step-up authentication or re-authentication to the users before allowing access to sensitive or high-privilege information.

-   **[OAuth Grant Types for MID Server](https://www.servicenow.com/docs/access?context=oauth-outbound&family=yokohama&ft:locale=en-US)**

Use the Authorization code, resource owner password credential, SAML bearer, and JWT bearer OAuth grant types of OAuth for outbound integration requests through the MID Server. Personal Auth is also supported through the MID server. MID Servers facilitate communication and data movement between a single ServiceNow® instance and external applications, data sources, and services.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Machine Identity Console](https://www.servicenow.com/docs/access?context=machine-identity-console&family=zurich&ft:locale=en-US)**

Manage your inbound integration with ServiceNow's Machine Identity Console. Inbound integration in Machine Identity Console provides a simplified configuration experience for your inbound integrations.

-   **[Multi-factor Authentication dashboard](https://www.servicenow.com/docs/access?context=mfa-dashboard&family=zurich&ft:locale=en-US)**

Use the new MFA Dashboard to understand insights such as MFA user enrollment, privileged admins who haven't opted in to MFA, and compliance. You can verify that all users have MFA enabled for enhanced security with the help of the MFA Dashboard.

-   **[Multi-factor Authentication Guided Setup](https://www.servicenow.com/docs/access?context=mfa-guided-setup&family=zurich&ft:locale=en-US)**

Use the new MFA Guided setup to configure multi-factor Authentication \(MFA\) for users who currently log in to ServiceNow with only a user name and password. This update enhances security by guiding administrators through the MFA setup process and verifying that all users are protected with an additional layer of authentication.


-   **[Attributes for OIDC](https://www.servicenow.com/docs/access?context=idp-attributes-oidc&family=zurich&ft:locale=en-US)**

Use the Identity Provider \(IDP\) Attributes received from the OIDC response from the Identity Provider as a filter criteria for authentication.


</td></tr><tr><td>

Australia

</td><td>

-   **[Authentication factors for AI voice service](https://www.servicenow.com/docs/access?context=authentication-factors&family=australia&ft:locale=en-US)**

Enable caller access to AI voice agents by configuring the required identification and authentication factors.

-   **[Web Embeddables](https://www.servicenow.com/docs/access?context=web-embeddables&family=australia&ft:locale=en-US)**

Secure the web embeddables feature for authenticating the ServiceNow®'s web components that are used in third-party portals.

-   **[Granular admin roles](https://www.servicenow.com/docs/access?context=granular-admin-roles&family=australia&ft:locale=en-US)**

The granular admin role enables developers and administrators to complete administrative configuration tasks for Authentication without requiring the full admin role.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Authentication features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Multi-factor Authentication \(MFA\)](https://www.servicenow.com/docs/access?context=mfa-config-landing&family=xanadu&ft:locale=en-US)**

Use the FIDO2 authenticator, passkeys, biometric authenticators, and hardware security keys as multi-factor authentication \(MFA\) factors without requiring an authenticator app setup.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[MFA enforcement](https://www.servicenow.com/docs/access?context=mfa-enforcement&family=yokohama&ft:locale=en-US)**

MFA is mandated and is enforced to all the non-SSO login users accessing ServiceNow®.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Enhanced SSO login and logout experience](https://www.servicenow.com/docs/access?context=c_MultipleProviderSingleSignOn&family=zurich&ft:locale=en-US)**

Use the enhanced SSO login and logout experience. Enhancement includes:

    -   Display of active SAML and OIDC Identity Providers \(IdPs\) on the ServiceNow platform and portal login pages.
    -   Assign users to specific groups during SAML and OIDC auto-provisioning.
    -   Set up OIDC with the same well-known URL. The OIDC configurations can use the same well-known URL of the IdPs for multiple SSO records.
    -   Display login failure reasons to the users who logged out of ServiceNow due to session expiry or other reasons. Use the login link on the external logout page to again log in to ServiceNow in case of successful logout.
    -   Display of a generic error message for unsuccessful single log out.
    -   Enhanced email notifications for SAML certificate and Encryption Key store update.
-   **[FIDO2 as an MFA factor](https://www.servicenow.com/docs/access?context=mfa-with-fido&family=zurich&ft:locale=en-US)**

Use the FIDO factor policy to enforce FIDO \(Hardware key or Biometric as second factor for authentication\) as second factor authentication to users who attempt to log in to the instance.

-   **[OAuth integrations](https://www.servicenow.com/docs/access?context=oauth-inbound-and-outbound&family=zurich&ft:locale=en-US)**

Configure OAuth integration that includes the following enhancements:

    -   You can provide a maximum client secret length up to 4096 characters to meet security requirements of the third-party systems.
    -   You can provide a JSON Web Key Set \(JWKS\) URL to automatically manage and update the public key for JSON Web Tokens \(JWT\) signature validation.
    -   You can request OAuth tokens using the JWT grant type signed with Elliptic Curve Digital Signature Algorithm \(ES\) signing algorithms, including ES256, ES384, and ES512, for inbound JSON Web Tokens \(JWT\). It also supports RS256, RS384, RS512, HS256, HS384, and HS512.
    -   You can customize the JWT ID \(JTI\) claim name in both inbound OpenID Connect \(OIDC\) and JWT Bearer flows.

</td></tr><tr><td>

Australia

</td><td>

-   **[OAuth enhancements](https://www.servicenow.com/docs/access?context=api-inbound-and-outbound&family=australia&ft:locale=en-US)**

Following are the OAuth enhancements:

    -   Use **Opaque** or **JWT** token option for your inbound integration endpoints.
    -   Use the **Allow access only to APIs in selected scope** option to enable access to the APIs that are explicitly listed in the selected scopes for your inbound integrations.
    -   Use the OAuth Entity Resource tab for outbound integrations to configure resource parameters so they flow into the OAuth token request and are reflected in the token from your OAuth provider.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Authentication features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Authentication features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   The MultiSSO v1 plugin is deprecated. Upgrade to MutliSSO v2 from MultiSSO v1. For more information on how to upgrade to MultiSSO v2, refer to the knowledge article [MultiSSO v2 upgrade instructions \[KB9756504\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0756504) in the Now Support Knowledge Base.
-   The SAML 1.1 and SAML 1.1 Single Sign-On - Update 1 plugin is deprecated. The SAML-based identity providers \(IdP\) have already migrated to SAML 2.0. To use SAML 2.0, you must activate the MultiSSO v2 plugin and configure your identity provider.
-   The OpenID SSO plugin is deprecated. To use OpenID Connect \(OIDC\), you must activate the MultiSSO v2 and configure your OIDC-based identity provider.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

Due to the launch of new simplified inbound integration configuration in Machine Identity Console, the following inbound integrations configurations in the Application registry page are deprecated:

-   OAuth API endpoint for external clients
-   OAuth JWT API endpoint for external clients
-   OIDC provider to verify ID tokens

</td></tr><tr><td>

Australia

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

Xanadu

</td><td>

Authentication is a ServiceNow AI Platform product that is active by default.

</td></tr><tr><td>

Yokohama

</td><td>

Authentication is a ServiceNow AI Platform product that is active by default.

</td></tr><tr><td>

Zurich

</td><td>

Authentication is a ServiceNow AI Platform product that is active by default.

</td></tr><tr><td>

Australia

</td><td>

Authentication is a ServiceNow AI Platform product that is active by default.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Authentication we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

-   **Coral theme**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Authentication we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Xanadu

</td><td>

-   Use the FIDO2 authenticator, passkeys, biometric authenticators, and hardware security keys as multi-factor authentication \(MFA\) factors without requiring an authenticator app setup.

 See [Authentication](https://www.servicenow.com/docs/access?context=c_Authentication&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

[Yokohama Patch 13](https://www.servicenow.com/docs/access?context=yokohama-patch-13&family=yokohama&ft:locale=en-US)

-   **[Knowledge-based factor enhancement for AI voice service](https://www.servicenow.com/docs/access?context=knowledge-based-authentication&family=yokohama&ft:locale=en-US)**

Following are the knowledge-based authentication \(KBA\) enhancements:

    -   [Voice input support for KBA questions](https://www.servicenow.com/docs/access?context=create-knowledge-based-questions&family=yokohama&ft:locale=en-US): Configure KBA questions to support Voice as an input type, allowing users to provide spoken responses during identification and authentication. When Voice input is enabled, you can configure the expected format, provide examples, and optionally define a validation pattern using regular expressions.
    -   [Script-based validation for external systems](https://www.servicenow.com/docs/access?context=create-knowledge-based-answers&family=yokohama&ft:locale=en-US): Configure KBA answers to validate that are created against external systems using custom scripts through the Script Configuration field. When set to Identification mode, you can write scoped scripts that validate caller identity against external authentication systems instead of internal ServiceNow AI Platform tables.

 [Yokohama Patch 11](https://www.servicenow.com/docs/access?context=yokohama-patch-11&family=yokohama&ft:locale=en-US)

-   **[Authentication factors for AI voice service](https://www.servicenow.com/docs/access?context=authentication-factors&family=yokohama&ft:locale=en-US)**

Enable caller access to AI voice agents by configuring the required identification and authentication factors.

-   **[OAuth enhancements](https://www.servicenow.com/docs/access?context=api-inbound-and-outbound&family=yokohama&ft:locale=en-US)**

Following are the OAuth enhancements:

    -   Use **Opaque** or **JWT token** option for your inbound integration endpoints.
    -   Use the **Allow access only to APIs in selected scope** option to enable access to the APIs that are explicitly listed in the selected scopes for your inbound integrations.
    -   Use the OAuth Entity Resource tab for outbound integrations to configure resource parameters so they flow into the OAuth token request and are reflected in the token from your OAuth provider.
-   **[Provider name for Inbound integrations](https://www.servicenow.com/docs/access?context=new-inbound-integrations&family=yokohama&ft:locale=en-US)**

Use the Provider name field to enter the details of your inbound integrations to distinguish between different inbound integrations on your ServiceNow AI Platform®. Update the Provider name in your API integrations to improve monitoring capabilities:

    -   For OAuth integrations, update the provider name using the Provider name field. To know more, see [OAuth Inbound](https://www.servicenow.com/docs/access?context=oauth-inbound&family=yokohama&ft:locale=en-US).
    -   For Basic authentication integrations, update the Provider name in the integration registration form.

 [Yokohama Patch 7](https://www.servicenow.com/docs/access?context=yokohama-patch-7&family=yokohama&ft:locale=en-US)

-   **OAuth token enhancement**

Use Opaque or JWT token option for your inbound integration endpoints.


 Yokohama

-   Use Continuous Authentication to require step-up authentication or re-authentication to the users before allowing access to sensitive or high-privilege information.
-   Multi-factor Authentication \(MFA\) is enforced by default for all non-SSO login to ServiceNow®.
-   Use the Authorization code, resource owner password credential, SAML bearer, and JWT bearer OAuth grant types of OAuth for outbound integration requests through the MID Server.

 See [Authentication](https://www.servicenow.com/docs/access?context=c_Authentication&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

[Zurich Patch 10](https://www.servicenow.com/docs/access?context=zurich-patch-10&family=zurich&ft:locale=en-US)

-   **[Knowledge-based factor enhancement for AI voice service](https://www.servicenow.com/docs/access?context=knowledge-based-authentication&family=zurich&ft:locale=en-US)**

Following are the knowledge-based authentication \(KBA\) enhancements:

    -   Email OTP as an authentication factor for AI voice service: Use Email OTP as a standalone factor, a primary factor, or a secondary factor in AI voice agent authentication flows. When a caller reaches the voice agent, a one-time password is sent to their registered email address. The caller provides the password to complete authentication.
    -   KBA for AI voice service: Use the KBA setup to configure Knowledge-Based Authentication \(KBA\) for the voice channel. Choose from base system questions at both the identification level and the authentication level. AI voice service mappings are populated automatically from your Assistant Designer selection, so manually mapping voice services is no longer a mandatory step in the KBA setup.
    -   Authenticate callers at the start of every call: Prompt callers for authentication or identification details at the start of every call, before the voice-only assistant responds to any request, using the Authenticate at the start of the call option on the Assistant Designer's Caller verification page.

 [Zurich Patch 4](https://www.servicenow.com/docs/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   **[Authentication factors for AI voice service](https://www.servicenow.com/docs/access?context=authentication-factors&family=zurich&ft:locale=en-US)**

Enable caller access to AI voice agents by configuring the required identification and authentication factors.

-   **[OAuth enhancements](https://www.servicenow.com/docs/access?context=api-inbound-and-outbound&family=zurich&ft:locale=en-US)**

Following are the OAuth enhancements:

    -   Use **Opaque** or **JWT** token option for your inbound integration endpoints.
    -   Use the **Allow access only to APIs in selected scope** option to enable access to the APIs that are explicitly listed in the selected scopes for your inbound integrations.
    -   Use the OAuth Entity Resource tab for outbound integrations to configure resource parameters so they flow into the OAuth token request and are reflected in the token from your OAuth provider.

 [Zurich Patch 3](https://www.servicenow.com/docs/access?context=zurich-patch-1&family=zurich&ft:locale=en-US)

-   **[Provider name for Inbound integrations](https://www.servicenow.com/docs/access?context=new-inbound-integrations&family=zurich&ft:locale=en-US)**

Use the Provider name field to enter the details of your inbound integrations to distinguish between different inbound integrations on your ServiceNow AI Platform®. Update the Provider name in your API integrations to improve monitoring capabilities:

    -   For OAuth integrations, update the provider name using the Provider name field. To know more, see [OAuth inbound](https://www.servicenow.com/docs/access?context=oauth-inbound&family=zurich&ft:locale=en-US).
    -   For Basic authentication integrations, update the Provider name in the integration registration form. To know more about the integration registration form, see [View dashboard](https://www.servicenow.com/docs/access?context=view-inbound-api-integration-usage-dashboard&family=zurich&ft:locale=en-US).

 [Zurich Patch 1](https://www.servicenow.com/docs/access?context=zurich-patch-1&family=zurich&ft:locale=en-US)

-   **OAuth token enhancement**

Use Opaque or JWT token option for your inbound integration endpoints.


 Zurich

-   Experience the new Inbound integration configuration in the Machine Identity Console.
-   Use the new MFA Dashboard to understand insights such as MFA user enrollment, privileged admins who haven't opted in to MFA, and compliance.
-   Use the FIDO factor policy to enforce FIDO-based authentication.
-   Use the enhanced SSO login and logout experience.
-   Configure the authentication policies to restrict access, reduce roles, or enforce MFA based on Identity Provider \(IdP\) attributes that are received from the OIDC response.

 See [Authentication](https://www.servicenow.com/docs/access?context=c_Authentication&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

[Australia Patch 3](https://www.servicenow.com/docs/access?context=australia-patch-3&family=australia&ft:locale=en-US)

-   **[Authentication factors enhancement for AI voice service](https://www.servicenow.com/docs/access?context=explore-authentication-factors&family=australia&ft:locale=en-US)**

Following are the authentication factors enhancements:

    -   Email OTP as an authentication factor for AI voice service: Use Email OTP as a standalone factor, a primary factor, or a secondary factor in AI voice agent authentication flows. When a caller reaches the voice agent, a one-time password is sent to their registered email address. The caller provides the password to complete authentication.
    -   KBA for AI voice service: Use the KBA setup to configure Knowledge-Based Authentication \(KBA\) for the voice channel. Choose from base system questions at both the identification level and the authentication level. AI voice service mappings are populated automatically from your Assistant Designer selection, so manually mapping voice services is no longer a mandatory step in the KBA setup.
    -   Authenticate callers at the start of every call: Prompt callers for authentication or identification details at the start of every call, before the voice-only assistant responds to any request, using the Authenticate at the start of the call option on the Assistant Designer's Caller verification page.

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

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

