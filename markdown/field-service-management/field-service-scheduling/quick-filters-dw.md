---
title: Quick task and calendar filters
description: Quick filters narrow the tasks in the task panel and the calendar in Dispatcher Workspace using criteria such as skill, parts, and SLA breach.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/field-service-scheduling/quick-filters-dw.html
release: brazil
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [quick filter, task panel, calendar filter]
breadcrumb: [Using Dispatcher Workspace, Assigning tasks from Dispatcher Workspace, Scheduling and dispatching, Use, Field Service Management]
---

# Quick task and calendar filters

Quick filters narrow the tasks in the task panel and the calendar in Dispatcher Workspace using criteria such as skill, parts, and SLA breach.

A quick filter is a set of one or more conditions that determines which work order tasks are relevant to a dispatcher. Quick filters apply to the task panel and the calendar. Both use the same criteria and operators, but each can be saved as a default independently, or scoped to apply to both at once.

The task panel and the calendar respond differently. A quick task filter removes non-matching tasks from the task panel list. A quick calendar filter never removes anything, it grays out the tasks that don't match the criteria.

Five criteria are available: State, Window End, Skill, Parts, and SLA Breach. Each supports its own subset of operators — Include Any, Include All, Exclude All, Contains, and Starts With — which determine how a value is matched. The Skill criterion evaluates only whether a skill is present on the task; it doesn't consider whether that skill is mandatory or what skill level it requires. Which table the Skill criterion reads from depends on the **com.snc.skills\_management.wm\_task\_migrate\_skills** system property:

-   When the property is set to true, the criterion evaluates the Task Skills \(**task\_m2m\_skill**\) table.
-   When the property is set to false, the criterion evaluates the skill field in the task table.

Each criterion is an implementation of a scripted extension point, including the five shipped by default. Implementation partners can extend the same point to add criteria based on other tables related to the work order task.

