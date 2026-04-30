---
title: Enforce GroupBy ACLs
description: Configure your instance to conduct ACL checks on groupby columns.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enforce GroupBy ACLs

Configure your instance to conduct ACL checks on groupby columns.

Use the **glide.security.groupby\_acl\_check** system property to configure your instance to conduct ACL checks on groupby columns. If this property is set to the recommended value of **true**, then ACLs on groupby columns are honored by default. A table's **groupby\_acl\_check** attribute takes precedent over the **glide.security.groupby\_acl\_check** property. If the property is set to **false**, then ensure that any table which should have ACL checks on groupby columns has the **groupby\_acl\_check** attribute set to **true**.

Ensure the property **glide.security.groupby\_acl\_check** is set to **true**.

## More information

<table id="table_hhv_dvg_1xb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.security.groupby\_acl\_check**

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

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.7
-   CVSS score: Low
-   Security risk details: Setting this property to **false** will disable ACLs check on groupby columns which could lead to information leakage.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

