---
title: Set safe content security policy for SVG files
description: The com.glide.csp.self\_script\_src\_svg property adds the script-src none directive to the HTTP Content-Security-Policy header when Scalable Vector Graphics \(SVGs\) are accessed through the Translation Memory Index \(IIX\) file extension.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Set safe content security policy for SVG files

The **com.glide.csp.self\_script\_src\_svg** property adds the **script-src none** directive to the HTTP Content-Security-Policy header when Scalable Vector Graphics \(SVGs\) are accessed through the Translation Memory Index \(IIX\) file extension.

The **com.glide.csp.self\_script\_src\_svg** system property adds "script-src none" to the Content-Security-Policy header when SVGs are accessed via the ".iix" file extension, which prevents the exploitation of stored XSS from crafted file attachments stored within the instance.

Ensure that the property **com.glide.csp.self\_script\_src\_svg** is set to **true**.

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

-   Severity score: 7.1
-   CVSS score: High
-   Security risk details: Without this policy, a malicious actor could trick a user into running arbitrary JavaScript code in their web browser leading to consequences such as data exfiltration or session takeover.

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

