---
title: Use the Apply Change Approval Policy flow action
description: Apply your change approval policy in the Change Management Workflow Studio action to control the approval process for a change request. You can create user and group approvals according to a change approval policy record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-service-management/change-management/use-apply-change-approval-policy-flow-activity.html
release: yokohama
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Creating change approval policies, Using Change Management, Change Management, IT Service Management]
---

# Use the Apply Change Approval Policy flow action

Apply your change approval policy in the Change Management Workflow Studio action to control the approval process for a change request. You can create user and group approvals according to a change approval policy record.

## Before you begin

Role required: admin

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

Source of the change request required by the policy. Select this field using the data pill picker icon \( \[Omitted image "data\_pill\_picker.png"\] Alt text: data pill picker icon.\). Alternatively, you can select the change request from the Change Request list.

</td></tr><tr><td>

Due Date

</td><td>

Due date for the approval policy. Select one of the following options:-   **None**: The approval has no due date.
-   **Approve**: Automatically approve the approval policy on the due date.
-   **Reject**: Automatically reject the approval policy on the due date.
-   **Cancel**: Automatically cancel the approval policy on the due date.


</td></tr></tbody>
</table>5.  Select **Submit**.


**Parent Topic:**[Creating change approval policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-service-management/change-management/using-change-approval-policies-cf.md)

