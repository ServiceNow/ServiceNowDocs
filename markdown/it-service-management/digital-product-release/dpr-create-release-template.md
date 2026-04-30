---
title: Create a release template
description: Create a release template to predefine the release process. The template contains templates for release phases, tasks, exit criteria for each of the phases, key dates, and approvals.Configure the DPR Release Task view to display the custom template fields on release task records of a release.
locale: en-US
release: zurich
product: Digital Product Release
classification: digital-product-release
topic_type: task
last_updated: "2026-02-17"
reading_time_minutes: 10
breadcrumb: [Configure, Digital Product Release, IT Service Management]
---

# Create a release template

Create a release template to predefine the release process. The template contains templates for release phases, tasks, exit criteria for each of the phases, key dates,and approvals.

## Before you begin

Identify phases, tasks within each phase, exit criteria for each phase, key dates,and required approvals for a release. If there are different processes followed for each kind of release or product, you should create multiple release templates.

Role required: sn\_dpr\_model.release\_template\_admin orsn\_dpr\_model.release\_admin

## About this task

The release teams can use these templates to create a release. All the phases, tasks, key dates,approvals, and phases' exit criteria from the template are applied to the new release. The release template helps the release team track and perform all the required tasks to complete the release on time.

**Note:** You can use the **Back** button to navigate to previous steps in the template creation wizard. The button is available in the Tasks, Policies, and Key dates activities. Data entered in a step is automatically saved when you navigate back.

## Procedure

1.  Navigate to **Workspaces** &gt; **Digital Product Release Workspace**.

2.  Select the release administration icon \(![Release administration icon.](../image/dpr-icon-release-admin.png)\).

3.  On the Release administration page, select the **Release templates** tab.

4.  Create a release template or update an existing one.

    -   To create a release template, select **New**.
    -   To modify an existing release template, open the release template from the list.
5.  On the Create release template dialog box, add details like name and short description.

6.  From the **Type** list, select a release type.

7.  Select **Enable release to validate product versions** to determine if a release created from this template can validate a new product versions.

8.  Select **Create**.

    A release template is created and opens in the release template setup playbook page to define the template.

9.  In the Release Process activity, select between a timeline-oriented or stage-oriented release process.

    |Release process|Description|
    |---------------|-----------|
    |**Timeline-oriented process**|This release process is appropriate for creating releases that have fixed deadlines and that follow a strict schedule.|
    |**Stage-oriented process**|This release process is appropriate for creating releases that prioritize completing objectives and features over following a strict schedule.|

10. Select **Mark as done**.

    The Release Process activity is marked as complete and can’t be edited further. The Phases activity becomes editable.

11. In the Phases activity, add phases to the release template.

    1.  Enter a unique phase name, the duration of the phase in days, and a short description.

        The **Duration** field appears only for the timeline-oriented process.The combined duration for all phases in the template must not exceed the maximum duration set in the **sn\_dpr.max\_template\_duration** system property.

    2.  Select **Add new phase** to add another phase.

        Repeat the steps to add more phases as required.

    3.  In the **Release readiness target phase** section, choose a phase from the **Select phase** list to align it with the release readiness.

        The selected phase's end date is considered as the release readiness target date.

    4.  In the **Schedule** section, choose a schedule from the **Select schedule** list as the default schedule.

        The list shows the schedule entries from the Schedule \[cmn\_schedule\] table of the type Excluded.

        Adding a schedule considers holidays and weekends and adjusts the phase and release durations accordingly. This helps improve release planning accuracy by including actual working days. For more information, see [Holiday schedules in a release](../concept/dpr-release-holiday-schedule.md).

        **Note:** This option is available only for the timeline-oriented release process.

    5.  Change the order of phases by selecting the move phase up \(![Move phase up icon.](../image/dpr-icon-up.png)\) or move phase down \(![Move phase down icon.](../image/dpr-icon-down.png)\) icons to define the sequence in which they’re processed in a release.

    6.  Select **Mark as done** to complete adding all required phases to the release template.

        The Phases activity is marked as complete. The Tasks activity becomes editable, displaying each phase in separate tabs.

12. In the Tasks activity, manage tasks to define the work that must be completed during each phase of a release.

    You can also attach supporting files and define template fields for tasks.

    1.  Select a phase tab in which you want to add a task.

    2.  In the **Task name** field, enter a unique name for the task.

    3.  In the **Need approval** field, select whether the task requires approval.

    4.  If approval is required for the task, select an approval definition from the **Approval definition** list.

        For more information, see [Create an approval definition in Digital Product Release](dpr-create-approval-definition.md).

    5.  Add supportive fields and documents to the task.

        1.  To include an additional field in the task, select a field from the **Field** list and its default value in the **Update to** field.

            The list shows fields from the Release Task \(sn\_dpr\_model\_release\_task\) table.

        2.  To add a document to the task, select **+ Add file**, and select a document.

            When you create a release from the template, selected fields and attached documents are copied to the release task records. These fields appear in the Release Task record form and documents in the Attachments pane and Activity stream.

            To display custom template fields on the release task record page in the workspace, you must add those fields to the DPR Release Task view. For more information, see [Display custom template fields on release task records](dpr-create-release-template.md#).

    1.  Select **Add new task** to add another task to the phase.

    2.  After all tasks are added to the current phase, select **Next phase**.

        The tasks you added to the current phase are saved. The next available phase tab is selected so you can add tasks for that phase.

        Repeat the steps to add more tasks as required for each phase.

    3.  After all tasks are added to all available phases, select **Save** on the last phase tab.

    4.  Change the order of tasks within a phase to define the sequence in which tasks are executed during a release.

        1.  Select **Reorder tasks** for the phase you want to reorder.

            The reorder icons appear next to each task in the selected phase.

        2.  Select the move task up \(![Move task up icon.](../image/dpr-icon-up.png)\) or move task down \(![Move task down icon.](../image/dpr-icon-down.png)\) icons to change the order in which they’re processed in a release.
        3.  Save or cancel the reorder operation.
            -   To save the new task order, select **Save order**.
            -   To discard the changes and revert to the original order, select **Cancel**.
        The tasks in the phase are reordered according to the new sequence.

    5.  Select **Mark as done** to complete adding tasks to phases as needed.

        The Tasks activity is marked as complete. The next activity becomes editable.

13. In the Key dates activity, add key dates as needed.

    **Note:** This activity is available only for the timeline-oriented release process.

    1.  Select a phase tab in which you want to add a key date.

    2.  Select **Add new key date** to add a key date to the phase.

        Alternatively, select anywhere on the timeline section. This action creates a key date with the number of days calculated and added to the new key date entry.

    3.  In the **Type** field, select the type of event to map to the phase.

    4.  In the **Key date** field, describe your key date.

    5.  Define your key date by selecting the number of days either from the beginning or before the end of the selected phase.

    6.  After all key dates are added, select **Mark as done** to complete adding key dates as needed.

        The Key dates activity is marked as complete. The Policies activity becomes editable, displaying each phase in separate tabs.

    When you create a release using the template, these key dates help you track the progress of the important events of the release.

14. In the Policies activity, map policies to each phase as needed.

    1.  Select a phase tab to which you want to map policies.

    2.  Select **Map policies**.

    3.  In the Map Policies dialog box, select policies from the list to map to the phase, and then select **Map policies**.

    4.  Select **Next phase** to save the mapped policies for the current phase and move to the next phase.

    5.  After policies are mapped to available phases, select **Save** from the last phase tab.

    6.  Select **Mark as done** to complete the Policies activity.

        The Policies activity is marked as complete.

15. In the Publish template pop-up window, select whether to publish the template.

    -   Select **Yes** to publish and activate the template.
    -   Select **No** to keep the template unpublished. You can publish and activate it later from the release template record form.

## Result

-   The release template is created and opens in the release template record form.
-   A published release template can be used for [creating releases](dpr-create-release.md).

## What to do next

On the release template record form, you can update, publish, delete, or duplicate it into a new template.

<table id="table_e3k_zwt_21c"><thead><tr><th>

Action

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

Publish the release template

</td><td>

Select **Publish template**.**Note:** The option to publish the template is only available if you didn't choose to publish it in the Publish template pop-up window.

</td></tr><tr><td>

Edit the release template

</td><td>

1.  Select the more actions button \(![More actions button icon.](../image/dpr-icon-more-actions.png)\) and select **Edit**.
2.  In the Edit template pop-up window, select **Yes** to confirm editing.

The release template becomes inactive and can't be used for creating a release.

The release template opens in the Playbook for editing.

3.  Update the template to add or change the phases, tasks, key dates, and policies as needed.
4.  To save all the changes in the template, select **Mark as done** in the Policies activity.

</td></tr><tr><td>

Duplicate the release template

</td><td>

1.  Select **Clone template**.
2.  In the Create release template pop-up window, enter the name, type, and description for the duplicate template and select **Create**.

A new release template is created identical to the current release template and is opened in the Playbook for editing.

3.  Update the template to add or change the phases, tasks, key dates, and policies as needed.

4.  Select **Mark as done** in the Policies activity to save all the changes in the template.

</td></tr><tr><td>

Delete the release template

</td><td>

Select the more actions button \(![More actions button icon.](../image/dpr-icon-more-actions.png)\) and select **Delete**.

</td></tr></tbody>
</table>**Related topics**  


[Release for a product or service](../concept/dpr-product-release.md)

[Create a release with a wizard](dpr-create-release-guided.md)

[Create a release for a product or service](dpr-create-release.md)

[Work on a timeline-oriented release for a single product or service](dpr-work-release.md#)

[Managing multiple releases through release bundles](../concept/dpr-release-bundle.md)

## Display custom template fields on release task records

Configure the DPR Release Task view to display the custom template fields on release task records of a release.

### Before you begin

Role required: sn\_dpr\_model.release\_template\_admin or sn\_dpr\_model.release\_admin

### About this task

Custom template fields that you add to tasks in a release template are stored on the release task record when a release is created. By default, these fields are not visible on the release task record page in the Digital Product Release Workspace. To display them, configure the DPR Release Task view to include the fields.

**Note:** This configuration applies at the table view level. All users with access to the DPR Release Task view see the custom fields after the view is updated.

### Procedure

1.  Navigate to **All** &gt; **Tables** &gt; **DPR Release Task \[sn\_dpr\_model\_release\_task\] table**.

2.  Open the DPR Release Task form view \(dpr\_rel\_task\_view\).

3.  Configure the form layout to add the custom fields on the form.

    For more information on configuring form layout, see [ServiceNow AI Platform® form administration](https://www.servicenow.com/docs/access?context=form-administration-landing-page&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

4.  Select **Save** to save the form view configuration.

    The custom fields appear on all release task records created from templates that include those fields. This is a one-time configuration — you do not need to repeat it for each release or template.


