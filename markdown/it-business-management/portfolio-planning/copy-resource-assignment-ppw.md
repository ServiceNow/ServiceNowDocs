---
title: Copy a resource assignment for demands
description: Copy a resource assignment to create one with inherited values, then adjust the fields before submitting. This reduces repetitive data entry when similar assignments recur across plans.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/portfolio-planning/copy-resource-assignment-ppw.html
release: australia
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2026-10-05"
reading_time_minutes: 1
breadcrumb: [Manage resources for demands, Use, Next Experience for Demand Management in Portfolio Planning, Portfolio Planning, Strategic Portfolio Management]
---

# Copy a resource assignment for demands

Copy a resource assignment to create one with inherited values, then adjust the fields before submitting. This reduces repetitive data entry when similar assignments recur across plans.

## Before you begin

Role required: it\_demand\_manager

## About this task

Copying a resource assignment opens a new assignment form with values from the source. These values include named resource or resource attributes, demand link, date range, and the allocated effort. You can modify any field before saving. The copy is an independent record. Changes to the copy don't affect the source, and later changes to the source don't flow into copies that are already created.

Use copy when:

-   The same resource continues onto a follow-on phase of work with a different date range or allocated effort.
-   A different resource takes on a comparable block of work and you want a fast starting point.
-   You want to split a single assignment into multiple shorter assignments by copying, then adjusting dates and effort on each.

Copy is not a substitute for split or reassign. Copying creates an independent new assignment rather than redistributing the original.

## Procedure

1.  Navigate to **Workspaces** &gt; **Portfolio Planning Workspace**.

2.  Select the Demands icon \[Omitted image "demands-icon.png"\].

3.  Open a demand from the **List** page.

4.  Select the **Resources** tab.

    The resource grid opens for the demand's timeline, grouped by **Primary Group**.

5.  Select the row context menu \(\[Omitted image "icon-row-context-menu.png"\] Alt text: Three vertical dots icon for row context menu.\) for the required task and select **Copy resource assignment**.

    Values are inherited from the source assignment.

6.  Review and update the inherited fields as needed, including the date range and allocated effort.

    Verify that the demand link reflects the work the new assignment belongs to especially when copying across planning items.

7.  Select **Submit**.


## Result

A new resource assignment is created. The source assignment is unchanged.

