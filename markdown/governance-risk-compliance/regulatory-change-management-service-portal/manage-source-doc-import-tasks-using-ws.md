---
title: Manage a source document import task
description: Manage the source document import tasks that are associated with the source document alerts. When a source document alert is marked as applicable, a source import document task is created automatically.
locale: en-US
release: yokohama
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Manage regulatory tasks, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Manage a source document import task

Manage the source document import tasks that are associated with the source document alerts. When a source document alert is marked as applicable, a source import document task is created automatically.

## Before you begin

Role required: sn\_grc\_reg\_change.manager, sn\_grc\_reg\_change.user

## About this task

A source document import task is used to ingest a particular source document that is received from the provider into the regulatory library.

## Procedure

1.  Navigate to **All** &gt; **Regulatory Change Management application** &gt; **Compliance Workspace**.

    The Regulatory Change Management application in the Compliance Workspace is displayed.

2.  Navigate to **Lists** &gt; **Regulatory Alerts** view.

3.  Select the source document alert that you assessed previously and select the import document task.

4.  In the Details tab, fill in the form.

<table id="table_qb1_rgw_xmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Import Document Task

</td></tr><tr><td>

Regulatory alert

</td><td>

Title of the regulatory alert associated with the import document task. This field is automatically set to display the alert title.

</td></tr><tr><td>

Instructions

</td><td>

Instructions related to the import document task.

</td></tr><tr><td class="sub-head" colspan="2">

Assignment

</td></tr><tr><td>

Assignment group

</td><td>

Assignment group for the record. The group is selected from the **Group Hierarchy** table.

</td></tr><tr><td>

Approver type

</td><td>

Approver type for the task. Choices are as follows:-   **User**
-   **Group**


</td></tr><tr><td>

Assigned to

</td><td>

User to which the task is assigned.

</td></tr><tr><td>

Approver or Approver group

</td><td>

If the approver type is a group, the **Approver group** field is displayed.

 If the approver type is a user, the **Approver** field is displayed.

</td></tr><tr><td class="sub-head" colspan="2">

Schedule

</td></tr><tr><td>

Due date

</td><td>

Due date for the source document import task.

</td></tr><tr><td>

Approved on

</td><td>

Date when the source document import task is approved. This field is automatically set to display the approval date.

</td></tr><tr><td class="sub-head" colspan="2">

Activity Journal

</td></tr><tr><td>

Watchlist

</td><td>

Users that are in the watchlist for this task.

</td></tr><tr><td>

Work notes list

</td><td>

Users that are in the work notes for this task.

</td></tr><tr><td>

Work notes \(Private\)

</td><td>

Work notes related to the task.

</td></tr><tr><td class="sub-head" colspan="2">

Compose

</td></tr><tr><td>

Worknotes

</td><td>

Worknotes typed in by the users. These work notes can be posted for reference.

</td></tr><tr><td class="sub-head" colspan="2">

Activity

</td></tr><tr><td>

Activity

</td><td>

Shows the activity and state of the task. Auto-populated field.

</td></tr><tr><td class="sub-head" colspan="2">

Attachments

</td></tr><tr><td>

Attachments

</td><td>

Attachments related to the task.

</td></tr></tbody>
</table>5.  Verify that the **Assigned to**, **Approver**, and **Due date** fields are updated.

6.  To save the changes, select **Save**.

7.  To update the selected source document import task, select **Work in progress**.

8.  Navigate to the Action tasks related list and add an action task if necessary.

    See [Create a new action task for the alert](create-action-task-using-ws.md) for creating a new action task.

9.  Navigate to the Issues related list and add an issue if necessary.

    See [Create or add an issue related to a regulatory task](create-an-issue-reg-change-comp-ws.md) for adding an issue.

10. In the Import Task section, insert a new citation or update an existing citation as described in the table.

<table id="choicetable_sdj_byp_crb"><thead><tr><th align="left" id="d304955e407">

Field

</th><th align="left" id="d304955e410">

Description

</th></tr></thead><tbody><tr><td id="d304955e416">

**Insert action**

</td><td>

Action associated with the citation. Select **Insert** to insert a new citation.**Note:** The **Insert** or **Update** action related to the citation is available only when the source document import task is in the **In progress** state.

</td></tr><tr><td id="d304955e440">

**Create under an existing Authority Document or Citation**

</td><td>

Option to create a new citation under an existing authority document or citation. When this option is selected, a child authority document or a child citation is created under an existing citation. This option is displayed only when the **Insert** action is selected.

</td></tr><tr><td id="d304955e452">

**Parent type**

</td><td>

Parent authority document or citation. This field is displayed only when the **Create under an existing Authority Document or Citation** option is enabled.

</td></tr><tr><td id="d304955e464">

**Parent authority document**

</td><td>

Parent authority document or citation from the library. This field is displayed only when the **Create under an existing Authority Document or Citation** option is enabled.

</td></tr><tr><td id="d304955e477">

**Update action**

</td><td>

Action associated with the citation. Select **Update** and add the citation in the **Target citation** field to update an existing citation.

</td></tr></tbody>
</table>11. Select **Request Approval**.


## Result

The state of the source document import task is updated to **Awaiting Approval**. Depending on the state of the approval, the action task is activated.

## What to do next

See [Create a new action task for the alert](create-action-task-using-ws.md) and [Complete the action task associated with the alert](create-action-task-src-document-alert.md) for information on creating a new action task and completing an action task associated with the alert.

