---
title: Sanitize All Translated HTML Fields \[New in Security Center 2.0\]
description: Learn how to configure the glide.translated\_html.sanitize\_all\_fields property to the secure value to ensure that all translated\_html elements are sanitized with an HTML sanitizer.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Sanitize All Translated HTML Fields \[New in Security Center 2.0\]

Learn how to configure the **glide.translated\_html.sanitize\_all\_fields** property to the secure value to ensure that all **translated\_html** elements are sanitized with an HTML sanitizer.

When the **glide.translated\_html.sanitize\_all\_fields** property is set to true, all **translated\_html** elements are sanitized with an HTML sanitizer. If the property is set to false, only elements with the dictionary attribute **html\_sanitize** set to true will be sanitized. This sanitization helps prevent attackers from embedding malicious content that could lead to cross-site scripting \(XSS\) attacks.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.translated\_html.sanitize\_all\_fields**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

boolean

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Category

</td><td>

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.6
-   CVSS score: Medium
-   Security risk details: Not configuring this property to the secure value of true, doesn’t sanitize all HTML elements, which increases the likelihood of a bad actor embedding malicious content in a field.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

Allows customers to access any table information if the widget is set to public and included in the property's value.

</td></tr></tbody>
</table>**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

