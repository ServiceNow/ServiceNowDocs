---
title: View Schedule Optimization run summaries
description: View run summaries to monitor the status and results of Schedule Optimization runs.
locale: en-US
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

3.  Select the Filter icon \(![filter icon](../image/filter-right-side.png)\) to filter or sort the list to find specific runs.

    -   Filter by run type \(batch or intraday\)
    -   Filter by status
    -   Sort by start or end time
4.  Select the **Run ID** to view detailed information about the optimization run.

    The record displays:

    -   Optimization objectives and constraints applied
    -   Run status and sub-states such as awaiting details, generating details, or details generated
    -   Task states: Optimized, assigned, unassigned, unchanged, or error
    -   Assignment group or territory states: Optimized or error
    -   Technician errors-technicians not sent for optimization due to errors
    -   Start and end times
    You can monitor optimization runs and review their results. The run summary details help you verify successful runs and address any issues that need attention.


**Related topics**  


[Configuring Schedule Optimization](../concept/schedule-optimization-engine.md)

[Optimizing technician schedules at set intervals throughout the day](optimize-your-schedules-intraday.md)

