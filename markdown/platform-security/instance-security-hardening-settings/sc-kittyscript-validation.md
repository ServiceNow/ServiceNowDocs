---
title: Enforce KittyScript validation for guest sessions
description: The com.glide.script.kittyscript.validation.mode property controls JavaScript validation for unauthenticated \(guest\) users before it runs in the server-side sandbox.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-kittyscript-validation.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [kittyscript validation, javascript validation]
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Enforce KittyScript validation for guest sessions

The **com.glide.script.kittyscript.validation.mode** property controls JavaScript validation for unauthenticated \(guest\) users before it runs in the server-side sandbox.

-   `block` or `block_guest`: Rejects scripts that use syntax or operations outside a minimal, restricted set.
-   `warn` or `ignore`: Reduces or removes enforcement, allowing guest scripts to run under the platform's legacy sandbox restrictions only.

Set the **com.glide.script.kittyscript.validation.mode** property to `block` or `block_guest` in the `sys_properties` table. If it doesn't exist, create it and set it to `block`.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.glide.script.kittyscript.validation.mode**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

String

</td></tr><tr><td>

Recommended value

</td><td>

block

</td></tr><tr><td>

Default value

</td><td>

block

</td></tr><tr><td>

Fallback value

</td><td>

block\_guest

</td></tr><tr><td>

Category

</td><td>

[Validation, sanitization, and encoding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/validation-sanitization-encoding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 9.1
-   CVSS rating: Critical
-   Security risk details:

Allowing unauthenticated users to execute server-side JavaScript is a critical security risk. This code runs with server-side privileges and bypasses ordinary access controls. No valid credentials or user interaction is required to trigger it.

An attacker who reaches this capability can use it to read, modify, or exfiltrate data, and to bypass the business logic and access restrictions that would otherwise apply.


</td></tr><tr><td>

Functional impact

</td><td>

This property controls how the server-side sandbox validates JavaScript in guest sessions.

 -   `ignore`: Disables validation. Guest scripts execute without sandbox restrictions.
-   `warn`: Allows guest script execution. Scripts that violate sandbox restrictions are logged.
-   `block_guest` or `block`: Enforces sandbox restrictions. Scripts using unsupported syntax or disallowed operations are blocked.

 After enabling enforcement, test guest-facing functionality that uses dynamic script evaluation such as reference qualifiers and scripted default values to confirm it still works.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

The **com.glide.script.sandbox.ks.watchdog.enabled** property must be set to `true`.

</td></tr></tbody>
</table>**Parent Topic:**[Validation, sanitization, and encoding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/validation-sanitization-encoding.md)

