---
title: Legacy: Incident Management dashboard
description: The Incident Management dashboard lets you see recent trends in incident creation, duration, and resolution. Use the information on this dashboard to spot problem areas and plan your incident management strategy going forward.
locale: en-US
release: zurich
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Legacy: Incident Management Platform Analytics Solutions, Analytics and reporting, Incident Management, IT Service Management]
---

# Legacy: Incident Management dashboard

The Incident Management dashboard lets you see recent trends in incident creation, duration, and resolution. Use the information on this dashboard to spot problem areas and plan your incident management strategy going forward.

**Important:**

Starting in Xanadu release, the Incident Management dashboard is deprecated. Users can use [Incident management dashboard](performance-analytics/incident.md) to view the recent trends in incident creation, duration, and resolution and plan the incident management strategy accordingly.

![Animated gif taking you through the tabs of the dashboard](../../performance-analytics/image/Incident-Management-dashboard_V2.gif "Tabs of the Incident Management dashboard")

## End user and roles

|End user and goal|Required role|
|-----------------|-------------|
|Incident Manager: Needs to know how the incident management process is doing so they can plan for the future.|itil|

## Indicators

-   **Number of open incidents**

    Daily count of the number of incidents that do not have a resolution date. This indicator is used as the basis of several other indicators on this dashboard.

-   **Number of open incidents not updated in last 5 days**

    Daily count of the number of incidents last updated more than five days ago.

-   **Number of open incidents not updated in last 30 days**

    Daily count of the number of incidents last updated more than 30 days ago.

-   **Number of new incidents**

    Daily count of the number of incidents opened 'today.'

-   **Number of resolved incidents**

    Daily count of indicators with State = Resolved.

-   **Incident Backlog Growth**

    Tracks the increase or decrease in open incidents. The score is calculated according to the formula \[\[Number of new incidents\]\] - \[\[Number of resolved incidents\]\].

-   **Average age of open incidents**

    The average age in days in which an incident has been open. The score is calculated according to the formula \[\[Summed age of open incidents\]\]/\(\[\[Number of open incidents\]\]\*24\).

-   **% of new critical incidents**

    The percentage of new incidents filtered on the Priority breakdown with the breakdown element 1 - Critical. The score is calculated according to the formula \( \[\[Number of new incidents &gt; Priority = 1 - Critical\]\] / \[\[Number of new incidents\]\] \) \* 100.

-   **Average resolution time of resolved incidents**

    The average number of days it takes to resolve an incident, provided it is resolved. The score is calculated according to the formula \[\[Summed duration of resolved incidents\]\] / \(\[\[Number of resolved incidents\]\] \* 24\).


The following indicators are not shown directly on the dashboard but are used in calculating formulas:

-   Summed age of open incidents
-   Summed duration of resolved incidents

## Breakdowns

-   Category
-   Priority
-   Age

**Parent Topic:**[Legacy: Incident Management Platform Analytics Solutions](incident-content-pack.md)

