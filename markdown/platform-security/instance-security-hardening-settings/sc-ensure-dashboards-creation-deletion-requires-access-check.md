---
title: Ensure dashboards creation/deletion requires access check \[New in Security Center 1.3 and updated in 2.0\]
description: The glide.processors.check\_access\_before\_process property enables access control list \(ACL\) enforcement for creating or deleting dashboards when a user is logged in.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Ensure dashboards creation/deletion requires access check \[New in Security Center 1.3 and updated in 2.0\]

The **glide.processors.check\_access\_before\_process** property enables access control list \(ACL\) enforcement for creating or deleting dashboards when a user is logged in.

Ensure the Glide Property **glide.processors.check\_access\_before\_process** exists and is set to the value true. If the property does not appear in the sys\_properties table, add a new record.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.processors.check\_access\_before\_process**

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

-   Severity score: 6.3
-   CVSS score: Medium
-   Security risk details: Disabling this property by setting it to false, enables an ACL bypass on dashboards. This allows all authenticated users with low privileges to delete and add dashboards.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

This property controls the ability to create new sys\_dashboards and delete existing dashboards when a user lacks the necessary access rights. When the value is set to false, users with inappropriate roles can add and delete sys\_dashboard entries \(though the GlideRecord layer should recheck the existing ACLs\). A value of true restricts add and delete operations for users without the required access rights.

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

