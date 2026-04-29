---
title: Enable Jelly JS interpolation protection for nested expressions
description: Manage the interpolation protection on your instance.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Enable Jelly JS interpolation protection for nested expressions

Manage the interpolation protection on your instance.

Use the **glide.ui.jelly.js\_interpolation.protect\_nested\_expressions** system property to turn on or off interpolation protection specifically for nested Jelly expressions. Interpolation protection ensures that when Jelly expressions are used in JavaScript, they must be deemed safe by either falling under certain categories OR being marked as SAFE in the expression itself. This property was added to protect against possibly dangerous Jelly expressions which are nested in another Jelly expression.

Ensure that the **glide.ui.jelly.js\_interpolation.protect\_nested\_expressions** system property exists and is set to the value **true**. If the property does not appear in the System Properties \[sys\_properties\] table, add a new record.

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

true

</td></tr><tr><td>

Fallback value

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
-   Security risk details: Unprotected interpolated jelly expression may result in a malicious actor sending a crafted GET parameter to a Jelly page and cause the contents of that parameter to be evaluated as server-side JavaScript with admin privileges.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

