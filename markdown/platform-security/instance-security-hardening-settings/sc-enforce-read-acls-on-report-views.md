---
title: Enforce read ACLs on report views
description: Manage how Read ACLs are enforced on your instance.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Architecture, design, and threat modeling, Hardening settings, Platform Security]
---

# Enforce read ACLs on report views

Manage how Read ACLs are enforced on your instance.

Use the **glide.report.report\_view.read\_acl** property to enforce the Read ACL \(table level\) on reporting functions when there is no Report View ACL on the table or field. If this property is not set to **enforce**, ACLs could be bypassed leading to sensitive information leakage.

## More information

<table id="table_hhv_dvg_1xb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.report.report\_view.read\_acl**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

string

</td></tr><tr><td>

Recommended value

</td><td>

enforce

</td></tr><tr><td>

Default value

</td><td>

enforce

</td></tr><tr><td>

Category

</td><td>

[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 7.1
-   CVSS score: High
-   Security risk details: Not setting this property to **enforce** could cause ACLs to be bypassed.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

