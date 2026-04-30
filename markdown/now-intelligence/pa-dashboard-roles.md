---
title: Platform Analytics dashboard roles
description: Platform Analytics dashboards have few role restrictions. Editing rights are granted by sharing, independent of role.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Dashboards in Platform Analytics, Platform Analytics experience, Platform Analytics]
---

# Platform Analytics dashboard roles

Platform Analytics dashboards have few role restrictions. Editing rights are granted by sharing, independent of role.

Users with any role can create dashboards and share them with groups, users, and roles. These users can share a dashboard that has been shared with them if sharing rights were also granted. They can pass along editing rights if granted.

The dashboard\_admin role allows a user to configure, edit, or delete any dashboards, regardless of ownership or editing rights. Certain configuration tasks also require dashboard\_admin.

Tasks that integrate dashboards with Process Mining require the sn\_process\_optimization\_analyst role.

Users with the analytics\_categories\_admin role can create, edit, or delete dashboard categories.

For a full guide to roles connected to Platform Analytics dashboards, see [Platform Analytics roles](../reference/platform-analytics-roles.md).

<table id="table_d1r_2vc_k2c"><thead><tr><th>

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

Any role to share a data visualization that you created or that was shared with you with sharing rights. With the viz\_admin role or higher, you can share any data visualization on the instance. When you share a data visualization, you can pass along the rights to share that visualization further. You also decide whether to share with editing rights or only viewing rights. If a data visualization has been shared with you with sharing and editing rights, you can also pass along editing rights.dashboard\_admin to share any dashboard

A role with read access to the Roles \[sys\_user\_role\] table to share with roles

</td></tr><tr><td>

Edit a dashboard

</td><td>

Any role, if you created the dashboard or have had it shared with you with editing rights.dashboard\_admin or higher for any dashboard

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

par\_scheduler for dashboards that you own or that have been shared with you.par\_scheduler\_admin or higher for any dashboard

</td></tr><tr><td>

Bookmark a dashboard

</td><td>

Any role, if you can view the dashboard.

</td></tr><tr><td>

Delete a dashboard

</td><td>

Any role, if you created the dashboard.dashboard\_admin or higher for any dashboard

</td></tr><tr><td>

[Configure dashboard details](../../dashboards/task/config-db-in-ac.md)

</td><td>

Any role, if you created the dashboard or have had it shared with you with editing rights.dashboard\_admin or higher for any dashboard

</td></tr><tr><td>

[Configure dashboard settings](../../dashboards/task/configure-ac-db-settings.md#)

</td><td>

Any role, if you created the dashboard or have had it shared with you with editing rights.dashboard\_admin or higher for any dashboard

</td></tr><tr><td>

[Configure dashboard tab cache timeout](../../dashboards/task/configure-ac-db-settings.md#)

</td><td>

admin

</td></tr></tbody>
</table>