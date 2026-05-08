---
title: Initiate an ad hoc approval for a legal matter or its artifact
description: Initiate an ad hoc approval for a legal matter or its artifacts from a user or a user group.
locale: en-US
release: australia
product: Legal Matter Management
classification: legal-matter-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Work on a legal matter, Use, Legal Matter Management, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Initiate an ad hoc approval for a legal matter or its artifact

Initiate an ad hoc approval for a legal matter or its artifacts from a user or a user group.

## Before you begin

Role required: sn\_lg\_ops.legal\_fulfiller

## About this task

Some cases where approvals can be requested for a legal matter or its artifact include:

-   Approval for legal contract documents from stakeholders.
-   Ad hoc approval for a legal matter that needs an authorization from the privacy team before it can be processed.

You can assign these approvals to any user or user group in your organization who have the legal\_user role. When you initiate an approval, the approvers receive an email notification and can review and act on the approval.

**Note:**

-   If a legal matter or artifact already has a pending approval record, you cannot initiate another approval for the same item.
-   Attachments that have an ad hoc approval record in the Requested state cannot be removed from a legal matter. To remove such attachments, either cancel the ad hoc approval request or obtain the approval first.
-   When you remove an attachment from a legal matter, it also deletes the associated ad hoc approval records.

As a collaborator added to a legal matter, you can access and work on the legal matter just as matter owners can. However, you can't modify the **Matter owner**, **Assignment group**, and **Assignment group permission** fields.

## Procedure

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.

2.  In the Legal Counsel Center tab, select the list icon \(![List icon](../../legal-request-management/image/lsd-lcc-list-icon.png)\).

3.  In the **Lists** tab, open a legal matter by selecting an option under **Matters**.

<table id="choicetable_qbl_2bj_gtb"><thead><tr><th align="left" id="d441102e150">

Option

</th><th align="left" id="d441102e153">

Steps

</th></tr></thead><tbody><tr><td id="d441102e159">

**As an assignee**

</td><td>

1.  Select the **Assigned to Me** option.
2.  Select a legal matter to work on.
3.  If the legal matter is newly assigned to you, select **Start** to start working on it.

The state of the legal matter updates to Work in Progress.

</td></tr><tr><td id="d441102e188">

**As a collaborator**

</td><td>

1.  Select the **Collaborations** option.
2.  Select a legal matter to work on.


</td></tr></tbody>
</table>4.  In the **Approvers** tab, click **Initiate Approval**.

    You can also initiate an approval by clicking the more actions button \(![More actions button icon.](../../legal-request-management/image/more-button-icon.png)\) and selecting **Initiate Approval**.

5.  On the Initiate Approval dialog box, fill in the fields.

<table id="table_y53_qfp_kjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Approval for

</td><td>

Item that needs an approval.-   **Matter**: Get approval for the entire legal matter.
-   **Artifact**: Get approval for one or all attachments in an artifact.


</td></tr><tr><td>

Select artifact

</td><td>

Artifact in the legal matter for which approval is required.This field appears only when **Artifact** is selected from **Approval for**.

</td></tr><tr><td>

Select attachment

</td><td>

Attachment in the selected artifact for which approval is required. Choose a specific attachment for approval, or leave the field empty to get approval for all attachments.This field appears only when you select an artifact in the **Select artifact** field.

</td></tr><tr><td>

Select document

</td><td>

Documents attached to the legal matter for which approval is required.This field appears only when **Document** is selected from **Approval for**.

**Note:** The Document option in the list appears only when the [external storage option is enabled](../../legal-request-management/task/associate-categories-practice-area.md) on the intake form.

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
-   If you selected **User group** in the **Approval by** field, select a user group from which the approval is required.
Only users and user groups with sn\_lg\_ops.legal\_user role will be available for selection.

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

If the external storage option is enabled, document in a legal matter artifact are stored in the external storage systems. Based on the approval request, the document access to the approvers is at the matter, artifact, or document level. For more information on document access, see [Document access in a legal matter](../concept/document-access-legal-matter.md).

The assigned approvers get an email notification with a link to open the record for review and action.

**Note:**

-   An attachment cannot be deleted after an ad hoc approval is initiated and is in the Requested state. To remove such attachments, either cancel the ad hoc approval request or obtain the approval first.
-   When you remove an attachment from a legal matter, it also deletes the associated ad hoc approval records. A work note is posted with the deletion details in the Activity stream of the legal matter.

The approval details appear under the **Approvals** tab on the Standard Ticket page.

## What to do next

Approvers can review and [approve or reject the requested item](approve-reject-legal-matter-artif.md).

-   **[Cancel an ad hoc approval for a legal matter](cancel-approval-legal-matter.md)**  
Cancel an ad hoc approval for a legal matter if it no longer requires any action.

**Parent Topic:**[Work on a legal matter](work-on-legal-matter-1.md)

