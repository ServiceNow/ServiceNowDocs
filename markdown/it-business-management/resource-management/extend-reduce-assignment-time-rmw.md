---
title: Extend or reduce duration of an assignment
description: Extend or reduce the duration of an assignment from the grid view in the Resource Management Workspace when the work duration shifts. The system updates the assignment dates and recalculates the allocated effort across the new date range based on the effort redistribution property.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/resource-management/extend-reduce-assignment-time-rmw.html
release: zurich
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2026-06-09"
reading_time_minutes: 1
keywords: [extend assignment, reduce assignment, resource assignment dates, resource management workspace]
breadcrumb: [Using Resource Management Workspace, Use, Resource Management Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Extend or reduce duration of an assignment

Extend or reduce the duration of an assignment from the grid view in the Resource Management Workspace when the work duration shifts. The system updates the assignment dates and recalculates the allocated effort across the new date range based on the effort redistribution property.

## Before you begin

-   Enable the com.snc.resource\_management.redistribute\_effort\_on\_extend\_reduce property from system properties. For more information, see [Resource Management properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/resource-management/r_ResourceProperties.md).
-   Captured actual efforts aren't affected.
-   Role required: it\_project\_manager or resource\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Resource Management Workspace**.

2.  Select the Resource cards icon \(\[Omitted image "rmw-resource-cards-L1-icon.png"\] Alt text: Resource cards icon.\) from the main menu and open a resource card.

3.  Select the chevron icon \(\[Omitted image "rmw-chevron-image.png"\] Alt text: Chevron icon.\) to expand the resource view.

4.  Locate the row for the resource assignment you want to update from either assigned work or unassigned work.

5.  Update one or both of the following date fields to extend or reduce the assignment:

    -   Start date: Move earlier to extend the assignment or later to reduce it.
    -   End date: Move later to extend the assignment or earlier to reduce it.
6.  Save the change.


## Result

The resource assignment reflects the updated start and end dates and the allocated effort redistributes proportionally across the new date range based on the configured allocation interval.

**Parent Topic:**[Using Resource Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/resource-management/using-rmw.md)

