---
title: Microsoft SharePoint Online Spoke
description: The Microsoft SharePoint Online spoke integrates your ServiceNow instance with Microsoft SharePoint Online so that you can automate various predefined actions as part of a Workflow. For example, you can rename a folder on Microsoft SharePoint Online when a record in the database is updated.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 14
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Microsoft SharePoint Online Spoke

The Microsoft SharePoint Online spoke integrates your ServiceNow® instance with Microsoft SharePoint Online so that you can automate various predefined actions as part of a Workflow. For example, you can rename a folder on Microsoft SharePoint Online when a record in the database is updated.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Microsoft SharePoint Online spoke v2.10.0 is the latest version.

**Note:** The Microsoft SharePoint online spokes does not support the On-premise SharePoint.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow Workflow Studio - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Integration Hub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Supported versions

Microsoft SharePoint Application Programming Interface \(API\) version v1.

## Spoke flows

The Microsoft SharePoint Online spoke provides sample flows in the draft state to demonstrate automating the Microsoft SharePoint Online tasks. To customize a sample flow, copy it to a new application scope. The following table shows the available sample flows.

|Flow|Description|
|----|-----------|
|New Attachment on Record creates folder, and copies attachment|When an attachment is created in a database table, a folder is created for a knowledge record on the Microsoft SharePoint Online spoke. Then, the attachment is copied to the folder.|
|Create Site For Knowledge Base|When a knowledge base is created in the database table, the flow creates a site for it on the Microsoft SharePoint Online|

**Note:**

-   If the single sign-on \(SSO\) is set up, you can use the action Look Up User Information By Login Name and verify that you're approved to perform the spoke actions.
-   Flow designers and action designers must ensure that the user authorization checks are performed before the flow or action is executed.

## Spoke subflows

The Microsoft SharePoint Online spoke provides a sample subflow in the draft state to demonstrate automating Microsoft SharePoint Online tasks. To customize the subflow, copy it to a new application scope.

<table id="table_h1n_zft_kfb"><thead><tr><th>

Subflow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Remove Then Add A User To A Group

</td><td>

Removes a user from a Microsoft SharePoint Online group and adds a new user.

</td></tr><tr><td>

Delete Modern Site \(without O365 Group\)

</td><td>

Deletes the modern site associated with Non O365 Group \(communication site\).

</td></tr><tr><td>

Submit Modern Site \(with O365 Group\) for Deletion

</td><td>

Submits a modern Site \(with O365 Group\) for Deletion.

**Note:** It may take up to 30 minutes for site to move under deleted sites section of SharePoint Admin portal.

</td></tr></tbody>
</table>**Note:** Flow designers and action designers must ensure that user authorization checks are performed before the flow or action is executed.

## Spoke actions

The Microsoft SharePoint Online spokeprovides actions to automate various Microsoft SharePoint Online tasks that are based on the triggers in the ServiceNow instance.

You can perform some actions by using the SharePoint Online connection and the remaining actions by using the SharePoint Graph connection.

The actions in the following table use the SharePoint Online connection and the credential alias record.

<table id="table_gsq_2gt_kfb"><thead><tr><th colspan="3">

Actions using the **Sharepoint Online** connection and credential alias record

</th></tr><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="10">

Site Management

</td><td>

Create Modern Site

</td><td>

Creates a modern site of types Communication sites and Non-group associated Team Sites.

</td></tr><tr><td>

Create Subsite

</td><td>

Creates a subsite on Sharepoint Online. The Tenant determines the root location.

</td></tr><tr><td>

Delete Modern Site

</td><td>

Deletes the modern site associated with non-O365 Group \(communication site\).

</td></tr><tr><td>

Delete Subsite

</td><td>

Removes a subsite from Sharepoint Online. The Connection URL used determines what is the Root location.

</td></tr><tr><td>

Look up Modern Site Information

</td><td>

Retrieves details of a modern site.

</td></tr><tr><td>

Look up Changes For Site

</td><td>

Retrieves the changes for a site that is based on the query conditions.

</td></tr><tr><td>

Look up Role Assignments

</td><td>

Retrieves all the role assignments that are defined on the site.

</td></tr><tr><td>

Look Up Site Collection ID

</td><td>

Looks up a specific site ID.

</td></tr><tr><td>

Look Up Subsite Details

</td><td>

Looks up information about a subsite.

</td></tr><tr><td>

Update Site Information

</td><td>

Updates a Microsoft SharePoint Online site.

</td></tr><tr><td rowspan="10">

Folder Management

</td><td>

Create Folder

</td><td>

Creates a folder in a document library on a Microsoft SharePoint Online site.

</td></tr><tr><td>

Delete Folder

</td><td>

Deletes a folder in Microsoft SharePoint Online.**Note:** You receive no warning or notification before the folder is removed.

</td></tr><tr><td>

List Files In A Folder

</td><td>

Gets a list of files in a folder.

</td></tr><tr><td>

List Folders In A Folder

</td><td>

Gets a list of the folders in a folder.

</td></tr><tr><td>

Look Up Folder

</td><td>

Looks up a folder in Microsoft SharePoint Online and returns its properties. For example, the output can contain the property "Relative URL".

</td></tr><tr><td>

Rename A Folder

</td><td>

Renames a folder in Microsoft SharePoint Online.

</td></tr><tr><td>

Share Folder With Group

</td><td>

Shares a folder with a group in Microsoft SharePoint Online. The group must belong to the Microsoft SharePoint Online tenant account.

</td></tr><tr><td>

Share Folder With User

</td><td>

Shares a folder with a user inMicrosoft SharePoint Online. The user must belong to the Microsoft SharePoint Online tenant account.

</td></tr><tr><td>

Unshare Folder With Group

</td><td>

Removes the access to a folder from a group. The group must belong to the Microsoft SharePoint Online tenant account.

</td></tr><tr><td>

Unshare Folder With User

</td><td>

Removes the access to a folder from a user. The user must belong to the Microsoft SharePoint Online tenant account.

</td></tr><tr><td rowspan="13">

File Management

</td><td>

Attach Sharepoint File To A Record

</td><td>

Attaches a Microsoft SharePoint Online file to a ServiceNow record.

</td></tr><tr><td>

Check-in File

</td><td>

Sets a file in the Microsoft SharePoint Online in the checked in state. To find the version number of the file after its state is set to checked in, use the Look Up File Details action,**Note:** The file is already uploaded and the action just updates the status of the file to be checked in.

</td></tr><tr><td>

Check-out File

</td><td>

Sets a file in the Microsoft SharePoint Online in the checked out state. To find the version number of the file after its state is set to checked out, use the Look Up File Details action,**Note:** The file is already downloaded and the action just updates the status of the file to checked out.

</td></tr><tr><td>

Copy Attachment To Folder

</td><td>

Copies a ServiceNow attachment to a Microsoft SharePoint Online folder.

</td></tr><tr><td>

Copy File

</td><td>

Copies a file with a new name.

</td></tr><tr><td>

Create A Text File

</td><td>

Creates a text file with the information that you provide.

</td></tr><tr><td>

Delete File

</td><td>

Deletes a file in Microsoft SharePoint Online.

</td></tr><tr><td>

Look Up File Details

</td><td>

Looks up the file details in Microsoft SharePoint Online.

</td></tr><tr><td>

Move File

</td><td>

Moves a file to another location in Microsoft SharePoint Online.

</td></tr><tr><td>

Share File With Group

</td><td>

Shares a file with a group inMicrosoft SharePoint Online. The group must belong to the Microsoft SharePoint Online tenant account.

</td></tr><tr><td>

Share File With User

</td><td>

Shares a file with a Microsoft SharePoint Online user. The user must belong to the Microsoft SharePoint Online tenant account.

</td></tr><tr><td>

Unshare File With Group

</td><td>

Removes the access to a file from a Microsoft SharePoint Online group. The group must belong to the Microsoft SharePoint Online tenant account.

</td></tr><tr><td>

Unshare File With User

</td><td>

Removes the access to a file from a Microsoft SharePoint Online user. The user must belong to the Microsoft SharePoint Online tenant account.

</td></tr><tr><td rowspan="3">

User Management

</td><td>

Look Up User Information By Login Name

</td><td>

Searches a Microsoft SharePoint Online site for information on a user and returns the information.

</td></tr><tr><td>

Look Up User Information By Email

</td><td>

Searches the specified Microsoft SharePoint Online site for a given user and return SharePoint information about that account.

</td></tr><tr><td>

Look Up User's Sharepoint Groups

</td><td>

Searches the Microsoft SharePoint Online site for information on all groups that a user is a member of and returns the information.

</td></tr><tr><td>

Search Management

</td><td>

Look up Search Query Results Stream

</td><td>

Searches the SharePoint Root site and retrieves the result based on the provided search query.

</td></tr><tr><td rowspan="9">

Group Management

</td><td>

Add Role To Site

</td><td>

Adds a role to a Microsoft SharePoint Online user or group.

</td></tr><tr><td>

Add User To Group

</td><td>

Adds a user to a Microsoft SharePoint Online site group.

</td></tr><tr><td>

Create Group

</td><td>

Creates a group in a Microsoft SharePoint Online site.

</td></tr><tr><td>

Delete Group

</td><td>

Deletes a group on a Microsoft SharePoint Online site.

</td></tr><tr><td>

Look Up Group By Name

</td><td>

Looks up a group by its name in a site location in the Microsoft SharePoint Online. If no site location is specified, the action searches the root site of the tenant.

</td></tr><tr><td>

Remove Role From Site

</td><td>

Removes permissions from a group or a user.

</td></tr><tr><td>

Remove User From Group

</td><td>

Removes a user from a Microsoft SharePoint Online site group.

</td></tr><tr><td>

Update Group Owner \(User\)

</td><td>

Updates a user as the group owner.

</td></tr><tr><td>

Look up M365 Members by Site Group

</td><td>

Retrieves a list of the users and M365 groups associated with a Microsoft SharePoint Online Site Group.

</td></tr><tr><td rowspan="6">

List Management

</td><td>

Create List

</td><td>

Creates a list in a Microsoft SharePoint Online site with its title and description.

</td></tr><tr><td>

Create List Subscription

</td><td>

Creates a webhook subscription for a list.

</td></tr><tr><td>

Delete List By ID

</td><td>

Deletes a list in a Microsoft SharePoint Online site by its ID.

</td></tr><tr><td>

Look Up List Details By ID

</td><td>

Looks up a list in a Microsoft SharePoint Online site by its ID.

</td></tr><tr><td>

Look Up List ID By Title

</td><td>

Looks up a list in a Microsoft SharePoint Online by its title.

</td></tr><tr><td>

Update list in a site by ID

</td><td>

Updates a list in a Microsoft SharePoint Online site by its ID.

</td></tr><tr><td rowspan="5">

List Item Management

</td><td>

Create List Item

</td><td>

Creates a list item inside a list.

</td></tr><tr><td>

Delete List Item By ID

</td><td>

Deletes a list item by both the list ID and the list item ID.

</td></tr><tr><td>

Look Up List Item By ID

</td><td>

Looks up a list item by both the list ID and the list item ID.

</td></tr><tr><td>

Look Up List Items In A List

</td><td>

Gets a list of items from a list in different formats.

</td></tr><tr><td>

Update List Item By ID

</td><td>

Updates a list item title by its ID.

</td></tr></tbody>
</table>**Note:** Flow designers and action designers must ensure that user authorization checks are performed before the flow or action is executed.

These actions use the SharePoint Graph connection and credential alias record:

<table id="table_idq_ysc_xpb"><thead><tr><th colspan="3">

Actions using the **SharePoint Graph** connection and credential alias record

</th></tr><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="3">

Change Management

</td><td>

Get Change Query Properties

</td><td>

Retrieves the change query properties that are used to define a query that is performed against the change log.

</td></tr><tr><td>

Get Delta Link Token For Drive

</td><td>

Retrieves the latest delta link token for a drive.

</td></tr><tr><td>

Get Next Token

</td><td>

Retrieves the next link token from the SharePoint Resource Next Link Token table.

</td></tr><tr><td rowspan="3">

File Management

</td><td>

Get File Download Link

</td><td>

Retrieves the download URL of the file.

</td></tr><tr><td>

Look up File Permissions

</td><td>

Gets the permissions for a file.

</td></tr><tr><td>

Look up Files

</td><td>

Retrieves all the files in a drive.

</td></tr><tr><td rowspan="5">

List Management

</td><td>

Create List Subscription

</td><td>

Creates a webhook subscription for a list.

</td></tr><tr><td>

Renew List Subscription

</td><td>

Renews a webhook subscription for a list.

</td></tr><tr><td>

Delete List Subscription

</td><td>

Deletes the webhook subscription for a list.

</td></tr><tr><td>

Get List

</td><td>

Retrieves the details of a list from the SharePoint tenant.

</td></tr><tr><td>

Look up Drives

</td><td>

Retrieves all the drives for a site.

</td></tr><tr><td rowspan="7">

Site Management

</td><td>

Delete Modern Site with O365 Group

</td><td>

Submit the modern site associated with the O365 Group \(team site\) for deletion. It deletes the associated 0365 group that deletes the site. **Note:** After execution, it can take up to 30 minutes for a site to be deleted.

</td></tr><tr><td>

Look up Modern Site Group Information

</td><td>

Retrieves the associated O365 group details of a modern site \(team site\).

</td></tr><tr><td>

Look up Site Collections

</td><td>

Retrieves all the site collections.

</td></tr><tr><td>

Look up Subsites

</td><td>

Retrieves details of all the subsites in a site.

</td></tr><tr><td>

Create Root Site Subscription

</td><td>

Creates a webhook subscription for a root site.

</td></tr><tr><td>

Look up Site Permissions

</td><td>

Retrieves all permissions for a site.

</td></tr><tr><td>

Get Site

</td><td>

Gets the site details.

</td></tr></tbody>
</table>## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See Create an agentic workflow for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See Find AI agents for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See Duplicate an AI agent for more information about creating a clone.
-   See Now Assist AI agents for information about AI agents.

Available AI agents include:

|AI agent|Description|
|--------|-----------|
|Microsoft SharePoint Online file management AI agent|Automates file-related tasks such as, sharing files with users or groups, copying files, moving files, creating text files, retrieving file details, and managing file permissions.|
|Microsoft SharePoint Online list management AI agent|Automates SharePoint operations such as, managing lists, creating and renewing subscriptions, retrieving list details, and automating workflows.|
|Microsoft SharePoint Online site management AI agent|Automates SharePoint operations such as, creating and deleting sites, managing site collections, retrieving site information, and automating SharePoint workflows.|
|Microsoft SharePoint Online group management AI agent|Automates group management processes such as, adding or removing users from groups, creating or deleting groups, updating group ownership, and managing roles within SharePoint sites.|
|Microsoft SharePoint Online list item management AI agent|Automates SharePoint operations such as, creating, updating, deleting, and retrieving list items.|
|Microsoft SharePoint Online user management AI agent|Automates user management tasks such as, a retrieving user's SharePoint groups, user information by login name, and user details by email.|
|Microsoft SharePoint Online folder management AI agent|Automates folder management tasks such as, renaming folders, creating folders, sharing and unsharing folders with users or groups, listing files and folders, and deleting folders.|
|Microsoft SharePoint Online change management AI agent|Perform the Get Next Token and Get Delta Link Token For Drive actions.|
|Microsoft SharePoint Online search management AI agent|Retrieves the required search query results and enables users to streamline processes.|

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see Find AI agents.

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## SharePoint Online account requirements

The Microsoft SharePoint Online spoke requires that you create a custom app on your SharePoint Online account to generate OAuth 2.0 tokens. See [Configure OAuth application in Microsoft Azure](../task/configure-oauth-application-in-microsoft-azure.md).

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

-   **Single tenant**

    This spoke includes the MicrosoftSharepointOnline alias record to authorize actions on Microsoft SharePoint Online. Select this alias in the Tenant record to authorize changes in Microsoft SharePoint Online for a single tenant.

-   **Multiple tenants**

    This spoke includes the MicrosoftSharepointOnline alias record to authorize actions on Microsoft SharePoint Online. Create a connection and credential alias record for each additional tenant site that you want to support. Select the correct alias in the Tenant record to authorize changes in Microsoft SharePoint Online. Create a connection and credential alias record for each additional tenant site that you want to support. Select the correct alias in the Tenant record to authorize changes in Microsoft SharePoint Online. See [Create aliases for multiple tenants](../task/create-aliases-sharepoint.md).


**Note:**

Three alias records are available by default with the spoke; Sharepoint Online, SharePoint Graph, and SharePoint Graph Root Site Subscription. Each alias record requires a tenant to be associated with it. If you intend to use all SharePoint Online, Graph, and Root Subscription actions in the spoke, you must ensure that you have created three tenant records in the Tenants tables of the Microsoft SharePoint Online spoke so that each tenant record is associated with its respective alias record.

-   If configuring an integration for a single tenant, use the existing **MicrosoftSharepointOnline** alias record.
-   You can use multiple tenants with the **Microsoft SharePoint Graph** connection alias only.

