---
title: Initiate an ad hoc approval for a contract document revision
description: Initiate an ad hoc approval for a contract document revision from a user or a user group.
locale: en-US
release: xanadu
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Non-disclosure agreement legal requests, Use Contract Management Pro for Legal Service Delivery, Contract Management Pro for Legal Service Delivery, Integration of Legal Service Delivery with ServiceNow applications, Legal Service Delivery, Employee Service Management]
---

# Initiate an ad hoc approval for a contract document revision

Initiate an ad hoc approval for a contract document revision from a user or a user group.

## Before you begin

Role required: sn\_lg\_cnt.contract\_fulfiller

## About this task

As a collaborator added to a request, you can access and work on the request just as assignees can. However, you can't modify the **Assigned to** and **Assignment group** fields.

You can assign these approvals to any user or user group in your organization who have the sn\_lg\_cnt.contract\_fulfiller role. When you initiate an approval, the approvers receive an email notification and can review and act on the approval.

**Note:** If a contract document revision already has a pending approval record, you cannot initiate another approval for the same item.

## Procedure

1.  Navigate to **All** &gt; **Legal request** &gt; **Legal Counsel Center**.

2.  Click the list icon \(![List icon](../../legal-request-management/image/lsd-lcc-list-icon.png)\).

3.  In the **Lists** tab, navigate to **Legal Requests** or **Contract Requests**.

<table id="choicetable_jhj_kb3_gtb"><thead><tr><th align="left" id="d471300e110">

Option

</th><th align="left" id="d471300e113">

Steps

</th></tr></thead><tbody><tr><td id="d471300e119">

**As an assignee**

</td><td>

1.  Select the **Assigned to Me** option.
2.  Select a contract request to work on.


</td></tr><tr><td id="d471300e140">

**As a collaborator**

</td><td>

1.  Select the **Collaborations** option.
2.  Select a contract request to work on.


</td></tr></tbody>
</table>4.  If you have opened contract request from the **Legal requests** listing, select **Contract request** tab.

5.  In the **Approvers** tab, click **Initiate Approval**.

    You can also initiate an approval by clicking the more actions button \(![More actions button icon.](../../legal-request-management/image/more-button-icon.png)\) and selecting **Initiate Approval**.

6.  On the Initiate Approval dialog box, fill in the fields.

<table id="table_y53_qfp_kjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Contract type

</td><td>

Contract type for which you need to initiate approval.

</td></tr><tr><td>

Document revision

</td><td>

This field is automatically populated with the latest document revision.

</td></tr><tr><td>

Approval by

</td><td>

Approval required at user level or user group level.-   **User**: Get approval from an individual user.
-   **User group**: Get approval from a set of users. The **Select user** field is replaced by the **Select user group** field.


</td></tr><tr><td>

Select user

</td><td>

User or user group who must approve the item.**Note:** Users or user groups with the sn\_lg\_cnt.contract\_fulfiller role are listed.

 -   If you selected **User** in the **Approval by** field, select a user from whom the approval is required.
-   If you selected **User group** in the **Approval by** field, select a user group from whom the approval is required.


</td></tr><tr><td>

Approval note

</td><td>

Note for the selected user or user group.

</td></tr></tbody>
</table>7.  Click **Initiate**.


## Result

Assigned approvers are added in the **Approvers** tab based on the following conditions:

-   If you selected **User** in the **Approval by** field, an approval record is created for the selected user.
-   If you selected **User group** in the **Approval by** field, an approval record for each user in the selected user group is created. Anyone from the group can approve.

The assigned approvers get an email notification with a link to open the record for review and action.

The approval details appear under the **Approvals** tab on the Standard Ticket page.

**Parent Topic:**[Non-disclosure agreement legal requests](../concept/snlc-request-nda-1.md)

