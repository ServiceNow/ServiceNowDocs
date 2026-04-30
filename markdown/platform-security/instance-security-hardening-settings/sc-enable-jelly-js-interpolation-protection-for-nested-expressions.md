---
title: Enable Jelly JS interpolation protection for nested expressions \[Updated in Security Center 2.0\]
description: Manage the interpolation protection on your instance.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Enable Jelly JS interpolation protection for nested expressions \[Updated in Security Center 2.0\]

Manage the interpolation protection on your instance.

Use the **glide.ui.jelly.js\_interpolation.protect\_nested\_expressions**property to manage interpolation protection. Interpolation protection ensures that when Jelly expressions are used in JavaScript, that they must be deemed as safe by either falling under certain categories or being marked as SAFE in the expression itself. Without this mitigation enabled, a bad actor can send a GET parameter to a Jelly page and cause the contents of that parameter to be evaluated as server-side JavaScript with admin privileges. If this property is not set to the recommended value of **true**, malicious Jelly expressions interpolated in JavaScript are allowed and a user can execute code using a Jelly template.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.ui.jelly.js\_interpolation.protect\_nested\_expressions**

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

false

</td></tr><tr><td>

Category

</td><td>

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 9
-   CVSS score: Critical
-   Security risk details: If the property is set to **false**, then malicious Jelly expressions are allowed.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

