---
title: Split resource assignments using Resources grid
description: Splitting a resource assignment at a specific date creates a resource assignment for the same user.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/portfolio-planning/split-resource-assignment-ppw.html
release: brazil
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2026-10-05"
reading_time_minutes: 1
breadcrumb: [Manage resources for demands, Use, Next Experience for Demand Management in Portfolio Planning, Portfolio Planning, Strategic Portfolio Management]
---

# Split resource assignments using Resources grid

Splitting a resource assignment at a specific date creates a resource assignment for the same user.

## Before you begin

-   When you split a resource assignment, a new assignment is created from the selected date. Both the assignments are assigned to the same user retaining the state of the assignment.
-   When you split a resource assignment, a new assignment is created from the selected date. Both the assignments are assigned to the same user with Approved state.
-   If a resource assignment has actuals captured for a certain duration, you can split the work only at the dates where there are no actuals captured.
-   Role required: it\_demand\_manager

## About this task

Use split when you need to divide a single resource's assignment into two time periods with different allocation levels, effort distributions, or tracking granularity. For example, split an assignment when a resource needs to reduce their allocation after a project milestone.

## Procedure

1.  Navigate to **Workspaces** &gt; **Portfolio Planning Workspace**.

2.  Select the Demands icon \[Omitted image "demands-icon.png"\].

3.  Open a demand from the **List** page.

4.  Select the **Resources** tab.

    The resource grid opens for the demand timeline, grouped by **Primary Group**.

5.  Select the chevron icon \(\[Omitted image "rmw-chevron-image.png"\] Alt text: Chevron\) to expand the resource view.

6.  Select the row context menu \(\[Omitted image "icon-row-context-menu.png"\] Alt text: Three vertical dots icon for row context menu.\) for the required work item and select **Split**.

    The Split modal appears with task insights such as the task name, resource name, start date, and end date.

7.  On the Split modal, select a date to split the resource assignment using the date picker.

8.  Select **Split**.


## Result

The resource assignment is split at the selected date and a copy of the resource assignment with new dates are displayed under the assignments of the selected resource.

## Example

Consider a resource assignment named Implement GenAI in docs assigned to Abel Tuter from July 16 through December 02. If you split the resource assignment at September 09, there will be two resource assignments with the same name and state assigned to Abel Tuter.

One resource assignment ranges from July 16 to September 09, and the other assignment ranges from September 10 to December 02.

