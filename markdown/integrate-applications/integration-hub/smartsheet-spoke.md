---
title: Smartsheet Spoke
description: The Smartsheet spoke integrates the ServiceNow platform with Smartsheet so that you can automate various actions, such as creating cells in a particular sheet when a database table is updated.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-01-14"
reading_time_minutes: 8
keywords: [AI Agents, Agentic AI]
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Smartsheet Spoke

The Smartsheet spoke integrates the ServiceNow® platform with Smartsheet so that you can automate various actions, such as creating cells in a particular sheet when a database table is updated.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Smartsheet spoke v2.6.1 is the latest version.

## Supported versions

This spoke was built for Smartsheet v1.0.1, but may be compatible with later versions.

## Spoke requirements

You must have a Smartsheet admin account.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Integration Hub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   The latest Smartsheet spoke plugin

**Note:** Some of these plugins are licensable features and need appropriate licenses, if used outside the spoke implementation. For information about licenses, contact your account manager.

## Spoke subflows

The Smartsheet spoke provides sample subflows to demonstrate automating Smartsheet tasks. To customize a sample subflow, copy it to a new application scope. The available sample subflows are described in the following table:

<table id="table_ytq_tvn_bwb"><thead><tr><th>

Subflow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Smartsheet Download Subscriptions

</td><td>

Downloads user subscriptions from the Smartsheet portal. To use this subflow, perform the steps outlined in [Integrating with Smartsheet](https://www.servicenow.com/docs/access?context=integrate-with-smartsheet&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US).

</td></tr><tr><td>

Smartsheet Update User Activity

</td><td>

Retrieves Smartsheet user activity.To use this subflow, perform the steps outlined in [Integrating with Smartsheet](https://www.servicenow.com/docs/access?context=integrate-with-smartsheet&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US).

</td></tr><tr><td>

Smartsheet Reclaim Subscription

</td><td>

Deactivates user accounts in Smartsheet.To use this subflow, perform the steps outlined in [Integrating with Smartsheet](https://www.servicenow.com/docs/access?context=integrate-with-smartsheet&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US).

</td></tr></tbody>
</table>## Spoke actions

The Smartsheet spoke provides actions to automate Smartsheet tasks when events occur in your ServiceNow instance. The available actions are described in the following table:

<table id="table_jrg_1hg_h4b"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="4">

Attachment Management

</td><td>

Attach File to Sheet

</td><td>

Attaches a file to a sheet.

</td></tr><tr><td>

Attach URL to Sheet

</td><td>

Attaches a URL to a sheet.

</td></tr><tr><td>

Look up Attachment by ID

</td><td>

Retrieves the information about the attachments on a sheet.

</td></tr><tr><td>

Look up Attachments Stream

</td><td>

Retrieves the information of all the attachments on a sheet.

</td></tr><tr><td>

Cell History

</td><td>

Look up Cell History Stream

</td><td>

Retrieves the information on the cell modification history.

</td></tr><tr><td rowspan="4">

Column Management

</td><td>

Create Column

</td><td>

Creates the columns in a sheet.

</td></tr><tr><td>

Look up Column by ID

</td><td>

Retrieves the information about a column in a sheet.

</td></tr><tr><td>

Look up Columns Stream

</td><td>

Retrieves the information of all the columns from the sheet.

</td></tr><tr><td>

Update Column

</td><td>

Updates a column in a sheet.

</td></tr><tr><td rowspan="4">

Comment Management

</td><td>

Create Comment

</td><td>

Creates a comment in a sheet.

</td></tr><tr><td>

Create Comment with Attachment

</td><td>

Creates a comment on a discussion with the attachment to a sheet. The comment provides context and useful information.

</td></tr><tr><td>

Look up Comment by ID

</td><td>

Retrieves the information on a comment.

</td></tr><tr><td>

Update Comment

</td><td>

Updates a comment on a sheet.

</td></tr><tr><td rowspan="3">

Cross Sheet Reference Management

</td><td>

Create Cross Sheet Reference

</td><td>

Creates the cross sheet reference between two sheets.

</td></tr><tr><td>

Look up Cross Sheet Reference by ID

</td><td>

Retrieves the information about a cross sheet reference on a particular sheet.

</td></tr><tr><td>

Look up Cross Sheet References Stream

</td><td>

Retrieves the information about all cross sheet references on a particular sheet.

</td></tr><tr><td>

Event Management

</td><td>

Check Event Reporting

</td><td>

Checks if the customer has the event reporting add-on enabled. If enabled, a value of 0 is returned. If not, a value of 1 is returned.

</td></tr><tr><td rowspan="3">

Folder Management

</td><td>

Create Folder

</td><td>

Creates a folder on the Home pane of the Smartsheet project.

</td></tr><tr><td>

Look up Folders Stream

</td><td>

Retrieves the information on all top-level child folders on the Home pane of the Smartsheet project.

</td></tr><tr><td>

Update Folder

</td><td>

Updates the name and the permalink of a folder.

</td></tr><tr><td rowspan="3">

Group Management

</td><td>

Create Group

</td><td>

Creates a group.

</td></tr><tr><td>

Look up Org Groups Stream

</td><td>

Retrieves information on all the groups in the organization.

</td></tr><tr><td>

Update Group

</td><td>

Updates the details of a group.

</td></tr><tr><td rowspan="3">

Row Management

</td><td>

Create Row

</td><td>

Creates a row in a sheet.

</td></tr><tr><td>

Look up Row by ID

</td><td>

Retrieves information on a row in a specific sheet.

</td></tr><tr><td>

Update Row

</td><td>

Updates a row in a sheet.

</td></tr><tr><td rowspan="3">

Send via Email Management

</td><td>

Email Report

</td><td>

Sends a report as an attachment to an email.

</td></tr><tr><td>

Email Sheet

</td><td>

Sends a sheet as an attachment to an email.

</td></tr><tr><td>

Send Rows via Email

</td><td>

Sends rows via email.

</td></tr><tr><td rowspan="3">

Sharing Management

</td><td>

Create Share Sheet

</td><td>

Shares a sheet with users and groups.

</td></tr><tr><td>

Look up Sheet Shares Stream

</td><td>

Retrieves a list of all users and groups that share a sheet.

</td></tr><tr><td>

Update Share Sheet

</td><td>

Updates the access level of a user or a group for a sheet.

</td></tr><tr><td rowspan="4">

Sheet Management

</td><td>

Create Sheet

</td><td>

Creates a sheet in the folder if the folder ID is provided. Else, it creates a sheet in the user's sheet folder.

</td></tr><tr><td>

Look up Sheet by ID

</td><td>

Retrieves information on a sheet.

</td></tr><tr><td>

Look up Sheets Stream

</td><td>

Retrieves a list of all the sheets that the user can access.

</td></tr><tr><td>

Update Sheet

</td><td>

Updates a sheet.

</td></tr><tr><td rowspan="8">

User Management

</td><td>

Create User

</td><td>

Creates a user.

</td></tr><tr><td>

Deactivate User

</td><td>

Deactivates the specified user account in Smartsheet.

</td></tr><tr><td>

Look up Admin User

</td><td>

Retrieves the details of the admin user that generated the access token.

</td></tr><tr><td>

Look up User Activity Stream

</td><td>

Gets the details of user activities.

</td></tr><tr><td>

Look up User by ID

</td><td>

Retrieves the details of a user.

</td></tr><tr><td>

Look up Users Stream

</td><td>

Retrieves the information of all the users.

</td></tr><tr><td>

Remove User

</td><td>

Deactivates a user account.

</td></tr><tr><td>

Update User

</td><td>

Updates the details of a user.

</td></tr><tr><td rowspan="6">

Webhooks Management

</td><td>

Create Webhook

</td><td>

Creates a webhook.

</td></tr><tr><td>

Delete Webhook

</td><td>

Deletes a webhook.

</td></tr><tr><td>

Look up Webhook by ID

</td><td>

Retrieves the details of a webhook.

</td></tr><tr><td>

Look up Webhooks Stream

</td><td>

Retrieves the details of all the webhooks.

</td></tr><tr><td>

Reset Webhook Shared Secret

</td><td>

Resets the shared secret for a webhook.

</td></tr><tr><td>

Update Webhook

</td><td>

Updates the details of a webhook.

</td></tr></tbody>
</table>**Note:** This spoke has a Look up User action and Software Asset Management related actions only.

## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See [Duplicate an AI agent](https://www.servicenow.com/docs/access?context=clone-ai-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for more information about creating a clone.
-   See [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for information about AI agents.

Available AI agents include:

|AI Agent|Description|
|--------|-----------|
|Smartsheet user management AI agent|Enables Process Analysts to automate user management workflows within Smartsheet using Integration Hub. It can automate tasks such as create, update, remove users, and retrieve user information.|
|Smartsheet sheet management AI agent|Enables Process Analysts to automate sheet management workflows within Smartsheet using Integration Hub. It can automate looking up sheets by their ID.|
|Smartsheet column management AI Agent|Assists the Process Analyst in managing and automating column-related tasks in Smartsheet which enables better design and execution of flows in Integration Hub. The agent performs tasks such as fetch list of available columns in a sheet, and a specific column in a sheet.|
|Smartsheet attachment management AI Agent|Enables the Process Analyst to improve Smartsheet workflows by automating attachment-related tasks such as attaching files or URLs, looking up attachment streams, and looking up attachments by ID.|
|Smartsheet group management AI Agent|Enables the Process Analyst to improve group management workflows by automating certain tasks. The Process Analyst can automate tasks such as getting the list of available groups, and update group name.|
|Smartsheet sharing management AI agent|Enables the Process Analyst to improve workflows related to sharing in Smartsheet by automating certain actions such as looking up sheet share streams, and creating share sheets.|
|Smartsheet cross sheet reference management AI agent|Improves workflows related to cross-referencing of sheets by automating certain tasks such as looking up cross-sheet references stream and by ID, and creating a cross-sheet.|
|Smartsheet row management AI agent|Automates row management by performing certain tasks such as creating new rows, helping users manage data effectively and optimize their processes.|
|Smartsheet comment management AI agent|Automates various tasks related to comments such as adding a comment, adding a comment with attachment, updating a comment, and look up for a comment.|
|Smartsheet cell history AI agent|Automates various tasks related to the history of the data in the cells such as looking up cell history stream to retrieve and analyze historical data from Smartsheet cells,|
|Smartsheet folder management AI agent|Automates folder-related tasks such as fetch list of available folders, create a new folder, and update a folder.|

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

