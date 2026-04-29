---
title: Microsoft Azure DevOps Boards Spoke
description: Automate the process of managing work items in Azure DevOps Boards from your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Microsoft Azure DevOps Boards Spoke

Automate the process of managing work items in Azure DevOps Boards from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Azure DevOps Boards spoke v3.1.0 is the latest version.

## Supported versions

This spoke was built for Azure DevOps Boards REST API version 4.1 and TFS 2018 Update 3, but may be compatible with later versions.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   iHub Spoke Util Pack \(com.snc.ihub\_spoke\_util\_pack\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke requirements

-   Azure DevOps instance
-   Personal access tokens \(PATs\) to authenticate Azure DevOps

See [Azure DevOps documentation](https://docs.microsoft.com/en-us/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate?view=azure-devops&tabs=preview-page) for information about creating personal access token.

## Spoke actions

The Azure DevOps Boards spoke provides actions manage work items when events occur in ServiceNow. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Core Process Management|Create Iteration|Creates an Azure DevOps iteration.|
|Delete Iteration|Deletes an Azure DevOps iteration by path.|
|Delete Team Iteration|Delinks or deletes the iterations from a team.|
|Look up Creatable Fields|Get the list of all fields in a required Azure DevOps project.|
|Look up Area Paths|Gets all the area paths in a Project.|
|Look up Editable Fields|Gets the list of all fields in a required Work Item for editing.|
|Look up Area Path of a Team|Get all the area paths of a Team.|
|Look up Iteration by Path|Get Iteration by Path.|
|Look up Iteration Paths|Get all Iteration Paths in a Project.|
|Look up Iteration Paths of a Team|Gets all the iteration paths of a Team.|
|Look up Processes|Gets the list of all Azure DevOps Processes.|
|Look up Projects Stream|Retrieves the details of all Azure DevOps projects.|
|Look up Work Item Revisions Stream|Retrieves the Reporting Work Item Revisions for batch processing.|
|Look up Work Item Links Stream|Retrieve Reporting Work Item Links for batch processing.|
|Look up Queries by Wiql|Gets the results of the query given its Wiql.|
|Look up Team Settings|Get Backlog and Default Iterations setting of a team.|
|Look up Teams|Get all Teams in a Project.|
|Look up Work Item Data by ID|Gets all the data of a Work Item.|
|Look up Work Item Relations by ID|Gets all relations of a Work Item.|
|Look up Work Item Types|Gets the list of all work item types in a required Azure DevOps project.|
|Look up Work Item Type Fields by Process|Gets the list of all fields of a Work Item Type by a process from Azure DevOps.|
|Post Iteration to Team|Adds an Azure DevOps iteration to an Azure DevOps team.|
|Reporting Work Items Revisions|Adds reporting work-item revisions for batch processing.|
|Update Iteration|Updates an Azure DevOps iteration.|
|Look up Projects Stream|Retrieves the list of all Azure DevOps projects.|
|Get Work Item Types By Process|Retrieves the list of all Work Item types in a required Azure DevOps process.|
|Get Work Item Types|Retrieves the list of all Work Item types in a required Azure DevOps project.|
|Look up Area by Path|Retrieves the area of a project by its path.|
|Look up Area Path of a Team|Gets all the area paths of a Team.|
|Look up Area Paths|Get all the area paths in a Project.|
|Look up Creatable Fields|Gets the list of all the fields in a required Azure DevOps project.|
|Look up Editable Fields|Gets the list of all fields in a required Work Item for editing.|
|Look up Iteration by Path|Gets Iteration by Path.|
|Look up Iteration Paths|Gets all the Iteration Paths in a Project.|
|Look up Iteration Paths of a Team|Gets all Iteration Paths of a Team.|
|Look up Processes|Gets the list of all Azure DevOps Processes.|
|Look up Work Items|Retrieves the list of work items.|
|Look up Team Settings|Gets the Backlog and Default Iteration settings of a team.|
|Look up Teams|Gets all Teams in a Project.|
|Look up Work Item Data by ID|Gets all Data of a Work Item.|
|Look up Work Item Relations by ID|Gets all relations of a Work Item.|
|Look up Work Item Type Fields by Process|Gets the list of all Fields of a Work Item Type by a Process from Azure DevOps.|
|Look up Work Item Types|Gets the list of all Work Item types in a required Azure DevOps project.|
|Look up Work Item Types by Process|Get the list of all Work Item Types by a Process from Azure DevOps.|
|Look up Queries by Wiql|Gets the results of the query given its Wiql.|
|Work Item Management|Create Link between Work Items|Creates parent-child relationships between the Work Items.|
|Create Work Item|Creates a new Work Item on your instance of the Azure DevOps cloud. The Work Item can be of a specific Work Item type or custom Work Item type, depending on how your organization has customized Azure DevOps.|
|Create Service Hook|Creates a new subscription to an Azure DevOps Service Hook.|
|Delete Work Item|Deletes the required Work Item in your Azure DevOps instance.|
|Delete Link between Work Items|Deletes the link between Work Items.|
|Update Work Item|Updates a Work Item in your instance of the Azure DevOps cloud.|
|Update Work Item Project Details|Moves between projects in the same organization.|
|Add Attachment|Adds an attachment associated with a ServiceNow record to the required work item on the Azure DevOps instance.|

## Spoke triggers

ServiceNow supports specific events on the Azure DevOps instance that create triggers. You must first configure a flow with a supported trigger definition. When an event, for example, a work item is commented on, occurs in Azure DevOps, it sends the payload via a webhook to the ServiceNow instance. After that, the flow that you configured is triggered at the ServiceNow instance to automate a workflow. The supported events are:

|Category|Trigger|Definition|
|--------|-------|----------|
|Work Item Management|Work item commented on|Trigger initiates when a work item is commented on.|
|Work item created|Trigger initiates when a new work item is created.|
|Work item deleted|Trigger initiates when a work item is deleted.|
|Work item restored|Trigger initiates when a work item is newly restored.|
|Work item updated|Trigger initiates when a work item is changed.|

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
|Microsoft Azure DevOps Boards core process management AI agent|Manages core process management tasks \(that is, look up a projects stream, look up area paths, look up an area path of a team, look up work item types by process, look up team settings, look up an iteration by path, look up work item data by ID, look up creatable fields, look up work item types, look up iteration paths of a team, look up processes, look up editable fields, look up an area by path, delete a team iteration, look up work item relations by ID, look up queries by Wiql, create an iteration, look up work item type fields by process, look up teams, post an iteration to a team, look up iteration paths, update an iteration, delete an iteration\) in Microsoft Azure DevOps Boards.|
|Microsoft Azure DevOps Boards work item management AI agent|Manages work item management tasks \(that is, add an attachment, delete a work item, create a link between work items, create a service hook, delete a link between work items, update work item project details\) inMicrosoft Azure DevOps Boards.|

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

If you want to use different connections in your flow, subflows, and actions, create the child alias and select the default alias record as its parent. To configure the child alias, perform the same steps that are needed to configure the parent alias. Depending on your requirement and set up, you can choose either the parent alias or child alias in your flow, subflows, and actions.

You can also use multiple Azure DevOps accounts. In this case, you should provide the respective **Password** while configuring the credential record and specify the relevant **Connection URL** while configuring the connection record.

-   If you want to set up the Microsoft Azure DevOps Boards spoke using OAuth, see [Set up the Microsoft Azure DevOps Boards spoke using OAuth](../task/setup-azdevops-boards-oauth.md#).
-   If you want to set up the Microsoft Azure DevOps Boards spoke using personal access token, see [Set up the Microsoft Azure DevOps Boards spoke using personal access token](../task/setup-azdevops-boards.md#).

