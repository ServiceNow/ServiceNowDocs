---
title: IFL policy field reference
description: Field descriptions for an identifier-first login \(IFL\) policy in the Authentication console.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/ngle-console-field-reference.html
release: brazil
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 1
keywords: [IFL policy fields, NGLE console field reference]
breadcrumb: [Authentication Console, Authentication, Access Management]
---

# IFL policy field reference

Field descriptions for an identifier-first login \(IFL\) policy in the Authentication console.

## IFL policy fields

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Name**

</td><td>

A unique name for the policy. Required.

</td></tr><tr><td>

**Description**

</td><td>

An optional description of the policy.

</td></tr><tr><td>

**Authentication method**

</td><td>

The authentication method applied when the policy matches: -   **SSO login** — Routes the user to an organization identity provider selected in Select an Identity Provider. Available only when the Multi-Provider SSO plugin is installed and at least one identity provider is configured.
-   **Use Password** — Routes the user to log in with a username and password managed within the platform.

</td></tr><tr><td>

**Select an Identity Provider**

</td><td>

The identity provider used when the authentication method is SSO login.

</td></tr><tr><td>

**Conditions**

</td><td>

The criteria that determine when the policy applies, built from Field and Operator rows. Combine conditions using and logic, and group them into condition sets with Add condition set. Fields include user-context attributes such as role, group, and IP address.

</td></tr><tr><td>

**Active**

</td><td>

Whether the policy is applied during user login. Only active policies are evaluated; inactive policies are skipped.

</td></tr><tr><td>

**Policy order**

</td><td>

A numeric value that defines the evaluation order \(for example, 100, 200, 300\). Required. Policies are evaluated by order value, and lower values are executed first.

</td></tr></tbody>
</table>