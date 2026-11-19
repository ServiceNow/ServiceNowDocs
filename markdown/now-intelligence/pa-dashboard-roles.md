---
title: Platform Analytics dashboard roles
description: Platform Analytics dashboards have few role restrictions. Editing rights are granted by sharing, independent of role.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/pa-dashboard-roles.html
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Reference, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Platform Analytics dashboard roles

Platform Analytics dashboards have few role restrictions. Editing rights are granted by sharing, independent of role.

Users with any role can create dashboards and share them with groups, users, and roles. These users can share a dashboard that has been shared with them if sharing rights were also granted. They can pass along editing rights if granted.

The dashboard\_admin role allows a user to configure, edit, or delete any dashboards, regardless of ownership or editing rights. Certain configuration tasks also require dashboard\_admin, as described in [Configuring dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/configuring-dashboards.md).

Tasks that integrate dashboards with Process Mining require the sn\_process\_optimization\_analyst role. These tasks are listed in [Configuring dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/configuring-dashboards.md).

Users with the analytics\_categories\_admin role can create, edit, or delete dashboard categories.

For a full guide to roles connected to Platform Analytics dashboards, see [Platform Analytics roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/platform-analytics-roles.md).

<table id="table_u4x_4xv_5kc"><thead><tr><th>

Role

</th><th>

Use case

</th></tr></thead><tbody><tr><td>

Any role

</td><td>

-   Create a dashboard
-   Edit a dashboard that you own or that was shared with you with editing rights. Technical dashboards also require ui\_builder\_admin.
-   Share a dashboard that you own or that was shared with you with sharing rights
-   Duplicate a dashboard, if you have viewing rights
-   Create a printer-friendly copy of a dashboard, if you have viewing rights
-   Export a dashboard, if you have viewing rights
-   Bookmark a dashboard, if you have viewing rights
-   Delete a dashboard, if you own it
-   [Configure dashboard details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/config-db-in-ac.md), if you own the dashboard or had it shared with you with editing rights
-   [Configure dashboard settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/configure-ac-db-settings.md) except scheduled refreshes, if you own the dashboard or had it shared with you with editing rights
-   [Assign categories to a dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/db-categories.md) if you have editing rights to the dashboard

</td></tr><tr><td>

dashboard\_admin

</td><td>

-   Share any dashboard
-   Edit any dashboard. Technical dashboards also require ui\_builder\_admin.
-   Delete any dashboard
-   [Configure dashboard details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/config-db-in-ac.md) for any dashboard
-   [Configure dashboard settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/configure-ac-db-settings.md) for any dashboard
-   [Schedule dashboard refreshes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/configure-ac-db-settings.md)

</td></tr><tr><td>

sn\_par\_sche\_export.par\_scheduler\_admin \(contained in dashboard\_admin\)

</td><td>

-   Schedule the export of a dashboard
-   Delete a schedule to export a dashboard

</td></tr><tr><td>

analytics\_category\_admin

</td><td>

-   [Create dashboard categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/db-categories.md)
-   [Assign categories to any dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/db-categories.md)

</td></tr></tbody>
</table><table id="table_d1r_2vc_k2c"><thead><tr><th>

Use case

</th><th>

Required role

</th></tr></thead><tbody><tr><td>

Create a dashboard

</td><td>

Any role

</td></tr><tr><td>

Share a dashboard

</td><td>

Any role to share a dashboard that you own or that was shared with you with sharing rights. With the viz\_admin role or higher, you can share any dashboard on the instance. When you share a dashboard, you can pass along the rights to share that dashboard further. You also decide whether to share with editing rights or only viewing rights. If a dashboard has been shared with you with sharing and editing rights, you can also pass along editing rights.dashboard\_admin to share any dashboard

A role with read access to the Roles \[sys\_user\_role\] table to share with roles

</td></tr><tr><td>

Edit a dashboard

</td><td>

Any role, if you own the dashboard or have had it shared with you with editing rights.dashboard\_admin or higher for any dashboard

Technical dashboards also require ui\_builder\_admin

</td></tr><tr><td>

Duplicate a dashboard

</td><td>

Any role, if you can view the dashboard. You cannot duplicate technical dashboards.

</td></tr><tr><td>

Create a printer-friendly copy of a dashboard

</td><td>

Any role, if you can view the dashboard.

</td></tr><tr><td>

Export a dashboard

</td><td>

Any role, if you can view the dashboard.

</td></tr><tr><td>

Schedule the export of a dashboard

</td><td>

par\_scheduler for dashboards that you own or that have been shared with you.sn\_par\_sche\_export.par\_scheduler\_admin \(contained in dashboard\_admin\) or higher for any dashboard

</td></tr><tr><td>

Delete the scheduled export of a dashboard

</td><td>

sn\_par\_sche\_export.par\_scheduler\_admin \(contained in dashboard\_admin\)

</td></tr><tr><td>

Bookmark a dashboard

</td><td>

Any role, if you can view the dashboard.

</td></tr><tr><td>

Delete a dashboard

</td><td>

Any role, if you own the dashboard.dashboard\_admin or higher for any dashboard

</td></tr><tr><td>

[Configure dashboard details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/config-db-in-ac.md)

</td><td>

Any role, if you own the dashboard or have had it shared with you with editing rights.dashboard\_admin or higher for any dashboard

</td></tr><tr><td>

[Configure dashboard settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/configure-ac-db-settings.md) except scheduled refreshes

</td><td>

Any role, if you own the dashboard or have had it shared with you with editing rights.dashboard\_admin or higher for any dashboard

</td></tr><tr><td>

[Schedule dashboard refreshes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/configure-ac-db-settings.md)

</td><td>

dashboard\_admin or higher

</td></tr><tr><td>

[Configure dashboard tab cache timeout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/configure-ac-db-timeout.md)

</td><td>

admin

</td></tr><tr><td>

[Create dashboard categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/db-categories.md)

</td><td>

analytics\_categories\_admin or higher

</td></tr><tr><td>

[Assign categories to a dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/db-categories.md)

</td><td>

Any role, if you can edit the dashboard.analytics\_categories\_admin or higher to assign a category to any dashboard.

</td></tr></tbody>
</table>**Parent Topic:**[Dashboard reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/dashboard-reference-page.md)

