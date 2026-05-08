---
title: Document Services Framework for Google Drive
description: Integrate the Document Services with Google Drive.Also reuse this short description in the release notes.
locale: en-US
release: australia
product: Document Management Services
classification: document-management-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Google Drive integration with Document Services, Integrate with Document Services, Multi Provider Document Services Framework, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Document Services Framework for Google Drive

Integrate the Document Services with Google Drive.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Supported versions

This Spoke was built for Document Services Framework V1.0, but may be compatible with Utah and later versions.

## Key features

Document Services Framework for Google Drive enables a flow designer to:

-   Upload the document to Google Drive
-   Collaborate
-   Manage versions
-   Download documents

## Spoke requirements

-   Google Drive Spoke
-   Google Directory Spoke
-   Google Docs Spoke

## Spoke dependencies

If you’re having trouble installing the app, verify that these dependent plugins are installed:

-   IHUB Spoke Util Pack \(com.snc.ihub\_spoke\_util\_pack\)
-   Multi Provider Document Services Framework \(com.snc.multiprovider\_documents\)
-   Remote Directory Sync \(com.snc.remote\_directory\_sync\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke subflows

The Document Services Framework for Google Drive provides sample subflows to demonstrate automating Google Drive tasks for My Drive and Shared drives. To customize a sample subflow, copy it to a new application scope. Available sample subflows include:

<table id="table_gqt_zng_yxb"><thead><tr><th>

Subflow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create Document

</td><td>

Copies the document to Google Drive and creates a record in the Documents table with the folder ID and created version in Version table under Multi Provider Documents.

</td></tr><tr><td>

Create Document V1

</td><td>

Copies the document to Google Drive and creates a record in the Documents table with shareable folder URL and created version in Version table under Multi Provider Document Services Framework Documents.

 **Note:** For shared drive copy the URL and the URL should be in the below the format and anything in between drive and folder needs to be removed while copying the URL.

https://drive.google.com/drive/folders/&lt;folder ID&gt;

</td></tr><tr><td>

Create Group

</td><td>

Creates a group as specified in Google Drive and updates the Permission Configurations table under Multi Provider Documents.

</td></tr><tr><td>

Add Collaborator To Group

</td><td>

Given a Group ID from Google Drive, this subflow will add the given collaborator as specified by role.

</td></tr><tr><td>

Collaborate Document

</td><td>

Adds a permission to a given user, group or domain, or to anyone, for a file. This permission is based on a permission type and role and is how collaboration is configured in Google Drive. If **User** or **Group** is selected, the email address is required for those users and groups. If **Domain** is selected, the domain name to create permission for is required. If **Anyone** is selected, then anyone has permission to the file or folder.

</td></tr><tr><td>

Connect Document From Google Drive Using ID

</td><td>

Connects the Google Drive document using the ID and can be tracked under Multi Provider Document Services Framework documents

</td></tr><tr><td>

Connect Document From Google Drive V1

</td><td>

Connects the Google Drive document using the shareable URL for the document and can be tracked under Multi Provider Document Services Framework documents.

</td></tr><tr><td>

Copy Google Drive Document Version

</td><td>

Copies the document with the given version from Google Drive to an attachment in ServiceNow.

</td></tr><tr><td>

Delete Document

</td><td>

Deletes the document in Google Drive and remove its corresponding records in documents and versions tables.

</td></tr><tr><td>

Delete Document Version

</td><td>

Deletes the document in Google Drive and remove its corresponding records in documents and version tables.

</td></tr><tr><td>

Get All Document Versions

</td><td>

Gets all the document versions from Google Drive and creates or updates records in the Versions table under Multi Provider Documents.

</td></tr><tr><td>

Get Document From Google Drive

</td><td>

Copies the document from Google Drive to the Document Name referred by creating a record in the documents table and all its versions in the Versions table under Multi Provider Documents.

</td></tr><tr><td>

Get Document Latest URL

</td><td>

Constructs the web view URL and web edit URL for the file by verifying if the file actually exists in Google Drive. Consuming APIs are required to verify if the file is present or not.

</td></tr><tr><td>

Get Oldest Document Version

</td><td>

Returns the oldest version of the document.

</td></tr><tr><td>

Reconnect Document From Google Drive

</td><td>

Reconnects the Google Drive document that can be tracked under Multi Provider Documents.

</td></tr><tr><td>

Sync Collaborator

</td><td>

Syncs all Google Drive users in a domain with the Collaborators table under Multi Provider Documents.

</td></tr><tr><td>

Update Document Content

</td><td>

Updates the document with the attached content in Google Drive corresponding with the document ID from table Multi Provider Documents sys\_id.

</td></tr></tbody>
</table>## Spoke actions

The Document Services Framework for Google Drive provides actions to automate Document Services tasks when events occurs in your ServiceNow instance. Available actions include:

<table id="table_iqt_zng_yxb"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Delete document and versions

</td><td>

Deletes the specified document along with versions from Multi Provider document and versions table.

</td></tr><tr><td>

Look Up Incremental Files and Folders

</td><td>

-   Returns a list of Google Drive files and folders under the given folder ID.
-   Retrieves the list of files and folders based on the given search query. Hierarchical search is not supported.

**Note:** Search results may vary due to Google Drive 's indexing behavior.


</td></tr><tr><td>

Look Up Files and Folders Stream

</td><td>

Retrieves the list of files and folders under the given folder.

</td></tr><tr><td>

Copy File Revision as Attachment

</td><td>

Copies the given Revision ID for a File ID to any record in ServiceNow.

</td></tr><tr><td>

Delete document version

</td><td>

Deletes the specified versions of a document from Multi Provider document versions table.

</td></tr><tr><td>

Look Up Target Record Existence

</td><td>

Checks for the existence of the target record in the specified target table.

</td></tr><tr><td>

Copy Doc File to Attachment

</td><td>

Copies the Google doc file toServiceNow as an attachment.

</td></tr><tr><td>

Copy Doc Revision as Attachment

</td><td>

Copies the given revision ID for a Google document file ID to any record in ServiceNow.

</td></tr><tr><td>

Get File Type Info

</td><td>

Returns the file type and information for the input mime-type.

</td></tr></tbody>
</table>## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up Document Services framework for Google Drive](../task/setup-gdrive-spoke-document-services.md).



**Parent Topic:**[Google Drive integration with Document Services](google-drive-integration.md)

