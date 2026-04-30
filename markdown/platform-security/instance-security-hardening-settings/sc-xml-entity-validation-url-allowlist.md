---
title: Restrict XML external entities \[Updated in Security Center 1.3 and 2.0\]
description: Configure system properties to ensure that your instance only processes XML from trusted sources to help prevent XML external entity \(XXE\) attacks.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-01-22"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Restrict XML external entities \[Updated in Security Center 1.3 and 2.0\]

Configure system properties to ensure that your instance only processes XML from trusted sources to help prevent XML external entity \(XXE\) attacks.

Use the **glide.xml.entity.whitelist** and **glide.xml.entity.whitelist** system properties to prevent your instance from processing XML from untrusted sources.

XML external entity \(XXE\) attacks occur when a malicious actor modifies incoming XML \(such as adding HTTP requests\) to access data or intact with otherwise restricted systems. To help prevent these attacks, the **glide.xml.entity.whitelist.enabled** system property limits the sources from which your instance executes XML. Use the **glide.xml.entity.whitelist** property to define a set of trusted sources.

Ensure that the **glide.xml.entity.whitelist** system property exists in the System Properties \[sys\_properties\] table, and is set to `http://java.sun.com/j2ee/dtds/`. Ensure that the **glide.xml.entity.whitelist.enabled** system property exists in the System Properties \[sys\_properties\] table and is set to the value `true`.

**Tip:**

Values other than `http://java.sun.com/j2ee/dtds/` can be included in the **glide.xml.entity.whitelist** property, but are unnecessary for the out of the box platform state. Review any additional values to determine if they are safe.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

-   **glide.xml.entity.whitelist**
-   **glide.xml.entity.whitelist.enabled**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

-   String
-   Boolean

String

</td></tr><tr><td>

Recommended value

</td><td>

-   http://java.sun.com/j2ee/dtds/
-   true

</td></tr><tr><td>

Default value

</td><td>

-   http://java.sun.com/j2ee/dtds/
-   true

</td></tr><tr><td>

Fallback value

</td><td>

-   http://java.sun.com/j2ee/dtds/
-   true

</td></tr><tr><td>

Category

</td><td>

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 9.8
-   CVSS score: Critical
-   Security risk details: An XML Eternal Entity \(XEE\) attack can allow attackers to access data or perform unauthorized actions via crafted XML payloads.

</td></tr><tr><td>

Functional impact

</td><td>

If the customization is using external entity, not inclusion listed in the **glide.xml.entity.whitelist** property, the NOW Platform might block further processing.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

