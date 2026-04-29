---
title: Enforce URL allowlist check
description: Use the glide.security.url.whitelist system property to add extra layer of validation to ensure whether any external URL introduced should be a part of inclusion listed URLs.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Enforce URL allowlist check

Use the **glide.security.url.whitelist** system property to add extra layer of validation to ensure whether any external URL introduced should be a part of inclusion listed URLs.

If the **glide.security.url.whitelist.strict\_check** system property isn't set to the recommended value of **true** then all external URLs are allowed for redirection when **glide.security.url.whitelist** is empty. If **glide.security.url.whitelist** is not empty, then only external URLs in the list are allowed. Either setting **glide.security.url.whitelist.strict\_check** to **true** or ensuring **glide.security.url.whitelist** is set to a non-empty value with the allowed external URLs leaves the instance in a secure state.

Ensure that the property **glide.security.url.whitelist.strict\_check** is set to **true** or the property **glide.security.url.whitelist.strict\_check** is set to a value.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

-   **glide.security.url.whitelist.strict\_check**
-   **glide.security.url.whitelist**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

-   Boolean
-   String

</td></tr><tr><td>

Recommended value

</td><td>

-   true
-   Comma-separated of permitted URLs

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

-   true
-   &lt;empty&gt;

</td></tr><tr><td>

Category

</td><td>

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 6.3
-   CVSS rating: Medium
-   Security risk details: If all external URLs are allowed for redirection, this could allow an attacker to redirect a user to a malicious website.

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enforces validation on logout page. It might have a functional impact on a user of an instance with an SSO/SAML configuration.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

