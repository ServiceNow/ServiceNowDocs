---
title: Quick task and calendar filters
description: Quick task filters narrow the tasks in the task panel and the calendar in Dispatcher Workspace using criteria such as skill, parts, and SLA breach.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/field-service-scheduling/quick-filters-dw.html
release: brazil
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2026-09-22"
reading_time_minutes: 2
keywords: [quick task filter, task panel, calendar filter]
breadcrumb: [Using Dispatcher Workspace, Assigning tasks from Dispatcher Workspace, Scheduling and dispatching, Use, Field Service Management]
---

# Quick task and calendar filters

Quick task filters narrow the tasks in the task panel and the calendar in Dispatcher Workspace using criteria such as skill, parts, and SLA breach.

A quick task filter is a set of one or more conditions that determines which work order tasks are relevant to a dispatcher. Quick task filters apply to the task panel and the calendar. Both can use the same criteria and operators, or different ones. Each can be saved as a default independently, or scoped to apply to both at once.

The task panel and the calendar respond differently. A quick task filter removes non-matching tasks from the task panel list. A quick calendar filter never removes anything, it dims out the tasks and events that don't match the criteria.

Five criteria are available: State, Window End, Skill, Parts, and SLA Breach. Each supports its own subset of operators, depending on the type of value it matches. Window End is a date and time field, so it uses Before, After, and Between. The remaining criteria use operators such as Include Any, Include All, Exclude All, Contains, and Starts With. The Skill criterion evaluates only whether a skill is present on the task. It doesn't consider whether that skill is mandatory, what skill level it requires, or its expiration status.

## Filter logic

The selected logic operator \(AND or OR\) applies only to the filter criteria you select. All selected criteria use the same operator — mixed logic isn't supported.

Task-based filters \(Pending Dispatch, All Active Tasks, and similar base filters\) are evaluated using AND logic against the selected filter criteria. This holds regardless of which operator you pick for your own selections.

If you select AND:

```
Task Base Filter
                AND
                (Skill Filter AND Window End Filter AND SLA Filter ...)
```

If you select OR:

```
Task Base Filter
                AND
                (Skill Filter OR Window End Filter OR SLA Filter ...)
```

## Building efficient filters

When using the Skill or Parts filters with the Contains or Starts With operators, enter complete words whenever possible. Avoid using only a few characters, as this can return a broader set of results and may impact performance.

Adding more filter criteria increases the time it takes to return results, especially when combining several criteria that search across related records, such as Skill or Parts. Using AND performs better than OR. For the best performance, apply AND logic when it meets your needs and avoid combining too many of these related-record criteria at once.

OR across multiple filters is supported, but it can slow down results, especially with a base filter that returns many tasks, such as All Active Tasks.

**Related topics**  


[Apply a quick task filter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-scheduling/apply-quick-task-filter.md)

[Apply a quick calendar filter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-scheduling/apply-quick-cal-filter.md)

[Create a custom quick task filter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/create-custom-quick-filter.md)

