---
title: Optimizing technician schedules in response to urgent events
description: Resolve urgent scheduling changes quickly and efficiently by configuring prioritized event optimization, which responds immediately to critical events and targets only the specific technicians and tasks affected, without reoptimizing all tasks and qualifiers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/field-service-scheduling/triggering-optimization-on-task-or-agent-availability-change.html
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Intraday optimization, Schedule Optimization, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Optimizing technician schedules in response to urgent events

Resolve urgent scheduling changes quickly and efficiently by configuring prioritized event optimization, which responds immediately to critical events and targets only the specific technicians and tasks affected, without reoptimizing all tasks and qualifiers.

## About intraday optimization for prioritized events

Prioritized event optimization enables same-day, event-driven schedule adjustments that run shortly after a prioritized event occurs. This mode targets a specific group of Field Service technicians and tasks without adjusting the entire qualifier.

The buffer window property determines how many minutes the system waits to collect additional priority events before running optimization. For example, with a one-minute buffer, the system waits one minute after detecting a priority event to capture any other events before starting optimization.

## Technician selection

The optimization engine considers technicians directly affected by events, such as those running late or early. The system also considers technicians already assigned to affected tasks. Unlike default intraday optimization, the engine ignores overlapping territories and only includes territories directly impacted by the events.

**Note:** Task filters configured in the scheduling attribute configuration don’t apply to prioritized intraday optimization.

## Task Selection

When only task-related events occur without technician events, the engine includes only existing task assignees. If no assignees exist, no technicians are considered.

Prioritized event optimization focuses on territories directly impacted by the events and doesn't include overlapping territories.

To set up intraday optimization for prioritized events, see [Configure optimization for prioritized events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/configure-immediate-optimization.md).

## Optimization with matching rules

You can apply matching rules to prioritized event optimization for improved control over job assignments. Matching rules are only available when [Territory-Based Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/territory-based-optimization.md) is enabled. [Territory-Based Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/territory-based-optimization.md) can't be used with optimization configurations that use assignment groups.

Matching rules identify a subset of relevant tasks and technicians to optimize based on criteria such as search radius, required skills, and time thresholds. When matching rules are configured, they determine which tasks and technicians are directly impacted by a prioritized event, including pending dispatch tasks with SLA breaches or tasks that have a window end within the next four hours. For example, when a technician calls in sick, matching rules identify all technicians with similar skills as directly impacted, enabling the optimization engine to reassign that technician's tasks efficiently. When a prioritized event occurs and creates a task event, the system generates a prioritized job and applies the configured matching rules to filter assignment options before making recommendations.

You can configure the maximum search radius and distance unit at the qualifier level to control the scope of optimization for each territory.

If you installed the Field Service Management Demo Data plugin, two example matching rules are available: Filter technicians for prioritized events and Filter tasks for prioritized events. These rules include criteria for affected technicians and affected tasks. You can use these example rules or create your own.

For more information about matching rules, see [Set up prioritized intraday optimization with matching rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/set-up-prioritized-intraday-optimization-with-matching-rules.md).

**Note:** If you have custom event types and flows for intraday optimization, migrate them to the Intraday Event Type table. Update your flows to populate the event type field with table references instead of drop-down values.

**Related topics**  


[Schedule Optimization properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/schedule-optimization-properties.md)

