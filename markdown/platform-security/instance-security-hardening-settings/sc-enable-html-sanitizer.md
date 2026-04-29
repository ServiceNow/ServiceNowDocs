---
title: Enable HTML Sanitizer within Virtual Agent
description: Use the com.glide.cs.html.sanitizer.enabled property to enable HTMLSanitizerService.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Enable HTML Sanitizer within Virtual Agent

Use the **com.glide.cs.html.sanitizer.enabled** property to enable HTMLSanitizerService.

The **com.glide.cs.html.sanitizer.enabled** system property controls the whether the HtmlSanitizerService is enabled. If **com.glide.cs.html.sanitizer.enabled** is not set to **true**, then a Stored Cross-Site Scripting \(XSS\) attack is possible in the VA web client.

Ensure that the property **com.glide.cs.html.sanitizer.enabled** is set to **true**.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.glide.cs.html.sanitizer.enabled**

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

-   Severity score: 8.0
-   CVSS rating: High
-   Security risk details: An XSS vulnerability can facilitate privilege escalation to higher-level roles, such as administrator, enabling broader lateral movement within the system.

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enforces HTML-output encoding mechanism before the user data is rendered back to the user. If customer has any customization that involves rendering of the HTML attribute or content data, then there is a functionality impact.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

