---
title: Assign a resource using AI resource finder
description: Use AI resource finder to identify and assign a resource to an unassigned resource assignment.
locale: en-US
release: australia
product: Now Assist for Strategic Portfolio Management \(SPM\)
classification: now-assist-for-strategic-portfolio-management-spm
topic_type: task
last_updated: "2026-04-21"
reading_time_minutes: 1
breadcrumb: [Using Now Assist for Strategic Portfolio Management \(SPM\), Now Assist for Strategic Portfolio Management \(SPM\), Strategic Portfolio Management]
---

# Assign a resource using AI resource finder

Use AI resource finder to identify and assign a resource to an unassigned resource assignment.

## Before you begin

Role required: it\_project\_manager or resource\_manager

To use AI rationale, verify that resource fit analysis skill is active.

## About this task

The AI resource finder uses generative AI to calculate AI rationale for available resources. Review the fit scores and availability before assigning a resource. Selecting a resource opens the existing assign resources modal where you can review allocations and distributions before confirming the assignment.

AI resource finder helps resource and project managers identify the best-fit resources for unassigned resource assignments in a project. The fit score indicates how well a resource matches a task based on the availability, past experience, similar kind of work and working on same projects. Resource managers review the AI-generated fit scores and rationale and decide which resource to assign to an unassigned assignment. The resource finder modal displays the following information for each resource:

-   Fit score: Percentage match of a resource for the task. The Fit score is deterministic and is not generated using AI.
-   Rationale: AI-generated explanation for the fit score.
-   Availability: The availability of the resource for a task.

## Procedure

1.  Navigate to **Workspaces** &gt; **Project Workspace** and open a project.

2.  View the resource assignment pane by enabling the Resource assignments toggle button.

    If the sn\_pw.enable\_resource\_planning property is set to true, then the Resource assignment toggle button and resource assignment pane are displayed in Project Workspace. The default value is false. You must have the pps\_admin role to enable this property.

3.  Create a unassigned resource assignment by selecting **Add resource** and selecting an attribute.

4.  From unassigned tasks pane, select the context menu row \(![3 vertical dots denoting the row context menu.](../../spw-financials/images/row-context-menu-icon.png)\) for any task and select **Resource finder**.

    ![Resource-finder-modal.](../images/resource-finder-modal.png)

5.  From Resource finder modal, select **Show monthly availability** toggle or weekly.

6.  Select the resource assignee and select **Assign resources**.

7.  From Assign resources modal, review the allocations and distributions and select **Assign**.

    ![assign-resources](../images/assign-resources-ai.png)

    The resource is assigned to the task.


**Parent Topic:**[Using Now Assist for Strategic Portfolio Management \(SPM\)](../concept/using-now-assist-for-spm.md)

