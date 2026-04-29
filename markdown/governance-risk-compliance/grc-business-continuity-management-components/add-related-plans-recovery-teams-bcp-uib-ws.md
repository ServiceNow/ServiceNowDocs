---
title: Add associated plans and recovery teams
description: Add your business continuity associated plans and recovery teams to your business continuity plan. You can then view the details in BCM UIB Workspace.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Structured workflows for BCPs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Add associated plans and recovery teams

Add your business continuity associated plans and recovery teams to your business continuity plan. You can then view the details in BCM UIB Workspace.

## Before you begin

Role required: sn\_bcm.admin, sn\_bcm.program\_manager, sn\_bcm.planner, sn\_bcp.plan\_manager

## About this task

You can add the associated plans that are listed in the Workspace view. When an associated plan is added in an exercise or event, it gets triggered from a task if the task is tagged as a dependency.

Previously, adding an associated plan would automatically include a link to the plan record in its record list. However, with the introduction of the Xanadu release, this process has changed to a one-way relationship, and the associated plan record no longer displays the link to the original plan record. To manually insert the link, you can navigate to the tab and add the link. This update provides the flexibility to designate the plan relationship as either a parent-child or sibling relationship.

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace**.

2.  In the List view, navigate to **Planning** and select the link to the plan record in the **Name** column.

3.  Select the **Associated plans** tab.

    **Note:** The **Related plans** tab has been renamed to the **Associated Plans** tab. It helps you to manage the cross-plan dependencies.

    The associated plan types are shown in the example:

    -   Upstream plans
    -   Downstream plans
    -   Related plans
    ![Associated plans.](../image/add-associated-plans.png)

    The **Is Associated to Task** field in the associated plans table is set to True if the associated plan is linked to a recovery task; or else it is set to False.

    **Note:** Related plans that are associated with a recovery task are created as child plans in events. If the related plans aren’t associated with any recovery task, they are created as related plans but not as child plans in events.

    Associated plans help you to identify when and where the plans are triggered in the flow, aiding in tracking and managing the plans during the recovery process.

4.  To add an upstream plan to the selected plan record, choose **Upstream plans** from the Associated plan types panel and then select **Add**.

    1.  To remove the upstream plan from the plan record, select the plan from the list view and choose the **Remove** option.

        A confirmation message is displayed asking you to confirm the deletion. Once you select **Delete All**, a confirmation message is displayed that the record has been successfully deleted.

    No UI actions are available for the Downstream plans.

5.  To add a related plan to the plan record, choose **Related plans** from the Associated plan types panel and then select **Add**.

    1.  To set the related plan as upstream plan, select **Set as upstream plan**.

        A confirmation message is displayed asking you to confirm the selection. Once you confirm, the plan is moved to the Upstream plans list.

    2.  To set the related plan as downstream plan, select **Set as downstream plan**.

        A confirmation message is displayed asking you to confirm the selection. Once you confirm, the plan is moved to the Downstream plans list.

    3.  To remove a related plan from the plan record, select the plan from the list view and choose the **Remove** option.

        A confirmation message is displayed asking you to confirm the deletion. Once you select **Delete All**, a confirmation message is displayed that the record has been successfully deleted.

6.  Verify that a cyclic dependency check is performed by the system and downstream tasks aren’t added in the upstream tasks.

    With the cyclic dependency check, you can add recovery tasks from the same downstream plan and upstream plan as dependencies. This provides a hierarchical approach to managing complex recovery sequences.

    The following example shows that recovery task t3 has a dependency on t4 \(another recovery task from same plan\) and on t1 which is a recovery task from the upstream plan.

    **Note:** Recovery tasks inside a business continuity plan \(BCP\) can now be linked to tasks from other plans, provided they belong to a direct parent plan. These recovery tasks are carried across to the event tasks.

    ![6.](../image/cp6-recovery-task-dependencies.png)

    By performing the cyclic dependency check, you can verify that child tasks aren’t added in the parent tasks and it isn’t a cyclic dependency.

7.  Select the **Recovery teams** tab and select **New**.

    1.  Add a recovery team to the plan.

        You can add a recovery team to the plan as shown in the examples.

        ![Recovery teams.](../image/recovery-teams-new.png)![Create New Recovery team form.](../image/add-new-recovery-team-form.png)

8.  Select **Save**.

    The plan record is updated and saved.

    The selected plans and recovery teams are added to the plan record.


-   **[Associating related plans to a recovery task](../concept/handling-related-plans.md)**  
You can now associate related plans with recovery tasks, making it easier to identify and manage plans during recovery. You can then use auto-generated nested plans in an event, reducing the manual effort of adding plans and improving system performance.

**Parent Topic:**[Structured workflows for BCPs](../concept/bcp-tasks-performed-by-bcp-owner.md)

