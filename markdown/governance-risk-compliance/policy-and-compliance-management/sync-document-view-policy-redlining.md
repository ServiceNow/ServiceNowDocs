---
title: Sync document and view policy text
description: Update the document and view the content in the Policy text field.
locale: en-US
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Policy authoring and redlining in Compliance Workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Sync document and view policy text

Update the document and view the content in the Policy text field.

## Before you begin

Role required: sn\_compliance\_ws.corporate\_compliance\_analyst; mp\_document\_user

## About this task

Contextually, Cloud refers to documents that reside in Microsoft OneDrive, Microsoft SharePoint and Google Drive.

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace**.

2.  In the Compliance Workspace, select the List icon \(![](../../grc-cam-workspace/image/ws-list-icon.png)\).

3.  Navigate to **Compliance library** &gt; **My policies**.

4.  Select a policy to open.

5.  Select the **Policy text** tab to view the contents of the policy.

6.  Select **Update**.

    The **Policy text** field is updated with the latest content from the document.

    As there are many collaborators on the policy, you must update the content to get the latest update. Last sync information helps you to know when the document was last synced.

    **Note:** If the document size exceeds 10 MB, then you can’t fetch the latest document to view its latest content in policy text tab.

7.  To open the content, select the document link next to **Sync with** in the **Policy text** field or select the **Open in Word** button in case of Microsoft OneDrive or the **Open in Google docs** button in case of Google Drive.

    -   The **Sync with** Word action is enabled or disabled by default for all the policy records that are redlining enabled based on the value in **Enable redlining document text sync by default** property that is set to **true** by the base system.

        You can opt to enable or disable sync at the individual policy level by selecting the sync toggle in the Policy text tab of the policy record.

    -   If you enable **Sync with**, then the document cannot be simultaneously edited both in the Cloud and in the **Policy text** field. The content can be updated in the Cloud and can be pulled into the **Policy text** field.
    -   If you disable Sync with, then your policy text document content is disconnected from the Cloud document and you can edit the content independently. You can save this content by selecting the **Save** button.

        In the disconnected state, if one of the reviewers had updated the policy text and logging in as a policy owner if you select the **Complete publishing checklist**, then the **Attach policy as PDF** becomes a required step to attach the PDF.

        You must manually remove the previous policy attachments, if any, and confirm before you attach the current policy as a PDF in the playbook.

    You can also view the policy text in the Details related list. If you update the policy text in the Details related list, then the policy text is automatically updated in the **Policy text** field of the Policy text related list.

    -   **For a policy that is redlining enabled or not**
        -   If you are a compliance user and if the policy is in the draft state, then you can edit the policy text.
        -   If you are an owner or a reviewer and if the policy is in the review state, then you can edit the policy text.
    -   **For redlining-enabled policy**

        In addition to the preceding conditions, you can also edit the policy text for a final review and correction after you complete the publishing checklist and before requesting approval and publishing.

    You can then complete the publishing checklist, request approval, and publish the policy.


