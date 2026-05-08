---
title: Dashboards in the library
description: Use Platform Analytics dashboards to access, organize, and share data in a visual format. Dashboards contain data visualizations, filters, and other visual elements.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Explore, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Dashboards in the library

Use Platform Analytics dashboards to access, organize, and share data in a visual format. Dashboards contain data visualizations, filters, and other visual elements.

## Dashboards overview

On Australia instances, you can find both Core UI dashboards and Platform Analytics experience dashboards in the Dashboards library.

To find dashboards in Platform Analytics, navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**. You can also navigate to this library from other Platform Analytics library pages.

Library pages like this one include a navigation pane that provides access to the other libraries and the Usage Insights page. Use it to navigate between the libraries without interrupting your workflow.

The configuration of the Dashboards page and the data access depends on the user roles. Users without an admin role have limited capabilities, as compared to the users with an admin role. For more information on the types of admin roles in Platform Analytics, see [Platform Analytics roles](../../par-for-workspace/reference/platform-analytics-roles.md). To know more about the dashboards for users with the admin roles, see [Dashboards for analytics admins](dashboards-for-admin-users.md).

For users without an admin role, the navigation pane provides a direct access only to the [Dashboards](find-dashboard-library.md), [Data Visualizations](../../performance-analytics/concept/explore-data-vis-library.md), and [Indicators](../../performance-analytics/concept/your-kpis.md) from the Platform Analytics library.

For information on role-based access for the left navigation pane and Platform Analytics overview page, see [Roles applicable for Platform Analytics overview page](../../performance-analytics/concept/analytics-center.md#table_a12_23s_k3c).

The following example shows what a user can see in the Platform Analytics Dashboards library for users without an admin role.

![Platform Analytics Dashboards for users without an admin role.](../../par-for-workspace/image/analytics-center-db-tab-non-admin.png "Platform Analytics Dashboards library for users without an admin role")

The following table shows the common elements that users with and without the admin roles can view in the Dashboards page. Refer to the numbered call-outs in the image and their descriptions in the table.

<table id="table_cjv_rd2_5fc"><thead><tr><th>

No.

</th><th>

Field \(or\) Element Name

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

**Search**

</td><td>

Option for searching dashboards by name or owner.

</td></tr><tr><td>

4

</td><td>

**Filter list**

</td><td>

Launches the condition builder. For more information on using the condition builder, see Create a condition statement using the condition builder.

 The condition builder for dashboards has the following extra options:

-   Saved filters: Options to use a previously saved filter or to save the filter you are currently building. If you save the current filter, you name it and set who can access it.
-   Show/Hide labels: Option to show or hide labels for the fields **Field** and **Operator** in the condition builder.

</td></tr><tr><td>

5

</td><td>

**Personalize List**

</td><td>

Option to add or remove columns in the dashboards list \(![Personalize list icon](../../par-for-workspace/image/icon-personalize-list.png)\).

</td></tr><tr><td>

6

</td><td>

**Column Filter** icon

</td><td>

Option for displaying the column filters. Select the operator and the subsequent value. By default, the **Column Filter** is turned off.![First two column filters and show/hide column filter control.](../../par-for-workspace/image/db-lib-column-filters.png)

</td></tr><tr><td>

7

</td><td>

**Dashboards list**

</td><td>

List of all dashboards. You can filter and sort the list by Name, Description, Views, and Certified.All Users can view the following columns:

-   Name: Name of the dashboard.
-   Description: Description of the dashboard.
-   Certified: Certification status of the dashboard:
    -   Certified: Selected if the dashboard is company approved and recommended for use.
    -   Not Certified: Selected if the dashboard isn’t company approved and not recommended for use.
-   Owned by: Owner of the dashboard.
-   Categories: Categories that are associated with the dashboard.
-   Updated: Date and timestamp when the dashboard was last updated.
-   Updated by: Name of the user who last updated the dashboard.
-   Created: Date and timestamp when the dashboard was created.
-   Created by: Name of the user who created the dashboard.

</td></tr><tr><td>

8

</td><td>

**Application navigator**

</td><td>

Provides direct access to the [Dashboards](find-dashboard-library.md), [Data Visualizations](../../performance-analytics/concept/explore-data-vis-library.md), and [Indicators](../../performance-analytics/concept/your-kpis.md) libraries. Depending on your roles, you might have access to the Scheduled Exports library or the Usage Insights dashboard.

</td></tr></tbody>
</table>**Parent Topic:**[Exploring Platform Analytics dashboards](../reference/ac-elements.md)

