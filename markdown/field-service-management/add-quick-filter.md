---
title: Configure quick filters using an extension point
description: Use script includes to add quick filters to Dispatcher Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/field-service-management/add-quick-filter.html
release: australia
topic_type: task
last_updated: "2026-09-22"
reading_time_minutes: 1
keywords: [quick filter, extension point, script include]
breadcrumb: [Dispatcher Workspace, CSM/FSM Configurable Workspace, Configure, Field Service Management]
---

# Configure quick filters using an extension point

Use script includes to add quick filters to Dispatcher Workspace.

## Before you begin

Role required: admin.

**Warning:** You must understand JSON code to perform this procedure.

## About this task

Dispatcher Workspace provides five quick filter criteria. To filter on a field that isn't included by default, create a script include, then add it as a new implementation so it appears as a selectable filter.

Which table the Skill criterion reads from depends on the **com.snc.skills\_management.wm\_task\_migrate\_skills** system property:

-   When the property is set to true, the criterion evaluates the Task Skills \(**task\_m2m\_skill**\) table.
-   When the property is set to false, the criterion evaluates the skill field in the task table.

Each criterion is an implementation of a scripted extension point, including the five shipped by default. Implementation partners can extend the same point to add criteria based on other tables related to the work order task.

## Procedure

1.  Create a new script include.

2.  Make additions or update the script include:

    -   Object.extendsObject\(DispatcherWorkspaceQuickFilterExtensionPoint, \{ ... \}\)
    -   Scope: sn\_fsm\_disp\_wrkspc
    -   Implement all required methods: isActive, getFilterType, getFilterId, getDisplayName, getFilterOptions, getOperators, getOperatorGroups, getFilterData, applyQueryCondition, matchesBatch, getOperatorExecutionModes, buildCondition
    -   getFilterType\(\) returns "task"
    -   getFilterId\(\) returns a stable unique string key
    -   getOperatorGroups\(\) uses groupId: 'positive' / groupId: 'negative'
    -   Use GlideRecordSecure \(not GlideRecord\)
    -   Guard empty searchString, empty selectedValues, empty taskSysIds
3.  Add the script include as a new implementation of the extension point:

    -   point: sn\_fsm\_disp\_wrkspc.DispatcherWorkspaceQuickFilterExtensionPoint
    -   script\_include: sys\_id of the Script Include above
    -   active: true
    -   sys\_scope: sn\_fsm\_disp\_wrkspc
    -   order: unique value \(existing ones use 100, 300 — pick next\)

