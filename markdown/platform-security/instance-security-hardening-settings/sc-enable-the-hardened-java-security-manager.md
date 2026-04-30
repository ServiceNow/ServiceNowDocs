---
title: Enable the hardened java security manager \[New in Security Center 1.3\]
description: The glide.security.manager property contains the Java classname of the current Java security manager.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Enable the hardened java security manager \[New in Security Center 1.3\]

The **glide.security.manager** property contains the Java classname of the current Java security manager.

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

**com.glide.sys.security.ContextualSecurityManager**

</td></tr><tr><td>

Default value

</td><td>

**com.glide.sys.security.ContextualSecurityManager**

</td></tr><tr><td>

Category

</td><td>

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 7.2
-   CVSS score: High
-   Security risk details: If **glide.security.manager** is not set to the recommended value of **com.glide.sys.security.ContextualSecurityManager**, then the instance may be using an obsolete Java security manager which is missing expected hardening policies. Without this hardening, a malicious actor with script execution access could get remote code execution on the instance.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

