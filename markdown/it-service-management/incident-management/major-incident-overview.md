---
title: Legacy: Major incident overview dashboard
description: Major Incident Overview module provides two versions of the Performance Analytics \(PA\) Dashboard to review major incident information at a glance.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Managing major incidents, Incident Management, IT Service Management]
---

# Legacy: Major incident overview dashboard

Major Incident Overview module provides two versions of the Performance Analytics \(PA\) Dashboard to review major incident information at a glance.

**Important:**

Starting in Xanadu release, the Major incident overview dashboard is deprecated. Users can use [Major incident dashboard](../../../use/dashboards/application-content-packs/performance-analytics/major-incident.md) to view the process and communication related metrics for Open and Closed major incidents.

Users with itil, sn\_incident\_write, major\_incident\_manager or communication\_manager role can access the dashboard.

The two versions of the Performance Analytics \(PA\) Dashboard are normal and premium. You must activate the Incident Management - Major Incident Management plugin \(com.snc.incident.mim\) to view the normal dashboard. To access the premium version of Major Incident Overview dashboard, activate Performance Analytics – Content Pack for Major Incident Management \(com.snc.pa.incident.mim\).

You can navigate to the dashboard in the following ways:

-   **Incident** &gt; **Major Incidents** &gt; **Overview**
-   **Self – Service** &gt; **Dashboard** &gt; **Major Incident Overview**

## Major incident overview

![major incident overview](../image/major-incident-overview.png "Major Incident Overview dashboard")

Major Incident Overview module provides information on the following content:

<table id="table_xcw_qrv_kbb"><thead><tr><th>

\#

</th><th>

UI component

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1

</td><td>

Dashboard controls

</td><td>

Provides options to create, duplicate, or delete a dashboard. You can copy the dashboard URL or duplicate the dashboard. In addition, you can add the dashboard in your favorite list, create a tab, or reset filters in the dashboard.

</td></tr><tr><td>

2

</td><td>

Dashboard overview

</td><td>

Takes you to the UI page where you view the recently accessed dashboard, dashboards owned or shared by you, or all the dashboards in the system. To create a new dashboard, click **New**.

</td></tr><tr><td>

3

</td><td>

Dashboard choice list

</td><td>

Provides options to select between different dashboards in the system.

</td></tr><tr><td>

4

</td><td>

Add widgets

</td><td>

Provides option to add widgets. You can drag to move or resize the widget on the dashboard.

</td></tr><tr><td>

5

</td><td>

Sharing

</td><td>

Provides option to specify groups, users, and roles for the dashboard.

</td></tr><tr><td>

6

</td><td>

Configuration

</td><td>

Provides the configuration pane to select a layout to snap the widgets against or to modify a layout as required.

</td></tr><tr><td>

7

</td><td>

Tabs

</td><td>

-   **Major Incidents Nearing Breach**: Number of active major incidents where the Major incident state is **Accepted** and the response or resolution SLA has reached 75% of the allotted time.
-   **Major Incidents Overdue**: Number of active major incidents where the Major incident state is **Accepted** and the response or resolution SLA has breached.
-   **Unassigned Major Incidents**: Number of active major incidents where **Assigned to** is empty.
-   **Open Major Incidents**: Major incidents which are open and has major incident state as **Accepted**.
-   **Major Incidents Opened Today**: Major incident state is **Accepted** and the major incident is created on the current day.

**Note:** Major incidents opened for that day includes both active and inactive incidents.

-   **Major Incidents Resolved Today**: Major incidents that are resolved on the current day and have the state as **Resolved**.
-   **Open Major Incidents – Grouped**: You can filter these incidents based on **Group by** and **Stacked by**.
-   **Open Major Incidents Older Than 7 Days – Grouped**: You can filter these incidents based on **Group by** and **Stacked by**.
-   **Major Incidents by Priority and State**
-   **Major Incidents by Priority and State Older than 7 Days**
-   **Major Incidents Opened per Week**
-   **Major Incidents Closed per Week**

</td></tr></tbody>
</table>## Major Incident Overview – Premium

Major Incident Overview – Premium provides the following additional functions:

-   **Process KPIs**: Provides information on **Active Major Incidents**, **Number of resolved major incidents**, **Average resolution time of Major Incidents**, and **New Major Incidents Vs Resolved**.
-   Interactive filters: Helps to filter incidents based on category, priority, assignment group, and state.

![Major incident overview - premium](../image/major-incident-overview-premium.png "Major Incident Overview – Premium dashboard")

**Parent Topic:**[Managing major incidents](major-incident-management.md)

**Related topics**  


[Create and use dashboards](https://www.servicenow.com/docs/access?context=create-and-edit-dashboards&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)

[Major incident workbench](major-incident-workbench.md)

