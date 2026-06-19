---
title: Copy a resource assignment
description: Copy an existing resource assignment to create one with inherited values, then adjust the fields before submitting. This reduces repetitive data entry when similar assignments recur across plans.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/resource-management/copy-ra-rmw.html
release: australia
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2026-06-04"
reading_time_minutes: 1
keywords: [copy resource assignment, duplicate resource assignment, resource assignment, resource management workspace]
breadcrumb: [Using Resource Management Workspace, Use, Resource Management Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Copy a resource assignment

Copy an existing resource assignment to create one with inherited values, then adjust the fields before submitting. This reduces repetitive data entry when similar assignments recur across plans.

## Before you begin

Role required: resource\_user, resource\_manager, it\_project\_manager

## About this task

Copying a resource assignment opens a new assignment form with values from the source such as named resource or resource attributes, planning item link, date range, and the allocated effort. You can modify any field before saving. The copy is an independent record, any changes to the copy don't affect the source, and later changes to the source don't flow into copies that are already created.

Use copy when:

-   The same resource continues onto a follow-on phase of work with a different date range or allocated effort.
-   A different resource takes on a comparable block of work and you want a fast starting point.
-   You want to split a single assignment into multiple shorter assignments by copying, then adjusting dates and effort on each.

Copy is not a substitute for split or reassign. Copying creates an independent new assignment rather than redistributing the original.

## Procedure

1.  Navigate to **Workspaces** &gt; **Resource Management Workspace**.

2.  Select the Resource cards icon \(\[Omitted image "rmw-resource-cards-L1-icon.png"\] Alt text: Resource cards icon.\) from the menu and open a resource card.

3.  Select the row context menu \(\[Omitted image "icon-row-context-menu.png"\] Alt text: Three vertical dots icon for row context menu.\) for the required task and select **Copy resource assignment**.

    Copy Resource Assignment form opens with values inherited from the source assignment.

4.  Review and update the inherited fields as needed, including the date range and allocated effort.

    Verify that the planning item link reflects the work the new assignment belongs to especially when copying across planning items.

5.  Select **Submit**.


## Result

A new resource assignment is created. The source assignment is unchanged.

**Parent Topic:**[Using Resource Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/resource-management/using-rmw.md)

