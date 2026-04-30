---
title: Create task and assessment-type action items
description: Use integration of crisis events and Smart Assessment for creating necessary action items related to the crisis event. The action items can be of task and assessment type.
locale: en-US
release: yokohama
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Creating action items in crisis events, Structured workflows for crisis events, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Create task and assessment-type action items

Use integration of crisis events and Smart Assessment for creating necessary action items related to the crisis event. The action items can be of task and assessment type.

## Before you begin

Role required: sn\_bcm.planner, sn\_bcm.program\_manager

## About this task

Verify that you have created Smart Assessment templates for integrating crisis events with the Smart Assessment Engine.

## Procedure

1.  In the List view, navigate to **Crisis events** &gt; **Pending** and select the crisis event in the list.

2.  Report the crisis event either from the home page or from the events page by creating an event.

    1.  Add the description of the event.

    2.  Assign it to a user by updating the **Assigned to** field.

    3.  Select **Save**.

    An event is created in the application. You can create action items related to the event by updating the **Action items** tab, even before the event starts.

3.  In the **Action items** tab of the event, select **New**.

    The Create New Action item form is displayed.

    ![Create New Action item.](../image/create-new-action-item-action-task.png)

4.  On the form, fill in the fields.

    For descriptions of all these fields, see [Create New Action item form for crisis events](../reference/create-new-action-item-crisis-event-form.md).

    1.  Add the description and short description of the action item.

    2.  Select the type of action task by selecting **Task** or **Assessment**.

    3.  Add an assignment group or a team member and an additional assignee list.

    4.  Assign a due date in the Timeline section.

    5.  Select **Save**.

    The Action item record is created in the **Open** state and the action item is displayed in the **Action items** tab of the event.

5.  To skip the action item if it is not needed, select **Skip task**.

6.  To work on the action item as a task, select **Task** in the **Type** field.

    1.  To work on the action item task, select **Work in progress**.

        The state of the action item is updated to **Work in progress**. The actual start date and time for the action item task is recorded and displayed in the Actual start column of the **Action items** tab.

    2.  To complete the action item task, select **Closed complete** in the action item record.

        The state of the action item is updated to **Closed complete**. The actual end date and time taken for the action item task is auto-captured and displayed in the Actual end date and Actual time taken columns of the **Action items** tab.

7.  To mark the action task as an assessment, select its type as **Assessment** in **Type** field in the Create New Action item form.

    1.  Select the assessment template in the **Assessment template** field.

        When you select the action task as an assessment, the **Assessment template** field is displayed in the form. The application uses Smart Assessment to perform the assessment. Ensure that BCM administrators have already created the necessary templates in the Assessment Workspace beforehand using the Smart Assessment Engine.

        **Note:** To make the desired Smart Assessment templates visible in the drop-down in the action item form in the Business Continuity Workspace, verify that following steps are completed in the Assessment Workspace.![Selections.](../image/event-action-item-sa-req-fields.png)

        1.  Select the necessary template, such as the Fire crisis template shown in the example, in the Details section.
        2.  Choose the **Threat assessment for crisis events** category in the **Assessment template categories** field. If you choose a different category, the desired template will not be shown in the Business Continuity Workspace.
        3.  Choose **Event** and **Action item** as the targets in the **Assessment targets** field.
        4.  To read the assessment, specify the reader role, such as the core viewer \(sn\_bcm.core\_viewer\) as the minimum role, in the **Assessment reader role** field of the Settings section. Usually, the core viewer \(sn\_bcm.core\_viewer\) role is specified as it is shared across all the roles.
        5.  Publish the assessment template.
        Only when these conditions are met, the template is available for selection in the drop-down of the action item form.

        For information on setting up Smart Assessment templates, see [Create an assessment template](../../assessment-engine/task/sae-asmnt-template-create.md).

    2.  Add an assignment group or a team member and additional assignee list, select the timeline, and save the record.

    3.  To continue working on the action item assessment, select **Work in progress**.

    4.  To view responses to the assessment as another user, select **View response**.

    5.  To respond to the assessment as the assignee, select **Take assessment**.

    6.  Respond to all the questions and select **Submit**.

    7.  Confirm that you have reviewed the answers and select **Submit** again in the modal.

        Your response is submitted and a confirmation is displayed on the screen.

    8.  To complete the action item assessment, select **Closed complete**.

        The state of the action item assessment is updated to **Closed complete**.

8.  To re-trigger the action task, select **Re-trigger**.

9.  To save the action task, select **Save**.

    This step completes the workflow of the action item record.


-   **[Create New Action item form for crisis events](../reference/create-new-action-item-crisis-event-form.md)**  
Use the Create New Action item form in the BCM Configurable Workspace to add action items about a crisis event.

**Parent Topic:**[Creating action items in crisis events](../concept/creating-action-items-in-crisis.md)

