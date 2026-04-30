---
title: Approval and rollback workflow activities
description: Approval and rollback activities generate and manage approvals.
locale: en-US
release: zurich
product: Workflow Activities
classification: workflow-activities
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Workflow activities reference, Workflow activities, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Approval and rollback workflow activities

Approval and rollback activities generate and manage approvals.

Approval and rollback activities are not available in some workflows.

-   With two exceptions, approval and rollback activities are only available when the workflow runs on a table that extends Task. The exceptions are the [**Approval - User**](../reference/r_ApprovalUser.md) and [**Approval Action**](../reference/r_ApprovalAction.md) activities, which are available globally.
-   Approval and rollback activities are available only if approval engines are turned off for the table on which the workflow runs. If approval engines are enabled for the table, approval activities appear greyed out and cannot be selected. To learn more about how workflow and approval engines interact, read [Approval workflow activities and approval engines](../../using-workflows/concept/wf-approvals-n-rollbacks.md#).

-   **[Approval Action workflow activity](../reference/r_ApprovalAction.md)**  
The **Approval Action** activity performs an approval action on the current task.
-   **[Approval Coordinator workflow activity](../reference/r_ApprovalCoordinator.md)**  
The **Approval Coordinator** activity creates an approval whose outcome depends on the outcome of one or more child activities, including one or more **Approval - User**, **Approval - Group**, and/or **Manual Approval** activities.
-   **[Approval - Group workflow activity](../reference/r_ApprovalGroup.md)**  
The **Approval - Group** activity creates approval records for each member of a specified group.
-   **[Approval - User workflow activity](../reference/r_ApprovalUser.md)**  
The **Approval - User** activity creates one or more individual user approvals.
-   **[Generate workflow activity](../reference/r_Generate.md)**  
The **Generate** activity immediately creates task or approval records from any task or approval activities placed after the **Generate** activity in the workflow path. These pre-generated tasks and approvals start when the task and approval activities are reached during flow execution. This allows a task to have a set of associated pre-generated sequential tasks or approvals, but still require them to be completed in order.
-   **[Manual Approvals workflow activity](../reference/r_ManualApprovals.md)**  
The **Manual Approvals** activity watches and manages any approvals that users add manually outside of the workflow process. This activity only selects approvals that are in the Not requested state.
-   **[Rollback To workflow activity](../reference/r_RollbackTo.md#)**  
The **Rollback To** activity transitions directly to the activity specified by the outgoing transition line arrow.

**Parent Topic:**[Workflow activities](../../using-workflows/concept/c_WorkflowActivities.md)

