---
title: Optimizing technician schedules in response to urgent events
description: Resolve urgent scheduling changes quickly and efficiently by configuring prioritized event optimization. Prioritized event optimization responds immediately to critical events and targets only the specific technicians and tasks affected, without reoptimizing all tasks and qualifiers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/field-service-scheduling/triggering-optimization-on-task-or-agent-availability-change.html
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Intraday optimization, Schedule Optimization, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Optimizing technician schedules in response to urgent events

Resolve urgent scheduling changes quickly and efficiently by configuring prioritized event optimization. Prioritized event optimization responds immediately to critical events and targets only the specific technicians and tasks affected, without reoptimizing all tasks and qualifiers.

## About intraday optimization for prioritized events

Prioritized event optimization enables same-day, event-driven schedule adjustments that run shortly after a prioritized event occurs. This mode targets a specific group of Field Service technicians and tasks without adjusting the entire qualifier.

The buffer window property determines how many minutes the system waits to collect additional priority events before running optimization. For example, with a one-minute buffer, the system waits one minute after detecting a priority event to capture any other events before starting optimization.

## Technician selection

The optimization engine considers technicians directly affected by events, such as those running late or early. The system also considers technicians already assigned to affected tasks.

**Note:** Task filters configured in the scheduling attribute configuration don’t apply to prioritized intraday optimization.

## Task Selection

When only task-related events occur without technician events, the engine includes only existing task assignees. If no assignees exist, no technicians are considered.

To set up intraday optimization for prioritized events, see [Configure optimization for prioritized events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/configure-immediate-optimization.md).

## Optimization with matching rules

You can apply matching rules to prioritized event optimization for improved control over job assignments. Matching rules are available only when Territory-Based Optimization is enabled and can't be used with optimization configurations that use assignment groups.

Matching rules identify a subset of relevant tasks and technicians to optimize based on criteria such as skills, search radius, and time thresholds. For detailed information about how matching rules work and the available matching dimensions, see [Matching rules for prioritized intraday optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/matching-rules-for-prioritized-intraday-optimization.md).

**Related topics**  


[Schedule Optimization properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/schedule-optimization-properties.md)

