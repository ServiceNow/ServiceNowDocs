---
title: Work on a stage-oriented release for a single product or service
description: Monitor and work on a release that follows the stage-oriented release process to release a single product or service.You can start over a stage-oriented release from any previously completed phase if you encounter an issue that requires you to go back.View the release status and work on its phases and tasks, and policies.
locale: en-US
release: australia
product: Digital Product Release
classification: digital-product-release
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Stage-oriented releases, Manage releases for digital products and services, Use, Digital Product Release, IT Service Management]
---

# Work on a stage-oriented release for a single product or service

Monitor and work on a release that follows the stage-oriented release process to release a single product or service.

## Before you begin

Role required: sn\_dpr\_model.product\_manager or sn\_dpr\_model.release\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Digital Product Release Workspace**.

2.  Select the releases icon \(![Releases icon.](../image/dpr-icon-release.png)\).

3.  Select a release from the list to open.

4.  If the release isn't in progress, select **Start release**.

5.  Select the **Overview** section to review and modify release details, get an overview of its status, or change its readiness target date.

    For more information, see [Review and update release details](dpr-work-release-details.md) and [Retarget a release](dpr-work-release-readiness-target.md).

6.  Select the **Release scope** section to review and update the scope of the release by adding or removing the product features and enhancements.

    For more information, see [Update the scope of a release](dpr-work-release-scope.md).

7.  Select the **Configuration items** section to review and manage the configuration items in the release.

    You can add more configuration items or remove the existing ones as needed. For more information, see [Manage configuration items in a release](dpr-work-release-config-items.md).

8.  Select the **Change requests** section to review and manage the change requests in the release.

    You can add new or existing change requests or remove the existing ones as needed. For more information, see [Manage change requests in a release](dpr-work-release-change-request.md).

9.  From the Release form header, select the number under the Artifacts to manage artifacts added to the release.

    For more information, see [Manage artifacts in a release](dpr-work-release-artifact.md).

10. Select the **Release notes** section to create and manage release notes for the release.

    You have the option to add release notes manually or generate using AI.

    -   To add release notes manually, select **Add manually** and then enter the release notes in the **Release notes** field.
    -   To generate release notes using AI, select **Generate**.

        For more information, see [Generate AI-powered release notes for a release](dpr-generate-release-notes.md).


## Restart the release phase

You can start over a stage-oriented release from any previously completed phase if you encounter an issue that requires you to go back.

### Before you begin

**Note:** When you restart a release from a completed phase, it resets that phase and any later phases up to the current one. It also resets the status of tasks, approval requests, and policies linked to each affected phase.

Role required: sn\_dpr\_model.release\_admin

### About this task

By restarting a phase, you can reassess and adjust the plan to overcome the new issues, ensuring that the release stays on track and meets its overall goals. For example, if a certain version of an artifact is being certified during the release process and it doesn't pass the validation, a new version of the artifact can be chosen. Then, you can restart the release from an earlier phase to repeat the same tasks, mapped policies, configuration items, and approvals from those phases.

### Procedure

1.  On the Release execution page, select the release phase action button \(![Release phase action icon.](../image/dpr-icon-menu.png)\) and then select **Restart phase**.

2.  On the Restart phase dialog box, select a phase from where you want to restart.

    The list displays the completed phases.

3.  Select **Restart**.


### Result

-   The state of the selected phase updates to In Progress and of all the later phases updates to Pending.
-   The state of the current phase updates to Restarted.
-   The state of all tasks in the affected phases updates to Open.
-   The configuration items associated with the affected phases are reassociated with the newly created corresponding phases.
-   The last run status of the policies mapped to theses phases updates to Not run.

## Execute the release

View the release status and work on its phases and tasks, and policies.

### Before you begin

Role required: sn\_dpr\_model.product\_manager or sn\_dpr\_model.release\_admin

### About this task

Automated email notifications are triggered at key release life cycle events. Notifications are sent to relevant stakeholders when:

-   A phase reaches its end date
-   A release task is 2 days from its due date
-   The release is 1 day from its readiness target
-   A phase's state changes
-   A policy is executed and resulted in non-compliant
-   A task approval request is submitted
-   A task approval request is rejected

For more information, see [Email notifications in Digital Product Release](../reference/dpr-email-notification.md).

### Procedure

1.  Select **Release execution** to view the release status and work on its phases, tasks, and policies.

    ![Release execution page of a stage-oriented release to track its progress.](../image/dpr-release-execution-stage2.png)

2.  Review the risk score for the current phase on the Release overview dashboard.

    The risk score for stage-oriented releases considers task completion, policy compliance, readiness dates, and progress thresholds. For more information, see [Risk score for stage-oriented releases](../concept/dpr-risk-score-release.md#).

3.  Update a release phase.

    **Note:** If the **stage\_workflow\_auto\_transition** system property is set to true, the phases are automatically closed when all tasks in it are closed and policies comply.

    1.  From the timeline, select a phase or use the arrow buttons to navigate to the previous or next phase.

    2.  When all tasks in the current phase are complete and mapped policies comply, mark the phase as complete by selecting **Complete phase**.

        **Note:** If any of the mapped policies is noncompliant, you can complete a phase only when you have any of the roles defined in the system property **sn\_dpr.complete\_phase\_override**.

        The state of the current phase is updated to Completed and the next phase is started. The actual end date of the current phase is updated to the current date.

4.  Add a task to a release phase.

    1.  From the timeline, select a phase or use the arrow buttons to navigate to the previous or next phase.

    2.  Select **Add task**.

    3.  On the Create task dialog box, add details for the task like its name, phase it belongs to, end date, and description.

    4.  If the task needs approval, perform the following steps:

        **Note:** You can select whether the task needs approval when creating it. This option can’t be changed after it’s saved.

        1.  Select **Yes** in the **Need approval** field.

            The **Assigned to** and **Approval definition** fields appear.

        2.  From the **Assigned to** list, select the user who would approve the task.
        3.  From the **Approval definition** list, select an approval definition to trigger the approval based on the predefined condition.
    5.  Select **Create task**.

    The task is created in the Pending state andadded to the selected phase.

    For an approval task, an approval record is created for the approvers to review and act.An email notification is also sent to them. For more information, see [Approve or reject a release task](dpr-approve-reject-release-task.md).

5.  Track and manage the progress of tasks for the selected phase.

    1.  From the timeline, select a phase or use the arrow buttons to navigate to the previous or next phase.

    2.  Select the **Tasks** tab to view all tasks in the phase.

        You can apply filters to view specific tasks or change the view type by selecting the **Kanban** or **List** option.

    3.  Select a task to open in the Task details pane.

    4.  Review the task in the Task details pane, or select **Full details** to open the task record in the form view.

    5.  Assign the task in the **Assigned to** field to the user who will work on it.

    6.  Review the approval status for an approval task in the **Approval** field.

    7.  Update the **State** field with the status of the task that doesn't need any approval.

        The state of an approval task is automatically updated when approved.

    8.  Select **Save** to save the changes.

        If you complete the current task and the system property **sn\_dpr.sequential\_task\_execution** is set to true, the next task in the order moves to the Open state.

6.  Manage mapping of policies to a release phase to validate it.

    1.  From the timeline, select a phase or use the arrow buttons to navigate to the previous or next phase.

        **Note:** Policies can’t be mapped to a completed or cancelled phase.

    2.  Select the **Policies** tab.

    3.  To map a policy to the selected phase,

        1.  Select **Add**.
        2.  On the Map Policies dialog box, select one or more policies from the list to map to the phase.
        3.  Select **Map policies**.
        The selected policies are mapped to the phase and are listed in the Policy Mappings list.

    4.  To delete an existing policy mapping,

        1.  Select the policies from the Policy Mappings list.
        2.  Select **Delete**, and confirm.
        Selected policies mappings are removed from the phase.

        **Note:** For an in-progress phase, if you remove a previously executed policy, the remaining policies are automatically run after its removal. The updated execution statuses of the individual policies are aggregated and shown in the **Policy status** field on the **Details** tab.

7.  Select **Run policies** to run policies on the current phase.

    All mapped policies are executed in the background for the current phase \(**In Progress** state\). You can check the execution status by refreshing the list on the **Policies** tab.

    When a policy execution results in a non-compliant status, an email notification is sent to the release admin and other relevant stakeholders.

    When multiple policies are mapped to a phase, their execution statuses are aggregated into the phase's overall status. You can view this aggregated status in the **Policy status** field on the **Details** tab.

8.  If a policy fails compliance, you can request an exception with justification.

    **Note:** This option is only available when both Digital Product Release and GRC: Policy and Compliance Management are installed.

    1.  Select the policy that failed.

    2.  Select Request exception.

    3.  In the Request policy exception, provide the reason, start date, end date, and business justification for the exception.

    4.  Select **Request**.

    The exception request is sent to the Compliance group. For more information about the review and approval of exception request, see Review the policy exception and extension request and Manage policy exceptions and extensions.

    After the exception is approved, the policy status shows as Compliant with exception in subsequent executions. The phase can be completed if all other policies are compliant.

9.  Close a release after verifying its completeness.

    For more information, see [Close a release](dpr-complete-release.md).

10. Cancel a release if it's no longer required.

    1.  Select **Cancel release**.

    2.  Enter the reason for cancellation and select **Cancel release**.


