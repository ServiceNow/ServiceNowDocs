---
title: Add associated plans and recovery teams
description: Add your business continuity associated plans and recovery teams to your business continuity plan. You can then view the details in BCM UIB Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/governance-risk-compliance/add-related-plans-recovery-teams-bcp-uib-ws.html
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 7
breadcrumb: [Structured workflows for BCPs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Add associated plans and recovery teams

Add your business continuity associated plans and recovery teams to your business continuity plan. You can then view the details in BCM UIB Workspace.

## Before you begin

Role required: sn\_bcm.program\_manager, sn\_bcm.planner, sn\_bcp.plan\_manager

## About this task

You can add the associated plans that are listed in the Workspace view. When an associated plan is added in an exercise or event, it gets triggered from a task if the task is tagged as a dependency.

Use the associated plan types to show how your plans depend on each other:

-   Upstream plans: Plans whose recovery tasks can be set as dependencies for recovery tasks in the selected plan.

    Example: The Payroll application recovery plan has the Data center recovery plan as an upstream plan. The Payroll task "Restore payroll database" can depend on the Data center task "Restore storage".

-   Downstream plans: Plans that have the selected plan as their upstream plan.

    Example: In the Data center recovery plan, the Payroll application recovery plan is listed as a downstream plan.

-   Related plans: Plans that are linked to the selected plan without an upstream or downstream relationship. You can later set a related plan as an upstream or downstream plan. A related plan that is linked to a recovery task is created as a child plan when the plan is triggered in an event.

    Example: The Facilities evacuation plan is a related plan of the Payroll application recovery plan. A Payroll recovery task triggers the Facilities plan. In an event, the Facilities plan is created as a child plan.


Adding an associated plan creates a one-way relationship. The associated plan record doesn't display a link to the original plan record. To insert the link manually, navigate to the **Associated plans** tab in the plan record and add the link. You can then set the relationship as an upstream, downstream, or related plan.

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace**.

2.  In the List view, navigate to **Planning** and select the link to the plan record in the **Name** column.

3.  Select the **Associated plans** tab.

    **Note:** The **Related plans** tab has been renamed to the **Associated plans** tab. It helps you to manage the cross-plan dependencies.

    The associated plan types are shown in the example:

    -   Upstream plans
    -   Downstream plans
    -   Related plans
    \[Omitted image "add-associated-plans.png"\] Alt text: Associated plans.

    The **Is Associated to Task** field in the associated plans table is set to True if the associated plan is linked to a recovery task; or else it is set to False.

    **Note:** Related plans that are associated with a recovery task are created as child plans in events. If the related plans aren’t associated with any recovery task, they are created as related plans but not as child plans in events.

    Associated plans help you to identify when and where the plans are triggered in the flow, aiding in tracking and managing the plans during the recovery process.

4.  To add an upstream plan to the selected plan record, choose **Upstream plans** from the Associated plan types panel and then select **Add**.

    1.  To remove the upstream plan from the plan record, select the plan from the list view and choose the **Remove** option.

        A confirmation message is displayed asking you to confirm the deletion. Once you select **Delete All**, a confirmation message is displayed that the record has been successfully deleted.

    No UI actions are available for the Downstream plans.

    The system doesn't allow the following when you add or remove an upstream plan:

    -   Relating a plan to itself.

        Example: You can't add the Payroll application recovery plan as an associated plan of itself.

    -   Adding a plan that is already related to the selected plan.

        Example: The Data center recovery plan is already related to the Payroll application recovery plan. You can't add it again.

    -   Removing an upstream plan while recovery tasks depend on tasks in that plan. Remove the task dependencies first.

        Example: The Payroll task "Restore payroll database" depends on the Data center task "Restore storage". You can't remove the Data center recovery plan as an upstream plan until you remove that dependency.

5.  To add a related plan to the plan record, choose **Related plans** from the Associated plan types panel and then select **Add**.

    The restrictions on relating a plan to itself and on adding a plan that is already related also apply to related plans. The system also doesn't allow the following when you set a related plan as an upstream or downstream plan:

    -   Setting a plan as an upstream or downstream plan while a recovery task in one plan activates the other plan. Remove the activation first.

        Example: A recovery task in the Payroll plan triggers the Facilities evacuation plan. You can't set the Facilities plan as a downstream plan until you remove that activation.

    -   Changing the relationship while recovery tasks depend on tasks in the upstream plan. Remove those task dependencies first.

        Example: The Payroll task "Restore payroll database" depends on the Data center task "Restore storage". You can't change the relationship between the two plans until you remove that dependency.

    -   Setting a plan as a downstream plan without write access to that plan.

        Example: You can edit the Payroll application recovery plan but not the Facilities evacuation plan. You can't set the Facilities plan as a downstream plan.

    1.  To set the related plan as upstream plan, select **Set as upstream plan**.

        A confirmation message is displayed asking you to confirm the selection. Once you confirm, the plan is moved to the Upstream plans list.

    2.  To set the related plan as downstream plan, select **Set as downstream plan**.

        A confirmation message is displayed asking you to confirm the selection. Once you confirm, the plan is moved to the Downstream plans list.

    3.  To remove a related plan from the plan record, select the plan from the list view and choose the **Remove** option.

        A confirmation message is displayed asking you to confirm the deletion. Once you select **Delete All**, a confirmation message is displayed that the record has been successfully deleted.

6.  Verify that a cyclic dependency check is performed by the system and downstream tasks aren’t added in the upstream tasks.

    With the cyclic dependency check, you can add recovery tasks from the same downstream plan and upstream plan as dependencies. This provides a hierarchical approach to managing complex recovery sequences.

    The example shows that recovery task t3 depends on t4 \(from the same plan\) and t1 \(from the upstream plan\).

    **Note:** Recovery tasks inside a business continuity plan \(BCP\) can now be linked to tasks from other plans, provided they belong to a direct parent plan. These recovery tasks are carried across to the event tasks.

    \[Omitted image "cp6-recovery-task-dependencies.png"\] Alt text: 6.

    By performing the cyclic dependency check, you can verify that child tasks aren’t added in the parent tasks and it isn’t a cyclic dependency.

    The system doesn't allow the following:

    -   Any relationship that creates a cyclic dependency.

        Example: The Data center plan is an upstream plan of the Payroll plan, and the Payroll plan is an upstream plan of the Reporting plan. You can't set the Reporting plan as an upstream plan of the Data center plan.

    -   Creating an event task that triggers a plan that is already in the activation chain of the event \(a circular activation\).

        Example: The Payroll plan triggers the Data center plan in an event. A task in the Data center plan then triggers the Payroll plan. The event task isn't created.

    -   Saving a recovery task that triggers a plan if the nested plans exceed the maximum allowed levels. Remove the related plan to save the task.

        Example: A recovery task triggers a plan that itself triggers other plans in a long chain. If the chain has more levels than the maximum, the task isn't saved.

7.  Select the **Recovery teams** tab and select **Add**.

    1.  Select one or more active recovery teams from the list and confirm the selection.

        The selected recovery teams are added to the plan, as shown in the example.

        \[Omitted image "recovery-teams-new.png"\] Alt text: Recovery teams.

        The recovery teams that you select are managed at a global level and can be added to more than one plan. Use the **Locations** field on a recovery team to associate one or more locations with it.

8.  Select **Save**.

    The plan record is updated and saved.

    The selected plans and recovery teams are added to the plan record.


-   **[Associating related plans to a recovery task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/handling-related-plans.md)**  
You can now associate related plans with recovery tasks, making it easier to identify and manage plans during recovery. You can then use auto-generated nested plans in an event, reducing the manual effort of adding plans and improving system performance.

**Parent Topic:**[Structured workflows for BCPs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/bcp-tasks-performed-by-bcp-owner.md)

