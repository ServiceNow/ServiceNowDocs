---
title: Viewing task assignments from Schedule Optimization runs
description: View the results of Schedule Optimization runs to understand how tasks were processed and assigned.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Scheduling and dispatching, Use, Field Service Management]
---

# Viewing task assignments from Schedule Optimization runs

View the results of Schedule Optimization runs to understand how tasks were processed and assigned.

## How Schedule Optimization runs

Schedule Optimization can run in three different modes depending on your scheduling needs and when optimization occurs. The modes are batch optimization, intraday optimization, and on-demand.

-   **Batch optimization**

    Batch optimization runs on a scheduled basis to create optimized schedules for upcoming work. This mode evaluates all available tasks and technicians within a specified time window and produces a complete schedule based on your configured objectives and constraints.

-   **Intraday optimization**

    Intraday optimization is an event-based mode of Schedule Optimization. It runs throughout the day in response to schedule disruptions such as technicians calling in sick, canceled tasks, new high-priority tasks, or technicians running late.

    By default, intraday optimization runs every 60 minutes and can be configured to run as frequently as every 15 minutes. When a trigger condition is met, the system creates an intraday event. During the next scheduled run, Schedule Optimization creates an optimization job for each affected assignment group or territory and reoptimizes the tasks. Schedule-locked tasks aren’t considered for reoptimization.

    Prioritized event optimization is a focused mode of intraday optimization that responds quickly to critical events. Instead of waiting for the next scheduled intraday run, this mode triggers optimization shortly after a high-priority event occurs and targets only the specific technicians and tasks affected by the event.

    For prioritized events, considers:

    -   Technicians with the qualifier role in directly impacted territories
    -   Active tasks that aren't schedule-locked
    -   Pending dispatch tasks with SLA breaches or due to end within the next hour
    -   Scheduled or assigned tasks for affected technicians
    You can apply matching rules to prioritized event optimization to control which tasks and technicians are included in optimization runs.

-   **On-demand intraday optimization**

    Schedule Optimization can be configured to run the optimization engine in batches overnight or at selected intervals throughout the day. Dispatchers can also [trigger optimization from Dispatcher Workspace](optimize-agent-schedules-on-demand-in-dispatcher-workspace.md) when on-demand optimization is configured, allowing them to run the optimization engine at any time.


Regardless of which mode runs, Schedule Optimization applies the configured policies. A policy is a grouping of objectives and constraints that defines the rules for optimization. Policy objectives prioritize how tasks are assigned to technicians. Policy constraints determine the criteria that must be met before a task can be assigned to a technician in an assignment group or territory.

## What happens during an optimization run

During a run, Schedule Optimization processes task and resource data and attempts to assign as many tasks as possible. Runs can produce complete assignments, partial results, or errors when tasks can’t be scheduled. Schedule Optimization records the run type, applied objectives and constraints, and any warnings or issues it encounters. This information helps you understand why tasks were scheduled in the way they were or why they weren’t scheduled at all.

## Viewing optimization run summaries

The Run Summary module provides a central location to track all optimization activity. Each time Schedule Optimization runs, whether batch or intraday optimization, the system creates a run summary record that captures the details of that run.

Run Summary records are created each time an optimization run is triggered. A single run summary may group multiple machine learning solutions under one record for easier tracking. As the optimization process progresses, the run summary updates to reflect the current state, including substates such as awaiting details, generating details, or details generated.

You can view detailed run summaries to see how Schedule Optimization evaluated tasks and technicians. These summaries show the objectives and constraints used during the run, the run status, and any validation or exception messages. The task-level results show how each task was handled, including assigned tasks, unassigned tasks, unchanged tasks, and tasks that produced errors. This visibility helps you confirm expected behavior, identify configuration issues, and troubleshoot unexpected scheduling results.

Viewing run summaries gives schedulers a clear picture of how each optimization run performed. You can verify that changes to configuration are working, confirm that technicians received the expected assignments, and quickly identify issues such as missing skills or invalid travel rules. The combination of run details and task outcomes helps you adjust your setup and resolve problems before they impact the schedule.

Each run summary provides:

-   Run type: Batch or intraday optimization.
-   Applied objectives and constraints.
-   Run status and timing.
-   Task states showing how each task was processed:
    -   Optimized: The task was sent to the optimization engine for processing.
    -   Assigned: The task was assigned to a technician.
    -   Unassigned: The task wasn’t assigned to a technician.
    -   Unchanged: The task wasn’t modified during the optimization run.
    -   Error: The task encountered an error during optimization.
-   Assignment group or territory states:
    -   Optimized: Assignment group or territory was sent to the optimization engine for processing.
    -   Error: Assignment group or territory encountered an error during optimization.
-   Technician errors identifying technicians that weren’t sent for optimization due to errors.
-   Validation and exception messages.

**Related topics**  


[Configuring Schedule Optimization](schedule-optimization-engine.md)

[Optimizing technician schedules at set intervals throughout the day](../task/optimize-your-schedules-intraday.md)

[Run optimization for your groups or territories from Dispatcher Workspace](optimize-agent-schedules-on-demand-in-dispatcher-workspace.md)

