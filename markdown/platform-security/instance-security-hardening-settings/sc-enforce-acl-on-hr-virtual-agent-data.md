---
title: Enforce ACL on HR Virtual Agent Data \[New in Security Center 2.0\]
description: Discover how to set the glide.enforce\_security\_scope.sn\_hr\_va property to a secure value, preventing data leakage from the Virtual Agent Conversations scoped application.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enforce ACL on HR Virtual Agent Data \[New in Security Center 2.0\]

Discover how to set the **glide.enforce\_security\_scope.sn\_hr\_va** property to a secure value, preventing data leakage from the Virtual Agent Conversations scoped application.

The **glide.enforce\_security\_scope.sn\_hr\_va** property restricts the access control lists \(ACLs\) of several human resources \(HR\) tables to only consider the sn\_hr\_va scope. If this property is not set to the recommended value of true, then data from the Human Resources: Virtual Agent Conversations scoped application will be exposed to ACLs from all other scopes. For example, this could allow the IT Administrator to access HR data.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.enforce\_security\_scope.sn\_hr\_va**

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
-   Security risk details: Failing to set this property to the secure value true could expose data from the Human Resources: Virtual Agent Conversations scoped application to ACLs from all other scopes.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

