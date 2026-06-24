---
title: Run optimization for your groups or territories from Dispatcher Workspace
description: Reassign tasks and maximize productivity by running Schedule Optimization on demand when scheduling conditions change.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/field-service-management/optimize-agent-schedules-on-demand-in-dispatcher-workspace.html
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Working in Dispatcher Workspace, Scheduling and dispatching work order tasks to agents, Using Field Service Management, Field Service Management]
---

# Run optimization for your groups or territories from Dispatcher Workspace

Reassign tasks and maximize productivity by running Schedule Optimization on demand when scheduling conditions change.

## Before you begin

-   Schedule Optimization must be activated. For more information, see [Activate Schedule Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/field-service-management/field-service-scheduling/schedule-optimization-engine-plugin.md).
-   Intraday optimization must be configured. For more information, see [Configure intraday optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/field-service-management/field-service-scheduling/configure-intraday-optimization.md).

Role required: schedule\_optimization\_user

## About this task

Schedule Optimization can be configured to run the optimization engine in batches overnight or at selected intervals throughout the day in response to canceled tasks and other triggers. This procedure describes how dispatchers can run optimization on demand from Dispatcher Workspace.

For more information on running the optimization engine automatically, see [Configuring Schedule Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/field-service-management/field-service-scheduling/schedule-optimization-engine.md).

Schedule Optimization considers the agent's start and end locations from the **Agent Schedule Attribute Plans** table for the given day if the Territory Planning plugin is activated. For more information, see [Activate Field Service Territory Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/field-service-management/workforce-optimization-for-field-service/Activate-fsm-territory-planning.md).

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching****&gt;Dispatcher Workspace**.

2.  Select **Dispatcher workspace** in the left navigation.

3.  Select **Optimization summary** in the contextual side panel.

4.  Select the pencil icon to edit the policy you want to use to run optimization.

5.  Select **Run optimization**.

6.  Select **Pause scheduled runs** to schedule tasks manually.

    **Note:** Schedule Optimization data does not auto refresh. Enable auto refresh in the settings.


