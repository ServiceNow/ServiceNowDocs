---
title: Matching rules for prioritized intraday optimization
description: Understand how matching rules identify and filter tasks and technicians affected by prioritized events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/field-service-scheduling/matching-rules-for-prioritized-intraday-optimization.html
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2026-09-02"
reading_time_minutes: 3
breadcrumb: [Optimization for prioritized events, Intraday optimization, Schedule Optimization, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Matching rules for prioritized intraday optimization

Understand how matching rules identify and filter tasks and technicians affected by prioritized events.

You can apply matching rules to prioritized event optimization for improved control over job assignments. Matching rules are only available when [Territory-Based Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/territory-based-optimization.md) is enabled. [Territory-Based Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/territory-based-optimization.md) can't be used with optimization configurations that use assignment groups.

## How matching rules work

Matching rules identify a subset of relevant tasks and technicians to optimize based on criteria such as search radius, required skills, and time thresholds. When matching rules are configured, they determine which tasks and technicians are directly impacted by a prioritized event. This includes pending dispatch tasks with SLA breaches or tasks that have a window end within the next four hours. For example, when a technician calls in sick, matching rules identify all technicians with similar skills as directly impacted. The optimization engine reassigns that technician's tasks efficiently. When a prioritized event occurs and creates a task event, the system generates a prioritized job. The configured matching rules are applied to filter assignment options before making recommendations.

## Matching dimensions

Matching rules work by combining one or more matching dimensions. Matching dimensions are the individual criteria or filters that determine which tasks and technicians are directly impacted by a prioritized event.

The following matching dimensions are available:

-   Affected technician\(s\): Identifies technicians directly affected by the prioritized event.
-   Affected task\(s\): Identifies tasks directly affected by the prioritized event.
-   Retrieve technician\(s\) based on skills: Identifies technicians whose skills match those required by affected tasks.
-   Retrieve task\(s\) based on skills: Identifies tasks whose required skills match the skills of affected technicians.
-   Retrieve technician\(s\) within radius: Identifies technicians located within a defined search radius of the prioritized event.
-   Retrieve task\(s\) within radius: Identifies tasks located within a defined search radius of the prioritized event.

Within a single matching rule, matching dimensions are combined using AND logic. AND logic means all criteria must match for a task or technician to be included. When you configure multiple matching rules in a single optimization configuration, the results are combined using OR logic. OR logic means matching any rule qualifies a task or technician for optimization.

## Overlapping territories

When optimizing with overlapping territories, Schedule Optimization considers qualifiers from overlapping territories within the configured search radius to expand the pool of available technicians and tasks. You can configure the maximum search radius and distance unit at the qualifier level to control the scope of optimization for each territory.

## Demo data and custom rules

If you installed the Field Service Management Demo Data plugin, two example matching rules are available: Filter technicians for prioritized events and Filter tasks for prioritized events. These rules include criteria for affected technicians and affected tasks. You can use these example rules or create your own.

## Configuration overview

-   To enable matching rules for your intraday configuration, see [Set up prioritized intraday optimization with matching rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/set-up-prioritized-intraday-optimization-with-matching-rules.md).
-   To create your own matching rule, see [Create matching rules for intraday events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/create-matching-rules-for-intraday-events.md).

**Related topics**  


[Configuring Schedule Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/schedule-optimization-engine.md)

[Optimizing technician schedules at set intervals throughout the day](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/optimize-your-schedules-intraday.md)

[Optimizing technician schedules in response to urgent events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/triggering-optimization-on-task-or-agent-availability-change.md)

