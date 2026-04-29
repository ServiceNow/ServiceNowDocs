---
title: Enforce strict security of session cookies
description: Use the glide.ui.secure\_cookies property to require properly formatted cookies
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Enforce strict security of session cookies

Use the **glide.ui.secure\_cookies** property to require properly formatted cookies

If **glide.ui.secure\_cookies** isn't set to the recommended value of **true**, then additional cookie security and strict cookie validation isn't performed.

Ensure that the property **glide.ui.secure\_cookies** is set to **true**.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.ui.secure\_cookies**

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

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

true

</td></tr><tr><td>

Category

</td><td>

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 7.1
-   CVSS rating: High
-   Security risk details: This could allow an attacker to bypass cookie validation leading to unauthorized resource access.

</td></tr><tr><td>

Functional impact

</td><td>

When the property is set to true, improperly formatted cookies are rejected. When such a cookie is rejected, the user must login again.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

