---
title: Use the Apply Change Approval Policy flow action
description: Apply your change approval policy in the Change Management Workflow Studio action to control the approval process for a change request. You can create user and group approvals according to a change approval policy record.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Creating change approval policies, Use, Change Management, IT Service Management]
---

# Use the Apply Change Approval Policy flow action

Apply your change approval policy in the Change Management Workflow Studio action to control the approval process for a change request. You can create user and group approvals according to a change approval policy record.

## Before you begin

Role required: admin

## About this task

This flow action uses the **Ask For Approval** flow action to apply approvals that are derived from the Change approval policy. For more information on how to configure approval policies, see [Create approval definitions](create-approval-definitions.md).

When approvals are being generated, the **Ask For Approval** action avoids generating more than one approval for the same user. For example, if the policy requires approval from two groups and both groups have the same user, then the shared user is notified only once for the approval.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer** &gt; **Flows**.

2.  Select the flow that you want to apply the change approval policy to.

3.  Select **Action** &gt; **Installed Spokes** &gt; **ITSM** &gt; **Change** &gt; **Apply Change Approval Policy**.

4.  On the form, fill in the fields:

<table id="table_eym_pgy_f4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Action Label

</td><td>

Unique label for the action.

</td></tr><tr><td>

Policy \[Change Approval Policy\]

</td><td>

Policy that you want to apply to your Change request.

</td></tr><tr><td>

Change Request

</td><td>

Source of the change request required by the policy. Select this field using the data pill picker icon \( ![data pill picker icon.](../image/data_pill_picker.png)\). Alternatively, you can select the change request from the Change Request list.

</td></tr><tr><td>

Due Date

</td><td>

Due date for the approval policy. Select one of the following options:-   **None**: The approval has no due date.
-   **Approve**: Automatically approve the approval policy on the due date.
-   **Reject**: Automatically reject the approval policy on the due date.
-   **Cancel**: Automatically cancel the approval policy on the due date.


</td></tr></tbody>
</table>5.  Click **Submit**.


**Parent Topic:**[Creating change approval policies](../concept/using-change-approval-policies-cf.md)

