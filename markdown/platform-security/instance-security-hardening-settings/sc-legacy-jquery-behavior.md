---
title: Disable legacy JQuery behavior
description: The glide.jquery.legacy is used to prevent older prepatched JQuery versions from being used which will introduce unpatched vulnerabilities in the library.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Architecture, design, and threat modeling, Hardening settings, Platform Security]
---

# Disable legacy JQuery behavior

The **glide.jquery.legacy** is used to prevent older prepatched JQuery versions from being used which will introduce unpatched vulnerabilities in the library.

If **glide.jquery.legacy** is not set to the recommended value of **false**, then older prepatched JQuery versions are used which introduce unpatched vulnerabilities in the library. When **false**, integrates the JQuery 1.12.3 and 2.2.3 security patches. The system property is a fail-safe in case any organizations depend on the non-patched versions of angularJS to run their custom implementations.

Ensure the property **glide.jquery.legacy** is set to **false**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.jquery.legacy**

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

[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 7.1
-   CVSS rating: High
-   Security risk details: This update could potentially lead to security risks arising from attacks on vulnerabilities discovered in outdated JQuery library versions.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

