---
title: Authentication release notes
description: The ServiceNow Authentication application supports many authentication mechanisms that enable you to validate the identity of users. Authentication was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
---

# Authentication release notes

The ServiceNow® Authentication application supports many authentication mechanisms that enable you to validate the identity of users. Authentication was enhanced and updated in the Yokohama release.

## Authentication highlights for the Yokohama release

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   **[Authentication factors for AI voice service](https://www.servicenow.com/docs/access?context=authentication-factors&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

    Enable caller access to AI voice agents by configuring the required identification and authentication factors.

-   **[OAuth enhancements](https://www.servicenow.com/docs/access?context=api-inbound-and-outbound&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

    Following are the OAuth enhancements:

    -   Use **Opaque** or **JWT token** option for your inbound integration endpoints.
    -   Use the **Allow access only to APIs in selected scope** option to enable access to the APIs that are explicitly listed in the selected scopes for your inbound integrations.
    -   Use the OAuth Entity Resource tab for outbound integrations to configure resource parameters so they flow into the OAuth token request and are reflected in the token from your OAuth provider.
-   **Provider name for Inbound integrations**

    Use the Provider name field to enter the details of your inbound integrations to distinguish between different inbound integrations on your ServiceNow AI Platform®. Update the Provider name in your API integrations to improve monitoring capabilities:

    -   For OAuth integrations, update the provider name using the Provider name field. To know more, see [OAuth Inbound](https://www.servicenow.com/docs/access?context=oauth-inbound&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).
    -   For Basic authentication integrations, update the Provider name in the integration registration form.

[Yokohama Patch 7](../quality/yokohama-patch-7.md)

-   **OAuth token enhancement**

    Use Opaque or JWT token option for your inbound integration endpoints.


Yokohama

-   Use Continuous Authentication to require step-up authentication or re-authentication to the users before allowing access to sensitive or high-privilege information.
-   Multi-factor Authentication \(MFA\) is enforced by default for all non-SSO login to ServiceNow®.
-   Use the Authorization code, resource owner password credential, SAML bearer, and JWT bearer OAuth grant types of OAuth for outbound integration requests through the MID Server.

See [Authentication](https://www.servicenow.com/docs/access?context=c_Authentication&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) for more information.

## New in the Yokohama release

-   **[Continuous Authentication](https://www.servicenow.com/docs/access?context=ca-homepage&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

    Use Continuous Authentication to require step-up authentication or re-authentication to the users before allowing access to sensitive or high-privilege information.

-   **[OAuth Grant Types for MID Server](https://www.servicenow.com/docs/access?context=oauth-outbound&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

    Use the Authorization code, resource owner password credential, SAML bearer, and JWT bearer OAuth grant types of OAuth for outbound integration requests through the MID Server. Personal Auth is also supported through the MID server. MID Servers facilitate communication and data movement between a single ServiceNow® instance and external applications, data sources, and services.


## Changed in this release

-   **[Multi-factor Authentication enforcement](https://www.servicenow.com/docs/access?context=mfa-enforcement&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

    MFA is mandated and is enforced to all the non-SSO login users accessing ServiceNow®.


## Activation information

Authentication is a ServiceNow AI Platform product that is active by default.

## Related ServiceNow applications and features

-   **[Secure your instance](https://www.servicenow.com/docs/access?context=platsec-landing&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

    Platform Security is built into all levels of the ServiceNow AI Platform. Implement the security features that are appropriate for your organization. Manage failed logins and encrypted password protection, access control rules, and audit logs.


**Parent Topic:**[ServiceNow AI Platform security release notes](now-platform-security-rn-landing.md)

