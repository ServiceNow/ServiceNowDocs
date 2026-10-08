---
title: Assign unassigned work for demands using Resource finder
description: Assign a resource for unassigned work for a demand using the suggestions which match the skill-set and primary attributes requirements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/strategic-planning/assign-resources-with-resource-finder-dw.html
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2026-09-30"
reading_time_minutes: 1
keywords: [resource assignment, demand management, resource finder]
breadcrumb: [Manage resources for demands, Use, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Assign unassigned work for demands using Resource finder

Assign a resource for unassigned work for a demand using the suggestions which match the skill-set and primary attributes requirements.

## Before you begin

ServiceNow Otto for Strategic Portfolio Management must be installed for AI generated suggestions.

Role required: it\_demand\_manager

## About this task

The resource finder uses generative AI to calculate AI rationale for available resources if ServiceNow Otto for Strategic Portfolio Management is installed. Otherwise, it generates only the fit scores and availability before assigning a resource. Selecting a resource opens the existing assign resources modal where you can review allocations and distributions before confirming the assignment.

The resource finder helps demand managers identify the best-fit resources for unassigned resource assignments in a demand. The fit score indicates how well a resource matches a task based on the availability, past experience, and similar work. Demand managers review the fit scores and rationale and decide which resource to assign to an unassigned assignment. The resource finder modal displays the following information for each resource:

-   Fit score: Percentage match of a resource for the task. The Fit score is deterministic and is not generated using AI.
-   Rationale: AI-generated explanation for the fit score. This field is available when ServiceNow Otto for Strategic Portfolio Management is installed.
-   Availability: The availability of the resource for a task.

For more information about how the Resource finder works and the resources are mapped, see [Manage resources for demands](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/strategic-planning/resource-planning-for-demands-dw.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace**.

2.  Select the Demands icon \[Omitted image "demands-icon.png"\].

3.  Open a demand from the **List** page.

4.  Select the **Resources** tab.

    The resource grid opens for the demand's timeline, grouped by **Primary Group**.

5.  Select the row context menu \(\[Omitted image "icon-row-context-menu.png"\] Alt text: Three vertical dots icon for row context menu.\) for any unassigned task and select **Resource finder**.

6.  Select the resource assignee and select **Assign resources**.

    \[Omitted image "demand-resource-finder1.png"\] Alt text: The available best fit resources are listed.

7.  From Assign resources modal, review the allocations and distributions and select **Assign**.

    \[Omitted image "demand-resource-finder2.png"\] Alt text: Distribution choices and preview options before assignment.

    The resource is assigned to the task.


