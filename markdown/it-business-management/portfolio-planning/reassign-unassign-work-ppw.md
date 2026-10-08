---
title: Reassign or unassign work using Resources grid
description: Reassign or unassign assigned work from the Resources grid of a demand. You can group the resource board by primary attributes to identify the resources with same primary attributes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/portfolio-planning/reassign-unassign-work-ppw.html
release: brazil
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2026-10-05"
reading_time_minutes: 2
breadcrumb: [Manage resources for demands, Use, Next Experience for Demand Management in Portfolio Planning, Portfolio Planning, Strategic Portfolio Management]
---

# Reassign or unassign work using Resources grid

Reassign or unassign assigned work from the Resources grid of a demand. You can group the resource board by primary attributes to identify the resources with same primary attributes.

## Before you begin

-   When you reassign work, both resources must have matching primary attributes. For more information about mapping primary attributes to resources, see [Map primary attributes to resources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/scenario-planning-in-spw/map-primary-attributes-cp.md).
-   You can reassign a work item when actual hours aren't captured.
-   You can't reassign a work item if it has associated actual hours captured for the entire duration.
-   You can't unassign a work item if it has any associated actual hours captured.
-   You can't unassign an assignment if it has any associated actual hours captured.
-   You can't reassign or unassign group resource assignments.

Role required: it\_demand\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Portfolio Planning Workspace**.

2.  Select the Demands icon \[Omitted image "demands-icon.png"\].

3.  Open a demand from the **List** page.

4.  Select the **Resources** tab.

    The resource grid opens for the demand timeline, grouped by **Primary Group**.

5.  Select the chevron icon \(\[Omitted image "rmw-chevron-image.png"\] Alt text: Chevron\) to expand the resource view.

6.  To reassign any assigned work:

    1.  Select the row context menu \(\[Omitted image "icon-row-context-menu.png"\] Alt text: Three vertical dots icon for row context menu.\) for the required work item.
    2.  Select **Reassign**.

        **Tip:** Group the resources grid by the primary attributes to drag the resource assignments to another resource to completely reassign work.

    3.  On the Reassign work window, enter a resource name in the **User** field to reassign work to and duration using the **Start month** and **End month** date picker.

        \[Omitted image "demand-reassign-work-window.png"\] Alt text: Reassign work window displaying current user assignment and options to select another resource to reassign work.

7.  Select **Reassign**.

    **Note:** Use the reassign feature to assign part of a task among resources without overlapping the assignment dates.

    The selected work item will be reassigned to the selected resource.

8.  To unassign any assigned work:

    1.  Select the row context menu \(\[Omitted image "icon-row-context-menu.png"\] Alt text: Three vertical dots icon for row context menu.\) for the required work item.
    2.  Select **Unassign**.
    The selected work item is unassigned.


## Example

Consider a development task spanning from January 1, 2024 to September 30, 2024 which is assigned to Tom, a developer who has the following primary attributes.

-   Primary Group - Development
-   Primary Skill - Java
-   Primary Role - Java Developer 1

Tom has actual hours captured from January 1, 2024 through March 31, 2024 and will be unavailable for next 2 months.

As a demand manager, you can either reassign this task in its entirety starting from April 1, 2024 till September 30, 2024 to Raj. Raj has the same primary attributes. Or reassign the task from April 1, 2024 to May 31, 2024 to Raj, leaving the rest of the assignment to Tom.

The actual hours captured by Tom are retained even though the task is reassigned. Raj can capture the actuals hours for the assigned period after completing the work.

## What to do next

You can allocate the unassigned work and approve the reassigned work. For more information, see [Assign and approve unassigned work](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-planning/assign-work-to-resources-ppw.md).

