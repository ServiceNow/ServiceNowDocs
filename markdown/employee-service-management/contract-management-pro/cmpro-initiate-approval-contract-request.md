---
title: Initiate an ad hoc approval for a contract document revision
description: Initiate an ad hoc approval for a contract document revision from a user or a user group.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Initiate an ad hoc approval for a contract document revision

Initiate an ad hoc approval for a contract document revision from a user or a user group.

## Before you begin

Role required: sn\_cm\_core.contract\_fulfiller

## About this task

You can request for approval of a revision for contract documents from stakeholders. Here is how the flow works:

-   You can assign the approvals to a user or user group in your organization. Users with the group manager or contract fulfiller roles who are in the **assigned to** or **collaborator** fields can raise the approval for the revision.
-   When you initiate an approval, the approvers receive an email notification and can act on the approval.
-   An approver who does not have access to the contract revision is granted read-only access to the record until the assigned approval record is completed.

**Note:** Only latest revision of specific contract type is sent for approval. If an approval of specific revision is pending, you cannot initiate another approval for the same.

## Procedure

1.  Navigate to your workspace.

2.  Click the list icon \(![List icon](../../legal-request-management/image/lsd-lcc-list-icon.png)\).

3.  In the **Lists** tab, open a request by selecting an option under **Contract Requests**.

<table id="choicetable_jhj_kb3_gtb"><thead><tr><th align="left" id="d87121e106">

Option

</th><th align="left" id="d87121e109">

Steps

</th></tr></thead><tbody><tr><td id="d87121e115">

**As an assignee**

</td><td>

1.  Select the **Assigned to Me** option.
2.  Select a request to work on.
3.  If the request is newly assigned to you, select **Start** to start working on the request.

The state of the request is Work in progress and the contract status is also work in progress.

</td></tr><tr><td id="d87121e144">

**As a collaborator**

</td><td>

1.  Select the **Collaborations** option.
2.  Select a request to work on.


</td></tr></tbody>
</table>4.  In the **Approvers** tab, click **Initiate Approval**.

    You can also initiate an approval by clicking the more actions button \(![More actions button icon.](../../legal-request-management/image/more-button-icon.png)\) and selecting **Initiate Approval**.

5.  On the Initiate Approval dialog box, fill in the fields.

<table id="table_y53_qfp_kjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Contract type

</td><td>

From the drop-down list, select only one category of the contract type, for example, **Order Form**.

**Note:** When you have only one contract type, then it is auto-populated.

</td></tr><tr><td>

Document revision

</td><td>

The latest revision of the document . For example `Order Form - 1.0`. The number reflects the latest document revision. The revision number is visible from the Approving field. **Note:** The revision number of the latest document is one higher than the previous revision number.

</td></tr><tr><td>

Approval by

</td><td>

Approval required at user level or user group level.-   **User**: Get approval from an individual user.
-   **User group**: Get approval from a set of users. The **Select user** field is replaced by the **Select user group** field.


</td></tr><tr><td>

Select user

</td><td>

User or user group who must approve the item. If you selected **User** in the **Approval by** field, select a user from whom the approval is required.**Note:** If you selected **User** in the **Approval by** field, an approval record is created for the selected user.

</td></tr><tr><td>

Select user group

</td><td>

User or user group who must approve the item. If you selected **User group** in the **Approval by** field, select a user group from whom the approval is required.**Note:** If you selected **User group** in the **Approval by** field, an approval record for each user in the selected user group is created. Anyone from the group can approve.

</td></tr><tr><td>

Approval note

</td><td>

Note for the selected user or user group.

</td></tr></tbody>
</table>6.  Click **Initiate**.

    All the approval records are listed and the approval status changes to **Requested**.


## Result

Assigned approvers are added in the **Approvers** tab with other approval details. The assigned approvers get an email notification with a link to open the record for action.

**Note:** The contract type revision number is visible from the Approving field of the **Approvers** tab.

## What to do next

Approvers can view and [Approve or reject a contract document](cmpro-approve-reject-request-docs.md).

-   **[Approve or reject a contract document](cmpro-approve-reject-request-docs.md)**  
Review a contract request or attachment and approve or reject it.
-   **[Cancel an ad hoc approval for a contract document revision](cmpro-cancel-approval-request.md)**  
Cancel an ad hoc approval for a contract document revision if it no longer requires any action.

**Parent Topic:**[Using Contract Management Pro](../concept/cncore-use-cmpro.md)

