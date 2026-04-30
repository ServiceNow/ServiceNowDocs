---
title: Legacy: Open Incidents Age Monitor dashboard
description: View average age and assignment times and breakdown incidents in different age buckets.
locale: en-US
release: yokohama
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Legacy: Incident Management Platform Analytics Solutions, Analytics and reporting, Incident Management, IT Service Management]
---

# Legacy: Open Incidents Age Monitor dashboard

View average age and assignment times and breakdown incidents in different age buckets.

**Important:**

Starting in Xanadu release, the Open Incidents Age Monitor dashboard is deprecated. Users can use [Incident management dashboard](performance-analytics/incident.md) to view the average age and assignment times and breakdown incidents in different age buckets.

![Open incidents age monitor workbench widget](../image/open-incidents-age-monitor.png "Open Incident Age Monitor")

## End user and roles

|End user and goal|Required role|
|-----------------|-------------|
|Incident Manager: Needs to know how the incident management process is doing so they can plan for the future.|itil|

## Indicators

-   **Number of open incidents**

    Daily count of the number of incidents that do not have a resolution date. This indicator is used as the basis of several other indicators on this dashboard.

-   **Average age of open incidents**

    The average age in days in which an incident has been open. The score is calculated according to the formula \[\[Summed age of open incidents\]\]/\(\[\[Number of open incidents\]\]\*24\).

-   **Average reassignment of open incidents**

    The average number of times currently open incidents have been reassigned. This indicator is shown as 'Average re-assignment times' in the Process by State tab. The score is calculated according to the formula \[\[Summed re-assignment of open incidents\]\] / \[\[Number of open incidents\]\].

-   **Average age of last update of open incidents**

    How long on average it has been since the last update to one of the currently open incidents, in days. The score is calculated according to the formula \[\[Summed age of last update of open incidents\]\] / \(\[\[Number of open incidents\]\] \* 24\)


The following indicators are not shown directly on the dashboard but are used in calculating formulas:

-   Summed age of open incidents
-   Summed re-assignment of open incidents
-   Summed age of last update of open incidents

## Breakdowns

-   Priority
-   Category
-   Assignment Group
-   State

**Parent Topic:**[Legacy: Incident Management Platform Analytics Solutions](incident-content-pack.md)

