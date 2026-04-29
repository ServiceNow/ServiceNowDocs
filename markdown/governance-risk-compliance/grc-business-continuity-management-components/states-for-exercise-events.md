---
title: States for an exercise and crisis event
description: This section describes the states of progression for an exercises and crisis event.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Structured workflows for exercises, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# States for an exercise and crisis event

This section describes the states of progression for an exercises and crisis event.

## States for an exercise and crisis event

<table id="table_lmp_l5p_cyb"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Pending**

</td><td>

First state of the event.

</td></tr><tr><td>

**Pending Approval**

</td><td>

State of the event when an approval is requested. When you select **Submit for Approval**, the event is set to the **Pending Approval** state. In this state, you can only update the **Work notes** field in the event form.

 If any approval rules are configured for the event, then the approvals are generated and sent to the approvers. If no approval records are associated with the event in the requested state, then you can either select **Reject** or **Approve**.

 You can view the approval details of an event in the **Approvals** tab with the name of the approver, level of approval, and state of the approval.

 You can view the approval history of the event in the **Approval History** tab such as the approval state, name of the approver, event number, and so on.

 **Note:** If you are a BCM program manager, you can see the **Approve** and **Reject** buttons.

</td></tr><tr><td>

**Returned**

</td><td>

State of the event when an event is rejected. The state is set to **Returned**. It can be moved to the **Submit for Approval**, **Closed Complete**, or **Closed Incomplete** states. Since this action is related to an event only, you can update the description, results, and work notes in the form.

 When an event is in the **Returned** state, you can edit the state of the event asset.

 From the **Returned** state onwards, you can only add your comments and the attachments to the event task.

</td></tr><tr><td>

**Closed Incomplete**

</td><td>

State of the event when an event is incomplete.

</td></tr><tr><td>

**Closed complete**

</td><td>

When all tasks are complete, the event moves from the **Work in progress** to the **Closed complete** state.

</td></tr><tr><td>

**Approved**

</td><td>

Approved state of the event. When an event is approved, the state is set to the **Approved** state.

 You can perform additional UI actions:

-   **Generate PDF**

Download the PDF of an exercise or crisis event for reference. When you select Generate PDF, the PDF attachment is available in the **Activity** panel of the **Details** tab.

For information on generating the PDF of an exercise or crisis event, see [Generate event reports in PDF or Microsoft Word](../task/generate-pdf-for-events.md).

-   **Copy**

Save a copy of an exercise or crisis event for future reference as a template.

-   **360º view**

Visualize the 360º representation of an exercise or crisis event.

For information on how to view 360º relationships of an exercise or crisis event, see [View 360° relationships for exercises and crises](../task/relationship-view-exercise-crisis.md).

-   **Delete**

Delete an exercise or crisis event.

-   **Edit**

Edit an exercise or crisis event.

-   **Save**

Save an exercise or crisis event.


</td></tr><tr><td>

**Closed**

</td><td>

Closed state of the event.

</td></tr></tbody>
</table>The state transitions of an event task are described in the table.

<table id="table_zz5_w5p_cyb"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Open**

</td><td>

Open state of the event task. When an event is started, its event tasks that do not have a dependent recovery task move to the **Open** state.

</td></tr><tr><td>

**Pending**

</td><td>

Pending state of the event task. The event tasks that are dependent on other recovery tasks are in the **Pending** state when the event is started. After the dependent tasks are closed, the parent event task moves to the **Open** state.

</td></tr><tr><td>

**Skip Task**

</td><td>

Skip Task action for the event task. This action is available only if you have logged in as the BCM program manager. The **Skip** action is displayed when the task is in the **Pending** or **Open** state and the event must be in **Work in Progress** state. Selecting **Skip Task** moves the task to the **Closed Skipped** state. The actual start time and actual end time at this state are empty.

</td></tr><tr><td>

**Trigger**

</td><td>

Trigger action for the event task. This action is available only if you have logged in as the BCM program manager. The task is in the **Pending** state. Selecting **Trigger** moves the task to the **Open** state irrespective of its dependencies.

</td></tr><tr><td>

**Work In Progress**

</td><td>

Work In Progress state of the event task. The task is in the **Open** state. Selecting **Work In Progress** moves the task to the **Work in Progress** state. You can update the actual start time of the task in the **Actual start** field in this state. If you do not update the actual start time, the current date and time are recorded as the actual start time. The next available options are **Closed Complete** or **Closed Incomplete** state.

</td></tr><tr><td>

**Closed Incomplete**

</td><td>

Closed Incomplete state of the event task. Actual end time of the task is recorded in the **Actual end** field. If you do not update the actual end time, the current date and time are recorded as the actual end time. Update necessary information in the **Work notes** field and save the task.

</td></tr><tr><td>

**Closed Complete**

</td><td>

Closed Complete state of the event task. The task is closed and complete in this state. Actual end time of the task is recorded in the **Actual end** field. If you do not update the actual end time, the current date and time are recorded as the actual end time.

</td></tr></tbody>
</table>**Parent Topic:**[Structured workflows for exercises](performing-tasks-to-manage-exercise-events.md)

