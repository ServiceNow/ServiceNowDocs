---
title: Dashboards for analytics admins
description: Use Platform Analytics dashboards to access, organize, and share data in a visual format. Dashboards contain data visualizations, filters, and other visual elements.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Explore, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Dashboards for analytics admins

Use Platform Analytics dashboards to access, organize, and share data in a visual format. Dashboards contain data visualizations, filters, and other visual elements.

## Dashboard overview for analytics admins

On Australia instances, you can find both Core UI dashboards and Platform Analytics experience dashboards in the Dashboards library.

To find dashboards in Platform Analytics, navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**. For users with admin roles, the dashboards page includes tools that are designed to help administrators efficiently manage the dashboards. Administrators can monitor the usage, perform dashboard-specific tasks, such as deleting or deactivating dashboards, and also identify the key insights with filters.

You can also directly access Dashboards from the left navigation in Platform Analytics library pages.

## Platform analytics library navigation

Library pages like this one include a navigation pane that provides access to the other libraries and the Usage Insights page. Use it to navigate between the libraries without interrupting your workflow.

## Dashboards for analytics admins

The following example shows the Dashboards library that includes all the common and additional elements that are visible to the users with sys\_admin and dashboard\_admin roles only. See [Dashboard elements for users with admin roles](dashboards-for-admin-users.md#table_h44_pqg_5fc) table for descriptions.

For information on role-based access for the left navigation pane and Platform Analytics overview page, see [Roles applicable for Platform Analytics overview page](../../performance-analytics/concept/analytics-center.md#table_a12_23s_k3c).

![Platform Analytics Dashboards library for analytics admins.](../../par-for-workspace/image/analytics-center-db-tab.png "Platform Analytics Dashboards library for analytics admins")

The following table shows the features that the Platform Analytics Dashboards page offers to analytics admins. Refer to the numbered call-outs in the image and their descriptions in the table.

<table id="table_h44_pqg_5fc"><thead><tr><th>

No.

</th><th>

Field or Element name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1

</td><td>

**Create Dashboard**

</td><td>

Option for creating dashboards. For more information on creating dashboards, see [Create a dashboard with the in-line editor](../task/create-db-in-ac.md).

</td></tr><tr><td rowspan="2">

2

</td><td>

**Filter by**

</td><td>

Option for filtering the Dashboards list to display the data based on the following conditions:-   **Bookmarked**: Your bookmarked dashboards. By bookmarking your dashboards, you can find them. For more information about bookmarking dashboards, see [Bookmark a Platform Analytics dashboard](../task/bookmark-dashboard-ac.md).
-   **Certified**: Dashboards that an administrator has certified \(company approved and recommended for use\). For more information, see [Certify a Platform Analytics dashboard](../task/certify-db-ac.md).
-   **Owned by me**: Dashboards that you own.
-   **Recently opened by me**: Dashboards that you recently opened.
-   **Shared with me**: Dashboards that other users have shared with you.

</td></tr><tr><td>

**Categories**

</td><td>

Available and applied categories for dashboards. As a user with analytics\_categories\_admin role, you can create and customize the categories for the dashboards. For more information on creating dashboard categories, see [Create dashboard categories](../task/db-categories.md#).

</td></tr><tr><td>

3

</td><td>

**Dashboard Statistics**

</td><td>

Dashboard scores. These scores highlight the key dashboard statistics that are based on the following filter conditions:-   Not viewed in 1 year
-   Not viewed in the last 6 months
-   Not viewed in the last 3 months
-   Deactivated for more than 3 months
-   Updated in the last 30 days

Select a score to filter and display the dashboards that match the condition.

</td></tr><tr><td>

4

</td><td>

**Search**

</td><td>

Option for searching dashboards by name or owner.

</td></tr><tr><td>

5

</td><td>

**Filter list**

</td><td>

Launches the condition builder. For more information on using the condition builder, see Create a condition statement using the condition builder.

 The condition builder for dashboards has the following extra options:

-   Saved filters: Options to use a previously saved filter or to save the filter you are currently building. If you save the current filter, you name it and set who can access it.
-   Show/Hide labels: Option to show or hide labels for the fields **Field** and **Operator** in the condition builder.

</td></tr><tr><td>

6

</td><td>

**Personalize List**

</td><td>

Option to add or remove columns in the dashboards list \(![Personalize list icon](../../par-for-workspace/image/icon-personalize-list.png)\).

</td></tr><tr><td>

7

</td><td>

**Delete**

</td><td>

Option to delete the selected dashboards. Available only when at least one dashboard is selected.

</td></tr><tr><td>

8

</td><td>

**Deactivate/Activate**

</td><td>

Option to deactivate or activate the selected dashboards. Available only when at least one dashboard is selected.

</td></tr><tr><td>

9

</td><td>

**Switch to Next UI**

</td><td>

Option to migrate the selected Core UI dashboard to Next Experience UI. Available only when at least one Core UI dashboard is still on the instance. Selecting this option redirects the user to the migration center.

</td></tr><tr><td>

10

</td><td>

**Column Filter** icon

</td><td>

Option for displaying the column filters. Select the operator and the subsequent value. By default, the **Column Filter** is turned off.![First two column filters and show/hide column filter control.](../../par-for-workspace/image/db-lib-column-filters.png)

</td></tr><tr><td>

11

</td><td>

**Selector**

</td><td>

Tick the checkboxes for dashboards to delete, activate/deactivate, or migrate them.

</td></tr><tr><td>

12

</td><td>

Dashboard list

</td><td>

You can see the following columns as a user with an admin role:

-   Name: Name of the dashboard.
-   Description: Description of the dashboard.
-   Active dashboards: Status of the dashboard:
    -   Active
    -   Inactive
-   Views: The number of views for the dashboards in the library.
-   Viewed: The date and time when the dashboard was last viewed.
-   UI version: The UI version of the dashboard:
    -   Next Experience
    -   Core UI
-   Ready to migrate: The migration capability of the Core UI dashboard. The possible values of this column are:
    -   Yes: This value indicates that the Core UI dashboard can be migrated to Next Experience.
    -   No: The Core UI dashboard can’t be migrated to Next Experience because the dashboards contains components that are not compatible with Next Experience.
    -   Already Migrated: This value indicates that the Core UI dashboard is already migrated to the Next Experience UI.
    -   Not Applicable: This value indicates that the dashboard is already on the Next Experience UI version.
-   Certified: Certification status of the dashboard:
    -   Certified: Selected if the dashboard is company approved and recommended for use.
    -   Not Certified: Selected if the dashboard isn’t company approved and not recommended for use.
-   Owned by: Owner of the dashboard.
-   Categories: Categories that are associated with the dashboard.
-   Updated: Date and timestamp when the dashboard was last updated.
-   Updated by: Name of the user who last updated the dashboard.
-   Created: Date and timestamp when the dashboard was created.
-   Created by: Name of the user who created the dashboard.
-   Visibility: The workspaces to which the dashboard can be added. For more information about adding a dashboard to a workspace, see [Add a dashboard to a Dashboards page](../../performance-analytics/task/add-dashboard-to-workspace.md).

</td></tr><tr><td>

13

</td><td>

**Application navigator**

</td><td>

Provides direct access to the [Dashboards](find-dashboard-library.md), [Data Visualizations](../../performance-analytics/concept/explore-data-vis-library.md), and [Indicators](../../performance-analytics/concept/your-kpis.md) libraries. Depending on your roles, you might have access to the Scheduled Exports library or the Usage Insights dashboard.

</td></tr></tbody>
</table>**Note:** A user with the dashboard\_admin role or higher might also see a panel with recommendations about problematic dashboards. For more information, see [Platform Analytics library recommendations](../../par-for-workspace/concept/pa-library-recommendations.md).

**Parent Topic:**[Exploring Platform Analytics dashboards](../reference/ac-elements.md)

