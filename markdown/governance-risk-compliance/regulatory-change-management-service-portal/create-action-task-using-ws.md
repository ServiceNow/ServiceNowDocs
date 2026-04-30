---
title: Create a new action task for the alert
description: Create a new action task for the alert so that you can assign the action tasks to the compliance and risk users and mark a due date for the action tasks.
locale: en-US
release: yokohama
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Manage regulatory tasks, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Create a new action task for the alert

Create a new action task for the alert so that you can assign the action tasks to the compliance and risk users and mark a due date for the action tasks.

## Before you begin

Role required: sn\_grc\_reg\_change.user

## About this task

The user with the sn\_grc\_reg\_change.user role assigns the selected action task to the users with the sn\_compliance.manager and sn\_risk.manager roles depending on the action area of the alert such as compliance or risk. Once the compliance and risk users complete the action tasks associated with the alert, the alert and the parent regulatory change task are closed automatically.

## Procedure

1.  Navigate to **All** &gt; **Regulatory Change Management** &gt; **Compliance Workspace**.

    The Regulatory Change Management application in the Compliance Workspace is displayed.

2.  In the List view, navigate to **Lists** &gt; **Regulatory Alerts** &gt; **Assigned Alerts** view.

3.  Complete one of the following tasks depending on the type of the alert.

    |Field|Description|
    |-----|-----------|
    |**Regulatory event alert**|Select the regulatory event alert for which the regulatory change task is in the **In progress** state and the Action tasks related list is displayed in the alert UI page.|
    |**Source document alert**|Select the source document alert for which the source document import task is in the **In progress** state and the Action tasks related list is displayed in the alert UI page.|

4.  Navigate to the Action Tasks related list and select **New**.

    **Note:** Only when the regulatory task is in **New**, **Work in Progress**, or **Implementation** states, you can create a new action task.

<table id="table_uqv_s2x_vqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

General

</td></tr><tr><td>

Name

</td><td>

Name of the action task.

</td></tr><tr><td>

Instructions

</td><td>

Instructions related to the action task.

</td></tr><tr><td class="sub-head" colspan="2">

Classification

</td></tr><tr><td>

Type

</td><td>

Type of the action task:-   None
-   Business Impact
-   Change Policies
-   Executive Briefing
-   Legal Review
-   Notification
-   Others


</td></tr><tr><td>

Priority

</td><td>

Priority of the action task:-   None
-   1 - Critical
-   2 - High
-   3 - Moderate
-   4 - Low
-   5 - Planning


</td></tr><tr><td class="sub-head" colspan="2">

Area of Impact

</td></tr><tr><td>

Impacted regulatory item

</td><td>

Table to obtain the impacted regulatory item from. For example, **Control objective**.

</td></tr><tr><td>

Impacted area

</td><td>

Specific impacted area of the selected table. For example, if you selected control objective in the impacted regulatory item, then you can select the **SOX-GLC-66 Location code/Internal order request interface from SURF to SAP objective** control objective.

</td></tr><tr><td class="sub-head" colspan="2">

Assignment

</td></tr><tr><td>

Assignment Group

</td><td>

Group that is assigned the action task. This field is automatically set to display the assignment group.

</td></tr><tr><td>

Assigned to

</td><td>

User who is assigned the task. This field is automatically set to display the assignee of the task.

</td></tr><tr><td class="sub-head" colspan="2">

Schedule

</td></tr><tr><td>

Due date

</td><td>

Date by which the action task must be complete.

</td></tr><tr><td>

Closed on

</td><td>

Date on which the action tasks is closed.

</td></tr><tr><td class="sub-head" colspan="2">

Additional Details

</td></tr><tr><td>

Title

</td><td>

Title of the regulatory alert

</td></tr><tr><td>

Description

</td><td>

Description of the regulatory alert

</td></tr><tr><td>

Regulatory Task

</td><td>

Unique identification number for the regulatory task. This field is automatically set to display the regulatory task identification number.

</td></tr><tr><td class="sub-head" colspan="2">

Activity Journal

</td></tr><tr><td>

Watch list

</td><td>

List of users who receive notifications about the updates.

</td></tr><tr><td>

Restrict worknotes to

</td><td>

Users to whom you want to restrict the worknotes.

</td></tr><tr><td>

Work notes \(Private\)

</td><td>

Log of the work notes.

</td></tr><tr><td>

Response notes

</td><td>

Displays the response notes.

</td></tr><tr><td class="sub-head" colspan="2">

Attachments

</td></tr><tr><td>

Attachments

</td><td>

Attachments related to the task.

</td></tr></tbody>
</table>5.  In the action tasks form, verify that the mandatory fields are updated.

    The action task is marked for the sn\_compliance.manager or the sn\_risk.manager users.

6.  To save the changes, select **Save**.


## Result

The action task is marked for the users with the sn\_compliance.manager or the sn\_risk.manager roles.

## What to do next

[Complete the action task associated with the alert](create-action-task-src-document-alert.md)

