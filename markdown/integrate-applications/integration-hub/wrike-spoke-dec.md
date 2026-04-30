---
title: Wrike Spoke
description: Manage approvals, attachments, folders, projects, and so on, in the Wrike account from your ServiceNow instance.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-09-02"
reading_time_minutes: 5
keywords: [AI Agents, Agentic AI]
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Wrike Spoke

Manage approvals, attachments, folders, projects, and so on, in the Wrike account from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Wrike spoke v1.3.0 is the latest version.

## Supported versions

This spoke was built for Wrike API version v4, but may be compatible with later versions.

**Note:** You must have the Wrike Enterprise account to create an app and obtain values of Client ID and Client Secret from the Wrike account.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Wrike spoke provides actions to automate Wrike tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Approvals Management|Create Approval for Folder|Creates an approval for the specified folder or project.|
|Create Approval for Task|Creates an approval for the specified folder task.|
|Delete Approval|Cancels the specified approval.|
|Look up Approvals|Retrieves details of the approvals based on the filter criteria.|
|Look up Approvals by Folder|Retrieves all approvals on the specified folder or project.|
|Look up Approvals by Task|Retrieves all approvals on the specified task.|
|Update Approval|Updates details of the specified approval.|
|Attachment Management|Delete Attachment|Deletes the specified attachment.|
|Download Attachment to ServiceNow|Downloads attachment to the specified ServiceNow record.|
|Look up Attachments|Retrieves list of attachments.|
|Update Attachment|Updates a previously uploaded attachment with the new version.|
|Update Attachment to Folder|Uploads an attachment to the specified folder.|
|Update Attachment to Task|Adds an attachment to a task record.|
|Comment Management|Create Comment in Folder|Creates a comment in the folder.|
|Create Comment in Task|Creates comment in task.|
|Delete Comment|Deletes the specified comment.|
|Look up Comments by Folder ID|Retrieves the folder comments.|
|Look up Comments by Task ID|Retrieves the task comments.|
|Update Comment|Updates the specified comment.|
|Folder and Project Management|Create Folder|Creates a folder within a folder.|
|Create Project|Creates a project within a folder.|
|Delete Folder or Project|Moves folder, project and all descendant folders and tasks to Recycle Bin unless they have parents outside of deletion scope.|
|Look up Folders|Retrieves the list of entries required to build a folder tree for the current account.|
|Update Folder|Updates details of the folder.|
|Update Project|Updates details of the project.|
|Group Management|Create Group|Creates group in account.|
|Delete Group|Deletes the specified group.|
|Look up Groups|Retrieves all groups in the account.|
|Update Group|Updates details of the specified group.|
|Task Management|Create Task|Creates a task in folder.|
|Delete Task|Deletes the specified task.|
|Look up Tasks|Retrieves details of all tasks in current account.|
|Update Task|Updates details of the specified task.|
|User Management|Get User Details|Retrieves information about the specified user.|
|Look up Contacts|Retrieves contacts of all users and user groups in the current account.|
|Update User Details|Updates details of the specified user.|

## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See [Duplicate an AI agent](https://www.servicenow.com/docs/access?context=clone-ai-agent&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information about creating a clone.
-   See [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for information about AI agents.

Available AI agents include:

|AI Agent|Description|
|--------|-----------|
|Wrike attachment management AI agent|Enables the Process Analysts to automate attachment-related workﬂows within Wrike using Integration Hub. It can automate actions such as updating attachments to tasks or folders, downloading attachments to ServiceNow, and deleting attachments.|
|Wrike approvals management AI agent|Enables the Process Analysts to automate approval workﬂows in Wrike using Integration Hub. It can automate tasks such as deleting approvals for tasks or folders.|
|Wrike comment management AI agent|Enables the Process Analyst to automate comment-related tasks in Wrike, such as creating, updating, and deleting comments by folder or task ID.|
|Wrike group management AI agent|Enables the Process Analysts to automate group-related tasks in Wrike using Integration Hub. It can automate actions such as deleting groups to enable efﬁcient group management.|
|Wrike task management AI agent|Enables the Process Analysts to automate tasks in Wrike such as deleting a task.|
|Wrike user management AI agent|Enables the Process Analysts to automate user and contact management tasks, such as updating user details and retrieving user details.|
|Wrike folder and project management AI agent|Enables the Process Analyst to automate folder and project management tasks such as deleting folders and projects.|

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Wrike spoke](../task/wrike-setup-dec.md).

