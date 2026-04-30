---
title: Google Drive Spoke
description: Use Google Drive as file storage in place of attachments in ServiceNow. Adds Google Drive storage to your ServiceNow instance and enables users to reference Google Drive files in ServiceNow records.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-09-02"
reading_time_minutes: 6
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Google Drive Spoke

Use Google Drive as file storage in place of attachments in ServiceNow. Adds Google Drive storage to your ServiceNow instance and enables users to reference Google Drive files in ServiceNow records.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Google Drive spoke v2.3.0 is the latest version.

## Supported versions

API version v3.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   Complex Object \(com.glide.cobject\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Spoke actions

The Google Drive spoke provides actions to perform Google Drive tasks when events occur in ServiceNow. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|File and Folder Management|Copy Attachment to Drive|Copies a ServiceNow attachment to a Google Drive folder. It either copies to the root drive of the current account or to the specified folder. To change the file name during the copy, use the optional file name.|
|Copy Doc File to Attachment|Copies a file Google Drive and attaches it to a ServiceNow record.|
|Copy File|Creates a copy of a Google Drive File and applies any metadata updates like a change in file name, file description, parent folder location, if file is starred, or shared by users with writer permissions.|
|Copy Drive File To Attachment|Copies a drive file to a ServiceNow attachment. If a ServiceNow record is supplied as input, the record should be attached to it.|
|Copy File Revision as Attachment|Copies the revision ID of a file ID to any record on the ServiceNow instance.|
|Create Folder|Creates a Google Drive folder that can be nested within other folders.|
|Delete Drive File Or Folder|Permanently deletes a drive file or folder owned by the Google Drive account user without moving it to the trash. To delete folders the user must be the owner of folder and its contents|
|Delete File Revision|Deletes a revision to a file.|
|Look up Files and Folders Stream|Retrieves the list of files and folders.|
|Look up File Revisions Stream|Retrieves the list of all revisions to a file.|
|Look up File|Retrieves the metadata information from a file ID.|
|Look up Files Stream|Retrieves a list of Google Drive files based on the given search parameters.|
|Look up Folders Stream|Retrieves a list of Google Drive folders based on the given search parameters.|
|Update Attachment To Drive|Updates the contents of a file, but maintains the previous versions and metadata. This action only updates the content of the Google Drive file. It does not update metadata.|
|Update File Or Folder Metadata|Updates the metadata on a file or folder. This can be a file name change, change to the file description, a move to a new parent folder, a change in starred status, or a change to sharing permissions.|
|Look up Files or Folders by Name|Retrieves the details of the files or folders including ID for the specified file name or folder name.|
|Permission Management|Create File or Folder Permission|Adds a permission to a given user, group, domain, or anyone for a file or folder. If User or Group is selected, the email address is required for those users and groups. If Domain is selected, the domain name is required. If Anyone is selected, then anyone has permissions to the file or folder.|
|Delete File Or Folder Permission|Removes a permission to a given user, group, domain, or anyone for a file or folder.|
|Look up Permissions Stream|Retrieves the list of files or shared drives permissions.|
|Transfer Ownership Of All User Data|Transfers the ownership of data from one user to another within a domain. All previous permissions of old owner are removed and new owner permissions are created for new user.|
|Update File Or Folder Permission|Updates a given permission by updating the role.|

## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See [Duplicate an AI agent](https://www.servicenow.com/docs/access?context=clone-ai-agent&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) for more information about creating a clone.
-   See [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) for information about AI agents.

Available AI agents include:

|AI Agents|Description|
|---------|-----------|
|Google Drive permission manager AI agent|Manages file or folder permissions\(create file or folder permission, transfer ownership of all user data, update file or folder permission, delete file or folder permission\) in Google Drive.|
|Google Drive file and folder manager AI agent|Manages files and folders\(copy doc file to attachment, copy file revision as attachment, delete file or folder, update attachment to drive, copy drive file to attachment, copy attachment to drive, copy file, delete file revision, create folder, look up files or folders by name, update file or folder metadata, look up file\) in Google Drive.|

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## Google Drive Online account requirements

The Google Drive spoke requires a custom app that you create in Google Drive Enterprise or [Google G Suite](https://gsuite.google.com/).

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up Google Drive spoke](../task/setup-gdrive.md#).

## MID Server requirements

These actions use REST calls that can run either on an instance or, optionally, through a MID Server. Use the connection record associated with the Google Drive alias to configure where actions run and, if needed, specify MID Server selection attributes. For more information, see [MID server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).

