---
title: Find a responsive dashboard
description: Use dashboard categories, dashboard groups, and dashboard lists to find the dashboard you want to use.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [what role is needed to see dashboards]
breadcrumb: [Working with responsive dashboards, Create and use dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Find a responsive dashboard

Use dashboard categories, dashboard groups, and dashboard lists to find the dashboard you want to use.

## Before you begin

**Note:** This topic refers to Dashboards in the Core UI. If your instance is migrated to Platform Analytics experience, see [Dashboards in the library](../concept/find-dashboard-library.md).

Role required: There are no specific permissions required to view dashboards. However, you must have permission to view at least one dashboard to see the Dashboards Overview and the dashboard picker. For more information about dashboard permissions, see [Solving permissions issues on a responsive dashboard](../../performance-analytics/task/troubleshoot-dashboard-permissions.md#).

## About this task

On the Dashboards Overview, each tile contains information about the dashboard it represents: Thumbnails of the widgets on the dashboard, the Dashboard group, your role on the dashboard, the name of the dashboard, and the owner of the dashboard. Dashboards that are not assigned a group by their creators are assigned the group **Other**.

![Dashboard tile example with callouts for dashboard group, the viewer's role, the widget types on the dashboard, and the dashboard name](../image/dashboard-tile-layout-p.png)

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Dashboards** or **All** &gt; **Performance Analytics** &gt; **Dashboards**. The Dashboards Overview shows tiles representing the most recent dashboards you have visited.

    If Platform Analytics experience is enabled, the dashboard picker shows both Core UI and Platform Analytics experience dashboards.

    ![Dashboards overview with Recent category selected.](../image/db-overview-p.png)

2.  Select a category:

    -   **Recent** shows up to nine dashboards that you have visited recently. The most recent are shown first.
    -   **Owned by me** shows the dashboards that you have created and those dashboards to which you have been assigned ownership.
    -   **Shared with me** shows the dashboards which have been shared with you as a user, or member of a group or role.
    -   **All** shows all the dashboards that you have access to.
    All tabs except for the Recent tab are sorted in ascending order by:

    1.  Dashboard group — Order

        The owner of the dashboard can specify an order number in the dashboard group's form. This field is optional.

    2.  Dashboard group — Name
    3.  Dashboard — Order

        The owner of the dashboard can specify an order number in the dashboard's form. This field is optional.

    4.  Dashboard — Name
3.  Select a group from the **Groups** list to filter the displayed tiles on a dashboard group.

    If no dashboards match the combination of category and group, a message is shown, for example, No dashboards shared with you match your search.

4.  Type a string in the **Search dashboard** box to filter the dashboards further.

    -   Put your search string in double quotes to find an exact match. Searching for `"Open Incidents"` returns the dashboard called Open Incidents, but not Open Incidents Age Monitor.
    -   Enter your search string without double quotes to return all matches that contain the string. Searching for `Open Incidents` returns the dashboards Open Incidents, Open Incidents Reports, and Open Incident State Monitor.
    **Note:** Neither of these search strings returns the keywords in a different order. For example, neither will return the dashboard Incidents Open This Week.

    Search results are limited to 100 results per category. To change this value, create and configure the system property **glide.cms.dashboards.sharing.search.maxRecords**. For more information see [Responsive dashboard properties](../reference/dashboard-properties.md).

5.  Select a dashboard tile to open that dashboard.

6.  On any open dashboard, select the Dashboards Overview icon \(![Dashboards overview icon](../image/db-grid-icon.png)\) to return to the Dashboards Overview.

7.  To find another dashboard, click the arrow next to the dashboard name to open the Dashboard Picker.

    You can:

    -   Start typing in the **Search by name or group** box to filter the list.
    -   Select the **Group filter** to filter the list on a specific dashboard group.

        The **Group filter** shows all dashboard groups in the instance. If you do not have permission to view any dashboards in a selected group, you will see the message, No dashboards shared with you match your search

    -   Scroll through all dashboards you have permission to open, starting with the most recent that you have viewed.
    ![Dashboard picker with callouts for the Dashboards Overview icon, the dashboard picker, and the dashboard group selector.](../image/db-picker-p.png)

8.  Select the name of a dashboard to replace the current dashboard with the new one.


