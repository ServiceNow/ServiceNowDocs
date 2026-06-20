---
title: Combined Authentication release notes for upgrades from Xanadu to Zurich
description: Consolidated page of all release notes for Authentication from Xanadu to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-xanadu-zurich/zurich-xanadu-authentication-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Authentication release notes for upgrades from Xanadu to Zurich

Consolidated page of all release notes for Authentication from Xanadu to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Authentication release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Authentication to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Authentication.

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

-   **[Continuous Authentication](https://servicenow-staging.fluidtopics.net/access?context=ca-homepage&family=yokohama&ft:locale=en-US)**

Use Continuous Authentication to require step-up authentication or re-authentication to the users before allowing access to sensitive or high-privilege information.

-   **[OAuth Grant Types for MID Server](https://servicenow-staging.fluidtopics.net/access?context=oauth-outbound&family=yokohama&ft:locale=en-US)**

Use the Authorization code, resource owner password credential, SAML bearer, and JWT bearer OAuth grant types of OAuth for outbound integration requests through the MID Server. Personal Auth is also supported through the MID server. MID Servers facilitate communication and data movement between a single ServiceNow® instance and external applications, data sources, and services.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Machine Identity Console](https://servicenow-staging.fluidtopics.net/access?context=machine-identity-console&family=zurich&ft:locale=en-US)**

Manage your inbound integration with ServiceNow's Machine Identity Console. Inbound integration in Machine Identity Console provides a simplified configuration experience for your inbound integrations.

-   **[Multi-factor Authentication dashboard](https://servicenow-staging.fluidtopics.net/access?context=mfa-dashboard&family=zurich&ft:locale=en-US)**

Use the new MFA Dashboard to understand insights such as MFA user enrollment, privileged admins who haven't opted in to MFA, and compliance. You can verify that all users have MFA enabled for enhanced security with the help of the MFA Dashboard.

-   **[Multi-factor Authentication Guided Setup](https://servicenow-staging.fluidtopics.net/access?context=mfa-guided-setup&family=zurich&ft:locale=en-US)**

Use the new MFA Guided setup to configure multi-factor Authentication \(MFA\) for users who currently log in to ServiceNow with only a user name and password. This update enhances security by guiding administrators through the MFA setup process and verifying that all users are protected with an additional layer of authentication.


-   **[Attributes for OIDC](https://servicenow-staging.fluidtopics.net/access?context=idp-attributes-oidc&family=zurich&ft:locale=en-US)**

Use the Identity Provider \(IDP\) Attributes received from the OIDC response from the Identity Provider as a filter criteria for authentication.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Authentication features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Multi-factor Authentication \(MFA\)](https://servicenow-staging.fluidtopics.net/access?context=mfa-config-landing&family=xanadu&ft:locale=en-US)**

Use the FIDO2 authenticator, passkeys, biometric authenticators, and hardware security keys as multi-factor authentication \(MFA\) factors without requiring an authenticator app setup.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Multi-factor authentication \(MFA\) enforcement](https://servicenow-staging.fluidtopics.net/access?context=mfa-enforcement&family=yokohama&ft:locale=en-US)**

MFA is mandated and is enforced to all the non-SSO login users accessing ServiceNow®.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Enhanced SSO login and logout experience](https://servicenow-staging.fluidtopics.net/access?context=c_MultipleProviderSingleSignOn&family=zurich&ft:locale=en-US)**

Use the enhanced SSO login and logout experience. Enhancement includes:

    -   Display of active SAML and OIDC Identity Providers \(IdPs\) on the ServiceNow platform and portal login pages.
    -   Assign users to specific groups during SAML and OIDC auto-provisioning.
    -   Set up OIDC with the same well-known URL. The OIDC configurations can use the same well-known URL of the IdPs for multiple SSO records.
    -   Display login failure reasons to the users who logged out of ServiceNow due to session expiry or other reasons. Use the login link on the external logout page to again log in to ServiceNow in case of successful logout.
    -   Display of a generic error message for unsuccessful single log out.
    -   Enhanced email notifications for SAML certificate and Encryption Key store update.
-   **[FIDO2 as an MFA factor](https://servicenow-staging.fluidtopics.net/access?context=mfa-with-fido&family=zurich&ft:locale=en-US)**

Use the FIDO factor policy to enforce FIDO \(Hardware key or Biometric as second factor for authentication\) as second factor authentication to users who attempt to log in to the instance.

-   **[OAuth integrations](https://servicenow-staging.fluidtopics.net/access?context=oauth-inbound-and-outbound&family=zurich&ft:locale=en-US)**

Configure OAuth integration that includes the following enhancements:

    -   You can provide a maximum client secret length up to 4096 characters to meet security requirements of the third-party systems.
    -   You can provide a JSON Web Key Set \(JWKS\) URL to automatically manage and update the public key for JSON Web Tokens \(JWT\) signature validation.
    -   You can request OAuth tokens using the JWT grant type signed with Elliptic Curve Digital Signature Algorithm \(ES\) signing algorithms, including ES256, ES384, and ES512, for inbound JSON Web Tokens \(JWT\). It also supports RS256, RS384, RS512, HS256, HS384, and HS512.
    -   You can customize the JWT ID \(JTI\) claim name in both inbound OpenID Connect \(OIDC\) and JWT Bearer flows.

</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Authentication features or functionality were removed.

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Authentication features or functionality were deprecated.

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

 See [Authentication](https://servicenow-staging.fluidtopics.net/access?context=c_Authentication&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

[Yokohama Patch 11](https://servicenow-staging.fluidtopics.net/access?context=yokohama-patch-11&family=yokohama&ft:locale=en-US)

-   **[Authentication factors for AI voice service](https://servicenow-staging.fluidtopics.net/access?context=authentication-factors&family=yokohama&ft:locale=en-US)**

Enable caller access to AI voice agents by configuring the required identification and authentication factors.

-   **[OAuth enhancements](https://servicenow-staging.fluidtopics.net/access?context=api-inbound-and-outbound&family=yokohama&ft:locale=en-US)**

Following are the OAuth enhancements:

    -   Use **Opaque** or **JWT token** option for your inbound integration endpoints.
    -   Use the **Allow access only to APIs in selected scope** option to enable access to the APIs that are explicitly listed in the selected scopes for your inbound integrations.
    -   Use the OAuth Entity Resource tab for outbound integrations to configure resource parameters so they flow into the OAuth token request and are reflected in the token from your OAuth provider.
-   **[Provider name for Inbound integrations](https://servicenow-staging.fluidtopics.net/access?context=new-inbound-integrations&family=yokohama&ft:locale=en-US)**

Use the Provider name field to enter the details of your inbound integrations to distinguish between different inbound integrations on your ServiceNow AI Platform®. Update the Provider name in your API integrations to improve monitoring capabilities:

    -   For OAuth integrations, update the provider name using the Provider name field. To know more, see [OAuth Inbound](https://servicenow-staging.fluidtopics.net/access?context=oauth-inbound&family=yokohama&ft:locale=en-US).
    -   For Basic authentication integrations, update the Provider name in the integration registration form.

 [Yokohama Patch 7](https://servicenow-staging.fluidtopics.net/access?context=yokohama-patch-7&family=yokohama&ft:locale=en-US)

-   **OAuth token enhancement**

Use Opaque or JWT token option for your inbound integration endpoints.


 Yokohama

-   Use Continuous Authentication to require step-up authentication or re-authentication to the users before allowing access to sensitive or high-privilege information.
-   Multi-factor Authentication \(MFA\) is enforced by default for all non-SSO login to ServiceNow®.
-   Use the Authorization code, resource owner password credential, SAML bearer, and JWT bearer OAuth grant types of OAuth for outbound integration requests through the MID Server.

 See [Authentication](https://servicenow-staging.fluidtopics.net/access?context=c_Authentication&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

[Zurich Patch 4](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   **[Authentication factors for AI voice service](https://servicenow-staging.fluidtopics.net/access?context=authentication-factors&family=zurich&ft:locale=en-US)**

Enable caller access to AI voice agents by configuring the required identification and authentication factors.

-   **[OAuth enhancements](https://servicenow-staging.fluidtopics.net/access?context=api-inbound-and-outbound&family=zurich&ft:locale=en-US)**

Following are the OAuth enhancements:

    -   Use **Opaque** or **JWT** token option for your inbound integration endpoints.
    -   Use the **Allow access only to APIs in selected scope** option to enable access to the APIs that are explicitly listed in the selected scopes for your inbound integrations.
    -   Use the OAuth Entity Resource tab for outbound integrations to configure resource parameters so they flow into the OAuth token request and are reflected in the token from your OAuth provider.

 [Zurich Patch 3](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-1&family=zurich&ft:locale=en-US)

-   **[Provider name for Inbound integrations](https://servicenow-staging.fluidtopics.net/access?context=new-inbound-integrations&family=zurich&ft:locale=en-US)**

Use the Provider name field to enter the details of your inbound integrations to distinguish between different inbound integrations on your ServiceNow AI Platform®. Update the Provider name in your API integrations to improve monitoring capabilities:

    -   For OAuth integrations, update the provider name using the Provider name field. To know more, see [OAuth inbound](https://servicenow-staging.fluidtopics.net/access?context=oauth-inbound&family=zurich&ft:locale=en-US).
    -   For Basic authentication integrations, update the Provider name in the integration registration form. To know more about the integration registration form, see [View dashboard](https://servicenow-staging.fluidtopics.net/access?context=view-inbound-api-integration-usage-dashboard&family=zurich&ft:locale=en-US).

 [Zurich Patch 1](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-1&family=zurich&ft:locale=en-US)

-   **OAuth token enhancement**

Use Opaque or JWT token option for your inbound integration endpoints.


 Zurich

-   Experience the new Inbound integration configuration in the Machine Identity Console.
-   Use the new MFA Dashboard to understand insights such as MFA user enrollment, privileged admins who haven't opted in to MFA, and compliance.
-   Use the FIDO factor policy to enforce FIDO-based authentication.
-   Use the enhanced SSO login and logout experience.
-   Configure the authentication policies to restrict access, reduce roles, or enforce MFA based on Identity Provider \(IdP\) attributes that are received from the OIDC response.

 See [Authentication](https://servicenow-staging.fluidtopics.net/access?context=c_Authentication&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-xanadu-zurich/rn-combined-intro.md)

