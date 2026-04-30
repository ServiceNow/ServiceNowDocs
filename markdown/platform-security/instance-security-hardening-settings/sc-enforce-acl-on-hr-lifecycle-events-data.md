---
title: Enforce ACL on HR Lifecycle Events Data \[New in Security Center 2.0\]
description: Learn how to prevent unauthorized access to data in the Human Resources Lifecycle Events application by verifying that the glide.enforce\_security\_scope.sn\_hr\_le property is set to the secured value.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enforce ACL on HR Lifecycle Events Data \[New in Security Center 2.0\]

Learn how to prevent unauthorized access to data in the Human Resources Lifecycle Events application by verifying that the **glide.enforce\_security\_scope.sn\_hr\_le property** is set to the secured value.

The **glide.enforce\_security\_scope.sn\_hr\_le** property limits the access control lists \(ACLs\) of several HR tables so that only the "sn\_hr\_le" scope is considered. If **glide.enforce\_security\_scope.sn\_hr\_le** isn’t set to the recommended value of true, then the data from the Human Resources: Lifecycle Events application will be exposed to ACLs from all other scopes which could lead to unauthorized users accessing sensitive data. For example, an IT administrator gaining access to HR data.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.enforce\_security\_scope.sn\_hr\_le**

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

false

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 6.5
-   CVSS score: Medium
-   Security risk details: Not setting this property to the value of true, could cause the Human Resources: Lifecycle Events application data to be exposed to ACLs from all other scopes. This could lead to unauthorized users accessing sensitive data.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

