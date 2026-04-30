---
title: Manage the regulatory change tasks
description: Manage the regulatory action tasks in the Regulatory Change Tasks module so that you can use these tasks to identify and comply with the regulatory changes.
locale: en-US
release: yokohama
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Regulatory change tasks, Regulatory Change Management Core UI, Use, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Manage the regulatory change tasks

Manage the regulatory action tasks in the Regulatory Change Tasks module so that you can use these tasks to identify and comply with the regulatory changes.

## Before you begin

Role required: sn\_grc\_reg\_change.manager, sn\_grc\_reg\_change.user, or sn\_grc\_reg\_change.admin

## About this task

Regulatory change tasks are automatically created whenever a regulatory event alert is marked as applicable after the applicability assessment. Regulatory Compliance team members craft an action plan to identify the changes that need to be implemented so that your organization complies with the regulatory change.

## Procedure

1.  Navigate to **All** &gt; **Application** &gt; **Regulatory Change Management** &gt; **Regulatory Change Tasks**.

2.  Select a regulatory change task.

3.  On the form, fill in the fields.

<table id="table_gxj_bv1_xmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assignment group

</td><td>

Assignment group of the task. The group is selected from the Group Hierarchy table.

</td></tr><tr><td>

Assigned to

</td><td>

Name of the user who is assigned the task.

</td></tr><tr><td>

Approver type

</td><td>

User or group who approves the task.

</td></tr><tr><td>

Approver

</td><td>

Approver of the regulatory change task. When the approver type is Group, the request is sent to the group members.

</td></tr><tr><td>

Due date

</td><td>

Due date for the regulatory change task.

</td></tr><tr><td>

Approved on

</td><td>

Date when the regulatory change task is approved.

</td></tr><tr><td>

Regulatory alert

</td><td>

Name of the regulatory alert.

</td></tr><tr><td>

Instructions

</td><td>

Instructions for the task.

</td></tr><tr><td>

Watch list

</td><td>

Watch list to add interested users.

</td></tr><tr><td>

Worknotes list

</td><td>

Users interested in the work notes.

</td></tr><tr><td>

Work notes

</td><td>

Log of the work notes.

</td></tr><tr><td>

Activities

</td><td>

Log of the activities.

</td></tr><tr><td class="sub-head" colspan="2">

Related list

</td></tr><tr><td>

Action Tasks

</td><td>

Regulatory action tasks. Select **New** to create a regulatory action task in response to the regulatory change task.**Note:**

If there are regulatory action tasks that are in progress when the parent regulatory task is closed manually, all the associated regulatory action tasks are moved to the Cancelled state with the following warning message: `Action tasks for this Regulatory Change Task/Document Import Task are in-progress. Selecting OK will cancel them. Do you want to proceed?`

If there are no regulatory action tasks associated or if the regulatory action tasks are closed, the following message is displayed: `Are you sure you want to close this task? Select OK to close the task.`

</td></tr><tr><td>

Issues

</td><td>

Issues observed during the regulatory change workflow or source document workflow.

</td></tr><tr><td>

Approvers

</td><td>

Approval records that get created when an approval is requested.

</td></tr></tbody>
</table>4.  Select **Update**.

5.  If you want to add new action tasks that are related to the regulatory change task, select **New** in the Action Tasks related list.

6.  To request an approval on the regulatory change task, log in as an approver and select **Request Approval** to request an approval.

    The state of the regulatory change task is updated to the **Awaiting Approval** state. In the Approvers related list of the regulatory change task, the state of the approval is updated to **Requested**. The manager with the sn\_grc\_reg\_change.manager role, the user with the sn\_grc\_reg\_change.user role, or the admin user with the sn\_grc\_reg\_change.admin role can view the request in **My Approvals** of the regulatory change tasks.

7.  Select **Approve** to approve the request.


## Result

The request is approved. The regulatory change task moves to the Implementation state. When the action task associated with the regulatory change task is completed, the regulatory change task is closed.

**Parent Topic:**[Regulatory change tasks](../concept/reg-change-task.md)

