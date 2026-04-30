---
title: Initiate an ad hoc approval for a legal request or its attachment
description: Initiate an ad hoc approval for a legal request or its attachments from a user or a user group.
locale: en-US
release: zurich
product: Legal Request Management
classification: legal-request-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Work on a legal request, Managing legal requests, Use, Legal Request Management, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Initiate an ad hoc approval for a legal request or its attachment

Initiate an ad hoc approval for a legal request or its attachments from a user or a user group.

## Before you begin

Role required: sn\_lg\_ops.legal\_fulfiller

## About this task

As a collaborator added to a request, you can access and work on the request just as assignees can. However, you can't modify the **Assigned to** and **Assignment group** fields.

Some cases where approvals can be requested for a legal request or its attachment include:

-   Approval for legal contract documents from stakeholders.
-   Ad hoc approval for a legal request that needs an authorization from the privacy team before it can be processed.

You can assign these approvals to any user or user group in your organization who have the legal\_user role. When you initiate an approval, the approvers receive an email notification and can review and act on the approval.

**Note:** If a legal request or attachment already has a pending approval record, you cannot initiate another approval for the same item.

## Procedure

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.

2.  Click the list icon \(![List icon](../image/lsd-lcc-list-icon.png)\).

3.  In the **Lists** tab, open a legal request by selecting an option under **Legal Requests**.

<table id="choicetable_jhj_kb3_gtb"><thead><tr><th align="left" id="d698060e133">

Option

</th><th align="left" id="d698060e136">

Steps

</th></tr></thead><tbody><tr><td id="d698060e142">

**As an assignee**

</td><td>

1.  Select the **Assigned to Me** option.
2.  Select a request to work on.
3.  If the request is newly assigned to you, select **Start Work** to start working on the request.

The state of the legal request is Work in progress and the document is Legal review.

</td></tr><tr><td id="d698060e171">

**As a collaborator**

</td><td>

1.  Select the **Collaborations** option.
2.  Select a request to work on.


</td></tr></tbody>
</table>4.  In the **Approvers** tab, click **Initiate Approval**.

    You can also initiate an approval by clicking the more actions button \(![More actions button icon.](../image/more-button-icon.png)\) and selecting **Initiate Approval**.

5.  On the Initiate Approval dialog box, fill in the fields.

<table id="table_y53_qfp_kjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Approval for

</td><td>

Item that needs an approval.-   **Request**: Get approval for the entire legal request.
-   **Attachment**: Get approval for an attachment in the legal request.


</td></tr><tr><td>

Select attachment

</td><td>

Attachment in the legal request for which approval is required.This field appears only when **Attachment** is selected from **Approval for**.

</td></tr><tr><td>

Select document

</td><td>

Documents attached to the legal request for which approval is required.This field appears only when **Document** is selected from **Approval for**.

**Note:** The Document option in the list appears only when the [external storage option is enabled](associate-categories-practice-area.md) on the intake form of the request type.

</td></tr><tr><td>

Approval by

</td><td>

Approval required at user level or user group level.-   **User**: Get approval from an individual user.
-   **User group**: Get approval from a set of users. The **Select user** field is replaced by the **Select user group** field.


</td></tr><tr><td>

Select user

</td><td>

User or user group who must approve the item.**Note:** Users or user groups with the legal\_user role are listed.

 -   If you selected **User** in the **Approval by** field, select a user from whom the approval is required.
-   If you selected **User group** in the **Approval by** field, select a user group from whom the approval is required.


</td></tr><tr><td>

Approval note

</td><td>

Note for the selected user or user group.

</td></tr></tbody>
</table>6.  Click **Initiate**.


## Result

Assigned approvers are added in the **Approvers** tab based on the following conditions:

-   If you selected **User** in the **Approval by** field, an approval record is created for the selected user.
-   If you selected **User group** in the **Approval by** field, an approval record for each user in the selected user group is created. Anyone from the group can approve.

The assigned approvers get an email notification with a link to open the record for review and action.

**Note:**

-   An attachment cannot be deleted after an ad hoc approval is initiated and is in the Requested state. To remove such attachments, either cancel the ad hoc approval request or obtain the approval first.
-   When you remove an attachment from a legal request, it also deletes the associated ad hoc approval records. A work note is posted with the deletion details in the activity stream of the legal request.

The approval details appear under the **Approvals** tab on the Standard Ticket page.

## What to do next

Approvers can review and [approve or reject the requested item](approve-reject-legal-request-attach.md).

-   **[Cancel an ad hoc approval for a legal request](cancel-approval-legal-request.md)**  
Cancel an ad hoc approval for a legal request if it no longer requires any action.

**Parent Topic:**[Work on a legal request](work-on-legal-request.md)

