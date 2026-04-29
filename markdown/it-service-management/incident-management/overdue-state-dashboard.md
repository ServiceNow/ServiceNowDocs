---
title: Legacy: Overdue by State dashboard
description: This dashboard lets you see incidents that are overdue according to an SLA, divided by the New, In Progress, and On Hold states.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Legacy: Incident SLA Management Platform Analytics Solutions, Reporting incidents, Incident Management, IT Service Management]
---

# Legacy: Overdue by State dashboard

This dashboard lets you see incidents that are overdue according to an SLA, divided by the New, In Progress, and On Hold states.

**Important:**

Starting in Xanadu release, the Overdue by State dashboard is deprecated. Users can use [Incident management dashboard](performance-analytics/incident.md) to view the incidents that are overdue according to an SLA, divided by the New, In Progress, and On Hold states.

You use this dashboard to view the average age of the incidents, the average number of times they have been reassigned, and how long on average since the last update. You can also group them by standard breakdowns like Priority and Assignment Group. This dashboard is inactive by default. Before using this dashboard, a Performance Analytics administrator or power user must open the Dashboard Properties, assign an owner, and select **Active**.

![Incident overdue by state dashboard with workbench widget](../image/incident-sla-overdue-state.png)

## End user and roles

|End user and goal|Required role|
|-----------------|-------------|
|Service Level Manager who is responsible for seeing that incident resolution meets the service level agreements.|sla\_manager|

## Indicators

-   **Number of open and overdue incidents**

    The number of incidents on the Incident.SLA.Open indicator source with the following characteristics:

    -   Related to an SLA task of type 'SLA' \(contract\_sla.type\)
    -   Not in stage 'Cancelled' \(task\_sla.stage\)
    -   The amount of time taken to work on the task is over the SLA limit, determined by having an elapsed percentage \(task\_sla.percentage\) value more than 100%.
-   **Average age open and overdue incidents**

    The score is calculated according to the following formula: \[\[Summed age of open and overdue incidents\]\] / \[\[Number of open incidents that should be resolved in time\]\]

-   **Average reassignments of open and overdue incidents**

    The score is calculated according to the following formula: \[\[Summed reassignments of open and overdue incidents\]\] / \[\[Number of open and overdue incidents\]\]

-   **Average age of updated since of open and overdue incidents**

    The average length of time in days since the last update of open, overdue incidents. The score is calculated according to the following formula: \[\[Summed age of updated since of open and overdue incidents\]\] / \[\[Number of open and overdue incidents\]\] / 24


The following indicators are used to calculate formulas but are not displayed directly on the dashboard:

-   **Number of open incidents that should be resolved in time**

    The number of open incidents with the following characteristics:

    -   Related to an SLA task of type 'SLA' \(contract\_sla.type\)
    -   Not in stage 'Cancelled' \(task\_sla.stage\)
-   **Summed age of open and overdue incidents**

    Summed age of open incidents related to an SLA task with the following characteristics:

    -   Related to an SLA task of type 'SLA' \(contract\_sla.type\)
    -   Not in stage 'Cancelled' \(task\_sla.stage\)
    -   The amount of time taken to work on the task is over the SLA limit, determined by having an elapsed percentage \(task\_sla.percentage\) value more than 100%.
-   **Summed age of updated since of open and overdue incidents**

    Sum of hours since the last update of all open and overdue incidents.

-   **Summed reassignments of open and overdue incidents**

    The sum of the Reassignment Count field of all open and overdue incidents.


## Breakdowns

-   State
-   Priority
-   Age
-   Assignment Group
-   SLA

**Parent Topic:**[Legacy: Incident SLA Management Platform Analytics Solutions](incident-sla-content-pack.md)

