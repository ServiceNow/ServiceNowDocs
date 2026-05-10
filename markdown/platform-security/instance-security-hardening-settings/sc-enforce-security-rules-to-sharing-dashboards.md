---
title: Enforce security rules to sharing dashboards
description: Use the glide.cms.dashboards.sharing\_with\_secure\_search property to control whether users can share dashboards.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enforce security rules to sharing dashboards

Use the **glide.cms.dashboards.sharing\_with\_secure\_search** property to control whether users can share dashboards.

When the **glide.cms.dashboards.sharing\_with\_secure\_search** system property is not set to **true**, a user can share a dashboard to groups and roles that they do not personally have access to. This property enforces ACLs on searching the User \[sys\_user\], Roles \[sys\_user\_role\], and Groups \[sys\_user\_group\] tables when sharing a dashboard.

Set the **glide.cms.dashboards.sharing\_with\_secure\_search** system property is set to **true**.

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

Boolean

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

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
-   Security risk details: Oversharing a dashboard may result in minor confidentiality impacts in cases where a user shares a dashboard with a user, group, or role that should not access to the dashboard.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/access-control.md)

</td></tr><tr><td>

Functional impact

</td><td>

This property applies security rules to the list of users, user groups, and roles that are visible when sharing dashboards.

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

