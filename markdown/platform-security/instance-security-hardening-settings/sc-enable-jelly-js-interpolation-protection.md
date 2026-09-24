---
title: Enable Jelly JS interpolation protection
description: Use the glide.ui.jelly.js\_interpolation.protect property to ensure that any JavaScript about to be executed on a Jelly page is protected from injection with the help of Jelly interpolation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-enable-jelly-js-interpolation-protection.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Enable Jelly JS interpolation protection

Use the **glide.ui.jelly.js\_interpolation.protect** property to ensure that any JavaScript about to be executed on a Jelly page is protected from injection with the help of Jelly interpolation.

The **glide.ui.jelly.js\_interpolation.protect** system property allows you to turn on or off interpolation protection. Interpolation protection ensures that when Jelly expressions are used in JavaScript, they must be deemed safe by either falling under certain categories OR being marked as SAFE in the expression itself. Without this mitigation enabled, a malicious actor can send a crafted GET parameter to a Jelly page and cause the contents of that parameter to be evaluated as server-side JavaScript with admin privileges.

Ensure that the property **glide.ui.jelly.js\_interpolation.protect** is set to **true**.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.ui.jelly.js\_interpolation.protect**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

Boolean

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

true in Australia and newer, false prior

</td></tr><tr><td>

Fallback value

</td><td>

true in Australia and newer, false prior

</td></tr><tr><td>

Category

</td><td>

[Validation, sanitization, and encoding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/validation-sanitization-encoding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 9.0
-   CVSS rating: Critical
-   Security risk details: Dangerous jelly expressions interpolated in JavaScript are allowed and user can execute code using jelly template.

</td></tr><tr><td>

Functional impact

</td><td>

Enabling this property causes the platform to reject Jelly JavaScript expressions that aren't explicitly recognized as safe or marked as SAFE. Instance owners should test custom UI pages, macros, and portal widgets that use Jelly-interpolated JavaScript expressions after making this change. Confirm that legitimate expressions continue to render as expected. Custom Jelly content that relies on dynamic, unmarked expressions require updates to use the SAFE designation to continue functioning.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Validation, sanitization, and encoding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/validation-sanitization-encoding.md)

