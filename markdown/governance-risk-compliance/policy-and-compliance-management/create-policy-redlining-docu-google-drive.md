---
title: Create and associate a policy text document in Google Drive
description: Create a policy text document in Google Drive and enable document editing with the approvers, reviewers, and contributors. You can share the document with your stakeholders and collaborate on the document editing in real-time.
locale: en-US
release: yokohama
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Creating and associating policy texts from Cloud documents, Policy authoring and redlining in Compliance Workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Create and associate a policy text document in Google Drive

Create a policy text document in Google Drive and enable document editing with the approvers, reviewers, and contributors. You can share the document with your stakeholders and collaborate on the document editing in real-time.

## Before you begin

Role required: sn\_compliance\_ws.corporate\_compliance\_analyst; mp\_document\_user

**Important:** Google document creation support is enabled from 19.1.1 version of Policy and Compliance Management application

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace**.

2.  In the Compliance Workspace, select the List icon \(![Lists icon.](../../grc-workspace-vrm/image/ws-list-icon.png)\).

3.  Navigate to **Compliance library** &gt; **My policies**.

    You can [create a new policy](../../grc-workspace-compliance/task/create-policy-ws.md) or open a record to enable the redlining feature.

4.  Select a policy to open.

5.  For Google Drive, select a Policy text related list to view the contents of the policy text.

    1.  Select the **Enable document editing** button.

        If the policy is in **Draft** state, then the policy owner can alone create a document or associate a document from Google Drive to enable the policy text for editing by the approvers, reviewers, and contributors.

    2.  To create a document as a policy owner, select **Create new document** in the **Enable document editing** list.

    3.  Copy the shareable folder link from Google Drive and paste it in the **Folder link** field in the Create a document pop-up.

        To get the folder link, right-click the folder in Google Drive, select the ![More actions icon](../../../reuse/icons/product-icons/ellipsis-vertical-outline-24.svg) icon. Select **Share** and **Copy link**.

    4.  Enter the name of the document in the **Document name** field.

    5.  Select the type of document that you want to create in the **Type** field.

        The options are:

        -   Google docs: You can create a Google document in Google Drive when you select this option.
        -   Word: You can create a Microsoft Word document in Google Drive that you can access through a browser and store in Google Drive.
    6.  Select **Create**.

        On selecting create, the document is created in the folder of the Google Drive account that you provided. If you're providing a link to a shared folder, then you must have edit access to create a file within that folder.

    7.  To view the document that is created, select the **Open in Google docs** button.

6.  To view the users that have read or write access to the document, navigate to the Document access related list.

7.  To create another document or connect to a different document for a redlining-enabled policy, select the **Enable document editing** button.

    -   To create another document, select **Create new document** that opens the Create a document pop-up.
    -   To connect to a different document, select **Connect existing document** that opens a Connect existing document pop-up.
8.  To update the content of the document in the **Policy text** field, select the Update link below the document link.

9.  If the policy has been drafted and is complete, the policy owner can request a review by selecting the **Request review** button.

10. Enter a message for the reviewers in the Request review pop-up.

11. Select **Request**.

    As a reviewer, you can view the policy, if ready for review, when you log in to **My pending tasks** in the Tasks view.

12. Select the **Submit review** button.

    You can review the policy text, add a comment in the Submit review pop-up, and submit it.

13. To preview the document and to get the latest update after your collaborators have edited, select the Update link in the **Policy text** tab.

    As a policy owner, you can edit the content of the document in Google Drive to maintain a sync between the document in Cloud and the policy text of the policy.

    All activities between the policy owner and the reviewers are captured in the **Activity** tab of the **Details** related list. If all reviewers have completed the review, then the policy owner can complete the publishing checklist.

14. Select the **Complete publishing checklist** button.

    If all reviews are complete, then as a policy owner you can complete the publishing process. This action creates a playbook. The policy owner must go through the publishing checklist before requesting approval. See, [Complete publishing checklist for the policy and request approval](complete-publishing-checklist-redlining.md).

15. To view the history of the policy, select the Policy history related list.

    For more information, see [View the history of a redlining-enabled policy](view-history-policy-redlining.md).


