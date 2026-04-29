---
title: Disable unauthenticated published reports
description: Deactivate this property to prevent the user from publishing or accessing reports. This property disables the published reports feature in reporting.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Architecture, design, and threat modeling, Hardening settings, Platform Security]
---

# Disable unauthenticated published reports

Deactivate this property to prevent the user from publishing or accessing reports. This property disables the published reports feature in reporting.

If the **glide.report.published\_reports.enabled** system property is not set to the recommended value of **false**, then reports stored on the instance can be made visible without authentication.

Ensure that the **glide.report.published\_reports.enabled** system property exists in the System Properties \[sys\_properties\] table and is set to the value **false**. If the property does not appear in the sys\_properties table, add a new record.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.report.published\_reports.enabled**

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

-   Severity score: 6.5
-   CVSS rating: Medium
-   Security risk details: Allowing unauthenticated access to sensitive data can cause inadvertent information disclosure to a malicious actor.

</td></tr><tr><td>

Functional impact

</td><td>

The user cannot publish reports.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

