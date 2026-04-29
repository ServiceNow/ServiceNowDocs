---
title: Miro Spoke
description: The Miro spoke provides actions to view and analyze meaningful usage data for Miro software subscriptions. Analyze usage for your Miro Enterprise account to determine which licenses are stale so that you can reclaim these licenses and realize your potential savings.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Miro Spoke

The Miro spoke provides actions to view and analyze meaningful usage data for Miro software subscriptions. Analyze usage for your Miro Enterprise account to determine which licenses are stale so that you can reclaim these licenses and realize your potential savings.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Miro spoke v3.3.1 is the latest version.

## Supported version

This spoke was built for Miro Enterprise version v2 and Miro SCIM version v1, but may be compatible with later versions.

## Spoke requirements

-   Miro Company Admin account
-   SSO/SAML enabled on your Miro account

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Integration Hub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Miro spoke provides actions to automate Miro tasks when events occurs in your ServiceNow instance. Available actions include:

**Note:** To prevent unauthorised access, make sure that the required scope in Miro has the least privileges for the spoke actions.

|Category|Action|Description|Miro required scopes|
|--------|------|-----------|--------------------|
|Board Item Management|Add Card Item to Board|Adds a card item to a board in Miro.|boards:write|
|Add Shape Item to Board|Adds a shape item to a board in Miro.|boards:write|
|Add Sticky Note Item to Board|Adds a sticky note item to a board in Miro.|boards:write|
|Add Text Item to Board|Adds a text item to a board in Miro.|boards:write|
|Board Management|Create Board|Creates a board in Miro.|boards:write|
|Delete Board|Deletes the specified board in Miro.|boards:write|
|Look up Board|Retrieves information about the specified board from Miro.|boards:read|
|Look up Boards Stream|Retrieves information about all the boards in Miro.|boards:read|
|Update Board|Updates the specified board in Miro.|boards:write|
|Team Management|Add User to Team|Adds a Miro user to the team.|organizations:teams:write|
|Create Team|Creates a new team in Miro.|organizations:teams:write|
|Delete Team|Deletes a team from the organization.|organizations:teams:write|
|Look up Team|Retrieves information about the specified team from Miro.|organizations:teams:read|
|Look up Teams Stream|Retrieves the list of teams in the organization.|organizations:teams:read|
|Remove User from Team|Removes a Miro user from the team.|organizations:teams:write|
|Update Team|Updates the specified team in Miro.|organizations:teams:write|
|User Management|Activate User|Activates the specified user in Miro account.|Not applicable. This is a Miro SCIM action.|
|Create User|Creates a user in Miro account.|Not applicable. This is a Miro SCIM action.|
|Deactivate User|Deactivates a Miro user account.|Not applicable. This is a Miro SCIM action.|
|Delete User|Deletes a user from a Miro account.|Not applicable. This is a Miro SCIM action.|
|Look up Authenticated User|Retrieves information about the authenticated user account.|None.|
|Look up Organization Members Stream|Retrieves the details of all the members in an organization.|organizations:read|
|Look up User|Retrieves information of the specified user.|Not applicable. This is a Miro SCIM action.|
|Look up Users Stream|Retrieves the list of users in an organization.|Not applicable. This is a Miro SCIM action.|
|Update User|Updates the specified user in Miro.|Not applicable. This is a Miro SCIM action.|

## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See [Duplicate an AI agent](https://www.servicenow.com/docs/access?context=clone-ai-agent&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for more information about creating a clone.
-   See [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for information about AI agents.

Available AI agents include:

|AI agent|Description|
|--------|-----------|
|Miro board item management AI agent|Manages board items tasks \(that is, add a sticky note item to a board, add a shape item to a board, add a card item to a board, add a text item to a board\) in Miro.|
|Miro team management AI agent|Manages team management tasks \(that is, update a team, remove a user from a team, delete a team, add a user to a team, look up a team, create a team\) in Miro.|
|Miro user management AI agent|Manages user management tasks \(that is, look up an authenticated user, delete a user, create a user, activate a user, deactivate a user, update a user, look up a user\) in Miro.|
|Miro board management AI agent|Manages board management tasks \(that is, create a board, update a board, look up a board, delete a board\) in Miro.|

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## Spoke flows

The Miro spoke provides sample flows to demonstrate automating the Miro tasks. To customize a sample flow, copy it to a new application scope. Available sample flows include:

|Flow|Description|
|----|-----------|
|Add User to Miro Team|Looks up a user and the related team in Miro based on the group member and group in your ServiceNow instance and then add the user to the Miro team.|
|Remove Deactivated User from Miro Teams|Looks up a user in Miro teams, group members in your ServiceNow instance and then removes the user from each team in Miro.|

## Spoke module

The Miro spoke adds a Miro Spoke module to your ServiceNow instance. The Miro Spoke module syncronizes and stores information about Miro Teams and Miro Users. The Miro spoke contains the following tables:

-   Miro Teams \(sn\_miro\_spoke\_teams\)
-   Miro Users \(sn\_miro\_spoke\_users\)

|Module|Description|
|------|-----------|
|Miro Teams|Lists all the teams in Miro.|
|Miro Users|Lists all the users in Miro.|

## Integration Hub imports

The Miro spoke adds the following Integration Hub imports to your ServiceNow instance. The Integration Hub imports help you import data from Miro account to your ServiceNow instance in an automated way. For more information about Integration Hub imports, see[Integration Hub - Import](../../integrationhub/concept/integrationhub-imports.md).

|Import|Description|
|------|-----------|
|Create or Update Miro Teams Records|Imports teams details from Miro account into the Miro Teams table.|
|Create or Update Miro Users Records|Import users details from Miro account into Miro Users table.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Miro spoke](../task/setup-miro.md#).

