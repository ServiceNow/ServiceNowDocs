---
title: Managed Documents plugin
description: This page describes the applications and modules, database table structure, scripts, and roles.
locale: en-US
release: australia
product: Document Management Services
classification: document-management-services
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managed Documents, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Managed Documents plugin

This page describes the applications and modules, database table structure, scripts, and roles.

## Database table structure

The following tables are added:

|Display Name \(Table Name\)|Description|
|---------------------------|-----------|
|Document \[dms\_document\]|The document details.|
|Revision \[dms\_revision\]|The document revisions.|
|Audience \[dms\_audience\]|The intended document readers.|
|Classifications \[classification\]|The document restriction level, such as public or confidential. \(Does not define access to the document. Document security is set in user and group permissions.\)|
|Type \[dms\_type\]|The document purpose.|
|Component \[dms\_component\]|The components of name formats. The value field is a dot-walking expression that is evaluated. An exception is made for the revision because it does not exist when the revision name is generated.|
|Name format \[dms\_name\_format\]|The composition of components to generate revision names.|
|Approval sequence \[approval\_sequence\]|The approval sequences that users must follow.|
|Approval Rule \[dms\_approval\_rule\]|The criteria that records of the dms\_document table must match. Used to automatically add approvers to a document.|
|Collection \[dms\_collection\]|The document groups created by the user.|

## Scripts

|Rule|Description|
|----|-----------|
|Update Document|Changes the state of a document depending on its revisions.|
|Add Approvers|Populates the list of approvers in the document.|

|Script include|Description|
|--------------|-----------|
|DocumentManagement|Contains the main logics for the Managed Documents plugin.|
|DocumentManagementDB|Contains methods to perform CRUD operations on the database.|
|DocumentManagementSecurity|Helps manage the security of the Managed Documents system.|
|DocumentManagementAjax|Updates the details of the temporary revision that is created when opening the upload/check in revision form.|
|DocumentAttachmentAjax|Renames an attachment file.|
|DocumentRevisionWorkflowHelper|Helps perform basic workflow operations on a revision.|
|DocumentManagementApprovalMatcher|Helps obtain the user and group approvers for a document that matches approval rules.|
|DocumentApproverHelper|Contains logics to handle document approvers.|
|DocumentManagementUtils|Useful methods.|
|DocumentReferenceQualifiers|Static methods that return reference qualifiers.|

|Rule|Description|
|----|-----------|
|Document type change|Updates the name format field in the revision settings section of the document. Each type has a default name format.|

## Roles

This plugin introduces two new roles:

|Role|Description|
|----|-----------|
|document\_management\_user|This role enables a user to access the Managed Documents plugin, create documents, and search for documents. Document reviewers and approvers need the document\_management\_user role to access the Managed Document plugin. \(Please note that reviewers and approvers can also access a document revision from an approval record.\)|
|document\_management\_admin|This role enables a user to change administrative settings for the Managed Documents plugin.|

**Note:** Each document has individual permissions, so even if a user is given the document\_management\_user role and has permissions to the application, the user can only view documents to which they have been given access.

-   **[Install the Managed Documents plugin](../task/t_InstallTheManagedDocumentsPlugin.md)**  
The Managed Documents plugin is available for activation by users with the admin role.

**Parent Topic:**[Managed Documents](../concept/c_ManagedDocuments.md)

