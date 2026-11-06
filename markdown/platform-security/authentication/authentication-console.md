---
title: Authentication Console
description: The Authentication Console enables administrators to configure and manage authentication behavior across a ServiceNow instance, including identifier-first login policies and related settings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/authentication/authentication-console.html
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Authentication Console, next-generation login experience, IFL, identifier first login, policy-based login, authentication configuration]
breadcrumb: [Authentication, Access Management]
---

# Authentication Console

The Authentication Console enables administrators to configure and manage authentication behavior across a ServiceNow instance, including identifier-first login policies and related settings.

The Authentication Console provides a centralized location for administrators to configure how users authenticate with a ServiceNow instance. The console ease presents authentication settings in a structured interface designed for administrators without requiring custom development.

The console is accessible to users with the `user_authn_admin` role. Navigate to **All** &gt; **Authentication** &gt; **Authentication Console** to open it.

## What the Authentication Console includes

The Authentication Console currently includes configuration for the policy-based login experience. Additional authentication configuration areas may be added in future releases.

-   **Identifier-first login policies**

    The Authentication Console enables administrators to configure identifier-first login for the instance. From this section, administrators can:

    -   Enable or disable the identifier-first login flow for the instance.
    -   View the list of all identifier-first login policies configured on the instance.
    -   Create, edit, activate, deactivate, and delete identifier-first login policies.
    -   Define conditions for each policy — such as IP address, role, and group — using a guided condition builder.
    -   Assign an authentication method to each policy — either SSO login or Use Password.
    -   Set and adjust the evaluation order of policies to control which policy takes precedence when multiple policies match a user.
    -   Configure the Override cookie-based redirects setting to control whether a previously stored IdP cookie is honored or bypassed during login routing.
-   **Settings**

    Contains instance-level toggles for the login experience, including the option to enable the identifier-first login flow and configure the Override cookie-based redirects setting.

    -   **Enable policy-based login** — the main setting that turns the experience on and determines the first authentication factor during login. See [Activate the policy-based login experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/activate-authentication-console.md).
    -   Identifier-first page options, such as showing identity provider tiles for direct login and showing recently used identifiers.
    -   SSO and identity provider routing options, which require the Multi-Provider SSO plugin. Without the plugin, these options are unavailable.
    -   Diagnostic options, such as detailed login-flow debug logging.

## Access and role requirements

Access to the Authentication Console is restricted to users with the `user_authn_admin` role. The following operations are available to users with this role:

|Operation|Description|
|---------|-----------|
|View identifier-first login policies|View the list of all identifier-first login policies and their current configuration.|
|Create identifier-first login policies|Create identifier-first login policies with conditions and an authentication method.|
|Edit identifier-first login policies|Modify the name, order, conditions, authentication method, or active status of an existing identifier-first login policy.|
|Activate or deactivate identifier-first login policies|Include or exclude a policy from login evaluation without deleting it.|
|Delete identifier-first login policies|Permanently remove an identifier-first login policy from the instance.|
|Manage instance settings|Enable or disable the policy-based login experience and configure the Override cookie-based redirects setting.|

