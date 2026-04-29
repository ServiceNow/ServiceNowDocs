---
title: Require authorization for data broker rest API \[Updated in Security Center 1.3\]
description: Use the glide.basicauth.required.databrokerrestapiprocessor property to require basic authorization for all inbound Data Broker Rest API requests.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Architecture, design, and threat modeling, Hardening settings, Platform Security]
---

# Require authorization for data broker rest API \[Updated in Security Center 1.3\]

Use the **glide.basicauth.required.databrokerrestapiprocessor** property to require basic authorization for all inbound Data Broker Rest API requests.

If the **glide.basicauth.required.databrokerrestapiprocessor** system property is not set to the recommended value of **true**, then basic authorization is not required for all inbound Data Broker Rest API requests.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.basicauth.required.databrokerrestapiprocessor**

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

Fallback value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 8.6
-   CVSS rating: High
-   Security risk details: This could lead to unauthenticated information disclosure from the instance.

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

