---
title: Connect an existing document from Google Drive to policy
description: Connect a document that exists in your Google Drive folder to a policy that you created. Use this existing document and enable redlining in the policy text instead of creating a document.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/policy-and-compliance-management/connect-google-drive-doc.html
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create and associate a policy text document in Google Drive, Creating and associating policy texts from Cloud documents, Policy authoring and redlining in Compliance Workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Connect an existing document from Google Drive to policy

Connect a document that exists in your Google Drive folder to a policy that you created. Use this existing document and enable redlining in the policy text instead of creating a document.

## Before you begin

Role required: sn\_compliance\_ws.corporate\_compliance\_analyst, mp\_document\_user

**Important:** Starting from version 19.1.1 Google documents are supported in the connect document policy.

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace**.

2.  In the Compliance Workspace, select the List icon \(\[Omitted image "ws-list-icon.png"\] Alt text: Lists icon.\).

3.  Navigate to **Compliance library** &gt; **My policies**.

4.  Select a policy.

5.  Select a Policy text related list to view the contents of the policy.

    If you already have a document on Google Drive with content in it, which you want to associate with the policy, then you can associate that document.

6.  To connect a document that is in your Google Drive folder.

    1.  Navigate to My Drive in [https://drive.google.com/](https://drive.google.com/)

        You can also connect documents stored in a Shared Drive. Navigate to the Shared Drive where the document resides, locate the document, and copy the link in the same way as for My Drive documents.

    2.  Select the document that you want to connect to the policy.

    3.  Select the More actions icon \(\[Omitted image "ellipsis-vertical-fill-24.svg"\] Alt text: More actions icon.\) in the document that you want to connect.

    4.  Select the **Copy link** option from the **Share** list.

7.  Navigate back to the Policy text tab of the policy record.

8.  Select the **Enable document editing** list.

    The policy must be in **Draft** state, only then the policy owner can associate a document from Google Drive to enable the policy text for the approvers, reviewers, and contributors to edit.

9.  Paste the copied Google Drive in the **File link** field of the Connect existing document pop-up.

10. Select **Connect**.

    1.  If personal authentication is enabled, an authentication prompt appears requesting that you select and authenticate with your Google account. Unlike SharePoint, Google Drive does not automatically pick your logged-in session. You must explicitly select the account you want to use from the account picker.
    2.  Google Drive requires two separate authentication steps: first for Google Drive access, and then for Google Docs access. Complete both authentication prompts and grant the requested permissions for each.
    3.  After both authentications are complete, the document is linked to the policy record and registered under your personal account identity.
    4.  You should be able to connect the document from the Google Drive to the policy record.

        **Note:** However, you can’t connect a Google document if it exceeds 10 MB.

    5.  The access on any previously linked document is removed and access on the newly connected document is granted. Because document access updates run asynchronously, there may be a short delay before the updated access is reflected.
11. Select **Update**.

    The Policy text field displays the text from the Google Drive document in the ServiceNow policy record.

    For more information on Google Drive Integration for Policy authoring and redlining, see the [Google Drive Integration for Policy authoring and redlining – General guidelines and Known limitations \[KB1587198\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1587198) article in the Now Support Knowledge Base.


