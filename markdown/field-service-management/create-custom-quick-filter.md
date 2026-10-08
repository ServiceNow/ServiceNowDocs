---
title: Create a custom quick task filter
description: Add a custom filter criterion to the quick task and calendar filters.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/field-service-management/create-custom-quick-filter.html
release: australia
topic_type: task
last_updated: "2026-08-26"
reading_time_minutes: 1
keywords: [quick task filter, extension point]
breadcrumb: [Dispatcher Workspace, CSM/FSM Configurable Workspace, Configure, Field Service Management]
---

# Create a custom quick task filter

Add a custom filter criterion to the quick task and calendar filters.

## Before you begin

Role required: admin. You must be a professional developer to implement this extension point.

## Procedure

1.  Navigate to the **All** menu, type `sys_extension_point.list`, and press Enter.

2.  Open the `DispatcherWorkspaceQuickFilterExtensionPoint` record.

3.  Select the **Create Implementation** related link.

    A new script include generates with the required method stubs for this extension point.

4.  In the generated script include, define the methods.

    For example:

    -   `getDisplayName` — the name shown for this filter in the quick filter modal.
    -   `getFilterType` — the value type this filter evaluates.
    -   `getFilterOptions` — the values available for this filter.
    -   `getOperatorGroups` — the operators available for this filter.
    -   `getFilterId` — a unique identifier for this filter implementation.
    -   `getFilterData` — the query logic that returns matching tasks.
    -   `processFilterRule` — how a selected value is applied to the filter.
5.  Save the script include.

6.  In the extension point record, verify the new implementation appears in the **Implementations** related list.


## Result

The new criterion is available to select in the quick task filter and quick calendar filter modals.

**Related topics**  


[Quick task and calendar filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/field-service-management/field-service-scheduling/quick-filters-dw.md)

[Apply a quick task filter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/field-service-management/field-service-scheduling/apply-quick-task-filter.md)

[Apply a quick calendar filter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/field-service-management/field-service-scheduling/apply-quick-cal-filter.md)

