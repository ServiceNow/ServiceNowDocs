---
title: Enable the hardened java security manager
description: The glide.security.manager property contains the Java classname of the current Java security manager.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Enable the hardened java security manager

The **glide.security.manager** property contains the Java classname of the current Java security manager.

The **glide.security.manager** system property contains Java classname of current Java security manager. ServiceNow has standardized on the Contextual Security Manager. If **glide.security.manager** is not set to the recommended value of `com.glide.sys.security.ContextualSecurityManager`, then the instance may be using an obsolete Java security manager, which is missing expected hardening policies.

Ensure the property **glide.security.manager** is set to `com.glide.sys.security.ContextualSecurityManager`.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.security.manager**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

string

</td></tr><tr><td>

Recommended value

</td><td>

com.glide.sys.security.ContextualSecurityManager

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback valye

</td><td>

com.glide.sys.security.ContextualSecurityManager

</td></tr><tr><td>

Category

</td><td>

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 7.2
-   CVSS score: High
-   Security risk details:Without this hardening, it may be possible for a malicious actor with script execution access to achieve remote code execution on the instance.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

