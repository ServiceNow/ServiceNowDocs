---
title: Disable JavaScript tags in embedded HTML
description: Use the glide.ui.security.codetag.allow\_script property to disable support for embedding HTML JavaScript code created using of the \[code\] tag.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-13"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Disable JavaScript tags in embedded HTML

Use the **glide.ui.security.codetag.allow\_script** property to disable support for embedding HTML JavaScript code created using of the \[code\] tag.

If **glide.ui.security.codetag.allow\_script** is not set to the recommended value of **false**, then this property allows rendered HTML in journal fields and forms which opens room for XSS attacks. Malicious HTML needs to be put between code tags for example \[code\]\[/code\].

Ensure that the **glide.ui.security.codetag.allow\_script** property exists in the System Properties \[sys\_properties\] table and is set to **false**.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.ui.security.codetag.allow\_script**

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

true

</td></tr><tr><td>

Category

</td><td>

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score:
-   CVSS rating:
-   Security risk details: Uncontrolled JavaScript risks Cross-Site Scripting \(XSS\) attacks, enabling malicious actors to inject and execute harmful scripts in the user's browser. Such attacks can lead to session hijacking, credential theft, and compromise of sensitive data.

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

