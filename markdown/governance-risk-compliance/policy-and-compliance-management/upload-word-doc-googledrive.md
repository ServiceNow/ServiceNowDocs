---
title: Upload a Microsoft Word document to Google Drive
description: Upload a Microsoft Word document that exists in your local machine to Google Drive and link the document with the policy. As a user, you can access the document from any device and enable multiple users to collaborate on the policy document.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/policy-and-compliance-management/upload-word-doc-googledrive.html
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create and associate a policy text document in Google Drive, Creating and associating policy texts from Cloud documents, Policy authoring and redlining in Compliance Workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Upload a Microsoft Word document to Google Drive

Upload a Microsoft Word document that exists in your local machine to Google Drive and link the document with the policy. As a user, you can access the document from any device and enable multiple users to collaborate on the policy document.

## Before you begin

Role required: sn\_compliance\_ws.corporate\_compliance\_analyst; mp\_document\_user

**Note:** Verify that you have set up the pre-requisite steps appropriately to upload the Microsoft Word document to cloud. For more information, see [Pre-requisites to enable policy redlining feature](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/policy-and-compliance-management/pre-req-policy-redlining.md).

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace**.

2.  In the Compliance Workspace, select the \[Omitted image "ws-list-icon.png"\] Alt text: List icon icon.

3.  Navigate to **Compliance library** &gt; **My policies**.

4.  Select a policy and select the Policy text related list.

    You can upload a Microsoft Word document that exists locally in your machine.

5.  To upload a Microsoft Word document that exists in your local machine to the Google Drive, and attach it to the policy, select the **Enable document editing** button.

6.  Select the **Upload a document** option.

7.  Enter the shareable link of the folder from Google Drive where the document must be uploaded in the **Folder link** field.

    You can upload to a folder in My Drive or in a Shared Drive. To get the folder link for a Shared Drive folder, navigate to the folder in the Shared Drive, right-click the folder, select Share, and copy the link.

8.  Select the **File type** field and click to choose a Google document or Microsoft Word document that you want to upload in the Google Drive.

    \[Omitted image "upload-doc-google-pc.png"\] Alt text: Upload a document to Google Drive to be attached to a policy.

    -   Google Docs: Upload as a Google document in Google Drive.
    -   Word: Upload as a Microsoft Word document in Google Drive.
9.  Select the Add File link to browse and open the document that exists in your local machine.

    The name of the Microsoft Word document defaults as the **Title** of the file in the Upload a file pop-up. If necessary, you can change the name of the file in the **Title** field.

    **Note:** You can upload only one file at a time to the folder.

10. After you have selected the file as an attachment, select **Upload**.

    1.  If personal authentication is enabled, an authentication prompt appears requesting that you select and authenticate with your Google account. Unlike SharePoint, Google Drive does not automatically pick your logged-in session. You must explicitly select the account you want to use from the account picker.
    2.  Google Drive requires two separate authentication steps: first for Google Drive access, and then for Google Docs access. Complete both authentication prompts and grant the requested permissions for each.
11. After the file is attached, select **Upload**.

    The selected file is uploaded to the Google Drive folder link that you'd specified. The document is registered in Google Drive under your personal account identity.


