---
title: Legacy: Incident Premium dashboard
description: This dashboard uses Workbench widgets and other advanced Platform Analytics features to give you all the information about the Incident process in one place.
locale: en-US
release: zurich
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Legacy: Incident Management Platform Analytics Solutions, Analytics and reporting, Incident Management, IT Service Management]
---

# Legacy: Incident Premium dashboard

This dashboard uses Workbench widgets and other advanced Platform Analytics features to give you all the information about the Incident process in one place.

**Important:**

Starting in Xanadu release, the Incident Premium dashboard is deprecated. Users can use [Incident management dashboard](performance-analytics/incident.md) for Workbench widgets and other advanced Platform Analytics features to know about the Incident process in one place.

![Incident Premium dashboard tabs](../image/incident-premium-tab-p.gif "Tabs of the Incident Premium dashboard")

## Access the Incident Premium dashboard

To access the Incident Premium dashboard, navigate to **All** &gt; **Self-Service** &gt; **Dashboard**. On the Dashboards Overview, search for Incident Premium dashboard.

![Incident premium dashboard search on dashboards](../image/incident-premium-location-p.png)

## End user and roles

<table id="table_dvp_m42_hsb"><thead><tr><th>

End user

</th><th>

Description

</th><th>

Required role

</th></tr></thead><tbody><tr><td>

IT Agent

</td><td>

Views the assigned work and group work, reports, and prioritize workload

</td><td>

-   itil
-   sn\_incident\_read
-   pa\_contributor
-   pa\_viewer

</td></tr><tr><td>

IT Manager

</td><td>

Views the group work and reports and also can edit the required data and dashboard layout

</td><td>

-   itil
-   sn\_incident\_read
-   pa\_contributor
-   pa\_viewer
-   pa\_admin
-   pa\_power\_user

</td></tr></tbody>
</table>## Indicators

-   **Number of open incidents**

    Daily count of the number of incidents that do not have a resolution date. This indicator is used as the basis of several other indicators on this dashboard.

-   **Number of new incidents**

    Daily count of the number of incidents opened 'today.'

-   **Number of closed incidents**

    Daily count of indicators with State = Closed.

-   **Number of resolved incidents**

    Daily count of indicators with State = Resolved.

-   **Average age of open incidents**

    The average age in days in which an incident has been open. The score is calculated according to the formula \[\[Summed age of open incidents\]\]/\(\[\[Number of open incidents\]\]\*24\).

-   **Average reassignment of open incidents**

    The average number of times currently open incidents have been reassigned. This indicator is shown as 'Average re-assignment times' in the Process by State tab. The score is calculated according to the formula \[\[Summed re-assignment of open incidents\]\] / \[\[Number of open incidents\]\].

-   **Average age of last update of open incidents**

    How long on average it has been since the last update to one of the currently open incidents, in days. The score is calculated according to the formula \[\[Summed age of last update of open incidents\]\] / \(\[\[Number of open incidents\]\] \* 24\)

-   **% of incidents not updated in last 5 days**

    The percentage of currently open incidents that have not been updated for the last five days. The score is calculated according to the formula \( \[\[Number of open incidents not updated in last 5 days\]\] / \[\[Number of open incidents\]\] \) \* 100

-   **% of incidents not updated in last 30 days**

    The percentage of currently open incidents that have not been updated for the last 30 days. The score is calculated according to the formula \( \[\[Number of open incidents not updated in last 30 days\]\] / \[\[Number of open incidents\]\] \) \* 100

-   **% of new critical incidents**

    The percentage of new incidents filtered on the Priority breakdown with the breakdown element 1 - Critical. The score is calculated according to the formula \( \[\[Number of new incidents &gt; Priority = 1 - Critical\]\] / \[\[Number of new incidents\]\] \) \* 100.

-   **Average close time of incidents**

    The average amount of time in days it takes to close an incident. The score is calculated according to the formula \[\[Summed duration of closed incidents\]\] / \(\[\[Number of closed incidents\]\] / 24\)

-   **% of incidents resolved without reassigning**

    The percentage of incidents with a State of Resolved that were never reassigned from the first assignment group. The score is calculated according to the formula \[\[Number of resolved incidents by first assigned group\]\] / \[\[Number of resolved incidents\]\] \* 100.

-   **% of incidents closed by self-service**

    The percentage of incidents with State = Closed and Close code = Closed/Resolved by Caller. The score is calculated according to the formula \[\[Number of incidents closed by self-service\]\] / \[\[Number of closed incidents\]\] \* 100.

-   **% of open incidents reassigned at least once**

    The percentage of incidents that are open and that have been transferred at least once. The score is calculated according to the formula \[\[Number of reassigned open incidents\]\] / \[\[Number of open incidents\]\] \* 100

-   **% of incidents resolved same day opened**

    The percentage of incidents with State = Resolved where the day in the Resolved field is the same as the day in the Opened field. The score is calculated according to the formula \[\[Number of incidents resolved on the same day opened\]\] / \[\[Number of resolved incidents\]\] \* 100.

-   **% of incidents not solved**

    The percentage of closed incidents where Close code = Not Solved \(Not Reproducible\) or Not Solved \(Too Costly\). The score is calculated according to the formula \[\[Number of incidents not solved\]\] / \[\[Number of closed incidents\]\] \* 100.


The following indicators are not shown directly on the dashboard but are used in calculating formulas:

-   Summed age of open incidents
-   Summed re-assignment of open incidents
-   Summed age of last update of open incidents
-   Number of open incidents not updated in last 5 days
-   Number of open incidents not updated in last 30 days
-   Summed duration of closed incidents
-   Number of resolved incidents by first assigned group
-   Number of incidents closed by self-service
-   Number of reassigned open incidents
-   Number of incidents resolved on the same day opened
-   Number of incidents not solved

## Breakdowns

-   Priority
-   Category
-   Assignment Group
-   State

## Data visualizations

|Title|Type|Description|
|-----|----|-----------|
|Incidents Opened Today|Single score \(![Singe score icon](../../reporting/image/icon-single-score-report-p.png)\)|Total number of incidents created on the current date.|
|Unassigned Incidents|Single score \(![Singe score icon](../../reporting/image/icon-single-score-report-p.png)\)|Total number of incidents that are still not assigned.|
|Overdue Incidents|Single score \(![Singe score icon](../../reporting/image/icon-single-score-report-p.png)\)|Total number of incidents that exceed its SLA.|
|Open Incidents|Single score \(![Singe score icon](../../reporting/image/icon-single-score-report-p.png)\)|Total number of incidents that do not have a resolution date.|
|Incidents not updated for 7 days|Single score \(![Singe score icon](../../reporting/image/icon-single-score-report-p.png)\)|Total number of incidents that were updated more than 7 days ago.|
|Open incidents older than 30 days|Single score \(![Singe score icon](../../reporting/image/icon-single-score-report-p.png)\)|Total number of open incidents that were created 30 days ago.|
|Open Incidents - Grouped|Vertical bar \(![Vertical bar](../../reporting/image/icon-bar-report-p.png)\)|Total number of open incidents grouped by priority.|
|Open incidents older than 30 days - Grouped|Horizontal bar \(![Horizontal bar](../../reporting/image/icon-horizontal-bar-report-p.png)\)|Total number of open incidents that were created more than 30 days ago.|
|Incidents by Priority and State|Heatmap icon \(![Heatmap icon](../../reporting/image/icon-heatmap-report-p.png)\)|Total number of incidents grouped by priority and state.|
|Incidents by Priority and State older than 30 days|Heatmap icon \(![Heatmap icon](../../reporting/image/icon-heatmap-report-p.png)\)|Total number of incidents grouped by priority and state that were created more than 30 days ago.|
|Incidents per week|Area icon \(![Area icon](../../reporting/image/icon-area-report-p.png)\)|Total number of incidents opened or closed in each week.|
|Open Incidents older than 30 days by Assignment Group and State|Heatmap icon \(![Heatmap icon](../../reporting/image/icon-heatmap-report-p.png)\)|Total number of incidents opened more than 30 days ago and that are grouped by assignment group and state of the incident.|
|Open Incidents Not Updated In Last 30 Days by Assignment Group and State|Heatmap icon \(![Heatmap icon](../../reporting/image/icon-heatmap-report-p.png)\)|Total number of open incidents updated more than 30 days ago and that are grouped by assignment group and state of the incident.|
|Open Incidents where assignee is not active|Heatmap icon \(![Heatmap icon](../../reporting/image/icon-heatmap-report-p.png)\)|Total number of incidents where the user in the **Assigned to** field have an inactive status.|
|Open Incidents with closed Problem|Heatmap icon \(![Heatmap icon](../../reporting/image/icon-heatmap-report-p.png)\)|Total number of open incidents that have an associated problem with closed status.|

## Filters

The dashboard includes the following filters:

|Name|Type|Description|
|----|----|-----------|
|Incident Priority|Choice list|Filter the report visualizations based on the **Priority** of the incident record.|
|Incident State|Choice list|Filter the report visualizations based on the **State** of the incident record.|
|Incident Assignment Group|Reference|Filter the report visualizations based on the **Assignment group** associated with the incident record.|
|Incident Category|Choice list|Filter the report visualizations based on the **Category** of the incident record.|
|Incident Opened|Date|Filter the report visualizations based on the date when the incident is created.|

**Parent Topic:**[Legacy: Incident Management Platform Analytics Solutions](incident-content-pack.md)

