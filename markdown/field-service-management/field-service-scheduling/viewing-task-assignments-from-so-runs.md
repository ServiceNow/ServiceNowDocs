---
title: Reviewing Schedule Optimization results
description: View the results of Schedule Optimization runs to understand how tasks were processed and assigned.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/field-service-scheduling/viewing-task-assignments-from-so-runs.html
release: brazil
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Monitoring Schedule Optimization assignments, Scheduling and dispatching, Use, Field Service Management]
---

# Reviewing Schedule Optimization results

View the results of Schedule Optimization runs to understand how tasks were processed and assigned.

## What happens during an optimization run

During a run, Schedule Optimization processes task and resource data and attempts to assign as many tasks as possible. The system monitors which shifts and technicians were evaluated, and records why certain assignments were or weren't made. Runs can produce complete assignments, partial results, or errors when tasks can't be scheduled. This detailed tracking helps you understand the optimization decisions and identify configuration adjustments needed.

## Viewing optimization run summaries

The Run Summary module provides a central location to track all optimization activity. Each optimization run is captured in a run summary record that updates as the process progresses through substates such as awaiting details, generating details, or details generated. Each run summary includes:

-   Run type: Batch or intraday optimization.
-   Applied objectives and constraints.
-   Optimization horizon: Start and end dates of the optimization time window.
-   Run status and timing.
-   Task states showing how each task was processed:
    -   Assigned: The task was assigned to a technician.
    -   Dropped: The task wasn't considered for optimization
    -   Unassigned: The task wasn't assigned to a technician.
    -   Unchanged: The task wasn't modified during the optimization run.
-   Assignment group or territory states:
    -   Optimized: Assignment group or territory was sent to the optimization engine for processing.
    -   Error: Assignment group or territory encountered an error during optimization.
-   Dropped Technicians: Technicians who were not considered for optimization. View individual Run Detail records to see optimization status and resource notes explaining why they were excluded.
-   Shifts Considered: All shifts evaluated during the optimization, showing which were optimized or dropped and why.
-   Run Summary Shifts: Shift plans and the tasks assigned to them.
-   Validation and exception messages.

**Related topics**  


[Configuring Schedule Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-scheduling/schedule-optimization-engine.md)

[Optimizing technician schedules at set intervals throughout the day](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-scheduling/optimize-your-schedules-intraday.md)

[Run optimization for your groups or territories from Dispatcher Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-scheduling/optimize-agent-schedules-on-demand-in-dispatcher-workspace.md)

