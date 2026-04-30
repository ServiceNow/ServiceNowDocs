---
title: Enforce security rules to sharing dashboards \[New in Security Center 1.3\]
description: Use the glide.cms.dashboards.sharing\_with\_secure\_search property to control whether users can share dashboards.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enforce security rules to sharing dashboards \[New in Security Center 1.3\]

Use the **glide.cms.dashboards.sharing\_with\_secure\_search** property to control whether users can share dashboards.

When the **glide.cms.dashboards.sharing\_with\_secure\_search** property is not set to **true**, users can share dashboard groups and roles that they do not have access to. Enabling this property enforces access control lists \(ACLs\) when searching the sys\_user, sys\_user\_role, and sys\_user\_group tables during the dashboard sharing process. Sharing a dashboard excessively can lead to users, groups, or roles accessing data that they should not have permission to view, potentially compromising sensitive information. Therefore, it is recommended to set **glide.cms.dashboards.sharing\_with\_secure\_search** to true so that dashboards are shared only with those who have the appropriate permissions.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.cms.dashboards.sharing\_with\_secure\_search**

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

-   Severity score: 3.5
-   CVSS score: Low
-   Security risk details: Not setting this property to the recommended value of true causes access control lists to not be enforced when searching the sys\_user, sys\_user\_role, and sys\_user\_group tables. This could lead to dashboards being shared with unauthorized users, exposing sensitive information.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

[Access control](https://www.servicenow.com/docs/access?context=access-control&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)

</td></tr><tr><td>

Functional impact

</td><td>

This property applies security rules to the list of users, user groups, and roles that are visible when sharing dashboards.

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

