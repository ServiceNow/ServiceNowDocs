---
title: Enforce HTML Sanitization
description: Use the com.glide.security.check\_unsanitized\_html property to enforce sanitization behavior of translated\_html fields on a global level for field assignments.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Enforce HTML Sanitization

Use the **com.glide.security.check\_unsanitized\_html** property to enforce sanitization behavior of translated\_html fields on a global level for field assignments.

The **com.glide.security.check\_unsanitized\_html** system property enforces sanitization behavior of translated\_html fields on a global level for field assignments.

Ensure that the property **com.glide.security.check\_unsanitized\_html** is set to `enforce`.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.glide.security.check\_unsanitized\_html**

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

enforce

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

log\_only

</td></tr><tr><td>

Category

</td><td>

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 7.3
-   CVSS rating: High
-   Security risk details: An attacker could be able to execute arbitrary javascript in the victim's browser \(XSS attacks\).

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

