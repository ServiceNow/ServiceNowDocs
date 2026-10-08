---
title: Extend or reduce duration of an assignment
description: Extend or reduce the duration of an assignment from the grid view in Resources when the work duration shifts. When you extend or reduce the assignment duration, the assignment dates update and the allocated effort recalculates across the new date range based on the effort redistribution property.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/strategic-planning/extend-reduce-dates-for-assignment-dw.html
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2026-09-30"
reading_time_minutes: 1
keywords: [resource management, assignment duration, extend assignment, reduce assignment]
breadcrumb: [Manage resources for demands, Use, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Extend or reduce duration of an assignment

Extend or reduce the duration of an assignment from the grid view in Resources when the work duration shifts. When you extend or reduce the assignment duration, the assignment dates update and the allocated effort recalculates across the new date range based on the effort redistribution property.

## Before you begin

Role required: it\_demand\_manager

The com.snc.resource\_management.redistribute\_effort\_on\_extend\_reduce property is enabled. For more information, see [Resource Management properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/resource-management/r_ResourceProperties.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace**.

2.  Select the Demands icon \[Omitted image "demands-icon.png"\].

3.  Open a demand from the **List** page.

4.  Select the **Resources** tab.

    The resource grid opens for the demand's timeline, grouped by **Primary Group**.

5.  Select the chevron icon \(\[Omitted image "rmw-chevron-image.png"\] Alt text: Chevron icon.\) to expand the resource view.

6.  Locate the row for the resource assignment you want to update.

7.  Update one or both of the following date fields to extend or reduce the assignment:

    -   Start date: Move earlier to extend the assignment or later to reduce it.
    -   End date: Move later to extend the assignment or earlier to reduce it.

## Result

After the dates are updated, the initial effort is recalculated for the entire assignment duration including the new date range.

