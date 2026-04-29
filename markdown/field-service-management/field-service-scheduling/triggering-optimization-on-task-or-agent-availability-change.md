---
title: Optimizing technician schedules in response to urgent events
description: Prioritized event optimization is a mode of intraday optimization that aims to run a faster, more focused intraday process. This mode specifically targets the most critical events.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Intraday optimization, Schedule Optimization, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Optimizing technician schedules in response to urgent events

Prioritized event optimization is a mode of intraday optimization that aims to run a faster, more focused intraday process. This mode specifically targets the most critical events.

## About intraday optimization for prioritized events

Prioritized event optimization enables same-day, event-driven schedule adjustments that run shortly after a prioritized event occurs. This mode targets a specific group of Field Service technicians and tasks without adjusting the entire qualifier.

The buffer window property determines how many minutes the system waits to collect additional priority events before running optimization. For example, with a one-minute buffer, the system waits one minute after detecting a priority event to capture any other events before starting optimization.

## Technician selection

The optimization engine considers technicians directly affected by events, such as those running late or early. The system also considers technicians already assigned to affected tasks. Unlike default intraday optimization, the engine ignores overlapping territories and only includes territories directly impacted by the events.

**Note:** Task filters configured in the scheduling attribute configuration don’t apply to prioritized intraday optimization.

## Task Selection

The optimization engine considers technicians directly affected by events, such as those running late or early. When a task-related event occurs, the system also considers technicians already assigned to affected tasks.

When only task-related events occur without technician events, the engine includes only existing task assignees. If no assignees exist, no technicians are considered.

Prioritized event optimization focuses on territories directly impacted by the events and doesn’t include overlapping territories.

To set up intraday optimization for prioritized events, see [Configure optimization for prioritized events](configure-immediate-optimization.md).

## Optimization with matching rules

You can apply matching rules to prioritized event optimization for improved control over job assignments. Matching rules are only available when [Territory-Based Optimization](territory-based-optimization.md) is enabled. [Territory-Based Optimization](territory-based-optimization.md) can’t be used with configurations that use assignment groups.

If you installed the Field Service Management Demo Data plugin, two example matching rules are available: Filter technicians for prioritized events and Filter tasks for prioritized events. These rules include criteria for affected technicians and affected tasks. You can use these example rules or create your own matching rules to identify subsets of tasks and technicians based on your defined criteria.

When matching rules are configured, they determine which tasks and technicians are directly impacted by a prioritized event. For example, when a technician calls in sick, matching rules identify all technicians with the same certifications as directly impacted, enabling the system to reassign that technician's tasks efficiently. Matching rules also limit optimization to tasks and technicians within a specific radius of a new high-priority task.

When a prioritized event occurs and creates a task event, the system generates a prioritized job. If matching rules are configured for intraday events, the optimization engine applies those rules to filter the assignment options before making recommendations.

To configure matching rules for intraday events, access the Intraday Event Type table from the Matching Rules table field. For more information about matching rules, see [Set up prioritized intraday optimization with matching rules](set-up-prioritized-intraday-optimization-with-matching-rules.md).

**Note:**

Note: If you have custom event types and flows for intraday optimization, migrate them to the Intraday Event Type table. Update your flows to populate the event type field with table references instead of drop-down values.

**Related topics**  


[Schedule Optimization properties](../reference/schedule-optimization-properties.md)

