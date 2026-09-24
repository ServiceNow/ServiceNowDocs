---
title: View Schedule Optimization run summaries
description: View run summaries to monitor the status and results of Schedule Optimization runs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/field-service-scheduling/view-optimization-run-summaries.html
release: brazil
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Run summaries overview, Monitoring Schedule Optimization assignments, Scheduling and dispatching, Use, Field Service Management]
---

# View Schedule Optimization run summaries

View run summaries to monitor the status and results of Schedule Optimization runs.

## Before you begin

Schedule Optimization must be configured and at least one optimization run must have been triggered.

Role required: wm\_admin

## Procedure

1.  Navigate to **All** &gt; **Schedule Optimization** &gt; **Run Summaries**.

2.  Review the list of optimization runs.

    Each row represents one optimization run.

3.  Select the Filter icon \(\[Omitted image "filter-right-side.png"\] Alt text: filter icon\) to filter or sort the list to find specific runs.

    -   Filter by run type \(batch or intraday\)
    -   Filter by status
    -   Sort by start or end time
4.  Select the **Run ID** to open the run summary record and review optimization details.

    The record displays: Optimization details

    -   Run type: Batch optimization, Intraday optimization
    -   Task state: assigned, dropped, unassigned, or unchanged
    -   Sub-state: such as awaiting details, generating details, or details generated
    -   Start time and end time of the optimization run
    -   Optimization horizon: start and end dates of the evaluated time period
    -   Travel estimate provider
    -   Objectives and constraints applied
5.  View the related list for more optimization details.

<table id="choicetable_cn3_5tb_3kc"><thead><tr><th align="left" id="d123297e164">

Tab

</th><th align="left" id="d123297e167">

Description

</th></tr></thead><tbody><tr><td id="d123297e173">

**Qualifiers**

</td><td>

The assignment groups or territories included in the optimization run.

</td></tr><tr><td id="d123297e182">

**Work Order Tasks**

</td><td>

The work order tasks evaluated and processed during the optimization run.

</td></tr><tr><td id="d123297e191">

**Dropped Technicians**

</td><td>

Technicians who were not considered for optimization.Select a technician to view the Run Detail record, which shows the optimization status and resource notes explaining why the technician was excluded from optimization.

</td></tr><tr><td id="d123297e202">

**Technician Schedules**

</td><td>

Schedules for technicians included in the optimization run.

</td></tr><tr><td id="d123297e212">

**Run Summary Shifts**

</td><td>

Shift plans and the tasks assigned to each plan.

</td></tr><tr><td id="d123297e221">

**Associated Batch Record**

</td><td>

The batch configuration associated with the optimization run.

</td></tr><tr><td id="d123297e230">

**Associated ML Solutions**

</td><td>

Machine learning solutions associated with this optimization run.

</td></tr></tbody>
</table>    Use run summaries to verify optimization results, investigate assignment decisions, and troubleshoot issues identified during optimization.


**Related topics**  


[Configuring Schedule Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-scheduling/schedule-optimization-engine.md)

[Optimizing technician schedules at set intervals throughout the day](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-scheduling/optimize-your-schedules-intraday.md)

