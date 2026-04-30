---
title: Complete publishing checklist and request policy approval
description: Use the playbook available with Compliance Workspace to complete the publishing checklist before you request approval. If approvals are complete, then the policy is automatically published.
locale: en-US
release: yokohama
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Policy authoring and redlining in Compliance Workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Complete publishing checklist and request policy approval

Use the playbook available with Compliance Workspace to complete the publishing checklist before you request approval. If approvals are complete, then the policy is automatically published.

## Before you begin

Role required: sn\_compliance\_ws.corporate\_compliance\_analyst; mp\_document\_user

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace**.

2.  In the Compliance Workspace, select the list icon \(![Lists icon.](../../grc-workspace-vrm/image/ws-list-icon.png)\).

3.  Navigate to **Compliance library** &gt; **My policies**.

4.  Select the policy publishing checklist icon \(![Publishing checklist icon.](../image/PublishingChecklistIcon.png)\) in the right panel.

    A playbook checklist is created.

5.  Complete the activities as a policy owner in the playbook.

<table id="table_dch_lfb_xsb"><thead><tr><th>

Activity

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Finalize document

</td><td>

Complete the task of accepting or rejecting the track changes and removing open comments. To avoid having internal comments in the published policy and thereafter in the Knowledge Base article, you must clean up the document.1.  Select **Open Document** to open the document and remove the comments.
2.  After the document is auto-saved, select **Mark Complete** to mark the step as complete and to pull the updated content from Microsoft OneDrive, Microsoft SharePoint, or Google Drive account to this section.


</td></tr><tr><td>

Review formatting

</td><td>

Review the formatting of the text in the **Policy text** field before it’s published as Knowledge Base article and select **Mark Complete**.

</td></tr><tr><td>

Review attachments

</td><td>

Review the existing policy attachments and remove documents that are outdated. You can also add new attachments to the policy at this stage.

</td></tr><tr><td>

Attach policy as PDF

</td><td>

Attach the policy document as a PDF to the Knowledge Base article. Attaching a PDF is recommended if your Microsoft OneDrive, Microsoft SharePoint, or Google Drive document and the **Policy text** field aren’t in sync.1.  Select **Attach** to append the PDF to the policy.
2.  Select **Mark Complete**.
**Note:** Starting with the Xanadu release you can also generate accessible PDFs. In order to generate an accessible PDF you must set the property **com.snc.document.conversion.accessibility\_enabled** to true. To enable the property, see [Enable accessibility features for DOCX to PDF conversion](https://www.servicenow.com/docs/access?context=enable-accessibility-docx-to-pdf&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Review Publishing settings

</td><td>

Refresh the browser after completing this step. Update the policy Knowledge base and the Policy template fields if necessary, and mark the step as complete.

</td></tr></tbody>
</table>    The **Complete publishing checklist** button is no longer available.

6.  To view your attachments, select ![Attachment icon.](../../../common/image/AttachmentIcon.png) in the right panel.

7.  Select the **Request approval** button to request approval for the policy.

8.  Select **Approvers** in the Request approval pop-up.

9.  Select **Request**.

    The policy moves to the **Awaiting approval** state.

    The policy approver can view the policy by navigating to the Approvals related list of the policy. Based on the approver's action, the policy either gets approved or rejected. If rejected, the policy moves back to the Draft state.

10. To edit a published policy, select the **Edit policy** button.


