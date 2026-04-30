---
title: Box Spoke
description: Move attachments to Box where they can be managed as shared documents.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-12-01"
reading_time_minutes: 12
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Box Spoke

Move attachments to Box where they can be managed as shared documents.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Box spoke v3.6.0 is the latest version.

## Supported versions

API version v2.

## Spoke requirements

Ensure that same languages are selected in your ServiceNow instance and Box account.

-   In your ServiceNow instance, select the required language by navigating to **User Profile** &gt; **Preferences** &gt; **Display**.

    ![Set language in ServiceNow instance.](../image/servicenow-language.png)

-   In your Box account, select the required language by navigating to **Account Settings** &gt; **Account** &gt; **General Options**.

    ![Set language in Box account.](../image/box-language.png)


## Spoke flows

The Box spoke provides sample flows in the draft state to demonstrate automating Box tasks. To customize a sample flow, copy it to a new application scope. Available sample flows include:

|Flow|Description|
|----|-----------|
|Move Attachment when created to Box|Moves attachment files from ServiceNow to Box when a new attachment record is added. Updates the trigger record with a shared link to the moved attachment file on Box.|
|On-boarding user|Creates a user in Box when you create a ServiceNow user in the **Box User** group.|

## Spoke actions

The Box spoke provides actions to automate Box tasks when events occur in ServiceNow. Available actions include:

<table id="table_qpz_ktb_x2b"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="3">

Box AI Management

</td><td>

Ask Question

</td><td>

Sends a prompt to the supported AI models using the provided context and returns a brief answer focused on the user’s question.

</td></tr><tr><td>

Extract Metadata Freeform

</td><td>

Sends a context‑aware request to supported AI models and extracts metadata as structured key‑value pairs.

</td></tr><tr><td>

Look up AI Agent Default Configuration

</td><td>

Retrieves the default configuration settings for the specified AI agent.

</td></tr><tr><td rowspan="3">

Box Hub Management

</td><td>

Look up Box Hub Info by ID

</td><td>

Retrieves details for a Box Hub using the specified Hub ID.

</td></tr><tr><td>

Look up Box Hub Items Stream

</td><td>

Retrieves all items associated with the specified Box Hub.

</td></tr><tr><td>

Look up Box Hubs Stream

</td><td>

Retrieves all Box Hubs available to the requesting user based on the Box credentials used to generate the access token.

</td></tr><tr><td rowspan="8">

Document Management

</td><td>

Add Metadata to File

</td><td>

Stores the provided attributes information by adding it as metadata for Box files.

</td></tr><tr><td>

Attach Box File to Record

</td><td>

Copies a file from Box and attaches it to the specified ServiceNow record.

</td></tr><tr><td>

Lookup File ID

</td><td>

Retrieves the ID of the specified file in Box.

</td></tr><tr><td>

Move Owned Item

</td><td>

Moves all items owned by the specified user in Box to the specified folder.

</td></tr><tr><td>

Remove File

</td><td>

Removes the specified file from Box.

</td></tr><tr><td>

Search Content Stream

</td><td>

Searches for files, folders, web links, and shared files across the user's content or across the entire enterprise.

</td></tr><tr><td>

Upload File

</td><td>

Uploads the specified file to Box.

</td></tr><tr><td>

Look up Archives Stream

</td><td>

Retrieves all available archives from the Box application.

</td></tr><tr><td rowspan="4">

Document Sharing

</td><td>

Add Collaborator

</td><td>

Grants a user or group a specified level of access to a particular file or folder. Collaborators have one of these access levels.-   Co-Owner
-   Editor
-   Previewer
-   Preview Uploader
-   Uploader
-   Viewer
-   Viewer Uploader

</td></tr><tr><td>

Create Shared Link

</td><td>

Create a direct and read-only link to a file or folder in Box.

</td></tr><tr><td>

Look up Folder Collaborators By ID

</td><td>

Retrieves all the collaborators associated to the specified folder ID.

</td></tr><tr><td>

Remove Collaborator

</td><td>

Removes the specified collaboration from a file or folder in Box.

</td></tr><tr><td>

File Management

</td><td>

Look up File Information

</td><td>

Retrieves detailed information for the specified file.

</td></tr><tr><td rowspan="5">

Folder Management

</td><td>

Create Folder

</td><td>

Creates a folder in Box on behalf of the specified Box user account.

</td></tr><tr><td>

Delete Folder

</td><td>

Deletes the specified folder in Box.

</td></tr><tr><td>

Lookup Folder ID

</td><td>

Retrieves the ID of the specified folder in Box.**Note:** Items added to Box require 10 minutes to become accessible. For example, if one action creates a folder, a Lookup Folder ID action won’t return results until after 10 minutes have passed.

</td></tr><tr><td>

Look up Folder Information

</td><td>

Retrieves details for the specified folder.

</td></tr><tr><td>

Look up Folder Items Stream

</td><td>

Retrieves all items within the specified folder, including files, subfolders, and web links.

</td></tr><tr><td rowspan="3">

Group Management

</td><td>

Create Group

</td><td>

Creates a group in Box with the specified invitation preferences.

</td></tr><tr><td>

Delete Group

</td><td>

Deletes the specified group in Box.

</td></tr><tr><td>

Update Group

</td><td>

Updates the specified group in Box with the specified preferences.

</td></tr><tr><td rowspan="9">

Legal Hold Management

</td><td>

Assign Legal Hold Policy

</td><td>

Assigns a legal hold policy to a file, file version, folder, or user.

</td></tr><tr><td>

Create Legal Hold Policy

</td><td>

Creates a legal hold policy.

</td></tr><tr><td>

Look up All Legal Hold Policies Stream

</td><td>

Retrieves a list of legal hold policies of an enterprise.

</td></tr><tr><td>

Look up Legal Hold Policy Assignment by ID

</td><td>

Retrieves a legal hold policy assignment for the specified ID.

</td></tr><tr><td>

Look up Legal Hold Policy Assignments Stream

</td><td>

Retrieves a list of items assigned to a legal hold policy.

</td></tr><tr><td>

Look up Legal Hold Policy by ID

</td><td>

Retrieves a legal hold policy for the specified ID.

</td></tr><tr><td>

Remove legal hold policy

</td><td>

Deletes an existing legal hold policy.

</td></tr><tr><td>

Unassign Legal Hold Policy

</td><td>

Removes the assignment of an item to a legal hold.

</td></tr><tr><td>

Update Legal Hold Policy

</td><td>

Updates a legal hold policy.

</td></tr><tr><td rowspan="5">

Metadata Management

</td><td>

Look up Metadata Instance on File By File ID

</td><td>

Retrieves the metadata instance of the file with the specified file ID.

</td></tr><tr><td>

Look up Metadata Instance on File by Scope and Template Key

</td><td>

Retrieves the metadata instance of a folder with the specified scope and template key.

</td></tr><tr><td>

Look up Metadata Instance on Folder By Folder ID

</td><td>

Retrieves all the metadata of the folder with the specified folder ID. **Note:** Don’t use this action on a root folder that has a folder ID value as zero.

</td></tr><tr><td>

Look up Metadata Instance on Folder by Scope and Template Key

</td><td>

Retrieves all the metadata of a folder with the specified scope and template key.

</td></tr><tr><td>

Query Files or Folders by Metadata Stream

</td><td>

Searches for files or folders using SQL-like syntax and returns the matching results.

</td></tr><tr><td rowspan="7">

Retention Policy Management

</td><td>

Assign Retention Policy

</td><td>

Assigns a retention policy to an item.

</td></tr><tr><td>

Create Retention Policy

</td><td>

Creates a retention policy.

</td></tr><tr><td>

Look up Retention Policies

</td><td>

Retrieves all the retention policies of an enterprise.

</td></tr><tr><td>

Look up Retention Policy Assignment By ID

</td><td>

Retrieves the retention policy with the specified ID.

</td></tr><tr><td>

Look up Retention Policy Assignments Stream

</td><td>

Returns a list of all retention policy assignments associated with a specified retention policy.

</td></tr><tr><td>

Look up Retention Policy by ID

</td><td>

Retrieves the retention policy with the specified ID.

</td></tr><tr><td>

Update Retention Policy

</td><td>

Updates a retention policy.

</td></tr><tr><td rowspan="7">

User Management

</td><td>

Add User to Group

</td><td>

Adds the specified user to the specified group in Box.

</td></tr><tr><td>

Create User

</td><td>

Creates a user account in Box.

</td></tr><tr><td>

Delete User

</td><td>

Deletes the specified user in Box.

</td></tr><tr><td>

Disable User

</td><td>

Sets the status of the specified user in Box to inactive.

</td></tr><tr><td>

Enable User

</td><td>

sets the status of the specified user in Box to active.

</td></tr><tr><td>

Lookup User ID

</td><td>

Retrieves the ID of the specified user in Box.

</td></tr><tr><td>

Update User

</td><td>

Updates the specified user in Box with the specified role changes.

</td></tr><tr><td rowspan="5">

Webhook Management

</td><td>

Create Webhook

</td><td>

Creates a webhook.

</td></tr><tr><td>

Look up Webhook By ID

</td><td>

Retrieves the webhook with the specified ID.

</td></tr><tr><td>

Look up Webhooks Stream

</td><td>

Retrieves all the defined webhooks for the specified application.

</td></tr><tr><td>

Remove Webhook

</td><td>

Removes a webhook.

</td></tr><tr><td>

Update Webhook

</td><td>

Updates a webhook.

</td></tr></tbody>
</table>## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See [Duplicate an AI agent](https://www.servicenow.com/docs/access?context=clone-ai-agent&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) for more information about creating a clone.
-   See [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) for information about AI agents.

Available AI agents include:

<table id="table_tmt_mkc_1fc"><thead><tr><th>

AI agent

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Box user management AI agent

</td><td>

Manages user management tasks \(that is, adds a user to group, enables a user, create user, delete user, update user, look up user ID, disable user\) in Box.**Note:** This AI agent is supported on Xanadu Patch 9 and later releases.

</td></tr><tr><td>

Box folder management AI agent

</td><td>

Manages folder management tasks \(that is, create a folder, look up the folder ID, delete a folder\) in Box.**Note:** This AI agent is supported on Xanadu Patch 9 and later releases.

</td></tr><tr><td>

Box document sharing AI agent

</td><td>

Manages document sharing tasks \(that is, remove a collaborator, add a collaborator, create a shared link, look up the folder collaborators by ID\) in Box.

 **Note:** This AI agent is supported on Xanadu Patch 9 and later releases.

</td></tr><tr><td>

Box group management AI agent

</td><td>

Manages group management tasks \(that is, update a group, create a group, delete a group\) in Box.**Note:** This AI agent is supported on Xanadu Patch 9 and later releases.

</td></tr><tr><td>

Box metadata management AI agent

</td><td>

Manages metadata retrieval tasks \(that is, look up a metadata instance on a file by scope and template key, look up a metadata instance on a folder by folder ID, look up a metadata instance on a folder by scope and template key, look up a metadata instance on a file by file ID\) in Box.**Note:** This AI agent is supported on Xanadu Patch 9 and later releases.

</td></tr><tr><td>

Box retention policy management AI agent

</td><td>

Manages retention policy management tasks \(that is, update a retention policy, look up a retention policies stream, look up a retention policy assignment by id, look up a retention policy by id, look up a retention policy assignments stream\) in Box.**Note:** This AI agent is supported on Xanadu Patch 9 and later releases.

</td></tr><tr><td>

Box document management AI agent

</td><td>

Manages document management tasks \(that is, remove a file, attach a box file to a record, upload a file, move an owned item, search a content stream, look up a file ID, add metadata to a file\) in Box.**Note:** This AI agent is supported on Xanadu Patch 9 and later releases.

</td></tr><tr><td>

Box legal hold management AI agent

</td><td>

Manages legal hold management tasks \(that is, create a legal hold policy, look up a legal hold policy assignment by ID, update a legal hold policy, look up all legal hold policies stream, look up a legal hold policy by ID, unassign a legal hold policy, remove a legal hold policy, look up a legal hold policy assignments stream\) in Box.**Note:** This AI agent is supported on Xanadu Patch 9 and later releases.

</td></tr></tbody>
</table>Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## Spoke triggers

ServiceNow supports specific events on Box that create triggers. You must first configure a flow with a supported trigger definition. When an event, for example, a push request, occurs on the Box, it sends the payload via a webhook to the ServiceNow instance. After that, the flow that you configured is triggered at the ServiceNow instance to automate a workflow. The supported events are:

|Category|Trigger|Description|
|--------|-------|-----------|
|File Management|File Downloaded|Flow is triggered when a file is downloaded.|
|File Locked|Flow is triggered when a file is locked.|
|File Moved|Flow is triggered when a file is moved.|
|File Renamed|Flow is triggered when a file is renamed.|
|File Unlocked|Flow is triggered when a file is unlocked.|
|File Uploaded|Flow is triggered when a file is uploaded.|
|Folder Management|Folder Created|Flow is triggered when a folder is created.|
|Folder Downloaded|Flow is triggered when a folder is downloaded.|
|Folder Moved|Flow is triggered when a folder is moved.|
|Folder Renamed|Flow is triggered when a folder is renamed.|

For information about setting up the triggers for the Box spoke, see [Set up triggers for the Box spoke](../task/box-spk-triggers-setup.md#). For more information about inbound integration, see [Conditional and event-driven inbound integration](../../integrationhub/concept/conditional-and-event-driven-inbound-integration.md).

## Spoke user roles

The following user roles are available with the spoke:

-   Policy User \(sn\_box\_spoke.box\_policies\_user\): Users with this role have access only to **Retention Policies** module.
-   Legal Hold Policy User \(sn\_box\_spoke.legal\_hold\_policy\_user\): Users with this role have access only to the **Legal Hold Policies** module.
-   Box Webhook Registry User \(sn\_box\_spoke.box\_webhook\_registry\_user\): Users with this role have access only to the **Box Webhook Registry** module.

## Box spoke module

Bi-directional webhooks can be set up to be notified about the required events. A webhook registry defines the conditions that must be met to notify the ServiceNow app. These conditions are based on the events in Box that you want to be notified about. When the conditions are met, the specified trigger name triggers the associated subflow, which in turn automates the Box tasks.

Webhooks require separate setup and can be used independently without using the spoke actions. The Box spoke adds the Box Spoke application to your instance and includes the following modules.

|Module|Description|
|------|-----------|
|Box Webhook Registry|Create and view the Box webhooks in ServiceNow.|
|Legal Hold Policies|View the list of available Box legal policies.|
|Retention Policies|View the list of available Box retention policies.|

## Box account requirements

The Box spoke requires creating a custom app on your Box account to generate OAuth 2.0 tokens. See [Create an OAuth application](../task/setup-box-spoke.md#).

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

This spoke uses the following alias records to authorize actions.

<table id="table_nnk_g2h_gfb"><thead><tr><th>

Connection &amp; Credential alias

</th><th>

Description

</th><th>

Connection alias requirements

</th></tr></thead><tbody><tr><td>

Box

</td><td>

Connection to the Box Collaboration and File Management APIs.

</td><td>

-   Connection type: HTTP
-   Connection URL: https://api.box.com

</td></tr><tr><td>

Box Upload

</td><td>

Connection to the Box upload service.

</td><td>

-   Connection type: HTTP
-   Connection URL: https://upload.box.com

</td></tr></tbody>
</table>To use the spoke connection aliases, create an associated Connection record and an associated Credential record for each alias. For information about setting up the spoke, see [Set up the Box spoke](../task/setup-box-spoke.md#).

