---
title: Dynamic operators
description: The dynamic operator, is \(dynamic\), lists predefined dynamic filter options where the condition value is computed from a value in a reference field.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Filters, Filters and breadcrumbs, Lists in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Dynamic operators

The dynamic operator, **is \(dynamic\)**, lists predefined dynamic filter options where the condition value is computed from a value in a reference field.

The following dynamic filter options are available by default.

**Note:** Administrators can [create new dynamic filter options](../task/t_DynamicFilterOptions.md).

|Target table of reference field|Option label|Description|
|-------------------------------|------------|-----------|
|User \[sys\_user\]|Me|The reference field contains the current user.|
|One of My Assignments|The reference field contains the current user or someone for whom the current user is a delegate for assignments.|
|One of My Approvals|The reference field contains the current user or someone for whom the current user is a delegate for approvals.|
|Users With Roles|The reference field contains users that have any role.|
|Group \[sys\_user\_group\]|One of My Groups|The reference field contains a group to which the current user belongs.|

The following table contains examples and descriptions of dynamic filter conditions.

|Field|Operator|Dynamic filter option|Description|
|-----|--------|---------------------|-----------|
|Caller|is \(dynamic\)|Me|Computes the value of Caller based on the current user viewing the list.|
|Assignment group|is \(dynamic\)|One of My Groups|Computes the value of Assignment group based on the current user viewing the list.|

**Parent Topic:**[Filters](../concept/c_Filters.md)

**Related topics**  


[Create a filter in List](../task/t_CreatingFilters.md)

[Add related list conditions](../../using-lists-v3/task/create-related-list-query.md)

[OR conditions](../concept/c_UsingORConditions.md)

[Filter on multiple string values](../task/t_FilteringOnMultipleStringValues.md)

