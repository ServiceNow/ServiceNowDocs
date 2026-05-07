---
title: Document Management in Workspace
description: With Document Management in workspaces you can organize documents into folders, manage document versions, control sharing permissions, and attach files from multiple sources to any ticket or record. The Documents component appears in the side panel of workspace record views and provides a centralized location for managing documents associated with a specific record.
locale: en-US
release: australia
product: Document Management Services
classification: document-management-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use, Document Management, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Document Management in Workspace

With Document Management in workspaces you can organize documents into folders, manage document versions, control sharing permissions, and attach files from multiple sources to any ticket or record. The Documents component appears in the side panel of workspace record views and provides a centralized location for managing documents associated with a specific record.

The Document Management component embeds a unified document workspace directly in the left-hand panel of the workspace view, giving you full access to your documents within the context of a record. You can search and browse documents and folders, upload new files, manage versions, adjust sharing permissions, rename, download, delete, and send documents for approval or review without leaving the record page.

## Document Management Component

The Document Management component is a panel that appears within a ticket or record and provides a central location for managing documents, folders, sharing permissions, and document versions.

**Note:** The Document Managementcomponent is visible only if it's configured in the Workspace.

From the Document Management component, you can search for documents within the ticket, select documents, view documents and folders organized in the Documents panel, track and create document versions, manage sharing permissions by role, user, group, or user criteria, rename, download, or delete documents, and submit documents for approval or review.

## Adding documents to a record

You can attach documents to a record page from a variety of sources. You can:

-   Link documents that already exist within ServiceNow, without creating duplicate copies.
-   Upload documents from an external provider such as Google Drive, OneDrive, or SharePoint to ServiceNow .
-   Upload a local copy directly from your device.

**Note:** Selecting multiple documents at once is not supported.

## File picker, folders, and files in documents panel

The Documents panel displays both documents and folders. When you attach a folder to a ticket or record, the folder appears in the Documents panel alongside individually attached documents. Selecting the folder name navigates inside it, displaying all child documents and subfolders. When a group of related documents is already organized into a folder, attaching the folder to a ticket is more efficient than attaching each document separately.

The folders enable you to organize documents in a structured hierarchy.

The file picker provides a unified view of documents across multiple sources and supports folder navigation, search, and multi-select. The file picker organizes available sources into the following three categories:

-   **Workspace documents**

    Browse and attach documents stored in the ServiceNow. The workspace documents section includes the following views:

    -   All documents
    -   Owned by me
    -   Shared with me
-   **External cloud**

    Browse and search documents stored in a connected external cloud storage provider. Supported providers include Microsoft OneDrive, Google Drive, and Microsoft SharePoint. When you select a document from an external drive, you can choose to attach the full file or to link only the URL of the external document to the record.

    -   Upload a copy to ServiceNow
    -   Link the URL

**Note:** You can attach only one external cloud document at a time. Multi-select is not supported for external cloud documents.

-   **Local drive**

    Upload a document directly from your device. Browse your file system, select the file you want to attach, and upload it to the record.


-   **[Add documents in Workspace](../task/attach-document-workspace.md)**  
Use the file picker to add documents from the documents repository, external cloud storage providers, or your local desktop to records.
-   **[Manage document files and folders in Workspace](../task/manage-folders-documents-workspace.md)**  
Manage folders and documents from the Documents component to download, rename, manage permissions, track versions, add reviewers and approvers directly in the record within the workspace.
-   **[Manage document versions in external cloud](../task/manage-documents-external-cloud.md)**  
Manage document versions from external cloud directly in the record within the workspace.
-   **[Send a document version for approval](../task/send-document-approval.md)**  
Add a single or multiple reviewers and approvers for the document approval and review.

**Parent Topic:**[Using Document Management](using-document-management.md)

