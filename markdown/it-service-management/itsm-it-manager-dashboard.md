---
title: Legacy: IT Manager dashboard
description: Follow the daily and weekly progress of incidents, problems, and requests for your assignment groups.Define generic industry-based fixed costs to analyze impact by channel using the IT Manager dashboard in ITSM Performance Analytics Solutions.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 10
breadcrumb: [Legacy: Performance Analytics ITSM Dashboards, Platform Analytics ITSM Dashboards, IT Service Management]
---

# Legacy: IT Manager dashboard

Follow the daily and weekly progress of incidents, problems, and requests for your assignment groups.

**Important:** Starting with the Xanadu release, the IT Manager dashboard is deprecated. Users can access the [ITSM Success Dashboards](../../../product/itsm-success-dashboard/concept/explore-success-dashboard-indicators.md) to view the metrics for their assignment groups.

![Animated tour of the tabs of the IT Manager dashboard](../image/itsm-it-manager.gif)

## End user and roles

|End user and goal|Required role|
|-----------------|-------------|
|IT Manager - Needs to track the progress of their group in resolving incidents, problems, and requests|pa\_viewer is required to see lists of indicators|

## Indicators

-   **% Closed Requests with Breached SLA**

    The results of the formula `([[Number of Closed Requests with Breached SLAs]]/[[Number of closed requests]]) * 100`

-   **% of incidents resolved by first assigned group**

    The results of the formula `( [[Number of resolved incidents by first assigned group]] / [[Number of resolved incidents]] ) * 100`

-   **% of open incidents missed SLA**

    The percentage of open incidents that did not meet the SLA, as calculated by the formula `[[Number of incidents missed SLA]] / [[Number of open incidents]] * 100`

-   **% of open incidents not updated in last 5 days**

    Number of open incidents not updated in last 5 days as a percentage of number of open incidents, according to the formula `( [[Number of open incidents not updated in last 5 days]] / [[Number of open incidents]] ) * 100`.

-   **% of open incidents with problem**

    The result of the formula `[[Number of open incidents with problem]] / [[Number of open incidents]] * 100`

-   **% of open problems not updated in last 30 days**

    The result of the formula `( [[Number of open problems not updated in last 30 days]] / [[Number of open problems]] ) * 100`

-   **% of open problems with at least one incident**

    The result of the formula `[[Number of open problems with at least one open incident]] / [[Number of open problems]] * 100`

-   **% open and overdue incidents**

    The result of the formula `( [[Number of open and overdue incidents]] / [[Number of open incidents that should be resolved in time]] ) * 100`

-   **% Resolved Incidents with Breached SLA**

    The result of the formula `([[Number of Resolved Incidents with Breached SLAs]]/[[Number of resolved incidents]]) * 100`

-   **Active Breached SLAs Today**

    The result in percentage of the formula `([[Number of breach task sla today]]/[[Number of active task sla]])*100`

-   **Average age of open problems**

    The result, in days, of the formula `[[Summed age of open problems]] / [[Number of open problems]] / 24`

-   **Average age of open requests**

    The result, in days, of the formula `[[Summed age of open requests]] / [[Number of open requests]] / 24`

-   **Average age open incidents**

    The result, in days, of the formula `[[Summed age of open incidents]] / [[Number of open incidents]] / 24`

-   **Average close time of requests**

    The result, in days, of the formula `[[Summed duration of closed requests]] / [[Number of closed requests]] / 24`

-   **Average Cost per Incident**

    The result of the formula `[[Cost of Incidents Resolved]]/[[Number of resolved incidents]]`, when the number of resolved incidents is more than zero.

-   **Average Cost per Request**

    The result of the formula `[[Cost of Requests Completed]]/[[Number of completed requests]]`, when the number of completed requests is more than zero.

-   **Average Cost per Request - Weekly**

    The result of the formula `[[Cost of Requests Completed / By week SUM +]]/[[Number of completed requests / By week SUM +]]`. In other words, the weekly sum of the cost of completed requests, including partial weeks, divided by the weekly sum of completed requests, including partial weeks.

-   **Average Cost per Resolved Incident - Weekly**

    The result of the formula `[[Cost of Incidents Resolved / By week SUM +]]/[[Number of resolved incidents / By week SUM +]]`. In other words, the weekly sum of the cost of resolved incidents, including partial weeks, divided by the weekly sum of resolved incidents, including partial weeks.

-   **Average reassignments of open and overdue incidents**

    The result of the formula `[[Summed reassignments of open and overdue incidents]] / [[Number of open and overdue incidents]]`

-   **Average resolution time of resolved incidents**

    The result of the formula `[[Summed duration of resolved incidents]] / [[Number of resolved incidents]] / 24`

-   **Closed workload**

    The result of the formula `[[Number of closed incidents]] + [[Number of closed problems]] + [[Number of closed requests]]`

-   **ITSM Average Overall Customer Satisfaction**

    Average of the normalized score for the Customer Satisfaction survey, as a result of the formula `[[ITSM normalized satisfaction score]] / [[ITSM survey instances]]`

-   **New workload**

    The result of the formula `[[Number of new incidents]] + [[Number of new problems]] + [[Number of new requests]]`

-   **Number of closed complete requests**

    Number of requests closed today as complete \(State = Complete\)

-   **Number of closed incidents**

    The number of incidents closed today

-   **Number of closed problems**

    The number of probems closed today

-   **Number of closed requests**

    The number of requests closed today

-   **Number of Closed Requests with Breached SLAs**

    Count Distinct of SLA tasks \[task\_sla\] with a task type of Request, Has breached = true, Stage != Cancelled, and closed today

-   **Number of new incidents**

    The number of incidents opened today

-   **Number of new problems**

    The number of incidents opened today

-   **Number of new requests**

    The number of incidents opened today

-   **Number of open changes planned in the next 7d**

    The number of Change Request \[change\_request\] records opened today with a Planned Start date between today and the end of next week

-   **Number of open incident unassigned**

    The number of open incidents not assigned to anyone

-   **Number of open incidents**

    Number of incidents with no Resolved date

-   **Number of open incidents not updated in last 5 days**

    Number of open incidents with an Updated date of more than five days ago

-   **Number of open and overdue incidents**

    The number of open incidents related to an SLA task that is not in the Cancelled stage \(task\_sla.stage\) and has an actual elapsed percentage greater than 100% \(task\_sla.percentage\).

-   **Number of open incidents that should be resolved in time**

    The count distinct of open incidents associated with an SLA task \[task\_sla\] that is not in the Cancelled stage.

-   **Number of open incidents with problem**

    The number of open incidents with a value in the Problem field

-   **Number of open problems**

    The number of problems opened on or before today and not yet closed.

-   **Number of open problems not updated in last 30 days**

    Number of open problems with an Updated date of more than 30 days ago

-   **Number of open problems with at least one open incident**

    The count distinct of open incidents where the Problem Active field value is true.

-   **Number of open requests**

    Number of requests opened on or before today and not yet closed

-   **Number of requests closed after due date**

    Number of requests that are closed after request due date \(sc\_request.closed\_at &gt; sc\_request.due\_date\)

-   **Number of resolved incidents**

    Number of incidents with a value in the Resolved date field

-   **Number of resolved incidents by first assigned group**

    Number of incidents that were resolved by the first group assigned to them

-   **Open workload**

    The result of the formula `[[Number of open incidents]] + [[Number of open problems]] + [[Number of open requests]]`

-   **Predicted Average Cost of Open Incidents**

    The result of the formula `[[Cost of Incidents Resolved / By week SUM +]]/[[Number of resolved incidents / By week SUM +]] * [[Number of open incidents]]`

-   **Predicted Average Cost of Open Requests**

    The result of the formula `[[Cost of Requests Completed / By week SUM +]]/[[Number of requests completed / By week SUM +]] * [[Number of open requests]]`

-   **Workload backlog growth**

    The result of the formula `[[New workload]] - [[Closed workload]]`


The following indicators do not appear on the dashboard but are used in formulas:

-   **Cost of Incidents Resolved**

    The daily sum of the Value field of incident\_metric records where the Definition field value is Incident Resolution Fixed Cost.

-   **Cost of Requests Completed**

    The daily sum of the Value field of sc\_request\_metric records where the Definition field value is Request Resolution Fixed Cost .

-   **ITSM normalized satisfaction score**

    Sum of the normalized score of metric results for the Customer Satisfaction survey

-   **ITSM survey instances**

    Number of the survey instances of the Customer Satisfaction survey

-   **Number of active task sla**

    The count of active SLA tasks on task\_sla with a start time before today and a stop time after today.

-   **Number of breach task sla**

    The count of active SLA tasks on task\_sla with a breach time before today

-   **Number of incidents missed SLA**

    The number of records on the incident\_sla table created on or before today, not yet closed, and that have breached SLA

-   **Number of open incidents with problem**

    The count of open incidents with a Problem referenced in the Problem field.

-   **Number of Resolved Incidents with Breached SLAs**

    Number of Incident-type SLA tasks that are not cancelled, that were resolved today, and where Has Breached is true

-   **Summed age of open incidents**

    The sum of hours between the time an incident was opened and now

-   **Summed age of open problems**

    The sum of hours between the time a problem was opened and now

-   **Summed age of open requests**

    The sum of hours between the time a request was opened and now

-   **Summed duration of closed requests**

    The sum of hours between the time a request was opened and the time it was closed

-   **Summed duration of resolved incidents**

    The sum of hours between the time an incident was opened and the time it was resolved

-   **Summed reassignments of open and overdue incidents**

    The summed reassignment count of all open Incident SLAs


## Breakdowns

-   Age \(Request, Incident, Problem, and Change\)
-   Assignment Group
-   Category \(Incident, Change\)
-   Contact Type \(Incident, Request\)
-   Location
-   Priority \(Request, Incident, Problem, and Change\)
-   Risk \(Change\)
-   SLA
-   SLA Definition
-   State \(Change, Request, Problem\)

**Parent Topic:**[Legacy: Performance Analytics ITSM Dashboards](itsm-dashboards-content-pack.md)

## Define fixed costs for IT Manager dashboard

Define generic industry-based fixed costs to analyze impact by channel using the IT Manager dashboard in ITSM Performance Analytics Solutions.

### Before you begin

Role required: admin

### About this task

Use the fixed cost model to analyze the cost for incidents and requests across channels \(email, phone, self-service, walk-up, virtual agent\) for cost management. For example, view current costs per channel and verify whether costs are reduced over time after implementing a solution.

Cost definitions are stored in the Fixed Cost Definitions \[fixed\_cost\_definitions\] table.

![ITManagerFixedCosts](../../../product/it-service-management/image/it-manager-fixed-costs.png "IT Manager Fixed Costs")

<table id="table_ohy_dcg_sfb"><thead><tr><th>

Area

</th><th>

KPI

</th></tr></thead><tbody><tr><td>

Volume

</td><td>

Total number of incidents

 Total number of requests

</td></tr><tr><td>

FCR

</td><td>

Number of incidents resolved on first assignment

 Number of requests resolved on first assignment

</td></tr><tr><td>

MTTR

</td><td>

Average time to resolve an incident

 Average time to resolve a request

</td></tr><tr><td>

SLA

</td><td>

% of incidents that breached SLAs

 % of requests that breached SLAs

</td></tr><tr><td>

CSAT

</td><td>

Average customer satisfaction score

</td></tr><tr><td>

Cost

</td><td>

Average cost to resolve an incident

 Average cost to resolve a service request

</td></tr></tbody>
</table>Breakdown:

-   Assignment group
-   Agent
-   Skill

### Procedure

1.  Navigate to **All** &gt; **Fixed Costs** &gt; **Define Fixed Cost** \(see table for field descriptions\).

<table id="table_bdl_14j_4fb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short Description

</td><td>

Description of the cost.

</td></tr><tr><td>

Table

</td><td>

Table that contains the field for the fixed cost condition.

</td></tr><tr><td>

Filter

</td><td>

Condition for the fixed cost definition, if applicable.

</td></tr><tr><td>

Cost Value

</td><td>

Currency type and fixed cost value.

</td></tr><tr><td>

Category

</td><td>

Category of the fixed cost.-   Total Fully Loaded Cost
-   Per Hour Cost


</td></tr><tr><td>

Source of the Cost

</td><td>

Source of the fixed cost.-   HDI
-   ServiceNow
-   Manual


</td></tr><tr><td>

Active

</td><td>

Check box to activate the fixed cost definition. Clear the check box to disable.

</td></tr></tbody>
</table>
### Cost per Network Incident

|Field|Value|
|-----|-----|
|Short Description|Incident in Network Category|
|Table|Incident \[incident\]|
|Filter|Category is Network|
|Cost Value|$15.56|
|Category|Total Fully Loaded Cost|
|Source of the Cost|HDI|
|Active|Selected|

