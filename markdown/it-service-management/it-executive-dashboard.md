---
title: Legacy: IT Executive dashboard
description: See a high-level view across all of ITSM.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Legacy: Performance Analytics ITSM Dashboards, ITSM dashboards, IT Service Management]
---

# Legacy: IT Executive dashboard

See a high-level view across all of ITSM.

IT executives can use the [ITSM Success Dashboards](../../../product/itsm-success-dashboard/concept/explore-success-dashboard-indicators.md) to view the metrics for ITSM.

![Animated tour of the tabs of the IT Executive dashboard](../image/itsm-it-executive.gif)

## End user and roles

|End user and goal|Required role|
|-----------------|-------------|
|IT Executive|None|

## Indicators

-   **% of new critical incidents**

    The result of the formula `( [[Number of new incidents > Priority = 1 - Critical]] / [[Number of new incidents]] ) * 100`

-   **% of new critical problems**

    The result of the formula `( [[Number of new problems > Priority = 1 - Critical]] / [[Number of new problems]] ) * 100`

-   **% of open incidents not updated in last 5 days**

    Number of open incidents not updated in last 5 days as a percentage of number of open incidents, according to the formula `( [[Number of open incidents not updated in last 5 days]] / [[Number of open incidents]] ) * 100`.

-   **% of open requested items before due date**

    The result of the formula `( [[Number of open requested items before due date]] / [[Number of open requested items]] ) * 100`

-   **% of overdue requested items**

    The result of the formula `100 - [[% of open requested items before due date]]`

-   **Active Breached SLAs Today**

    The result in percentage of the formula `([[Number of breach task sla today]]/[[Number of active task sla]])*100`

-   **Average age open incidents**

    The result, in days, of the formula `[[Summed age of open incidents]] / [[Number of open incidents]] / 24`

-   **Average Cost per Resolved Incident - Weekly**

    The result of the formula `[[Cost of Incidents Resolved / By week SUM +]]/[[Number of resolved incidents / By week SUM +]]`. In other words, the weekly sum of the cost of resolved incidents, including partial weeks, divided by the weekly sum of resolved incidents, including partial weeks.

-   **Average reassignment of open incidents**

    The result of the formula `[[Summed re-assignment of open incidents]] / [[Number of open incidents]]`

-   **Average resolution time of resolved incidents**

    The result of the formula `[[Summed duration of resolved incidents]] / [[Number of resolved incidents]] / 24`

-   **ITSM Average Overall Customer Satisfaction**

    Average of the normalized score for the Customer Satisfaction survey, as a result of the formula `[[ITSM normalized satisfaction score]] / [[ITSM survey instances]]`

-   **Number of new incidents**

    The number of incidents opened today

-   **Number of new problems**

    The number of incidents opened today

-   **Number of open incidents**

    Number of incidents with no Resolved date

-   **Number of open incidents not updated in last 5 days**

    Number of open incidents with an Updated date of more than five days ago

-   **Number of open requested items**

    Number of requests with a registration date on or before today and no closed date, or a closed date after today

-   **Number of open requested items before due date**

    Number of requested items open today \(before midnight on collection date\) and a due date after midnight on the collection date.

-   **Number of resolved incidents**

    Number of incidents with a value in the Resolved date field


The following indicators do not appear on the dashboard but are used in formulas:

-   **Cost of Incidents Resolved**

    The daily sum of the Value field of incident\_metric records where the Definition field value is Incident Resolution Fixed Cost.

-   **ITSM normalized satisfaction score**

    Sum of the normalized score of metric results for the Customer Satisfaction survey

-   **ITSM survey instances**

    Number of the survey instances of the Customer Satisfaction survey

-   **Number of active task sla**

    The count of active SLA tasks on task\_sla with a start time before today and a stop time after today.

-   **Number of breach task sla today**

    The count of active SLA tasks on task\_sla with a breach time before today

-   **Summed age of open incidents**

    The sum of hours between the time an incident was opened and now

-   **Summed duration of resolved incidents**

    The sum of hours between the time an incident was opened and the time it was resolved

-   **Summed reassignments of open incidents**

    The summed reassignment count of all open incidents


## Breakdowns

-   Age \(Requested Item, Incident\)
-   Assignment Group
-   Backordered \(Requested Item\)
-   Category \(Incident\)
-   Contact Type \(Incident\)
-   Item
-   Opened by Department
-   Priority \(Requested Item, Incident, Problem\)
-   Requested by Department \(Requested Item\)
-   SLA Definition
-   Stage \(Requested Item\)
-   State \(Change, Request, Problem\)

**Parent Topic:**[Legacy: Performance Analytics ITSM Dashboards](itsm-dashboards-content-pack.md)

