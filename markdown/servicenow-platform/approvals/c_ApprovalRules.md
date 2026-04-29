---
title: Approval rules
description: Many organizations rely on an approval process to ensure that requests are reasonable and fit an organization's budget.
locale: en-US
release: australia
product: Approvals
classification: approvals
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Classic approvals, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Approval rules

Many organizations rely on an approval process to ensure that requests are reasonable and fit an organization's budget.

**Important:** Classic approval rules have been replaced by the Workflow Studio [Ask for Approval action](https://www.servicenow.com/docs/access?context=ask-approval-flow-designer&version=australia&pubname=australia-build-workflows&ft:locale=en-US). Use Workflow Studio to create workflow-driven approval logic that is easier to maintain and provides better reporting information.

The service catalog can use these classes of approvals:

-   Gating approvals: Must occur before a request can be initiated. For example, allow a manager to reject an employee's request for a company car. To learn more about gating approvals, see [Gating approvals](c_GatingApprovals.md).
-   Process approvals: Take place within an execution plan process that has been initiated. For example, allow the security group to reject a request for access to SSN even though the employee's manager approved it. To learn more about process approvals, see [Process approvals](c_ProcessApprovals.md).

**Note:** To enable approval processes to operate smoothly, make sure that the appropriate users have the correct role, and that the role grants access to the necessary tables for users in all the relevant departments and domains.

-   **[Set automatic approval rules](../reference/r_SetAutomaticApprovalRules.md)**  
Approval rules can automatically set the approval state to something other than Not yet requested. As a result, an approval rule can create a set of approvers. You can also start the approval process by setting the approval state to **Requested**.
-   **[Gating approvals](c_GatingApprovals.md)**  
A gating approval acts as a gate through which a request must pass before it can start.
-   **[Process approvals](c_ProcessApprovals.md)**  
Once a request has passed its gating approvals, any relevant execution plans are initiated.
-   **[Approve with a process guide](../task/t_ProcessGuideApprovals.md)**  
Process guides work similarly to approval rules in that their execution is controlled via a condition.
-   **[Schematic of a hypothetical approval process](c_SchematicOfAHypoApprovalProc.md)**  
In the diagram below of a hypothetical approval process, the gating approval is color coded blue and an in-process approval is orange.

**Parent Topic:**[Classic approvals](../reference/r_Approvals.md)

