---
title: Document security and access
description: Document access permissions for users and groups provide you with security for your documents.
locale: en-US
release: yokohama
product: Document Management Services
classification: document-management-services
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Document Management, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Document security and access

Document access permissions for users and groups provide you with security for your documents.

## Owner access to documents

By default, the document owner has all privileges to the document and can do the following:

-   Update the document parameters
-   Upload document versions
-   Create document references
-   Share a document with other users
-   Delete a document

**Note:**

If the document owner changes, the new owner obtains all rights to the document and the previous owner loses access. If the previous owner wants to keep access to the document, the document should be shared instead of transferring owner access.

## Document access settings

You can access documents through three different settings.

<table id="table_ls2_rfm_hsb"><thead><tr><th>

Access

</th><th>

Description

</th></tr></thead><tbody><tr><td>

By referenced records

</td><td>

When a document is referenced to a parent record, any user with access to the parent record has access to the document.

</td></tr><tr><td>

Admin access

</td><td>

All document users with admin access can access the document.

</td></tr><tr><td>

Shared permissions

</td><td>

Enables sharing a document with other users as Reader, Writer, or Owner at different permission levels such as:-   User Permissions
-   Group Permissions
-   Role Permissions
-   User Criteria Permissions

</td></tr></tbody>
</table>## Sharing permissions and roles

Users can give permissions to other users based on their own access to the document. The permission levels are:

-   Owner
-   Writer
-   Reader

To share documents with other users and groups you must have write access to the document record and roles to share at different levels.

|Sharing permissions|User permissions required|Role required|
|-------------------|-------------------------|-------------|
|[User Permissions](../task/share-docs-users.md)|All users even if they don’t have a role assigned|No role required. All users can share documents with other user|
|[Group Permissions](../task/share-docs-groups.md)|Writers and Owners can assign access based on their access permissions|dm\_user\_group\_read|
|[Role Permissions](../task/share-docs-roles.md)|Writers and Owners can assign access based on their access permissions|dm\_user\_role\_read|
|[User Criteria Permissions](../task/share-docs-user-criteria.md)|Writers and Owners can assign access based on their access permissions|dm\_user\_criteria\_read|

-   **[Share documents with users](../task/share-docs-users.md)**  
Assign Reader, Writer or Owner permissions to users to enable them to read, download, update, or delete documents.
-   **[Share documents with groups](../task/share-docs-groups.md)**  
As a Writer or Owner, assign access to user groups based on your access permissions.
-   **[Share documents with roles](../task/share-docs-roles.md)**  
As a Writer or Owner, assign access and permissions based on user roles.
-   **[Share documents with user criteria](../task/share-docs-user-criteria.md)**  
As a Writer or Owner assign access to a document based on the user criteria permissions.

**Parent Topic:**[Document Management](doc-management-landing.md)

