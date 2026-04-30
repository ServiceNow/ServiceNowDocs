---
title: Platform Analytics roles
description: Platform Analytics has both unique roles and roles from other applications that apply to it.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 13
breadcrumb: [Reference, Platform Analytics experience, Platform Analytics]
---

# Platform Analytics roles

Platform Analytics has both unique roles and roles from other applications that apply to it.

## Users with any role

Users with any role can create visualizations in dashboards that they have editing rights to. They need access to the data that they wish to display. They can add data visualizations that have been shared with them to their dashboards. In the Visualization Designer, they can bookmark or export such visualizations, and if a visualization has been shared with them with sharing rights, they can share it with other groups and users. Specific roles are needed to create or edit visualizations in the Visualization Designer.

Users with any role can create dashboards and share them with groups, users, and roles. If a data visualization has been shared with them, they can add this visualization to their dashboards from the library. These users can share a dashboard that has been shared with them if sharing rights were also granted. They can pass along editing rights if granted.

## User groups

Simplify user administration by creating groups that contain all the roles necessary for specific personas rather than to individual users. You can then assign individual users to those groups. When users transition to new roles, you can then re-assign their group memberships, and avoid scenarios where users retain unexpected roles.

For details on the administration of users, groups, and roles, see [User Administration](https://www.servicenow.com/docs/access?context=c_UserAdministration&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## Role description

The following table provides the following information about each role associated with Platform Analytics.

-   **Role name**

    Name of the role from the **Name** field in the Roles \[sys\_user\_role\] table.

-   **Description**

    Description of the role and its intended use.

-   **Contains Roles**

    List of roles contained within the role.

-   **Contained by roles \(except admin\)**

    Any roles, besides admin, that contain the role. The admin role contains all the roles.


The following attributes are shared by all of the roles:

-   None of the roles are assigned to a group by default.
-   None of the roles require users to be allocated as part of a paid subscription, although a paid subscription is required for most Performance Analytics functionality.
-   None of the roles are elevated, meaning none grant access to High Security Settings.
-   All of the roles are included in the base system, except for analytics\_admin and sn\_process\_optimization\_analyst, which are included with User Experience Analytics and Process Mining, respectively.

**Tip:** Try to assign the least inclusive role that still provides the necessary access. For example, if you want a user to be able to create data visualizations in the library and share them with users, but not schedule their export, grant that user viz\_creator and not viz\_admin.

<table id="table_tz4_y22_jxb"><thead><tr><th>

Role name

</th><th>

Description

</th><th>

Contains Roles

</th><th>

Contained by roles \(besides admin\)

</th></tr></thead><tbody><tr><td>

admin

</td><td>

Can create dashboards. Can create data visualizations in the Visualization Designer, which are automatically saved to the Library. Can edit, duplicate, share, and delete any dashboard and data visualizations. Can add filters to the filter library or edit or delete any filter. Has User Experience Analytics administrator privileges.

</td><td>

All other roles in this table

</td><td>

Not applicable

</td></tr><tr><td>

platform\_analytics\_admin

</td><td>

Role for administrative privileges in the Platform Analytics experience. This role includes administrative privileges for products and features that are part of Platform Analytics, including Performance Analytics and User Experience Analytics. Has the rights of all roles listed here except report\_admin rights to Core UI reports.

 Equivalent to admin role from a security perspective.

</td><td>

-   analytics\_admin
-   analytics\_categories\_admin
-   analytics\_filter\_admin
-   dashboard\_admin
-   pa\_admin
-   par\_scheduler
-   viz\_admin

</td><td>

None

</td></tr><tr><td>

analytics\_admin

</td><td>

Role for User Experience Analytics administrative privileges

</td><td>

All other User Experience Analytics admin and viewer roles. For more information, see [Roles installed with User Experience Analytics](../../../administer/user-exp-analytics/reference/components-installed-user-exp-analytics.md).

</td><td>

platform\_analytics\_admin

</td></tr><tr><td>

analytics\_categories\_admin

</td><td>

Role for creating, editing, or deleting category tags on dashboards.

</td><td>

None

</td><td>

-   platform\_analytics\_admin
-   dashboard\_admin

</td></tr><tr><td>

analytics\_filter\_admin

</td><td>

Role for editing or deleting any Platform Analytics filter. Can add filters to the filter library. For more information, see [Filters in Platform Analytics](../concept/interactive-filters-workspace.md).

</td><td>

None

</td><td>

-   platform\_analytics\_admin
-   dashboard\_admin
-   pa\_admin
-   report\_admin
-   viz\_admin

</td></tr><tr><td>

dashboard\_admin

</td><td>

Can create, edit, duplicate, share, and delete any dashboard. These rights extend to both Platform Analytics and responsive dashboards. For more information, see [Dashboard permissions](../../dashboards/concept/c_DashboardRoles.md).Can schedule the export of all dashboards on an instance. Can also delete scheduled exports.

</td><td>

-   analytics\_filter\_admin
-   analytics\_categories\_admin
-   sn\_par\_sche\_export.par\_scheduler\_admin
-   par\_scheduler

</td><td>

platform\_analytics\_admim

</td></tr><tr><td>

now\_assist\_explorer\_user

</td><td>

-   Can view the trigger point to start a AI Data Explorer exploration from data visualizations, Lists, or the Now Assist panel.
-   Can edit an exploration.
-   Can create a new exploration

</td><td>

 

</td><td>

 

</td></tr><tr><td>

pa\_kpi\_signal\_admin

</td><td>

Can activate KPI Signals for an indicator. For more information, see [Activate KPI Signals monitoring for an indicator \(KPI\)](../task/activate-signals-monitor.md).

</td><td>

None

</td><td>

None. However, pa\_admin has the same privileges

</td></tr><tr><td>

pa\_admin

</td><td>

Role for Performance Analytics administrative privileges. Equivalent to admin role from a security perspective.

</td><td>

-   viz\_admin
-   analytics\_filter\_admin
-   All other Performance Analytics roles. For more information, see [Performance Analytics roles](../../performance-analytics/reference/r_PARoles.md).

</td><td>

platform\_analytics\_admin

</td></tr><tr><td>

par\_scheduler

</td><td>

Can create and edit the scheduled email distribution of any dashboard or data visualization they can view or edit

</td><td>

None

</td><td>

sn\_par\_sche\_export.par\_scheduler\_admin

</td></tr><tr><td>

sn\_par\_sche\_export.par\_scheduler\_admin

</td><td>

Same as par\_scheduler, but has full CRUD rights to the par\_export table, including deletion

</td><td>

par\_scheduler

</td><td>

-   dashboard\_admin
-   viz\_admin

</td></tr><tr><td>

sn\_process\_optimization\_analyst

</td><td>

Can configure a Process Mining map on a dashboard. For more information, see [Configure a Process Mining map on a dashboard](../task/configure-po-map.md).

</td><td>

None

</td><td>

None

</td></tr><tr><td>

viz\_creator

</td><td>

Can create data visualizations in the Visualization Designer, which are then available in the library. Can also edit, export, and share data visualizations in the Visualization Designer, if they own that visualization or have had it shared with them with the relevant rights. Can only delete visualizations that they created. Can share visualizations only with groups and users.

</td><td>

None

</td><td>

-   viz\_admin \(implicit\)
-   itil
-   report\_user

</td></tr><tr><td>

viz\_admin

</td><td>

-   Can create data visualizations in the Visualization Designer, which are then available in the library.
-   Can access all data visualizations in the library, either to add to a dashboard or open in the Visualization Designer.
-   Can perform all actions in the Visualization Designer on any visualization.
-   Can share a visualization with groups, users, or roles.
-   Can schedule the export of all data visualizations on an instance. Can also delete scheduled exports.

</td><td>

-   analytics\_filter\_admin
-   sn\_par\_sche\_export.par\_scheduler\_admin

 Also includes the same privileges as viz\_creator

</td><td>

-   platform\_analytics\_admin
-   pa\_admin
-   pa\_power\_user

</td></tr><tr><td>

report\_admin

</td><td>

As viz\_admin, but can also create, edit, delete, and export all Core UI reports, including those on the Service Portal.

</td><td>

-   viz\_admin
-   analytics\_filter\_admin
-   report\_user

</td><td>

 

</td></tr></tbody>
</table>The role hierarchy in the table is also shown in the following diagram:![Platform analytics role hierarchy.](../image/platform-analytics-role-hierarchy.png)

## Role lookup by use case

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

par\_scheduler for dashboards that you own or that have been shared with you.dashboard\_admin or higher for any dashboard

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

Any role, if you created the dashboard.dashboard\_admin or higher for any dashboard

</td></tr><tr><td>

[Configure dashboard details](../../dashboards/task/config-db-in-ac.md)

</td><td>

Any role, if you created the dashboard or have had it shared with you with editing rights.dashboard\_admin or higher for any dashboard

</td></tr><tr><td>

[Configure dashboard settings](../../dashboards/task/configure-ac-db-settings.md) except scheduled refreshes

</td><td>

Any role, if you created the dashboard or have had it shared with you with editing rights.dashboard\_admin or higher for any dashboard

</td></tr><tr><td>

[Schedule dashboard refreshes](../../dashboards/task/configure-ac-db-settings.md)

</td><td>

dashboard\_admin or higher

</td></tr><tr><td>

[Configure dashboard tab cache timeout](../../dashboards/task/configure-ac-db-timeout.md)

</td><td>

admin

</td></tr><tr><td>

[Create dashboard categories](../../dashboards/task/db-categories-create.md)

</td><td>

analytics\_categories\_admin or higher

</td></tr><tr><td>

[Assign categories to a dashboard](../../dashboards/task/db-categories-assign.md)

</td><td>

Any role, if you can edit the dashboard.analytics\_categories\_admin or higher to assign a category to any dashboard.

</td></tr></tbody>
</table><table id="table_c3f_kwc_k2c"><thead><tr><th>

Use case

</th><th>

Required role

</th></tr></thead><tbody><tr><td>

Create a data visualization

</td><td>

Anyone with access to data can create a visualization of that data on a dashboard that they own. Users with the viz\_creator role can create a visualization in the Visualization Designer. If you create a visualization in the Visualization Designer, it is saved to the library.

</td></tr><tr><td>

Edit a data visualization

</td><td>

You can edit any visualization that you created or that was shared with you with editing rights, if it is not in the library. If it is in the library, you also need the viz\_creator role.Edit any visualization on the instance with viz\_admin or higher.

</td></tr><tr><td>

Add a visualization from the library to a dashboard

</td><td>

Any role, if the visualization has been shared with you.viz\_creator to add any visualization from the library.

</td></tr><tr><td>

Add a visualization that was created in a dashboard to the library

</td><td>

viz\_creator or higher and the right to edit the dashboard

</td></tr><tr><td>

Unlink a data visualization on a dashboard from the library, creating a version that is local to that dashboard.

</td><td>

Any role, if you can edit the dashboard containing the visualization

</td></tr><tr><td>

Duplicate a visualization in the Visualization Designer

</td><td>

viz\_creator or higher

</td></tr><tr><td>

Share a visualization with users or groups

</td><td>

Any role to share a data visualization that you created or that was shared with you with sharing rights. With the viz\_admin role or higher, you can share any data visualization on the instance. When you share a data visualization, you can pass along the rights to share that visualization further. You also decide whether to share with editing rights or only viewing rights. If a data visualization has been shared with you with sharing and editing rights, you can also pass along editing rights.

</td></tr><tr><td>

Share a data visualization with roles

</td><td>

viz\_admin or higher

</td></tr><tr><td>

Export a visualization

</td><td>

Any role, if you can view the visualization in the Visualization Designer.

</td></tr><tr><td>

Schedule the export of a data visualization

</td><td>

par\_scheduler or higher to schedule the export of a data visualization that you can edit. viz\_admin or higher to schedule the export of any data visualization on the instance.

</td></tr><tr><td>

Delete the scheduled export of a data visualization

</td><td>

sn\_par\_sche\_export.par\_scheduler\_admin \(contained in viz\_admin\)

</td></tr><tr><td>

Delete a visualization

</td><td>

Any role, to delete a data visualization that you created. viz\_admin or higher to delete any data visualization on the instance.

</td></tr><tr><td>

[Control data source availability by role](../task/dv-use-data-source-acl.md)

</td><td>

admin

</td></tr><tr><td>

[Configure chart interactions](../../reporting/task/configure-go-data.md)

</td><td>

Any role if you have the right to edit the data visualization. The viewer needs the right to view any data they drill down to.

</td></tr><tr><td>

[Use service catalog variables in data visualizations](../../reporting/concept/dv-rep-sc-variables.md#)

</td><td>

viz\_creator or higher

</td></tr><tr><td>

[Create coloring rules for data visualizations](../../performance-analytics/concept/colors-dv.md#)

</td><td>

Any role if you have the right to edit the data visualization.

</td></tr></tbody>
</table><table id="table_tm2_v15_32c"><thead><tr><th>

Use case

</th><th>

Role

</th></tr></thead><tbody><tr><td>

Add a filter or a filter group to a dashboard

</td><td>

Any role, if the user has editing rights to the dashboard.dashboard\_admin or higher to add a filter or filter group to any dashboard

</td></tr><tr><td>

Edit a filter on a dashboard

</td><td>

Any role, for a filter that is not in the library, if the user has editing rights to the dashboard.analytics\_filter\_admin or higher is also needed if the filter is in the library. Alternatively, the user can detach the filter on the dashboard from the library and edit a local copy.

</td></tr><tr><td>

Add a local filter on the dashboard to the library

</td><td>

analytics\_filter\_admin or higher, and editing rights to the dashboard

</td></tr><tr><td>

Create or edit a filter in the Filter Designer

</td><td>

analytics\_filter\_admin or higher

</td></tr></tbody>
</table>|Use case|Role|
|--------|----|
|[Configure a Process Mining map on a dashboard](../task/configure-po-map.md)|sn\_process\_optimization\_analyst|
|[Activate KPI Signals monitoring for an indicator \(KPI\)](../task/activate-signals-monitor.md)|pa\_kpi\_signal\_admin|
|Create or edit an exploration in [AI Data Explorer](../task/launch-now-assist-explorer.md)|now\_assist\_explorer\_user|

**Parent Topic:**[Platform Analytics experience reference](../concept/platform-analytics-exp-reference.md)

**Related topics**  


[Performance Analytics roles](../../performance-analytics/reference/r_PARoles.md)

[Roles installed with User Experience Analytics](../../../administer/user-exp-analytics/reference/components-installed-user-exp-analytics.md)

[Reporting roles](../../reporting/reference/reporting-roles.md#)

[Creating dashboards and other common dashboard tasks](../../dashboards/concept/common-dashboard-tasks.md)

[Common data visualization tasks](../../reporting/concept/common-dv-tasks.md)

