---
title: Slack Spoke
description: Use the Slack spoke to post messages and manage access to channels.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Slack Spoke

Use the Slack spoke to post messages and manage access to channels.

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf). To learn more about the subscription, contact your account manager.

## Spoke version

The Slack spoke v1.8.0 is the latest version.

## Slack account requirements

The Slack spoke requires creating a workspace and custom app on your Slack account to generate the OAuth 2.0 tokens for the Slack spoke. See [Configure Slack app](../tasks/configure-slack-workspace.md).

**Note:** The spoke set up procedure outlined here requires bot user tokens only. You can't use the Create User and Deactivate User actions while using the bot token scopes. To use these actions, you must obtain user token from your Slack account.

## Spoke subflows

The Slack spoke provides some sample subflows to demonstrate automating the Slack workspace tasks. To customize a sample subflow, copy it to a new application scope. Available sample subflows include:

<table id="table_xg2_mgg_3mb"><thead><tr><th>

Subflow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Insert Slack User Details by Member ID

</td><td>

Inserts details of the required user in the Slack User Cache module, based on the Member ID.

</td></tr><tr><td>

Insert Slack User Details by User ID

</td><td>

Inserts details of the required user in the Slack User Cache module, based on the User ID.

</td></tr><tr><td>

Post Actionable Message

</td><td>

Posts an actionable message to a Slack channel.**Note:** This subflow requires an outbound configuration as an input. Customize the default outbound configurations or create an outbound configuration as per your requirement. For more information, see [Configure outbound configurations in ServiceNow instance](../../integrationhub-store-spokes/task/conf-outbound-slack.md).

</td></tr><tr><td>

Post Approval Message

</td><td>

Posts an approval message to a Slack channel.**Note:** This subflow requires an outbound configuration as an input. Customize the default outbound configurations or create an outbound configuration as per your requirement. For more information, see [Configure outbound configurations in ServiceNow instance](../../integrationhub-store-spokes/task/conf-outbound-slack.md).

</td></tr><tr><td>

Respond to Slack Approval Message

</td><td>

Posts an acknowledgment message on a Slack channel.

</td></tr><tr><td>

Respond to Slack Command

</td><td>

Posts a response to a command on a Slack channel.

</td></tr><tr><td>

Respond to Slack Message Action

</td><td>

Posts a notification on a Slack channel.

</td></tr></tbody>
</table>While customizing the subflows, make sure that the subflows are configured to avoid infinite loops.

## Spoke actions

The Slack spoke provides actions to automate the Slack workspace tasks when events occur in the ServiceNow instance. Available actions include:

<table id="table_u1p_kh2_hfb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="12">

Conversation Management

</td><td>

Add User to Channel

</td><td>

Adds an existing user to the specified channel in the Slack workspace.

</td></tr><tr><td>

Archive Channel

</td><td>

Archives a channel in a Slack workspace.

</td></tr><tr><td>

Rename Conversation

</td><td>

Renames a conversation.

</td></tr><tr><td>

Look up Conversation Info

</td><td>

Retrieves information about a conversation.

</td></tr><tr><td>

Create Channel

</td><td>

Creates a channel in a Slack workspace.

</td></tr><tr><td>

Look Up Attachments Stream By Conversation or Member ID

</td><td>

Retrieves attachments related with the relevant channel, member, or bot user.

</td></tr><tr><td>

Look up Channel History Stream

</td><td>

Retrieves the history of a channel. You must provide the channel ID, and the start and end date as inputs.

</td></tr><tr><td>

Look up Conversation

</td><td>

Retrieves the conversation messages for a thread from the specified channel.

</td></tr><tr><td>

Open Conversation

</td><td>

Opens or resumes a direct message or a multi-person direct message.

</td></tr><tr><td>

Look up Conversation IDs Stream by Member ID

</td><td>

Retrieves details of the Conversation IDs related with the specified member on Slack.

</td></tr><tr><td>

Set Topic for Channel

</td><td>

Sets the topic for a Slack channel.

</td></tr><tr><td>

Remove User from Channel

</td><td>

Removes a user from a channel in the Slack workspace.

</td></tr><tr><td rowspan="8">

Notification Management

</td><td>

Post Actionable Message

</td><td>

Posts an actionable message to a Slack channel.**Note:** This action requires an outbound configuration as an input. Customize the default outbound configurations or create an outbound configuration as per your requirement. For more information, see [Configure outbound configurations in ServiceNow instance](../../integrationhub-store-spokes/task/conf-outbound-slack.md).

</td></tr><tr><td>

Post Approval Message

</td><td>

Posts an approval message to a Slack channel.**Note:** This action requires an outbound configuration as an input. Customize the default outbound configurations or create an outbound configuration as per your requirement. For more information, see [Configure outbound configurations in ServiceNow instance](../../integrationhub-store-spokes/task/conf-outbound-slack.md).

</td></tr><tr><td>

Post Change Details

</td><td>

Posts Change record details to a channel.

</td></tr><tr><td>

Post Incident Details

</td><td>

Posts Incident record details to a channel.

</td></tr><tr><td>

Post Message

</td><td>

Posts a message to a Slack Channel.

</td></tr><tr><td>

Post Response to Slack

</td><td>

Posts a response to Slack.

</td></tr><tr><td>

Update Approval Record

</td><td>

Updates an approval record.

</td></tr><tr><td>

Post Problem Details

</td><td>

Posts a Problem record detail to a channel.

</td></tr><tr><td rowspan="6">

User Management

</td><td>

Create User

</td><td>

Creates a user in the Slack workspace.**Note:** This action requires a user token from the Slack account. If you have bot user tokens, you can't use this action.

</td></tr><tr><td>

Deactivate User

</td><td>

Deactivates the specified user from the Slack workspace.**Note:**

This action requires a user token from the Slack account. If you have bot user tokens, you can't use this action.

</td></tr><tr><td>

Look up User

</td><td>

Returns information about the specified user or bot. The information can be name, time zone, workspace admin rights, and team ownership of a user or bot.

</td></tr><tr><td>

Deactivate Subscription

</td><td>

Deactivates a user subscription in Slack. To use this action, perform the steps outlined in the Create a Slack Enterprise Grid application and Create a Slack Enterprise connection section in Integrating with Slack.

</td></tr><tr><td>

Look up Access Logs Stream

</td><td>

Retrieves the access logs for all users since the provided oldest date. To use this action, perform the steps outlined in the Create a Slack workspace application and Create a Slack workspace connection section in Integrating with Slack.

</td></tr><tr><td>

Look up Users Stream

</td><td>

Retrieves all users in the Slack Enterprise grid. To use this action, perform the steps outlined in the Create a Slack Enterprise Grid application and Create a Slack Enterprise connection section in Integrating with Slack.

</td></tr></tbody>
</table>**Note:**

-   Create User and Deactivate User actions require the admin scope. The spoke set up procedure outlined here requires bot user tokens only. You can't use the Create User and Deactivate User actions while using the bot token scopes. To use these actions, you must obtain user token from your Slack account.
-   The admin scope is available to Slack workspace owners only.

## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See Create an agentic workflow for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See Find AI agents for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See Duplicate an AI agent for more information about creating a clone.
-   See Now Assist AI agents for information about AI agents.

Available AI agents include:

|AI Agent|Description|
|--------|-----------|
|Slack user manager|Manages Slack users and integrates Slack actions with the ServiceNow workflows. It looks up users and streamlines user management and communication within the Slack Channels.|
|Slack notification manager|Automates workflows by executing the Slack Spoke actions. It enables the users to send notifications and updates such as details of incidents, problems, changes, and requests to the Slack channels. It streamlines communication and manages notifications better.|
|Slack conversation manager|Performs actions such as setting channel topics, renaming conversations, adding or removing users from channels, creating and archiving channels.|

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see Find AI agents.

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## Spoke modules

The Slack spoke adds the Slack application to your ServiceNow instance. The Slack application includes these modules:

<table id="table_czw_rch_3mb"><thead><tr><th>

Module

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Slack Modal Configuration

</td><td>

Create modals and specify fields that should be displayed in your Slack modal.

</td></tr><tr><td>

Slack User Cache

</td><td>

Access information about users who have performed actions on the Slack channel that needed updates in the ServiceNow instance or a response from the ServiceNow instance.

</td></tr><tr><td>

Slack Channel Cache

</td><td>

Access information about the channels on which actions are performed that needed updates in the ServiceNow instance or response from ServiceNow instance.

</td></tr><tr><td>

Inbound Decisions

</td><td>

Specify events in Slack application for which actions must be performed in ServiceNow instance.For example, you can specify inbound decisions to update the task details in your ServiceNow instance when an approver approves the task on the relevant Slack channel. Five sample inbound decisions are available for your reference. Customize these decisions or create inbound decisions as per your requirement.

 When the conditions mentioned in the inbound decisions are met, the associated subflow is triggered and a record is created in the Slack User Cache module for the Slack user, who initiated the inbound action.

</td></tr><tr><td>

Inbound Decisions for Modals

</td><td>

Specify subflows that must be triggered when the required inbound decisions are met.When the conditions mentioned in the inbound decisions are met, the associated subflow is triggered and a record is created in the Slack User Cache module for the Slack user, who initiated the inbound action.

</td></tr><tr><td>

Slack Outbound Choices

</td><td>

Choices that should be displayed as a list on the Slack channels.

</td></tr><tr><td>

Inbound Slack Message

</td><td>

Access information about the inbound messages to your ServiceNow instance from the Slack application.

</td></tr><tr><td>

Outbound Configurations

</td><td>

Specify events in ServiceNow instance for which actions must be performed on Slack application.For example, you can specify outbound configurations to send a message on Slack channel asking for approval when a task is created in your ServiceNow instance. Three sample outbound configurations are available for your reference. Customize these configurations or create outbound configurations as per your requirement.

 The outbound configurations also provide a template to the Post Actionable Message and Post Approval Message actions. For example, you can configure the outbound configurations to display the **Approve** and **Reject** buttons in the approval message that is sent on the relevant Slack channel.

 When the configurations mentioned in the outbound configurations are met, the relevant subflow is triggered to perform actions in the Slack application.

</td></tr><tr><td>

Slack Configurations

</td><td>

Provide information about the Slack app and Signing Key.

</td></tr></tbody>
</table>Data in these modules is populated from these spoke tables:

<table id="table_zys_1bq_gnb"><thead><tr><th>

Table

</th><th>

Fields

</th></tr></thead><tbody><tr><td>

Slack Channel Cache \[sn\_slack\_ah\_v2\_slack\_channel\_cache\]

</td><td>

-   Channel ID
-   Channel Link
-   Channel Name
-   Creator
-   Document ID
-   Is Archived
-   Is Private
-   Source table

</td></tr><tr><td>

Slack Configurations \[sn\_slack\_ah\_v2\_slack\_configurations\]

</td><td>

-   Client Secret
-   Connection Alias
-   Property Name
-   Slack App

</td></tr><tr><td>

Slack Credential \[sn\_slack\_ah\_v2\_slack\_credential\]

</td><td>

-   Authentication Key
-   Active
-   Context Name
-   Domain Name
-   Privacy Key

</td></tr><tr><td>

Slack Outbound Choices \[sn\_slack\_ah\_v2\_slack\_outbound\_choices\]

</td><td>

-   Name
-   Active
-   Language
-   Sequence
-   Domain
-   Value

</td></tr><tr><td>

Slack User Cache \[sn\_slack\_ah\_v2\_slack\_user\_details\]

</td><td>

-   Display Name
-   Slack Member ID
-   Team ID
-   User

</td></tr><tr><td>

Slack Workspace Tokens \[sn\_slack\_ah\_v2\_slack\_workspace\_tokens\]

</td><td>

-   Connection Alias
-   Slack App
-   Workspace Name

</td></tr><tr><td>

Slack Modal Configuration \[sn\_slack\_ah\_v2\_slack\_modal\_configuration\]

</td><td>

-   Modal Title
-   Name
-   Script Validation
-   Custom Modal

</td></tr></tbody>
</table>## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up Slack spoke](../../integrationhub-store-spokes/task/set-up-slack.md).

