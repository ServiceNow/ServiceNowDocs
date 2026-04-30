---
title: Disable GlideRecord Scope Fencing Legacy Behavior \[New in Security Center 1.3 and updated in 1.5 and 2.0\]
description: The glide.record.legacy\_cross\_scope\_access\_policy\_in\_script property disables scope fencing allowing scoped apps to access global script interfaces. It was created as a patch to GlideRecord's cross scope access.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Architecture, design, and threat modeling, Hardening settings, Platform Security]
---

# Disable GlideRecord Scope Fencing Legacy Behavior \[New in Security Center 1.3 and updated in 1.5 and 2.0\]

The **glide.record.legacy\_cross\_scope\_access\_policy\_in\_script** property disables scope fencing allowing scoped apps to access global script interfaces. It was created as a patch to GlideRecord's cross scope access.

GlideRecord provided cross scope create/update access to tables that were not configured with that level of access. In order to prevent customers from having applications broken when this scoped access behavior was patched, the property **glide.record.legacy\_cross\_scope\_access\_policy\_in\_script** was created. When true, cross scope access falls back onto legacy behavior \(insecure\). This property disables scope fencing, allowing scoped apps to access global script interfaces.

It is best security practice to have scope fencing restrictions in place. Scoping ensures applications can only access resources with explicit access or within their scope, following the principle of least privilege. Disabiling this feature could lead to confidentiality, availability, and integrity impacts.

Set the Glide Property **glide.record.legacy\_cross\_scope\_access\_policy\_in\_script** to false. When not present in the sys\_properties table, the default value is true.

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

[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5
-   CVSS score: Medium
-   Security risk details: Scoping ensures applications can only access resources with explicit access or within their scope following the principle of least privilege. Disabling this feature could lead to confidentiality, availability, and integrity impacts.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

