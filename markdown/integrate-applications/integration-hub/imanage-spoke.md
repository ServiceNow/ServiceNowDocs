---
title: iManage Spoke
description: Automate document, folder, workspace, and user management while enabling seamless collaboration within iManage. This automation solution facilitates tasks such as creating, downloading, uploading, updating, and removing files on iManage directly from the ServiceNow AI Platform.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# iManage Spoke

Automate document, folder, workspace, and user management while enabling seamless collaboration within iManage. This automation solution facilitates tasks such as creating, downloading, uploading, updating, and removing files on iManage directly from the ServiceNow AI Platform.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

iManage spoke v1.1.0 is the latest version.

## Roles

All iManage users are assigned to the predefined Default role. Because the default role is automatically assigned to all users, for security reasons it has limited privileges. The iManage administrator can modify this role's privileges but cannot delete it. Other roles can be created, deleted, or modified as required.

The iManage spoke user \[sn\_imanage\_spk.user\] is available when the iManage spoke is installed. The role is required for users accessing iManage external storage.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow® IntegrationHub Action Step — REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow® IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow® IntegrationHub Action Template — Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Supported versions

iManage Work API \(REST API v2\).

## Spoke actions

iManage provides actions to automate the tasks in the following table when events occur in ServiceNow.

**Note:** To prevent unauthorised access, make sure that the required users has the least privileges for the spoke actions.

|Category|Action|Description|
|--------|------|-----------|
|Authentication|Look up Discovery|Retrieves the Customer ID and other details.|
|User Management|Look up Library Users Stream|Retrieves a list of users from the specific library.|
|Workspace Management|Look up Workspace Security|Retrieves the default security of the workspace and a list of users and groups who have access to the workspace.|
|Look up User Access Permission for Workspace|Retrieves a list of users in the specified library optionally filtered by search criteria.|
|Create Workspace|Creates a workspace.|
|Delete Workspace|Deletes a specified workspace.|
|Look up Library Workspaces Stream|Retrieves a list of the workspaces in the specific library.|
|Look up Workspace|Retrieves the workspace profile, and when the list of allowed operations for the Workspace ID is fetched, depending on the request.|
|Look up Workspaces|Retrieves a list of all workspaces.|
|Create Root Level Workspace Folder|Creates a folder at the root level of the specified workspace.|
|Look up User Workspace Operations|Retrieves the operations that the current user is able to perform on the specific workspace.|
|Update Workspace|Updates the information of a specified workspace.|
|Update Workspace Users and Groups Security|Updates the default security of the specified workspace and the access to the workspace by users and groups.|
|Look up Workspace Container Stream|Retrieves the folder structure from a specified template.|
|Folder Management|Delete Folder|Deletes a specified folder.|
|Look up Folder Content Stream|Retrieves the content of the specified folder.|
|Look up Library Folders Stream|Retrieves a list of folders from the specified library.|
|Look up Folder Profile|Retrieves the folder profile of the specified folder ID.|
|Look up Folder Security|Retrieves details of the access permission and default security of the specified folder.|
|Update Folder Properties|Updates the folder properties with the specified properties.|
|Create Subfolders|Creates a folder within the specified folder.|
|Look up Folder Path|Retrieves the path of the specified folder.|
|Look up Folder Operations|Retrieves the operations that the current user has permission to execute on the specified folder.|
|Update Folder Security|Updates the access permissions and default security of a folder.|
|Remove Document from Folder|Deletes the specified document from the folder.|
|Document Management|Delete Document|Deletes the document associated with a document ID.|
|Look up Document Operations|Retrieves the set of operations that the current user is able to perform on a document.|
|Upload Document To Folder|Uploads a document to a specific folder.|
|Look up Document Profile|Retrieves the profile of a specified document.|
|Look up Documents|Retrieves documents that match the specified document profile fields.|
|Look up Document Versions Stream|Retrieves the profiles of all versions of a document.|
|Upload New Document Version|Creates and uploads a new version of the specified document.|
|Look up Library Documents Stream|Retrieves all documents that match specified search criteria.|
|Download Document with Filename|Downloads and saves a document to a local machine.|
|Download Document|Downloads the specific document to the local machine.|
|Look up Parent Folders of Specified Documents Stream|Retrieves a list of the direct parent folders of a specified document.|
|Promote Document Version|Creates a version of the document from a saved document state.|
|Look up Latest Document Version Number|Retrieves the latest version of a specified document.|
|Look up User Access on Document|Retrieves the access permission of a user for the specified document.|
|Look up Document Security|Retrieves the access permission and default security for the document associated with the specified document ID.|
|Update Document Security|Updates the access permission or default security or both of the document associated with the specified document ID.|

## iManage online account requirements

The iManage spoke requires an iManage work account and access to the iManage Control Center to generate OAuth 2.0 tokens.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up iManage spoke](../task/set-up-imanage-spoke.md#).

