---
title: Legacy: Incident SLA Management dashboard
description: See how well the incidents that are subject to a Service Level Agreement meet the deadlines of those SLAs.
locale: en-US
release: zurich
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Legacy: Incident SLA Management Platform Analytics Solutions, Analytics and reporting, Incident Management, IT Service Management]
---

# Legacy: Incident SLA Management dashboard

See how well the incidents that are subject to a Service Level Agreement meet the deadlines of those SLAs.

**Important:**

Starting in Xanadu release, the Incident SLA Management dashboard is deprecated. Users can use [Incident management dashboard](performance-analytics/incident.md) to view whether the incidents that are subject to a Service Level Agreement, meet the deadlines of those SLAs.

The dashboard title indicates that it is inactive because you activate the solution after configuration and data collection.

![image.incident-sla-management]

## End user and roles

|End user and goal|Required role|
|-----------------|-------------|
|Service Level Manager who is responsible for seeing that incident resolution meets the service level agreements.|sla\_manager, and pa\_viewer for the Incident SLA Assignment tab|

## Indicators

-   **Number of open and overdue incidents**

    The number of open incidents with the following characteristics:

    -   Related to an SLA task of type 'SLA' \(contract\_sla.type\)
    -   Not in stage 'Cancelled' \(task\_sla.stage\)
    -   The amount of time taken to work on the task is over the SLA limit, determined by having an elapsed percentage \(task\_sla.percentage\) value more than 100%.
-   **Number of open incidents that should be resolved in time**

    The number of open incidents with the following characteristics:

    -   Related to an SLA task of type 'SLA' \(contract\_sla.type\)
    -   Not in stage 'Cancelled' \(task\_sla.stage\)
-   **% open and overdue incidents**

    The percentage of open incidents that are overdue. The score is calculated according to the formula \( \[\[Number of open and overdue incidents\]\] / \[\[Number of open incidents that should be resolved in time\]\] \) \* 100.

-   **Number of incidents resolved in time**

    The number of SLA tasks related to an incident with the following characteristics:

    -   The resolution date \(incident.resolved\_at\) is the date that the score is collected.
    -   The type is 'SLA' \(contract\_sla.type\).
    -   The stage is not 'cancelled' \(task\_sla.stage\).
    -   The amount of time taken to close the task is under the SLA limit, determined by having an elapsed percentage \(task\_sla.percentage\) value less than or equal to 100%.
-   **Number of incidents resolved that should have been resolved in time**

    Number of incidents resolved that should have been resolved in time is measured daily as unit \#.

    The goal for this indicator is to maximize.

    The score is the COUNT DISTINCT on the data source Incidents.SLA.Resolved, which is using the table Incident SLA \[incident\_sla\] with the following conditions:

    -   The resolution date \(incident.resolved\_at\) is the date that the score is collected.
    -   The type is 'SLA' \(contract\_sla.type\).
    -   The stage is not 'cancelled' \(task\_sla.stage\).
-   **% incidents resolved in time**

    The percentage of resolved incidents that were resolved in time. The score is calculated according to the formula \( \[\[Number of incidents resolved in time\]\] / \[\[Number of resolved incidents that should be resolved in time\]\] \) \* 100.

-   **Average Resolution Time In Hours For Resolved Incident SLA Tasks**

    The score is calculated according to the following formula: \[\[Summed duration time of resolved incident SLA tasks in hours\]\]/\[\[Total resolved Incident SLA tasks\]\].

-   **Total resolved Incident SLA tasks**

    The score is the COUNT on the data source Incidents.SLA.Resolved, which is using the table Incident SLA \[incident\_sla\] with the following conditions:

    -   The resolution date \(incident.resolved\_at\) is the date that the score is collected.
    -   The type is 'SLA' \(contract\_sla.type\).
    -   The stage is not 'cancelled' \(task\_sla.stage\).
-   **Number of incident assignments responded to in time**

    The number of SLA tasks related to an incident with the following characteristics:

    -   The close date \(task\_sla.end\_time\) is the date that the score is collected.
    -   The type is 'OLA' \(contract\_sla.type\), meaning that it is a response task.
    -   The stage is not 'cancelled' \(task\_sla.stage\).
    -   The amount of time taken to close the task is under the SLA limit, determined by having an elapsed percentage \(task\_sla.percentage\) value less than or equal to 100%.
-   **Number of incident assignments that should have been responded to in time**

    The number of SLA tasks related to an incident with the following characteristics:

    -   The close date \(task\_sla.end\_time\) is the date that the score is collected.
    -   The type is 'OLA' \(contract\_sla.type\), meaning that it is a response task.
    -   The stage is not 'cancelled' \(task\_sla.stage\).
-   **Number of open and overdue incident assignments**

    The number of SLA tasks related to an incident with the following characteristics:

    -   The type is 'OLA' \(contract\_sla.type\), meaning that it is a response task.
    -   The stage is not 'cancelled' \(task\_sla.stage\).
    -   The amount of time taken to work on the task is over the SLA limit, determined by having an elapsed percentage \(task\_sla.percentage\) value more than 100%.
-   **Number of open incident assignments that should be responded to in time**

    The number of open incidents related to an SLA task with the following characteristics:

    -   The type is 'OLA' \(contract\_sla.type\), meaning that it is a response task.
    -   The stage is not 'cancelled' \(task\_sla.stage\).
    -   The response task is still open.
-   **% incident assignments responded to in time**

    The percentage of response tasks that were responded to within the SLA limit. The score is calculated according to the following formula: \( \[\[Number of incident assignments responded to in time\]\] / \[\[Number of incident assignments that should have been responded to in time\]\] \) \* 100.

-   **% open and overdue incident assignments**

    The percentage of open incident assignments that are overdue according to the SLA limit. The score is calculated according to the following formula: \( \[\[Number of open and overdue incident assignments\]\] / \[\[Number of open incident assignments that should be responded to in time\]\] \) \* 100.

-   **Summed duration time of resolved incident SLA tasks in hours**

    This indicator sums the results of a script run on the Incident SLA \[incident\_sla\] table that calculates the time it took for an incident SLA task to be resolved. This indicator is used to calculate formulas but is not displayed directly on the dashboard:


## Breakdowns

-   State
-   Priority
-   Category
-   Assignment Group
-   Task SLA Breached Status

**Parent Topic:**[Legacy: Incident SLA Management Platform Analytics Solutions](incident-sla-content-pack.md)

