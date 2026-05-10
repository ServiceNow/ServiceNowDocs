---
title: Work on a timeline-oriented release for a single product or service
description: Monitor and work on a release that follows the timeline-oriented release process to release a single product or service.View the release status and work on its phases and tasks, and policies.
locale: en-US
release: australia
product: Digital Product Release
classification: digital-product-release
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Timeline-oriented releases, Manage releases for digital products and services, Use, Digital Product Release, IT Service Management]
---

# Work on a timeline-orientedrelease for a single product or service

Monitor and work on a release that follows the timeline-oriented release process to release a single product or service.

## Before you begin

Role required: sn\_dpr\_model.product\_manager or sn\_dpr\_model.release\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Digital Product Release Workspace**.

2.  Select the releases icon \(![Releases icon.](../image/dpr-icon-release.png)\).

3.  Select a release from the list to open.

4.  Select the **Details** tab and add or update the schedule in the **Schedule** list to account for holidays during the release period.

    The list shows schedule entries that are of the type Excluded from the Schedule \[cmn\_schedule\] table.

    **Note:** The selected schedule must be within the release duration \(release target date\).

    The phase start and end dates are updated and the release duration is recalculated by considering the non-working days in the schedule. For more information on how schedules impact the dates of phases and release target, see [Holiday schedules in a release](../concept/dpr-release-holiday-schedule.md).

5.  If the release isn't in progress, select **Start release**.

6.  Select the **Overview** section to review and modify release details, get an overview of its status, or change its readiness target date.

    For more information, see [Review and update release details](dpr-work-release-details.md) and [Retarget a release](dpr-work-release-readiness-target.md).

7.  Select the **Release scope** section to review and update the scope of the release by adding or removing the product features and enhancements.

    For more information, see [Update the scope of a release](dpr-work-release-scope.md).

8.  Select the **Configuration items** section to review and manage the configuration items in the release.

    You can add more configuration items or remove the existing ones as needed. For more information, see [Manage configuration items in a release](dpr-work-release-config-items.md).

9.  Select the **Change requests** section to review and manage the change requests in the release.

    You can add new or existing change requests or remove the existing ones as needed. For more information, see [Manage change requests in a release](dpr-work-release-change-request.md).

10. From the Release form header, select the number under the Artifacts to manage artifacts added to the release.

    For more information, see [Manage artifacts in a release](dpr-work-release-artifact.md).

11. Select the **Release notes** section to create and manage release notes for the release.

    You have the option to add release notes manually or generate using AI.

    -   To add release notes manually, select **Add manually** and then enter the release notes in the **Release notes** field.
    -   To generate release notes using AI, select **Generate**.

        For more information, see [Generate AI-powered release notes for a release](dpr-generate-release-notes.md).


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

1.  Select **Release execution** to view the release status and work on its phases and tasks, and manage key dates.

    ![Release execution page of a time-oriented release to track its progress.](../image/dpr-release-execution.png)

2.  Review the risk score for the current phase on the Release overview dashboard.

    The risk score of timeline-oriented releases combines overdue task scores and policy failure scores, weighted by their respective importance. For more information, see [Risk score for timeline-oriented releases](../concept/dpr-risk-score-release.md#).

3.  Update a release phase.

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

    A scheduled job runs daily to execute the policies that are mapped to the phase. The Execution status column on the Policies list for each phase is updated to show the compliance status after each run.

    When multiple policies are mapped to a phase, their execution statuses are aggregated into the phase's overall status. You can view this aggregated status in the **Policy status** field on the **Details** tab.

8.  If a policy fails compliance, you can request an exception with justification.

    **Note:** This option is only available when both Digital Product Release and GRC: Policy and Compliance Management are installed.

    1.  Select the policy that failed.

    2.  Select Request exception.

    3.  In the Request policy exception, provide the reason, start date, end date, and business justification for the exception.

    4.  Select **Request**.

    The exception request is sent to the Compliance group. For more information about the review and approval of exception request, see [Review the policy exception and extension request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-compliance-management-workspace/review-policy-ext-and-extension-req-ws.md) and [Manage policy exceptions and extensions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-compliance-management-workspace/manage-policy-exceptions-ws.md).

    After the exception is approved, the policy status shows as Compliant with exception in subsequent executions. The phase can be completed if all other policies are compliant.

9.  Add or update key dates in a timeline-oriented release that should be in relation to the release target date.

    These key dates help you define and track important events that can happen during the release period.

    -   Add a new key date to the release:
        1.  Select the more actions icon next to the **Add task** button and then select **Add key date**.

            ![Add key date button on the Release execution tab.](../image/dpr-icon-add-keydate.png)

        2.  In the Add key date dialog box, fill in the fields.

            For more information, see [Release key date form](../reference/release-key-date-form.md).

        3.  Select **Save**.
    -   Update the existing key dates in the release:
        1.  Select a key date in the timeline bar to open the Key date details form in the side-panel.

            Alternatively, you can select the number under **Key dates** in the form header to view a list of key dates for the release, and then open a key date.

        2.  On the Key date form, update the fields.
        3.  Select **Save**.
10. Close a release after verifying its completeness.

    For more information, see [Close a release](dpr-complete-release.md).

11. Cancel a release if it's no longer required.

    1.  Select **Cancel release**.

    2.  Enter the reason for cancellation and select **Cancel release**.


