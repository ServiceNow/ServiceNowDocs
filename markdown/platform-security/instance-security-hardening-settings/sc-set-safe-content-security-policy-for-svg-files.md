---
title: Set safe content security policy for svg files \[New in Security Center 1.3\]
description: The com.glide.csp.self\_script\_src\_svg property adds the script-src none directive to the HTTP Content-Security-Policy header when Scalable Vector Graphics \(SVGs\) are accessed through the Translation Memory Index \(IIX\) file extension.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Set safe content security policy for svg files \[New in Security Center 1.3\]

The **com.glide.csp.self\_script\_src\_svg** property adds the **script-src none** directive to the HTTP Content-Security-Policy header when Scalable Vector Graphics \(SVGs\) are accessed through the Translation Memory Index \(IIX\) file extension.

The **com.glide.csp.self\_script\_src\_svg** property prevents malicious file attachments that stores cross site scripting \(XSS\) attacks from running in an instance. Without this policy, a bad actor could cause a user to run arbitrary JavaScript code in their web browser which could lead to security vulnerabilities such as data exfiltration and session takeover.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.glide.csp.self\_script\_src\_svg**

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

Category

</td><td>

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 7.1
-   CVSS score: High
-   Security risk details: Not setting this property to the recommended value of true could cause a user to run arbitrary JavaScript code from a bad actor.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

This property prevents scalable vector graphics \(SVG\) files from accessing external scripts.

</td></tr></tbody>
</table>**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

