---
title: Microsoft OneDrive Spoke
description: Automate file and folder management and collaboration in Microsoft OneDrive. Adds Microsoft OneDrive data to your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Microsoft OneDrive Spoke

Automate file and folder management and collaboration in Microsoft OneDrive. Adds Microsoft OneDrive data to your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Microsoft OneDrive spoke v2.8.2 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Supported versions

API version v1.

## Spoke flows

The Microsoft OneDrive spoke gives sample flows in the draft state to demonstrate automating Microsoft OneDrive tasks. To customize a sample flow, copy it to a new application scope. Available sample flows include:

|Flow|Description|
|----|-----------|
|Renew Subscriptions|Renews the expired subscriptions by updating the expiration date of the subscription.|

## Spoke subflows

The Microsoft OneDrive spoke provides sample subflows in the draft state to demonstrate automating Microsoft OneDrive tasks. To customize a sample subflow, copy it to a new application scope. Available sample subflows include:

|Subflow|Description|
|-------|-----------|
|Download New OneDrive File to ServiceNow|Downloads the new files uploaded in a resource to a ServiceNow record|
|Subscribe to Webhook|Subscribes a listener application to receive notifications when data changes.|
|Sync Changes|Tracks changes to a drive and its children over time.|
|Get Document Latest URL|Gets the latest path of a file in OneDrive using the Sys ID of the document as an input. To use this subflow, a corresponding OneDrive connection and credential must be created, and a OneDrive authorization token should be available.|
|Reconnect Document from Microsoft OneDrive|Gets the latest web URL and webdav URL of a document from the Microsoft OneDrive by using the Document Sys ID, Provider Detail Sys ID, Target Table Name, Target Table Sys ID, and the Document Name. To use this subflow, a corresponding OneDrive connection and credential must be created, and a OneDrive authorization token must be available.|

## Spoke actions

The Microsoft OneDrive spoke provides actions to automate Microsoft OneDrive tasks when events occur in ServiceNow. Available actions include:

<table id="table_gsq_2gt_kfb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Drive Management

</td><td>

Look up Drive Info

</td><td>

Gets the metadata of a specific Microsoft OneDrive drive

</td></tr><tr><td rowspan="4">

Folder Management

</td><td>

Move File Or Folder Item

</td><td>

Moves a file or folder in Microsoft OneDrive to the target location.

</td></tr><tr><td>

Create Folder

</td><td>

Creates a folder in Microsoft OneDrive.

</td></tr><tr><td>

Update File Or Folder Name

</td><td>

Updates the name for a file or folder item by ID.

</td></tr><tr><td>

Delete File Or Folder Item

</td><td>

Deletes a file or folder from Microsoft OneDrive.

</td></tr><tr><td rowspan="15">

File Management

</td><td>

Check In File

</td><td>

Checks in a drive item and sends a sharing invitation. When you check in a file, other users can access the checked-in file.

</td></tr><tr><td>

Check Out File

</td><td>

Checks out a drive item from OneDrive. When you check out a drive item, other users cannot edit the document. Other users also cannot see the changes that you made in the document until you check in the document.

</td></tr><tr><td>

Copy OneDrive File to Attachment

</td><td>

Copies a file in Microsoft OneDrive to an attachment in a record in a ServiceNow record.

</td></tr><tr><td>

Copy Attachment to OneDrive

</td><td>

Copies an attachment record in ServiceNow to Microsoft OneDrive

</td></tr><tr><td>

Copy File Or Folder Item

</td><td>

Asynchronously creates a copy of a Microsoft OneDrive item \(including children\), under a new parent item or with a new name.

</td></tr><tr><td>

Look up Items

</td><td>

Retrieves a list of drive items from a path or the source and source ID of a drive item.

</td></tr><tr><td>

Look up File Or Folder Item Info By ID

</td><td>

Gets file metadata information from the file or folder ID in Microsoft OneDrive.

</td></tr><tr><td>

Look up File Or Folder Item Info By Path

</td><td>

Gets file metadata information from the file path in Microsoft OneDrive.

</td></tr><tr><td>

Copy Attachment To OneDrive Using Path

</td><td>

Copies an attachment record in ServiceNow to OneDrive.

</td></tr><tr><td>

Copy OneDrive File To Attachment Using File Path

</td><td>

Copies a file using its path in OneDrive to an attachment in a record in ServiceNow.

</td></tr><tr><td>

Copy OneDrive File Version To Attachment

</td><td>

Copies a file in OneDrive to an attachment in a record in ServiceNow.

</td></tr><tr><td>

Delete Version of a File

</td><td>

Deletes the specified version of a file from OneDrive.

</td></tr><tr><td>

Look up All Versions of a File

</td><td>

Retrieves all the versions a file in OneDrive.

</td></tr><tr><td>

Restore File Version

</td><td>

Restores the specified file version and make this version the latest.

</td></tr><tr><td>

Upload and Replace File

</td><td>

Uploads the updated version of an existing file or replaces the existing file with a new file. **Note:** The maximum size of the file cannot exceed 4 MB.

</td></tr><tr><td>

Search Documents

</td><td>

Search Files or Folder Items

</td><td>

Searches the drive items \(files or folders\) based on metadata attributes such as the item name.

</td></tr><tr><td rowspan="3">

Document Sharing

</td><td>

Add Collaborator

</td><td>

Adds a collaborator and their permissions to a file or a folder. You can identify the collaborator by their Azure AD Alias or an Object ID.

</td></tr><tr><td>

Look up Collaborators

</td><td>

Lists all the collaborator details associated with a file or folder in Microsoft OneDrive.

</td></tr><tr><td>

Remove Collaborator

</td><td>

Removes a collaborator from a file or folder in Microsoft OneDrive.

</td></tr><tr><td rowspan="5">

Permission Management

</td><td>

Add Permission

</td><td>

Sends a sharing invitation for a drive item. A sharing invitation allows the recipients to access the drive item and optionally sends them an email with a sharing link.

</td></tr><tr><td>

Create Sharing Link

</td><td>

Creates a sharing link which allows you to share a drive item with other users.

</td></tr><tr><td>

Delete Permission

</td><td>

Removes access to a drive item.

</td></tr><tr><td>

Look up Permissions

</td><td>

Retrieves the sharing permissions of a drive item.

</td></tr><tr><td>

Update Permission

</td><td>

Updates the expiration date of the subscription.

</td></tr><tr><td rowspan="6">

Webhook Management

</td><td>

Subscribe Webhook

</td><td>

Creates a subscription that sends notifications when data changes.

</td></tr><tr><td>

Unsubscribe Webhook

</td><td>

Deletes the specified subscription ID.

</td></tr><tr><td>

Get SyncToken for Subscription

</td><td>

Retrieves the latest sync token for the specified subscription ID.

</td></tr><tr><td>

Look up Subscriptions

</td><td>

Retrieves the list of active subscriptions.

</td></tr><tr><td>

Renew Subscription

</td><td>

Updates the expiration date of the subscription.

</td></tr><tr><td>

Sync Changes

</td><td>

Tracks changes to a drive and drive's children over time.

</td></tr></tbody>
</table>## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See [Duplicate an AI agent](https://www.servicenow.com/docs/access?context=clone-ai-agent&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for more information about creating a clone.
-   See [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for information about AI agents.

Available AI agents include:

|AI Agent|Description|
|--------|-----------|
|Microsoft OneDrive sharing management AI agent|Adds or removes a collaborator and manages their permissions for a file or folder in Microsoft OneDrive. Also, lists all the collaborator details associated with a file or folder.|
|Microsoft OneDrive drive management AI agent|Retrieves the metadata of a specific drive in Microsoft OneDrive.|
|Microsoft OneDrive file management AI agent|Manages files, file versions, and attachments in Microsoft OneDrive. Also, retrieves details of the required file.|
|Microsoft OneDrive folder management AI agent|Manages folders in Microsoft OneDrive.|
|Microsoft OneDrive permission management AI agent|Creates sharing link for a drive item and manages permissions.|

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## Spoke module

Bi-directional webhooks can be set up to get notifications about the required events. Routing policy defines conditions that must be met to notify the ServiceNow app. These conditions are based on the events in OneDrive that you want to be notified about. When the conditions are met, a routing policy triggers the associated subflow, which in turn automates the OneDrive tasks.

The bi-directional webhooks require separate setup and can be used independently without using the spoke actions. By default, the OneDrive Webhooks application is available in the OneDrive spoke and has the following modules:

|Module|Description|
|------|-----------|
|OneDrive SyncToken|Enables you to view SyncTokens of OneDrive.|
|OneDrive Webhook Registries|Enables you to create and view the OneDrive webhooks in ServiceNow.|
|OneDrive Webhook Routing Policy|Enables you to create and view the routing policies for the OneDrive webhooks in ServiceNow. You can also customize the conditions in the routing policies as per your requirement.|

## OneDrive Online account requirements

The Microsoft OneDrive spoke requires a custom app that you create in Microsoft Azure.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

-   **Single tenant**

    The OneDrive spoke includes the OneDrive alias record to authorize actions on Microsoft OneDrive. Select this alias in the Tenant record to authorize changes in Microsoft OneDrive for a single tenant.


For information about setting up the spoke, see [Set up Microsoft OneDrive spoke](../task/setup-msonedrive.md#).

## MID Server requirements

These actions use REST calls that can run either on an instance or, optionally, through a MID Server. Use the connection record associated with the Microsoft OneDrive alias to configure where actions run and, if needed, specify MID Server selection attributes. For more information, see [MID server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).

