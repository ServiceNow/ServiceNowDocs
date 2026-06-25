---
title: View Schedule Optimization run summaries
description: View run summaries to monitor the status and results of Schedule Optimization runs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/field-service-scheduling/view-optimization-run-summaries.html
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [View Schedule Optimization task assignments, Scheduling and dispatching, Use, Field Service Management]
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
4.  Select the **Run ID** to view detailed information about the optimization run.

    The record displays:

    -   Optimization objectives and constraints applied
    -   Run status and sub-states such as awaiting details, generating details, or details generated
    -   Task states: Optimized, assigned, unassigned, unchanged, or error
    -   Assignment group or territory states: Optimized or error
    -   Technician errors: Technicians not sent for optimization due to errors
    -   Start and end times
    -   Travel estimate configuration data used for the optimization run
    -   Qualifiers considered for the run and qualifiers dropped from the run
    -   Tasks considered for the run
    -   Assigned and unassigned tasks with the reason they were not assigned
5.  Select the **Technicians** tab to view technicians that were dropped from the optimization run.

    Dropped technicians are technicians that the system excluded before sending data to the optimization engine because they don't have valid work schedules. Each dropped technician appears with an **Error** status and the reason for exclusion in the **Resource Notes** field.

6.  Select the **Work Order Tasks** tab to view tasks from the optimization run, including tasks that were assigned, unchanged, considered but not optimized, and dropped due to invalid data.

    Tasks with an **Unchanged** status are conflict tasks that the optimization engine couldn't assign because the suggested assignment overlapped with an existing assignment for the same technician. The reason appears in the **Resource Notes** field.


## Result

The run summary details help you identify successful runs and address any issues that need attention.

**Related topics**  


[Configuring Schedule Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/schedule-optimization-engine.md)

[Optimizing technician schedules at set intervals throughout the day](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/optimize-your-schedules-intraday.md)

