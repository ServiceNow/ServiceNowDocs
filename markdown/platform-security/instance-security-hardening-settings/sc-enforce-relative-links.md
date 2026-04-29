---
title: Enforce relative links
description: Use the glide.cms.catalog\_uri\_relative property to enforce relative links from the URI parameter on /ess/catalog.do.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Enforce relative links

Use the **glide.cms.catalog\_uri\_relative** property to enforce relative links from the URI parameter on `/ess/catalog.do`.

The **glide.cms.catalog\_uri\_relative** system property enforces relative links from the URI parameter on /ess/catalog.do. If **glide.cms.catalog\_uri\_relative** is not set to the recommended value of **true**, then the URL isn't sanitized with the enforceRelativeURL\(url\) function.

**Note:** This property impacts the legacy Content Management System \(CMS\) which has been replaced with Service Portal.

Ensure that the property **glide.cms.catalog\_uri\_relative** is set to **true**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.cms.catalog\_uri\_relative**

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

-   Severity score: 2.6
-   CVSS rating: Low
-   Security risk details: Absolute URLs can pose a security risk when used as a part of parameter or a field value, thus redirecting the source page to an adversary-controlled website.

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enforces validation on Catalog page such that only Relative URLs are permitted. Existing links to external web applications become broken.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

