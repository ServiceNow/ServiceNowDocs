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

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   **[Knowledge-based factor enhancement for AI voice service](https://www.servicenow.com/docs/access?context=knowledge-based-authentication&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Following are the knowledge-based authentication \(KBA\) enhancements:

    -   [Voice input support for KBA questions](https://www.servicenow.com/docs/access?context=create-knowledge-based-questions&version=zurich&pubname=zurich-platform-security&ft:locale=en-US): Configure KBA questions to support Voice as an input type, allowing users to provide spoken responses during identification and authentication. When Voice input is enabled, you can configure the expected format, provide examples, and optionally define a validation pattern using regular expressions.
    -   [Script-based validation for external systems](https://www.servicenow.com/docs/access?context=create-knowledge-based-answers&version=zurich&pubname=zurich-platform-security&ft:locale=en-US): Configure KBA answers to validate that are created against external systems using custom scripts through the Script Configuration field. When set to Identification mode, you can write scoped scripts that validate caller identity against external authentication systems instead of internal ServiceNow AI Platform tables.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   **[Authentication factors for AI voice service](https://www.servicenow.com/docs/access?context=authentication-factors&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Enable caller access to AI voice agents by configuring the required identification and authentication factors.

-   **[OAuth enhancements](https://www.servicenow.com/docs/access?context=api-inbound-and-outbound&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Following are the OAuth enhancements:

    -   Use **Opaque** or **JWT** token option for your inbound integration endpoints.
    -   Use the **Allow access only to APIs in selected scope** option to enable access to the APIs that are explicitly listed in the selected scopes for your inbound integrations.
    -   Use the OAuth Entity Resource tab for outbound integrations to configure resource parameters so they flow into the OAuth token request and are reflected in the token from your OAuth provider.

[Zurich Patch 3](../quality/zurich-patch-1.md)

-   **[Provider name for Inbound integrations](https://www.servicenow.com/docs/access?context=new-inbound-integrations&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Use the Provider name field to enter the details of your inbound integrations to distinguish between different inbound integrations on your ServiceNow AI Platform®. Update the Provider name in your API integrations to improve monitoring capabilities:

    -   For OAuth integrations, update the provider name using the Provider name field. To know more, see [OAuth inbound](https://www.servicenow.com/docs/access?context=oauth-inbound&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).
    -   For Basic authentication integrations, update the Provider name in the integration registration form. To know more about the integration registration form, see [View Inbound API Integration Usage dashboard](https://www.servicenow.com/docs/access?context=view-inbound-api-integration-usage-dashboard&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   **OAuth token enhancement**

    Use Opaque or JWT token option for your inbound integration endpoints.


Zurich

-   Experience the new Inbound integration configuration in the Machine Identity Console.
-   Use the new MFA Dashboard to understand insights such as MFA user enrollment, privileged admins who haven't opted in to MFA, and compliance.
-   Use the FIDO factor policy to enforce FIDO-based authentication.
-   Use the enhanced SSO login and logout experience.
-   Configure the authentication policies to restrict access, reduce roles, or enforce MFA based on Identity Provider \(IdP\) attributes that are received from the OIDC response.

See [Authentication](https://www.servicenow.com/docs/access?context=c_Authentication&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) for more information.

## New in the Zurich release

-   **[Machine Identity Console](https://www.servicenow.com/docs/access?context=machine-identity-console&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Manage your inbound integration with ServiceNow's Machine Identity Console. Inbound integration in Machine Identity Console provides a simplified configuration experience for your inbound integrations.

-   **[Multi-factor Authentication dashboard](https://www.servicenow.com/docs/access?context=mfa-dashboard&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Use the new MFA Dashboard to understand insights such as MFA user enrollment, privileged admins who haven't opted in to MFA, and compliance. You can verify that all users have MFA enabled for enhanced security with the help of the MFA Dashboard.

-   **[Multi-factor Authentication Guided Setup](https://www.servicenow.com/docs/access?context=mfa-guided-setup&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Use the new MFA Guided setup to configure multi-factor Authentication \(MFA\) for users who currently log in to ServiceNow with only a user name and password. This update enhances security by guiding administrators through the MFA setup process and verifying that all users are protected with an additional layer of authentication.


-   **[Identity Provider attributes for OpenID Connect](https://www.servicenow.com/docs/access?context=idp-attributes-oidc&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Use the Identity Provider \(IDP\) Attributes received from the OIDC response from the Identity Provider as a filter criteria for authentication.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Enhanced SSO login and logout experience](https://www.servicenow.com/docs/access?context=c_MultipleProviderSingleSignOn&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Use the enhanced SSO login and logout experience. Enhancement includes:

    -   Display of active SAML and OIDC Identity Providers \(IdPs\) on the ServiceNow platform and portal login pages.
    -   Assign users to specific groups during SAML and OIDC auto-provisioning.
    -   Set up OIDC with the same well-known URL. The OIDC configurations can use the same well-known URL of the IdPs for multiple SSO records.
    -   Display login failure reasons to the users who logged out of ServiceNow due to session expiry or other reasons. Use the login link on the external logout page to again log in to ServiceNow in case of successful logout.
    -   Display of a generic error message for unsuccessful single log out.
    -   Enhanced email notifications for SAML certificate and Encryption Key store update.
-   **[FIDO2 as an MFA factor](https://www.servicenow.com/docs/access?context=mfa-with-fido&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Use the FIDO factor policy to enforce FIDO \(Hardware key or Biometric as second factor for authentication\) as second factor authentication to users who attempt to log in to the instance.

-   **[OAuth integrations](https://www.servicenow.com/docs/access?context=oauth-inbound-and-outbound&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

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

-   **[Secure your instance](https://www.servicenow.com/docs/access?context=platsec-landing&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    [Platform Security](https://www.servicenow.com/docs/access?context=platsec-landing&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) is built into all levels of the ServiceNow AI Platform. Implement the security features that are appropriate for your organization. Manage failed log in and encrypted password protection, access control rules, and audit logs.


**Parent Topic:**[ServiceNow AI Platform security release notes](now-platform-security-rn-landing.md)

