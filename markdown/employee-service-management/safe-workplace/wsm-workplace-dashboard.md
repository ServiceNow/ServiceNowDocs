---
title: Workplace dashboard in Workplace Service Portal
description: Use the Workplace Dashboard from Workplace Service Portal to visually analyze the available workspace capacity, space request and reservation trends, and monitor the maintenance tasks of your workplace. You can also reserve a space for an employee or create a workplace maintenance task directly from this Workplace Service Portal page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/safe-workplace/wsm-workplace-dashboard.html
release: australia
product: Safe Workplace
classification: safe-workplace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Workplace dashboards, Workplace Core, Safe Workplace, Health and Safety, Employee Service Management]
---

# Workplace dashboard in Workplace Service Portal

Use the Workplace Dashboard from Workplace Service Portal to visually analyze the available workspace capacity, space request and reservation trends, and monitor the maintenance tasks of your workplace. You can also reserve a space for an employee or create a workplace maintenance task directly from this Workplace Service Portal page.

To open the Workplace dashboard on the Workplace Service Portal, navigate to **Workplace Core** &gt; **Dashboard**.

Selecting a region and site in the filter at the top displays reports for available campuses in separate tabs.

**Important:** For new customers, from Workplace Core \(sn\_wsd\_core\) version 2.2, the **Dashboard** is removed from the Workplace Service Portal and Service Portal. Customers using Workplace Core version 2.1 and below can still access the dashboard after an upgrade.

\[Omitted image "workplace-dashboard.png"\] Alt text: Workplace dashboard displaying example data

## End user and roles

<table id="table_ov2_tj4_2fb"><thead><tr><th>

End user and goal

</th><th>

Required role

</th><th>

Benefits

</th></tr></thead><tbody><tr><td>

Workplace manager: Needs clear visibility into the real-time status of the workplace space utilization and cleaning activities for shifts.

</td><td>

sn\_wsd\_core.workplace\_manager

</td><td>

-   Can plan for the phased return of employees to the workplace after an emergency situation
-   Can monitor progress of workplace tasks for various office locations

</td></tr></tbody>
</table>## Data visualizations

The data displayed in visualizations corresponds to the selected campus.

|Title|Type|Description|
|-----|----|-----------|
|Today's capacity|Single score \[Omitted image "single-score.png"\] Alt text: Single-score icon|Number of active workspaces available today.|
|Today's shifts|Single score \[Omitted image "single-score.png"\] Alt text: Single-score icon|Number of shifts used in today's reservations.|
|Today's reservable spaces|Single score \[Omitted image "single-score.png"\] Alt text: Single-score icon|Number of active workspaces available to reserve.|
|Today's reservations|Single score \[Omitted image "single-score.png"\] Alt text: Single-score icon|Number of today's active reservations.|
|Reservations per day|Trend \[Omitted image "column-time-icon.png"\] Alt text: Trend over time icon|Trend of the number of active reservations per day in the last seven days for which the end date is today or later.|
|Reserved spaces per day|Spline \[Omitted image "spline-ts-icon.png"\] Alt text: Spline trend icon|Trend of the number of reserved workspaces per day for all reservations made in the last seven days that are active starting today or later.|
|Reservable spaces per building|Bar \[Omitted image "column-icon.png"\] Alt text: Bar graph icon|Breakdown of active workspaces that are available to reserve for each building on the campus.|
|Cleaning tasks for this campus|
|Unassigned cleaning tasks|Single score \[Omitted image "single-score.png"\] Alt text: Single-score icon|Number of active workplace tasks that are not assigned to anyone and not in the Closed state.|
|Planned tasks|Single score \[Omitted image "single-score.png"\] Alt text: Single-score icon|Number of active planned workplace tasks that are not yet closed.|
|Cleaning tasks by day|Trend \[Omitted image "column-time-icon.png"\] Alt text: Trend over time icon|Trend of the number of active cleaning tasks per day for which the due date is between today and the next seven days, or for which no due date is defined. The tasks in this report are grouped by the workplace task type.|
|Workplace requests for this campus|
|Pending workplace requests|Single score \[Omitted image "single-score.png"\] Alt text: Single-score icon|Number of workplace requests that are pending.|
|Workplace requests created today|Single score \[Omitted image "single-score.png"\] Alt text: Single-score icon|Total number of workplace reservation requests created by the employees today.|
|Workplace requests by day|Trend \[Omitted image "column-time-icon.png"\] Alt text: Trend over time icon|Trend of the number of workplace reservation requests created per day.|

**Parent Topic:**[Workplace dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

**Related topics**  


[Create workplace reservations for an employee](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/safe-workplace/reserve-workspaces-for-employees.md)

[Create an ad hoc workplace task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/safe-workplace/create-adhoc-workplace-task.md)

