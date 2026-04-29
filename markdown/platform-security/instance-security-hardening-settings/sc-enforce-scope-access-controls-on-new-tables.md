---
title: Enforce Scope Access Controls on New Tables
description: Use a system property to enforce cross-scope access checks for newly created tables.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enforce Scope Access Controls on New Tables

Use a system property to enforce cross-scope access checks for newly created tables.

The table dictionary attribute `enforce_dot_walk_cross_scope_access=true` enforces dot-walk cross-scope access enforcement for the applicable table. This enforcement applies to dot-walking across scope boundaries using a reference field to the applicable table. When the **glide.script.dot\_walk.add\_attribute\_on\_table\_create** system property is not set to `false`, the attribute is added to the dictionary element of all new tables. This attribute is only added for new tables created after zBoot.

Ensure that the **glide.script.dot\_walk.add\_attribute\_on\_table\_create** system property set to `true` in the System Properties \[sys\_properties\] table.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.script.dot\_walk.add\_attribute\_on\_table\_create**

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

null

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.3
-   CVSS score: Medium
-   Security risk details: An application can access data in tables outside of it's application scope, leading to information disclosure.

</td></tr><tr><td>

Functional impact

</td><td>

Cross-scope access checks are enforced by default for newly created tables. This prevents applications from accessing data outside their scope through a bypass. The behavior could be turned off on a table-by-table basis.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

 

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

