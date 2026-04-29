---
title: Disable AJAXEvaluate
description: Use the glide.script.allow.ajaxevaluate to protect the system API from vulnerabilities of Client script execution through AJAX calls.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Disable AJAXEvaluate

Use the **glide.script.allow.ajaxevaluate** to protect the system API from vulnerabilities of Client script execution through AJAX calls.

The AjaxEvaluator processor executes these scripts in sandbox however there are several additional properties which can allow the scope of activities in the sandbox to expand or be turned off entirely. In a worst case scenario a user can easily execute scripts as an admin privilege.

Ensure that the **glide.script.allow.ajaxevaluate** system property is set to **false**.

Elevation to the security\_admin role is required to edit the property.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.script.allow.ajaxevaluate**

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

false

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

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

-   Severity score: 7.3
-   CVSS rating: High
-   Security risk details: If this property is not set to **false**, then the system API can be vulnerable to client script execution through AJAX calls.

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

