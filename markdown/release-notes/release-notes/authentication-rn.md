---
title: Authentication release notes
description: The ServiceNow Authentication application supports many authentication mechanisms that enable you to validate the identity of users. Authentication was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
---

# Authentication release notes

The ServiceNow® Authentication application supports many authentication mechanisms that enable you to validate the identity of users. Authentication was enhanced and updated in the Yokohama release.

## Authentication highlights for the Yokohama release

[Yokohama Patch 13](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-13.md)

-   **Knowledge-based factor enhancement for AI voice service**

    Following are the knowledge-based authentication \(KBA\) enhancements:

    -   Voice input support for KBA questions: Configure KBA questions to support Voice as an input type, allowing users to provide spoken responses during identification and authentication. When Voice input is enabled, you can configure the expected format, provide examples, and optionally define a validation pattern using regular expressions.
    -   Script-based validation for external systems: Configure KBA answers to validate that are created against external systems using custom scripts through the Script Configuration field. When set to Identification mode, you can write scoped scripts that validate caller identity against external authentication systems instead of internal ServiceNow AI Platform tables.

[Yokohama Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-11.md)

-   **Authentication factors for AI voice service**

    Enable caller access to AI voice agents by configuring the required identification and authentication factors.

-   **OAuth enhancements**

    Following are the OAuth enhancements:

    -   Use **Opaque** or **JWT token** option for your inbound integration endpoints.
    -   Use the **Allow access only to APIs in selected scope** option to enable access to the APIs that are explicitly listed in the selected scopes for your inbound integrations.
    -   Use the OAuth Entity Resource tab for outbound integrations to configure resource parameters so they flow into the OAuth token request and are reflected in the token from your OAuth provider.
-   **Provider name for Inbound integrations**

    Use the Provider name field to enter the details of your inbound integrations to distinguish between different inbound integrations on your ServiceNow AI Platform®. Update the Provider name in your API integrations to improve monitoring capabilities:

    -   For OAuth integrations, update the provider name using the Provider name field. To know more, see .
    -   For Basic authentication integrations, update the Provider name in the integration registration form.

[Yokohama Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-7.md)

-   **OAuth token enhancement**

    Use Opaque or JWT token option for your inbound integration endpoints.


Yokohama

-   Use Continuous Authentication to require step-up authentication or re-authentication to the users before allowing access to sensitive or high-privilege information.
-   Multi-factor Authentication \(MFA\) is enforced by default for all non-SSO login to ServiceNow®.
-   Use the Authorization code, resource owner password credential, SAML bearer, and JWT bearer OAuth grant types of OAuth for outbound integration requests through the MID Server.

See Authentication for more information.

## New in the Yokohama release

-   ****

    Use Continuous Authentication to require step-up authentication or re-authentication to the users before allowing access to sensitive or high-privilege information.

-   **OAuth Grant Types for MID Server**

    Use the Authorization code, resource owner password credential, SAML bearer, and JWT bearer OAuth grant types of OAuth for outbound integration requests through the MID Server. Personal Auth is also supported through the MID server. MID Servers facilitate communication and data movement between a single ServiceNow® instance and external applications, data sources, and services.


## Changed in this release

-   ****

    MFA is mandated and is enforced to all the non-SSO login users accessing ServiceNow®.


## Activation information

Authentication is a ServiceNow AI Platform product that is active by default.

## Related ServiceNow applications and features

-   ****

    Platform Security is built into all levels of the ServiceNow AI Platform. Implement the security features that are appropriate for your organization. Manage failed logins and encrypted password protection, access control rules, and audit logs.


**Parent Topic:**[ServiceNow AI Platform security release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-platform-security-rn-landing.md)

