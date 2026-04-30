---
title: Manage regulatory change tasks
description: Manage the regulatory change tasks that are associated with the regulatory event alert. When a business entity owner completes the impact assessment on the regulatory event alert, the user with the sn\_grc\_reg\_change.user role reviews the assessment summary and marks the alert as applicable.
locale: en-US
release: zurich
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Manage regulatory tasks, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Manage regulatory change tasks

Manage the regulatory change tasks that are associated with the regulatory event alert. When a business entity owner completes the impact assessment on the regulatory event alert, the user with the sn\_grc\_reg\_change.user role reviews the assessment summary and marks the alert as applicable.

## Before you begin

Role required: sn\_grc\_reg\_change.manager, sn\_grc\_reg\_change.user

## About this task

The coordinator of the regulatory event alert identifies the steps to comply with the regulatory change and manages the regulatory change task.

## Procedure

1.  Navigate to **All** &gt; **Regulatory Change Management application** &gt; **Compliance Workspace**.

    The Regulatory Change Management application in the Compliance Workspace is displayed.

2.  Navigate to **Lists** &gt; **Regulatory Alerts** view.

3.  Select the regulatory event alert for which a business entity owner has completed the assessment.

4.  Review the impact assessment and mark the alert using one of the following options.

<table id="choicetable_utb_d4n_brb"><thead><tr><th align="left" id="d33039e110">

Field

</th><th align="left" id="d33039e113">

Description

</th></tr></thead><tbody><tr><td id="d33039e119">

**Applicable**

</td><td>

Mark the alert as applicable. After marking the regulatory event alert as **Applicable**, a new regulatory change task is automatically created in the Regulatory Tasks related list in the regulatory alert UI page.

</td></tr><tr><td id="d33039e131">

**Not applicable**

</td><td>

Mark the alert as not applicable.

 When you mark the alert as not applicable, a message window displays. Select one of the following reasons in the **Reasons** list and select **Submit**:

-   No action required on the alert
-   Duplicate alert
-   Other
As a result of this action, the stepper component displays the alert stage as **Completed**.

</td></tr><tr><td id="d33039e167">

**Cancel regulatory alert**

</td><td>

Cancel the regulatory alert.

</td></tr><tr><td id="d33039e176">

**Defer**

</td><td>

Defer the alert to a later date.

</td></tr></tbody>
</table>5.  For the applicable alert, select the **Regulatory Tasks** related list and select the regulatory change task that is created automatically for the alert.

6.  In the Details tab, fill in the form.

<table id="table_qb1_rgw_xmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Regulatory Change Task

</td></tr><tr><td>

Regulatory alert

</td><td>

Title of the regulatory alert associated with the source document import task. This field is automatically set to display the title of the alert.

</td></tr><tr><td>

Instructions

</td><td>

Instructions related to the source document import task.

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

User to whom the regulatory change is assigned.

</td></tr><tr><td>

Approver

</td><td>

If the approver type is a group, the **Approver group** field is displayed.

</td></tr><tr><td>

Approver group

</td><td>

If the approver type is a user, the **Approver** field is displayed.

</td></tr><tr><td class="sub-head" colspan="2">

Schedule

</td></tr><tr><td>

Due date

</td><td>

Due date for the source document or regulatory event alert import task.

</td></tr><tr><td>

Approved on

</td><td>

Date when the source document import task is approved. This field is automatically set to display the approval date.

</td></tr><tr><td class="sub-head" colspan="2">

Activity Journal

</td></tr><tr><td>

Watchlist

</td><td>

Users whom you want to add as watchers for this task.

</td></tr><tr><td>

Work notes list

</td><td>

Users who have added the work notes for this task.

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

Activity and state of the task.

</td></tr><tr><td class="sub-head" colspan="2">

Attachments

</td></tr><tr><td>

Attachments

</td><td>

Attachments related to the task.

</td></tr></tbody>
</table>7.  Verify that the mandatory fields such as **Approver**, **Assigned to**, and **Due date** are updated.

8.  Select **Respond**.

    The **Respond** action triggers the impact radius calculation in the background. For information on impact radius calculation, see [Impact radius for regulatory alerts of type regulatory event](../../grc-rcm/concept/impact-calculation-approval.md). The regulatory change task is updated with the **Responded** state.

9.  Add an action task if necessary.

    See [Create a new action task for the alert](create-action-task-using-ws.md) for creating an action task.

10. Add issues if necessary.

    See [Create or add an issue related to a regulatory task](create-an-issue-reg-change-comp-ws.md) for more information.

11. After creating necessary action tasks and issues, select **Request Approval**.

    Depending on the state of the approval, the action task is activated. When the action task is closed, the associated source document import task is automatically closed.


## Result

Verify that the regulatory change task is updated with the **Responded** state and the Action tasks related list is displayed for the regulatory event alert.

## What to do next

[Create a new action task for the alert](create-action-task-using-ws.md)

