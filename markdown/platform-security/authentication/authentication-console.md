---
title: Authentication Console
description: The Authentication Console enables administrators to configure and manage authentication behavior across a ServiceNow instance, including identifier-first login policies and related settings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/authentication-console.html
release: brazil
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

The Authentication Console currently includes configuration for the next-generation login experience. Additional authentication configuration areas may be added in future releases.

-   **Identifier-first login \(IFL\) policies**

    The Authentication Console enables administrators to configure identifier-first login \(IFL\) for the instance. From this section, administrators can:

    -   Enable or disable the identifier-first login flow for the instance.
    -   View the list of all IFL policies configured on the instance.
    -   Create, edit, activate, deactivate, and delete IFL policies.
    -   Define conditions for each policy — such as IP address, role, group, department, company, domain, and location — using a guided condition builder.
    -   Assign an authentication method to each policy — either an SSO provider or local login.
    -   Set and adjust the evaluation order of policies to control which policy takes precedence when multiple policies match a user.
    -   Configure SSO cookie override behavior to control whether a previously stored SSO session cookie is honored or bypassed during login routing.
-   **Settings**

    Contains instance-level toggles for the login experience, including the option to enable the identifier-first login flow and configure SSO cookie override behavior.

    -   **Enable policy-based login** — the main setting that turns the experience on and determines the first authentication factor during login. See [Activate the policy-based login experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/activate-authentication-console.md).
    -   Identifier-first page options, such as showing identity provider tiles for direct login and showing recently used identifiers.
    -   SSO and identity provider routing options, which require the Multi-Provider SSO plugin. Without the plugin, these options are unavailable.
    -   Diagnostic options, such as detailed login-flow debug logging.

## Access and role requirements

Access to the Authentication Console is restricted to users with the `user_authn_admin` role. The following operations are available to users with this role:

|Operation|Description|
|---------|-----------|
|View IFL policies|View the list of all IFL policies and their current configuration.|
|Create IFL policies|Create IFL policies with conditions and an authentication method.|
|Edit IFL policies|Modify the name, order, conditions, authentication method, or active status of an existing IFL policy.|
|Activate or deactivate IFL policies|Include or exclude a policy from login evaluation without deleting it.|
|Delete IFL policies|Permanently remove an IFL policy from the instance.|
|Manage instance settings|Enable or disable the next-generation login experience and configure SSO cookie override behavior.|

