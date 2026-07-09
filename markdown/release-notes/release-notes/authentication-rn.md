---
title: Authentication release notes
description: The ServiceNow Authentication application supports many authentication mechanisms that enable you to validate the identity of users. Authentication was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
---

# Authentication release notes

The ServiceNow® Authentication application supports many authentication mechanisms that enable you to validate the identity of users. Authentication was enhanced and updated in the Zurich release.

## Authentication highlights for the Zurich release

[Zurich Patch 10](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-10.md)

-   **[Knowledge-based factor enhancement for AI voice service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/knowledge-based-authentication.md)**

    Following are the knowledge-based authentication \(KBA\) enhancements:

    -   Email OTP as an authentication factor for AI voice service: Use Email OTP as a standalone factor, a primary factor, or a secondary factor in AI voice agent authentication flows. When a caller reaches the voice agent, a one-time password is sent to their registered email address. The caller provides the password to complete authentication.
    -   KBA for AI voice service: Use the KBA setup to configure Knowledge-Based Authentication \(KBA\) for the voice channel. Choose from base system questions at both the identification level and the authentication level. AI voice service mappings are populated automatically from your Assistant Designer selection, so manually mapping voice services is no longer a mandatory step in the KBA setup.
    -   Authenticate callers at the start of every call: Prompt callers for authentication or identification details at the start of every call, before the voice-only assistant responds to any request, using the Authenticate at the start of the call option on the Assistant Designer's Caller verification page.

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   **[Authentication factors for AI voice service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/authentication-factors.md)**

    Enable caller access to AI voice agents by configuring the required identification and authentication factors.

-   **[OAuth enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/api-inbound-and-outbound.md)**

    Following are the OAuth enhancements:

    -   Use **Opaque** or **JWT** token option for your inbound integration endpoints.
    -   Use the **Allow access only to APIs in selected scope** option to enable access to the APIs that are explicitly listed in the selected scopes for your inbound integrations.
    -   Use the OAuth Entity Resource tab for outbound integrations to configure resource parameters so they flow into the OAuth token request and are reflected in the token from your OAuth provider.

[Zurich Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)

-   **[Provider name for Inbound integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/new-inbound-integrations.md)**

    Use the Provider name field to enter the details of your inbound integrations to distinguish between different inbound integrations on your ServiceNow AI Platform®. Update the Provider name in your API integrations to improve monitoring capabilities:

    -   For OAuth integrations, update the provider name using the Provider name field. To know more, see [OAuth inbound](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/oauth-inbound.md).
    -   For Basic authentication integrations, update the Provider name in the integration registration form. To know more about the integration registration form, see [View Inbound API Integration Usage dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/web-services/view-inbound-api-integration-usage-dashboard.md).

[Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)

-   **OAuth token enhancement**

    Use Opaque or JWT token option for your inbound integration endpoints.


Zurich

-   Experience the new Inbound integration configuration in the Machine Identity Console.
-   Use the new MFA Dashboard to understand insights such as MFA user enrollment, privileged admins who haven't opted in to MFA, and compliance.
-   Use the FIDO factor policy to enforce FIDO-based authentication.
-   Use the enhanced SSO login and logout experience.
-   Configure the authentication policies to restrict access, reduce roles, or enforce MFA based on Identity Provider \(IdP\) attributes that are received from the OIDC response.

See [Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/c_Authentication.md) for more information.

## New in the Zurich release

-   **[Machine Identity Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/machine-identity-console.md)**

    Manage your inbound integration with ServiceNow's Machine Identity Console. Inbound integration in Machine Identity Console provides a simplified configuration experience for your inbound integrations.

-   **[Multi-factor Authentication dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/mfa-dashboard.md)**

    Use the new MFA Dashboard to understand insights such as MFA user enrollment, privileged admins who haven't opted in to MFA, and compliance. You can verify that all users have MFA enabled for enhanced security with the help of the MFA Dashboard.

-   **[Multi-factor Authentication Guided Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/mfa-guided-setup.md)**

    Use the new MFA Guided setup to configure multi-factor Authentication \(MFA\) for users who currently log in to ServiceNow with only a user name and password. This update enhances security by guiding administrators through the MFA setup process and verifying that all users are protected with an additional layer of authentication.


-   **[Identity Provider attributes for OpenID Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/idp-attributes-oidc.md)**

    Use the Identity Provider \(IDP\) Attributes received from the OIDC response from the Identity Provider as a filter criteria for authentication.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Enhanced SSO login and logout experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/c_MultipleProviderSingleSignOn.md)**

    Use the enhanced SSO login and logout experience. Enhancement includes:

    -   Display of active SAML and OIDC Identity Providers \(IdPs\) on the ServiceNow platform and portal login pages.
    -   Assign users to specific groups during SAML and OIDC auto-provisioning.
    -   Set up OIDC with the same well-known URL. The OIDC configurations can use the same well-known URL of the IdPs for multiple SSO records.
    -   Display login failure reasons to the users who logged out of ServiceNow due to session expiry or other reasons. Use the login link on the external logout page to again log in to ServiceNow in case of successful logout.
    -   Display of a generic error message for unsuccessful single log out.
    -   Enhanced email notifications for SAML certificate and Encryption Key store update.
-   **[FIDO2 as an MFA factor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/mfa-with-fido.md)**

    Use the FIDO factor policy to enforce FIDO \(Hardware key or Biometric as second factor for authentication\) as second factor authentication to users who attempt to log in to the instance.

-   **[OAuth integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/oauth-inbound-and-outbound.md)**

    Configure OAuth integration that includes the following enhancements:

    -   You can provide a maximum client secret length up to 4096 characters to meet security requirements of the third-party systems.
    -   You can provide a JSON Web Key Set \(JWKS\) URL to automatically manage and update the public key for JSON Web Tokens \(JWT\) signature validation.
    -   You can request OAuth tokens using the JWT grant type signed with Elliptic Curve Digital Signature Algorithm \(ES\) signing algorithms, including ES256, ES384, and ES512, for inbound JSON Web Tokens \(JWT\). It also supports RS256, RS384, RS512, HS256, HS384, and HS512.
    -   You can customize the JWT ID \(JTI\) claim name in both inbound OpenID Connect \(OIDC\) and JWT Bearer flows.

## Deprecations

Due to the launch of new simplified inbound integration configuration in Machine Identity Console, the following inbound integrations configurations in the Application registry page are deprecated:

-   OAuth API endpoint for external clients
-   OAuth JWT API endpoint for external clients
-   OIDC provider to verify ID tokens

## Activation information

Authentication is a ServiceNow AI Platform product that is active by default.

## Related ServiceNow applications and features

-   **[Secure your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/platsec-landing.md)**

    [Platform Security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/platsec-landing.md) is built into all levels of the ServiceNow AI Platform. Implement the security features that are appropriate for your organization. Manage failed log in and encrypted password protection, access control rules, and audit logs.


**Parent Topic:**[ServiceNow AI Platform security release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-platform-security-rn-landing.md)

