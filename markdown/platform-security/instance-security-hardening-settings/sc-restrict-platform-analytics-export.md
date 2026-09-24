---
title: Restrict platform analytics export to authorized roles
description: The glide.par.export.allowed\_roles property is a comma-separated list of role names permitted to export Platform Analytics dashboards and visualizations to PDF or PPT format.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-restrict-platform-analytics-export.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [platform analytics, export, roles, security]
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Restrict platform analytics export to authorized roles

The **glide.par.export.allowed\_roles** property is a comma-separated list of role names permitted to export Platform Analytics dashboards and visualizations to PDF or PPT format.

This property determines which roles can export Platform Analytics dashboards and visualizations. When this property is not configured, any user who can reach the export action is allowed to export, with no additional role check. When populated, only users holding at least one of the listed roles may export; all others are denied and logged.

This property only takes effect when the **glide.par.export.enabled** property is also set to `true`.

To configure this property:

1.  Navigate to `/sys_properties_list.do` on the instance.
2.  Set the **glide.par.export.allowed\_roles** property to a comma-separated list of role names that should be permitted to export Platform Analytics content.

## More information

<table id="table_property_details-restrict-platform-analytics-export"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.par.export.allowed\_roles**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

String, Comma-separated list of role names

</td></tr><tr><td>

Recommended value

</td><td>

Customer-specified roles authorized to export Platform Analytics dashboards and visualizations

</td></tr><tr><td>

Default value

</td><td>

Empty \(no role restriction\)

</td></tr><tr><td>

Fallback value

</td><td>

Empty \(no role restriction\)

</td></tr><tr><td>

Category

</td><td>

[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   By default, the **glide.par.export.allowed\_roles** property is empty, allowing any authenticated user who can view a dashboard or visualization and reach its export action to generate an export. No role-based restriction beyond whatever access already let them view it on screen.
-   Converting on-screen, view-only access into a downloadable file materially changes the risk profile of that data. An export can be freely shared, stored outside the instance, or removed from the organization's control. Unlike an on-screen view, there is no way to revoke or audit it after the fact. This applies to every user who can reach the export feature, not a narrow population of privileged users.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

This property has no effect unless the **glide.par.export.enabled** property is also set to `true`. If the **glide.par.export.enabled** property is set to `false`, export is already turned off entirely.

</td></tr><tr><td>

Functional impact

</td><td>

Populating this property restricts export to only the listed roles. Users without one of those roles will not be able to see or trigger export actions. This may be a visible change for existing users who previously exported without any role requirement. Instance owners should identify which roles genuinely need to distribute exported dashboard content and list only those roles. There is no single correct role list that applies to all instances, because this depends on each organization's own reporting and data-handling policies.

</td></tr></tbody>
</table>**Parent Topic:**[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)

