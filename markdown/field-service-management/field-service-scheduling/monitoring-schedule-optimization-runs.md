---
title: Monitoring Schedule Optimization runs
description: Monitor Schedule Optimization runs to verify your configuration is working correctly and understand assignment decisions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/field-service-scheduling/monitoring-schedule-optimization-runs.html
release: brazil
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Scheduling and dispatching, Use, Field Service Management]
---

# Monitoring Schedule Optimization runs

Monitor Schedule Optimization runs to verify your configuration is working correctly and understand assignment decisions.

Schedule Optimization includes:

-   [Batch optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-scheduling/schedule-optimization-engine.md)
-   [Intraday optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-scheduling/optimize-your-schedules-intraday.md)
-   [Prioritized event optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-scheduling/triggering-optimization-on-task-or-agent-availability-change.md)
-   [On-demand optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-scheduling/optimize-agent-schedules-on-demand-in-dispatcher-workspace.md)
-   [Run summaries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-scheduling/viewing-task-assignments-from-so-runs.md)

Schedule Optimization evaluates available tasks and technicians to produce optimized schedules. Each optimization run applies configured policies that define optimization objectives, constraints, and the scope of assignment groups or territories included in the run.

After Schedule Optimization runs, you can review the results to understand how tasks were processed and assigned. Monitoring optimization activity helps you verify that configurations are working as intended, confirm assignment outcomes, and identify scheduling or configuration issues.

Schedule Optimization provides detailed run summaries for every optimization run. Run summaries show the tasks, technicians, and shifts that were evaluated during optimization, and which resources or shifts were dropped. Each summary includes which tasks were assigned, which resources or shifts were excluded, and any validation or exception messages generated during the run. This information helps you understand optimization decisions and troubleshoot unexpected results.

Use the Run Summary module to:

-   Track all optimization activity in a central location
-   Monitor the status and progress of optimization runs
-   Review detailed results showing task assignments and technician decisions
-   Understand why assignments were or were not made
-   Troubleshoot configuration issues and scheduling problems
-   Verify that policy objectives and constraints are working as intended

