---
title: Authentication release notes
description: The ServiceNow Authentication application supports many authentication mechanisms that enable you to validate the identity of users. Authentication was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
---

# Authentication release notes

The ServiceNow® Authentication application supports many authentication mechanisms that enable you to validate the identity of users. Authentication was enhanced and updated in the Australia release.

## Authentication highlights for the Australia release

[Australia Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-3.md)

-   **Authentication factors enhancement for AI voice service**

    Following are the authentication factors enhancements:

    -   Email OTP as an authentication factor for AI voice service: Use Email OTP as a standalone factor, a primary factor, or a secondary factor in AI voice agent authentication flows. When a caller reaches the voice agent, a one-time password is sent to their registered email address. The caller provides the password to complete authentication.
    -   KBA for AI voice service: Use the KBA setup to configure Knowledge-Based Authentication \(KBA\) for the voice channel. Choose from base system questions at both the identification level and the authentication level. AI voice service mappings are populated automatically from your Assistant Designer selection, so manually mapping voice services is no longer a mandatory step in the KBA setup.
    -   Authenticate callers at the start of every call: Prompt callers for authentication or identification details at the start of every call, before the voice-only assistant responds to any request, using the Authenticate at the start of the call option on the Assistant Designer's Caller verification page.

[Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md)

-   **[Knowledge-based factor enhancement for AI voice service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/knowledge-based-authentication.md)**

    Following are the knowledge-based authentication \(KBA\) enhancements:

    -   [Voice input support for KBA questions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/create-knowledge-based-questions.md): Configure KBA questions to support Voice as an input type, allowing users to provide spoken responses during identification and authentication. When Voice input is enabled, you can configure the expected format, provide examples, and optionally define a validation pattern using regular expressions.
    -   [Script-based validation for external systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/create-knowledge-based-answers.md): Configure KBA answers to validate that are created against external systems using custom scripts through the Script Configuration field. When set to Identification mode, you can write scoped scripts that validate caller identity against external authentication systems instead of internal ServiceNow AI Platform tables.

Australia

-   Enable caller access to AI voice agents by configuring the required identification and authentication factors.
-   Secure the web embeddables feature for authenticating the ServiceNow®'s web components that are used in third-party portals.
-   Use the granular roles to complete administrative configuration tasks for Authentication without requiring the full admin role.
-   Use the enhanced Auth Scope for your Inbound Integrations.

See [Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/c_Authentication.md) for more information.

## New in the Australia release

-   **[Authentication factors for AI voice service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication-factors.md)**

    Enable caller access to AI voice agents by configuring the required identification and authentication factors.

-   **[Web Embeddables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/web-embeddables.md)**

    Secure the web embeddables feature for authenticating the ServiceNow®'s web components that are used in third-party portals.

-   **[Granular admin roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/granular-admin-roles.md)**

    The granular admin role enables developers and administrators to complete administrative configuration tasks for Authentication without requiring the full admin role.


## Changed in this release

-   **[OAuth enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/api-inbound-and-outbound.md)**

    Following are the OAuth enhancements:

    -   Use **Opaque** or **JWT** token option for your inbound integration endpoints.
    -   Use the **Allow access only to APIs in selected scope** option to enable access to the APIs that are explicitly listed in the selected scopes for your inbound integrations.
    -   Use the OAuth Entity Resource tab for outbound integrations to configure resource parameters so they flow into the OAuth token request and are reflected in the token from your OAuth provider.

## Deprecated features

-   Due to the launch of new simplified inbound integration configuration in Machine Identity Console, the following inbound integrations configurations in the Application registry page are deprecated:
    -   OAuth API endpoint for external clients
    -   OAuth JWT API endpoint for external clients
    -   OIDC provider to verify ID tokens
-   The \(`glide.login.no_blank_password`\) property is deprecated, since the property is no longer used and changing this property value doesn't effect login behavior.

## Activation information

Authentication is a ServiceNow AI Platform product that is active by default.

## Accessibility information

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Related ServiceNow applications and features

-   **[Secure your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/platsec-landing.md)**

    [Platform Security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/platsec-landing.md) is built into all levels of the ServiceNow AI Platform. Implement the security features that are appropriate for your organization. Manage failed log in and encrypted password protection, access control rules, and audit logs.


