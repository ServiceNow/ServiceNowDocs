---
title: Assign unassigned work using Resource finder
description: Assign resource using the AI suggestions which match the skill-set and primary attributes requirements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/resource-management/assign-resources-using-resource-finder.html
release: australia
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2026-04-27"
reading_time_minutes: 1
breadcrumb: [Using Resource Management Workspace, Use, Resource Management Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Assign unassigned work using Resource finder

Assign resource using the AI suggestions which match the skill-set and primary attributes requirements.

## Before you begin

Role required: resource\_user, resource\_manager

## About this task

The AI resource finder uses generative AI to calculate AI rationale for available resources. Review the fit scores and availability before assigning a resource. Selecting a resource opens the existing assign resources modal where you can review allocations and distributions before confirming the assignment.

AI resource finder helps resource and project managers identify the best-fit resources for unassigned resource assignments in a project. The fit score indicates how well a resource matches a task based on the availability, past experience, similar kind of work and working on same projects. Resource managers review the AI-generated fit scores and rationale and decide which resource to assign to an unassigned assignment. The resource finder modal displays the following information for each resource:

-   Fit score: Percentage match of a resource for the task. The Fit score is deterministic and is not generated using AI.
-   Rationale: AI-generated explanation for the fit score.
-   Availability: The availability of the resource for a task.

For more information regarding how the Resource finder works and the resources are mapped, see [Resource finder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/resource-management/explore-rmw.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Resource Management Workspace**.

2.  Select the Resource cards icon \(\[Omitted image "rmw-resource-cards-L1-icon.png"\] Alt text: Resource cards icon.\) from the menu and open a resource card.

    Alternatively, you can view unassigned tasks using the Unassigned assignment requests widget from the overview dashboard.

3.  From unassigned tasks pane, select the context menu row \(\[Omitted image "row-context-menu-icon.png"\] Alt text: 3 vertical dots denoting the row context menu.\) for any task and select **Resource finder**.

    \[Omitted image "resource-finder-modal.png"\] Alt text: Resource-finder-modal.

4.  From Resource finder modal, select **Show monthly availability** toggle or weekly.

5.  Select the resource assignee and select **Assign resources**.

6.  From Assign resources modal, review the allocations and distributions and select **Assign**.

    \[Omitted image "assign-resources-ai.png"\] Alt text: assign-resources

    The resource is assigned to the task.


**Parent Topic:**[Using Resource Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/resource-management/using-rmw.md)

