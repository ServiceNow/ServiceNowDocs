---
title: Enforce application scope restrictions \[New in Security Center 1.3 and removed in 1.5\]
description: Use the glide.record.legacy\_cross\_scope\_access\_policy\_in\_script property to control the permissions of scoped apps.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enforce application scope restrictions \[New in Security Center 1.3 and removed in 1.5\]

Use the **glide.record.legacy\_cross\_scope\_access\_policy\_in\_script** property to control the permissions of scoped apps.

If the **glide.record.legacy\_cross\_scope\_access\_policy\_in\_script** property is set to true, scoped apps can call APIs which should only be available to global apps. This property bypasses the intended access controls for creating and updating developers for those scoped apps.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.record.legacy\_cross\_scope\_access\_policy\_in\_script**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

boolean

</td></tr><tr><td>

Recommended value

</td><td>

false

</td></tr><tr><td>

Default value

</td><td>

true \(when the property does not exist in the sys\_properties table.\)

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.5
-   CVSS score: Low
-   Security risk details: If this property is not set to the recommended value, then scoped apps and delegated developers for those scoped apps can create and update records in global tables such as Incident.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

