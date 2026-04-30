---
title: Connect an existing document from Google Drive to policy
description: Connect a document that exists in your Google Drive folder to a policy that you created. Use this existing document and enable redlining in the policy text instead of creating a document.
locale: en-US
release: xanadu
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create and associate a policy text document in Google Drive, Creating and associating policy texts from Cloud documents, Policy authoring and redlining in Compliance Workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Connect an existing document from Google Drive to policy

Connect a document that exists in your Google Drive folder to a policy that you created. Use this existing document and enable redlining in the policy text instead of creating a document.

## Before you begin

Role required: sn\_compliance\_ws.corporate\_compliance\_analyst; mp\_document\_user

**Important:** Starting from version 19.1.1 Google documents are supported in the connect document policy.

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace**.

2.  In the Compliance Workspace, select the List icon \(![Lists icon.](../../grc-workspace-vrm/image/ws-list-icon.png)\).

3.  Navigate to **Compliance library** &gt; **My policies**.

4.  Select a policy.

5.  Select a Policy text related list to view the contents of the policy.

    If you already have a document on Google Drive with content in it, which you want to associate with the policy, then you can associate that document.

6.  To connect a document that is in your Google Drive folder.

    1.  Navigate to My Drive in [https://drive.google.com/](https://drive.google.com/)

    2.  Select the document that you want to connect to the policy.

    3.  Select the More actions icon \(![More actions icon.](../../../reuse/icons/product-icons/ellipsis-vertical-fill-24.svg)\) in the document that you want to connect.

    4.  Select the **Copy link** option from the **Share** list.

7.  Navigate back to the Policy text tab of the policy record.

8.  Select the **Enable document editing** list.

    The policy must be in **Draft** state, only then the policy owner can associate a document from Google Drive to enable the policy text for the approvers, reviewers, and contributors to edit.

9.  Paste the copied Google Drive in the **File link** field of the Connect existing document pop-up.

10. Select **Connect**.

    You should be able to connect the document from the Google Drive to the policy record.

    **Note:** However, you can’t connect a Google document if it exceeds 10 MB.

11. Select **Update**.

    The Policy text field displays the text from the Google Drive document in the ServiceNow policy record.

    For more information on Google Drive Integration for Policy authoring and redlining, see the [Google Drive Integration for Policy authoring and redlining – General guidelines and Known limitations \[KB1587198\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1587198) article in the Now Support Knowledge Base.


