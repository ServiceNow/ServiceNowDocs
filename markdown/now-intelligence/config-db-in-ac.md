---
title: Configure Platform Analytics dashboard details
description: You can change a dashboard name, add a description, certify it, configure visibility, and specify the requester, the owner, the owner group.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
keywords: [How to change dashboard visibility, How to add dashboard description, How to certify a dashboard, How to set dashboard owner, How to see dashboard creator, How to see whom the dashboard has been shared with, How to make a dashboard available on a workspace]
breadcrumb: [Dashboards in Platform Analytics, Platform Analytics experience, Platform Analytics]
---

# Configure Platform Analytics dashboard details

You can change a dashboard name, add a description, certify it, configure visibility, and specify the requester, the owner, the owner group.

## Before you begin

You can edit **Dashboard Details** for both dashboards created in UI Builder and dashboards created with the inline editor.

Role required: dashboard\_admin for all dashboards, or any role for dashboards that you own or ones that you have been given the right to edit. See [Platform Analytics dashboard roles](../../par-for-workspace/concept/pa-dashboard-roles.md) for more information about viewing and editing rights on dashboards.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**.

2.  On the **Dashboards** overview, choose the dashboard you want to configure.

3.  Select the info button \(![information button](../../reporting/image/icon-info.png)\) to open the **Details** panel.

    On the **Details** panel, you can edit several aspects of the dashboard.

    1.  Edit the **Name** field to change how the dashboard appears in the Analytics Center and the Dashboard Overview.

    2.  Fill in the **Description** to provide further context about what the dashboard is for.

    3.  Mark the dashboard as **Certified** to inform the user that the dashboard is recommended for use across your organization.

        **Note:** You must have an admin role to mark a dashboard as **Certified**. For more information, see [Certify a Platform Analytics dashboard](certify-db-ac.md).

    4.  In **Dashboard Visibility**, view, add, or remove workspaces to which the dashboard can be added.

        **Important:** Specifying a workspace here does not make the dashboard visible in that workspace. It only enables you to add the dashboard to that workspace. For more information about adding a dashboard to a workspace, see [Add a dashboard to a Dashboards page](../../performance-analytics/task/add-dashboard-to-workspace.md).

    5.  Specify who requested the dashboard.

        This user is considered a responsible user. The data visualization is shared with them, with editing rights.

    6.  Specify the owner of the dashboard.

        By default, the owner is the creator of the dashboard, but the creator or owner can assign ownership to another user.

    7.  Specify an owner group.

        The owner of a dashboard can be an entire group rather than a single person.

    8.  See who created the dashboard.

    9.  See who the dashboard has been shared with.

    ![inline editor dashboard details example.](../image/db-ac-details-ex.png)


