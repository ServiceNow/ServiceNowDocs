---
title: Add documents to records
description: Link documents from your workspace, cloud storage, or local drives to authorization packages, boundaries, and engagements. You can organize documents into folders and grant access to other users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/t\_add\_documents\_to\_auth\_package.html
release: australia
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 2
keywords: [authorization package, documents, add documents, link documents]
breadcrumb: [Document reuse across records, Continuous authorization and monitoring tasks in the CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Add documents to records

Link documents from your workspace, cloud storage, or local drives to authorization packages, boundaries, and engagements. You can organize documents into folders and grant access to other users.

## Before you begin

Role required:

-   sn\_irm\_cont\_auth.system\_owner
-   sn\_irm\_cont\_auth.info\_system\_sec\_officer
-   sn\_irm\_cont\_auth.authorization\_official
-   sn\_irm\_cont\_auth.info\_system\_sec\_manager
-   sn\_irm\_cont\_auth.admin
-   sn\_irm\_cont\_auth.information\_owner
-   sn\_irm\_cont\_auth.sec\_control\_assessor
-   sn\_irm\_cont\_auth.system\_user

In general, any role with write access to the record can add, edit, or modify the docs.

**Note:** You can add documents only when the record is in an active state. Inactive records don't allow changes to linked documents.

## About this task

Authorization packages, boundaries, and engagements include a Documents side panel where you can manage all linked documents. You can add documents from workspace sources, external cloud repositories, or create folders to organize documents hierarchically.

## Procedure

1.  Open the record and select the **Documents** icon on the right.

    The **Documents** panel appears only when the record is active.

2.  In the **Documents** panel, select **Select docs/folders**.

    The Select documents dialog box opens, showing available documents and options to browse from different sources.

3.  Select the document source.

    You can browse documents from the following locations:

    1.  All documents: Shows all documents available in your workspace

    2.  Owned by me: Shows only the documents you created

    3.  Shared with me: Shows documents other users have shared with you

    4.  External drive: Shows Google Drive, One Drive, or SharePoint \(when configured by your administrator\)

    5.  Local drive: Local system drives \(when configured\)

4.  Select the document you want to link.

    The document list shows the document name, owner, last modified date, file type, and file size. You can select multiple documents in a single operation.

5.  Select **Add** to link the selected documents to the authorization package.

    The selected documents now appear in the **Documents** panel of the record. You can link the same document to multiple packages.

6.  You can organize documents in the **Documents** panel.

    You can create folders and sub-folders to build a hierarchical structure. Open a folder by double-clicking it. Use the breadcrumb trail at the top to navigate between folder levels.

    1.  To add a folder, select the + icon and select **Create Folder**.

    2.  Enter a name for the folder.

    3.  To add documents into a folder, open the folder and select **Select docs/folders**.

        Documents are now organized within the folder structure. You can navigate the hierarchy using the breadcrumb trail or by double-clicking folders to enter and exit them.

    Documents are successfully linked to your record and appear in the Documents panel. You can now manage permissions, create versions, and set up approval workflows for these documents.


**Parent Topic:**[Document reuse across records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/c_cam_document_management_system.md)

