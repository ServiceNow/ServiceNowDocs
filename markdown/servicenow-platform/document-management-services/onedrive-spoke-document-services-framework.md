---
title: Document Services Framework for Microsoft OneDrive
description: Integrate the Document Services Framework with Microsoft OneDrive. Also reuse this short description in the release notes.
locale: en-US
release: zurich
product: Document Management Services
classification: document-management-services
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Microsoft OneDrive integration with Document Services, Integrate with Document Services, Multi Provider Document Services Framework, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Document Services Framework for Microsoft OneDrive

Integrate the Document Services Framework with Microsoft OneDrive.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Microsoft OneDrive spoke for Document Services Framework spoke v 1.2.2 is the latest version.

## Supported versions

This spoke was built for Microsoft OneDrive Spoke for Document Services Framework V1.1, but might be compatible with later versions.

## Key features

Microsoft OneDrive Spoke for Document Services Framework enables a flow designer to do the following:

-   Upload documents to Microsoft OneDrive
-   Collaborate
-   Manage versions
-   Download documents

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   Complex Object \(com.glide.cobject\)
-   IHUB Spoke Util Pack \(com.snc.ihub\_spoke\_util\_pack\)
-   Multi Provider Document Services Framework \(com.snc.multiprovider\_documents\)
-   Remote Directory Sync \(com.snc.remote\_directory\_sync\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)

**Note:** Some of these plugins are licensable features and require appropriate licenses if used outside the spoke implementation.

## Spoke subflows

The Microsoft OneDrive Spoke for Document Services Framework provides sample subflows to demonstrate the automation of Document Services tasks. To customize a sample subflow, copy it to a new application scope. The following tables list the available sample subflows for V1 and V2.

**Note:** Only V2 subflows support the Microsoft SharePoint site.

<table id="table_tld_tby_wtb"><thead><tr><th>

Subflow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Add Collaborator To Group

</td><td>

Adds the supplied CollaboratorID as the Member or Owner specified by Type.

</td></tr><tr><td>

Collaborate Document

</td><td>

Associates a document with a group or a user on Microsoft OneDrive.

</td></tr><tr><td>

Collaborate Document With Recipient Type

</td><td>

Associates a document with a specified Recipient Type

</td></tr><tr><td>

Connect Document From OneDrive Using Path

</td><td>

Connects the Microsoft OneDrive document.

</td></tr><tr><td>

Copy OneDrive Document Version

</td><td>

Copies the document with the specified version from Microsoft OneDrive to an attachment in the ServiceNow instance.

</td></tr><tr><td>

Create Document

</td><td>

Copies the document to Microsoft OneDrive, creates a record in the Multi Provider Document \[mp\_document\] table, and adds a version in the Multi Provider Document Version \[mp\_document\_version\] table.

</td></tr><tr><td>

Create Group

</td><td>

Creates a group as specified in Microsoft OneDrive and updates the Multi Provider Permission Configuration \[mp\_permission\_configuration\] table.

</td></tr><tr><td>

Delete Document

</td><td>

Deletes the document in Microsoft OneDrive and removes its corresponding records in the Multi Provider Document Version \[mp\_document\_version\] tables.

</td></tr><tr><td>

Delete Document Version

</td><td>

Deletes the specified version of the document in Microsoft OneDrive and the ServiceNow instance and deletes a record in the Multi Provider Document Version \[mp\_document\_version\] table.

</td></tr><tr><td>

Get All Document Version

</td><td>

Retrieves all document versions from Microsoft OneDrive and creates and updates records in the Multi Provider Document Version \[mp\_document\_version\] table.

</td></tr><tr><td>

Get Document from OneDrive

</td><td>

Copies the document from Microsoft OneDrive to the specified document name. It also creates a record in the Multi Provider Document \[mp\_document\] table and in all document versions in the Multi Provider Document Version \[mp\_document\_version\] table.

</td></tr><tr><td>

Restore Document Version

</td><td>

Restore the document to the version in Microsoft OneDrive.

</td></tr><tr><td id="sync-collab-onedrive">

Sync Collaborators

</td><td>

Syncs all Microsoft Azure users into the Multi Provider Collaborators \[mp\_collaborators\] table.If the user is deleted or updated, the user's record in the Multi Provider Collaborators \[mp\_collaborators\] table is checked, if it’s present then the record is deleted or updated.

If the user is newly added, then it creates an entry in the Multi Provider Collaborators \[mp\_collaborators\] table under Multi Provider Documents.

**Note:** The scheduled job with the name **Sync Collaborators** triggers the subflow for Sync Collaborators. You can choose from the available run a script option. The default option is **On Demand**. The job is run based on the set schedule and collaborators are synchronized accordingly. For more information, see [Automatically run a script of your choosing](https://www.servicenow.com/docs/access?context=t_ScheduleAScriptExecution&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Delete Collaborator Record

</td><td>

Deletes the specified collaborator record from the Multi Provider Collaborators \[mp\_collaborators\] table.

</td></tr><tr><td>

Update Document Content

</td><td>

Updates the specified document with the provided attachment in Microsoft OneDrive that corresponds to the document ID. The attachment name should match the name of the document in Microsoft OneDrive.

</td></tr><tr><td>

Upload Large File

</td><td>

Uploads an attachment to Microsoft OneDrive. The maximum size of the file can’t exceed 60 MB.

</td></tr><tr><td>

Get Latest URL

</td><td>

Gets the latest URL to a document in the Microsoft OneDrive.

</td></tr><tr><td>

Reconnect Document from Microsoft OneDrive

</td><td>

Reconnects to a document in Microsoft OneDrive. **Note:** Before using the subflow, ensure that the corresponding Microsoft OneDrive connection and credential are created and the Microsoft OneDrive authorization token is available.

</td></tr></tbody>
</table><table id="table_qxf_dbr_zzb"><thead><tr><th>

Subflow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Get Document Latest URL V2

</td><td>

Gets the latest URL from Microsoft OneDrive for the referred document ID.

</td></tr><tr><td>

Update Document Content V2

</td><td>

Updates the specified document with the provided attachment content in Microsoft OneDrive corresponding to the document ID from table Multi Provider Document sys\_id. The attachment name should match with the name of the document in Microsoft OneDrive.

</td></tr><tr><td>

Collaborate Document V2

</td><td>

Associates a document with a specified recipient type.

</td></tr><tr><td>

Connect Document From OneDrive Using Path V2

</td><td>

Connects the Microsoft OneDrive document that can also be tracked under Multi Provider Documents.

</td></tr><tr><td>

Copy OneDrive Document Version V2

</td><td>

Copies the document with the specified version from Microsoft OneDrive to an attachment in the ServiceNow instance.

</td></tr><tr><td>

Create Document V2

</td><td>

Copies the document to Microsoft OneDrive and creates a record in the Multi Provider Document \[mp\_document\] table and the Multi Provider Document Version \[mp\_document\_version\] table for Multi Provider Documents.

</td></tr><tr><td>

Delete Document V2

</td><td>

Deletes the document in Microsoft OneDrive and removes its corresponding records in the Multi Provider Document \[mp\_document\] table and the Multi Provider Document Version \[mp\_document\_version\] tables.

</td></tr><tr><td>

Delete Document Version V2

</td><td>

Deletes the particular version of the document in bothMicrosoft OneDrive and deletes a record in the Multi Provider Document Version \[mp\_document\_version\] table under Multi Provider Documents.

</td></tr><tr><td>

Get All Document Versions V2

</td><td>

Retrieves all the document versions from Microsoft OneDrive and creates or updates records in the Multi Provider Document Version \[mp\_document\_version\] table under Multi Provider Documents. This subflow supports documents from different sources supported by Microsoft OneDrive.

</td></tr><tr><td>

Get Document from OneDrive V2

</td><td>

Copies the document from Microsoft OneDrive to the specified document name. It also creates a record in the Multi Provider Document \[mp\_document\] table and all its versions in the Multi Provider Document Version \[mp\_document\_version\] table under Multi Provider Documents.

</td></tr><tr><td>

Reconnect Document from Microsoft OneDrive V2

</td><td>

Reconnects to a document in the Microsoft OneDrive.**Note:** Before using the subflow, ensure that the corresponding Microsoft OneDrive connection and credential are created and the Microsoft OneDrive authorization token is available.

</td></tr><tr><td>

Restore Document Version V2

</td><td>

Restores the document to the version provided in the Microsoft OneDrive.

</td></tr><tr><td>

Sync Collaborators V2

</td><td>

Syncs all Microsoft Azure users into the Collaborators \[mp\_collaborators\] table under Multi Provider Documents.

</td></tr><tr><td>

Upload Large File V2

</td><td>

Uploads an attachment to Microsoft OneDrive. The maximum size of the file can't exceed 60 MB.

</td></tr><tr><td>

Remove Document Collaboration

</td><td>

Removes collaboration on a Microsoft OneDrive document.

</td></tr><tr><td>

Update Document Collaboration

</td><td>

Updates collaboration on a Microsoft OneDrive document.

</td></tr></tbody>
</table>**Note:** The V2 subflows work only for documents attached to the platform using the Create Document V2 or Connect Document V2 subflows.

## Spoke Actions

The Microsoft OneDrive Spoke for Document Services Framework provides sample actions to automate Document Services tasks when events occur in ServiceNow. The following table lists the available sample actions.

<table id="table_ddl_cq2_ytb"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Delete Collaborator Record

</td><td>

Deletes the specified collaborator record from the Multi Provider Collaborators \[mp\_collaborators\] table.

</td></tr><tr><td>

Delete document

</td><td>

Deletes the document record from the Multi Provider Document \[mp\_document\] table.

</td></tr><tr><td>

Delete document and versions

</td><td>

Deletes the specified document and all of its versions from the Multi Provider Document Version \[mp\_document\_version\] table.

</td></tr><tr><td>

Delete document version

</td><td>

Deletes specified versions of a document from the Multi Provider Document Version \[mp\_document\_version\] table.

</td></tr><tr><td>

Delete versions of document

</td><td>

Deletes all versions of a specified document.

</td></tr><tr><td>

Look up Target Record Existence

</td><td>

Checks for the existence of a target record in the specified target table.

</td></tr><tr><td>

Look Up Incremental Files and Folders

</td><td>

-   Retrieves the list of files and folders under the given Folder ID for the selected Source and Source ID. If no source is selected, then it lists the contents of the root folder by default.
-   Retrieves the list of files and folders based on the given search query. Hierarchical search is also supported, allowing navigation through folder structures.

**Note:** Search results may vary due to Microsoft OneDrive 's indexing behavior.


</td></tr><tr><td>

Look up Sites Based On Query String Stream

</td><td>

Lists all the sites satisfying the specified query string.

</td></tr><tr><td>

Update Delta Token

</td><td>

Updates the system property **deltaToken** with the specified delta token.

</td></tr></tbody>
</table>## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up Microsoft OneDrive spoke](https://www.servicenow.com/docs/access?context=setup-msonedrive&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).

**Parent Topic:**[Microsoft OneDrive integration with Document Services](one-drive-integration.md)

