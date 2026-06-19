---
title: Create a quick recovery task
description: Create a quick recovery task from Recovery tasks or as part of the planned recovery strategy for a business continuity plan. Using the quick insert feature, you can create tasks without navigating to a separate form. Tasks can be ordered, inserted in sequence \(before, after, or in parallel with existing tasks\), and dependencies are updated automatically.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/create-quick-recovery-task.html
release: australia
topic_type: task
last_updated: "2026-04-01"
reading_time_minutes: 8
breadcrumb: [Structured workflows for BCPs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Create a quick recovery task

Create a quick recovery task from Recovery tasks or as part of the planned recovery strategy for a business continuity plan. Using the quick insert feature, you can create tasks without navigating to a separate form. Tasks can be ordered, inserted in sequence \(before, after, or in parallel with existing tasks\), and dependencies are updated automatically.

## Before you begin

Role required: sn\_bcm.admin, sn\_bcm.program\_manager, or sn\_bcm.planner

## About this task

The Recovery tasks tab on a business continuity plan allows you to create and manage recovery tasks directly from the plan record. When a plan has no tasks yet, selecting **Quick insert** enables you to create a recovery task directly from a pop-up modal without leaving your current page. The modal displays only the required fields and enforces mandatory field validation before submission. You can move and resize the modal as needed.

Before this enhancement, creating a recovery task opened the full recovery-task form on a separate page. After saving, the user remained on the new task record and had to navigate back to the plan to add the next task. The quick insert flow keeps you on the plan page so that the context of the plan, its existing tasks, and their dependencies remains visible while you add each task. For the full long-form workflow, see [Add recovery tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/add-a-recovery-task.md).

Once tasks exist, the quick insert form provides additional options to control where and how the new task is inserted relative to existing tasks. You can insert tasks in the following positions:

-   After — inserts the new task after a selected task and automatically sets the dependency.
-   Before — inserts the new task before a selected task, updating dependencies accordingly.
-   In parallel — creates the new task with the same dependencies as the selected task, so both run concurrently.
-   In no order — creates a task without any dependency, assigning it order 1.

The Create a quick recovery task button is available in two locations:

-   On the plan page
-   Within the loss scenario recovery strategy

Task template groups can also be applied in bulk using the **Add groups** control in the **Recovery tasks** tab toolbar. Template groups pre-populate loss scenario associations, recovery strategies, and planned durations for each task they contain.

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace** &gt; **Plan record** &gt; **Recovery tasks** or **Workspaces** &gt; **Business Continuity Workspace** &gt; **Plan record** &gt; **Loss scenarios** &gt; **Recovery strategies** tab.

    You can open the plan record and open the **Recovery tasks** tab or the **Recovery strategies** tab in Loss scenarios.

    When no recovery tasks exist, the tab shows an empty list with an Insert button.

    \[Omitted image "rt-insert-menu.png"\] Alt text: Insert menu.

2.  To open the Create a quick recovery task modal, select **Insert**.

    The panel opens on the right side of the screen. When the plan has no tasks, only the basic task fields are shown — Short description \(required\), Phase, Plan recovery strategy, Tag assets, and Planned duration \(Days, Hours, Minutes, Seconds\). The Assignment details section includes Owner, Assignment group, Additional assignees, and Recovery team.

    \[Omitted image "rt-panel.png"\] Alt text: Insert panel.

3.  Complete the required fields for the recovery task such as Phase, Plan recovery strategy, and Planned duration.

    The modal displays only the fields necessary for task creation. For the first task in the plan, the Phase and Plan recovery strategy fields let you categorize the task within the recovery workflow. In the following example, Phase is set to Preparation and Plan recovery strategy is set to RS1.

    \[Omitted image "rt-prep-rs.png"\] Alt text: Phase and strategy.

4.  Select a **Plan loss scenario** to scope the task to a specific disruption context, and verify the **All assets from plan** field in the **Assignment details** section.

    The **Plan loss scenario** field ensures the task is surfaced only when the plan is exercised under that scenario type. The **All assets from plan** field defaults to all assets in the plan; update it to narrow the asset scope for the task.

    \[Omitted image "qi-create-reco-task-panel.png"\] Alt text: Quick recovery task panel showing the Plan loss scenario field and the All assets from plan field in the Assignment details section alongside Planned duration Hours, Minutes, and Seconds fields.

5.  Drag the modal to reposition it or re-size it by selecting and dragging its edges if needed.

6.  Review your entries to verify that all mandatory fields are filled in.

7.  To create the recovery task, select **Save**.

    The task is created in the Recovery tasks list and it is associated with the current plan without navigating away from the page. The count in the tab header updates to reflect the new total.

    \[Omitted image "rt11.png"\] Alt text: Count in the tab.

8.  To insert additional tasks, select **Insert** again.

    For plans with existing tasks, the quick insert panel now shows an Insert task positioning bar at the top. Use the Insert task drop-down to choose where to position the new task relative to an existing one. The available options are: after, before, in parallel, and in no order.

    \[Omitted image "rt.png"\] Alt text: Order.

    \[Omitted image "quick-form-insert-position.jpg"\] Alt text: Create a quick recovery task modal with the Insert task drop-down expanded to show after, before, in parallel, and in no order.

9.  Select a positioning option and choose a reference task in the adjacent field.

    -   After — the new task is added following the selected task. Its dependency is automatically set to that task. For example, if you insert after task1, the new task gets task1 as its dependency.
    -   Before — the new task is inserted before the selected task. Dependencies of the surrounding tasks are recalculated. For example, inserting before task2 places the new task between task1 and task2, and task2's dependency updates to indicate the new task.
    -   In parallel — the new task receives the same dependencies as the selected task, so both tasks can run concurrently. An optional check box labeled "Runs new task in parallel with next tasks" appears when an existing task has following tasks that would also run in parallel.
    -   In no order — the task is created without any dependency and is assigned order 1.
    Example — After: With Task 1 already in the plan, select **after** and choose **Task 1** as the reference task, then save the new task as **Task 2**. The **Dependencies** column for Task 2 is automatically populated with Task 1, and the **Planned order** values are recalculated.

    Example — In parallel: With Task 1 and Task 2 in the plan, select **in parallel** and choose **Task 2** to create **Task 2.1**. Task 2.1 receives the same dependency \(Task 1\) as Task 2 and is assigned the same planned order, so the two tasks run concurrently. Selecting **Runs new task in parallel with next tasks** extends the parallel behavior to any downstream tasks of the reference task. \(When you insert before a task, this check box is instead labeled **Runs new task in parallel with previous tasks**.\)

    \[Omitted image "tasks-with-dependencies.jpg"\] Alt text: Task 1 and Task 2, with Task 2's dependency set to Task 1.

    \[Omitted image "parallel-task-insert.jpg"\] Alt text: Modal shows "After" selected, Task 1 as the reference, and the parallel check box checked — with Task 2.2 listed as running alongside Task 2.1 and Task 2.

10. Fill in the short description and any other fields, then select **Save**.

    For more information on the fields in the form, see [Create a quick recovery task form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-quick-recovery-task-form.md).

    The system recalculates task order based on dependencies and updates all planned order values in the list. The new task appears in its correct position on the Recovery tasks tab.

11. Continue adding tasks as needed.

12. To insert a task relative to a specific row, select the check box on that row first, then select **Insert**.

    When a row is selected, the Insert task reference field in the quick insert panel is pre-populated with that task name, so you do not have to search for it manually. This is especially useful when the plan contains many tasks.

13. Review the completed task list to confirm planned order, dependencies, phases, and recovery strategies are correct.

    The Planned order column reflects the sequence calculated from task dependencies. Tasks without dependencies are assigned the lowest order number \(1\). Tasks that depend on others receive a higher order. Tasks sharing the same order run in parallel.

    **Note:**

    -   If a plan has more than 500 tasks, order is not recalculated automatically. Use the Update dependencies button on the plan or task record to manually trigger recalculation.
    -   The Insert task reference field is pre-populated when you select a row check box before selecting Insert, reducing the effort of searching through lengthy task lists.
    -   The quick insert panel can be repositioned by dragging. Its position is preserved during the current session.
    -   Selecting a task's order number opens the full task form in a separate page view. To stay in the quick insert experience, use the Insert button rather than navigating directly to a task record.

## Result

To save a task into a reusable group, select the task row in the list, then select **Save as group** &gt; **Save tasks**. To append it to an existing group, select **Save as group** &gt; **Add to group**.

Group names are unique. Reusing an existing group name surfaces an inline error in the **Create task template group** modal.

\[Omitted image "qi-save-tasks.png"\] Alt text: Recovery tasks tab toolbar showing the Save as group dropdown expanded with Save tasks and Add to group options.

-   **[Create a quick recovery task form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-quick-recovery-task-form.md)**  
Use the Create a quick recovery task form in the BCM Configurable Workspace to insert details on the recovery task quickly.

**Parent Topic:**[Structured workflows for BCPs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/bcp-tasks-performed-by-bcp-owner.md)

