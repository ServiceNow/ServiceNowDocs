---
title: Microsoft Dynamics CRM Spoke
description: Provide the baseline actions to interact with Microsoft Dynamic Entities through introspection.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-10-27"
reading_time_minutes: 6
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Microsoft Dynamics CRM Spoke

Provide the baseline actions to interact with Microsoft Dynamic Entities through introspection.

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Microsoft Dynamics CRM spoke v1.9.0 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow Flow Designer - Dynamic Outputs \(com.glide.hub.dynamic\_outputs\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream​\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke flows

The Infoblox spoke provides sample flows to create an opportunity in Dynamics CRM.

<table id="table_sqr_rch_gqb"><thead><tr><th>

Flow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create Opportunity in Dynamics CRM

</td><td>

Creates an opportunity in Dynamics CRM and updates the opportunity record in your ServiceNow instance.

</td></tr></tbody>
</table>## Spoke subflows

This spoke ships with the following subflows.

|Subflow|Description|
|-------|-----------|
|Process Dynamics CRM Webhook|Receives the Dynamic CRM webhook notification and converts it into an array of objects and logs the details.|
|Process Dynamics CRM Webhook for Opportunity​|Receives the Dynamic CRM webhook notification and updates the opportunity table record.|

## Available sample conversational subflows

Install Now Assist for Conversational Spokes and start using the conversational ability of Integration Hub spokes. For more information, see [Now Assist in Conversational Spokes](../../integrationhub/concept/conv-spokes-na.md).

|Conversational subflow|Usage|
|----------------------|-----|
|Look up Opportunities - Sample|Retrieves opportunity details from Microsoft Dynamics CRM based on the specified filter criteria.|
|Look up Contacts - Sample|Retrieves contact details from Microsoft Dynamics CRM based on the specified filter criteria.|
|Look up Accounts - Sample|Retrieves account details from Microsoft Dynamics CRM based on the specified filter criteria.|
|Look up Leads - Sample|Retrieves leads details from Microsoft Dynamics CRM based on the specified filter criteria.|
|Create Lead - Sample|Creates lead in Microsoft Dynamics CRM.|

In this example, a lead is created for John Smith who is interested in CRM Software and is focused on improving sales processes.

![Example showing lead creation.](../image/dyn-crm-conv-subflow.png)

## Spoke actions

The Microsoft Dynamics CRM spoke provides the baseline actions to interact with Microsoft Dynamic Entities through introspection. Available actions include:

<table id="table_xtv_cwt_g3bb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="3">

Account Management

</td><td>

Create Account

</td><td>

Create an account in Microsoft Dynamics CRM.

</td></tr><tr><td>

Look up Account Details by Account ID

</td><td>

Retrieve the details of the required account in Microsoft Dynamics CRM.

</td></tr><tr><td>

Look up Accounts Stream

</td><td>

Retrieve details of all the accounts in Microsoft Dynamics CRM.

</td></tr><tr><td rowspan="2">

Case Management

</td><td>

Create Case

</td><td>

Create case in Microsoft Dynamics CRM.

</td></tr><tr><td>

Look up Case Details by Case ID

</td><td>

Retrieve details of the specified case in Microsoft Dynamics CRM.

</td></tr><tr><td rowspan="3">

Contact Management

</td><td>

Create Contact

</td><td>

Create contact in Microsoft Dynamics CRM.

</td></tr><tr><td>

Look up Contact Details by Contact ID

</td><td>

Retrieve details of the required contact in Microsoft Dynamics CRM.

</td></tr><tr><td>

Look up Contacts Stream

</td><td>

Retrieve details of all the opportunities in Microsoft Dynamics CRM.

</td></tr><tr><td rowspan="2">

Lead Management

</td><td>

Create Lead

</td><td>

Create lead in Microsoft Dynamics CRM.

</td></tr><tr><td>

Look up Lead Details by Lead ID

</td><td>

Retrieve details of the required lead in Microsoft Dynamics CRM.

</td></tr><tr><td rowspan="4">

Metadata Retrieval

</td><td>

Look up Entities

</td><td>

Retrieve all the entities and their logical names in Microsoft Dynamics CRM.

</td></tr><tr><td>

Look up Entity Metadata

</td><td>

Retrieve all the metadata available for the required entity type in Microsoft Dynamics CRM.

</td></tr><tr><td>

Look up Entity URL

</td><td>

Retrieve all the entities and its entity set name \(public URL name\) available in Microsoft Dynamics CRM.

</td></tr><tr><td>

Look up Field Choice List

</td><td>

Retrieve all the choice lists for the fields that are in the name and label pair format.

</td></tr><tr><td rowspan="3">

Opportunity Management

</td><td>

Create Opportunity

</td><td>

Create an opportunity in Microsoft Dynamics CRM.

</td></tr><tr><td>

Look up Opportunities Stream

</td><td>

Retrieves details of all the opportunities in Microsoft Dynamics CRM.

</td></tr><tr><td>

Look up Opportunity Details by Opportunity ID

</td><td>

Retrieve the details of the required opportunity in Microsoft Dynamics CRM.

</td></tr><tr><td rowspan="9">

Record Management

</td><td>

Create Record

</td><td>

Create a record in Microsoft Dynamics CRM.

</td></tr><tr><td>

Delete Record

</td><td>

Deletes a record in Microsoft Dynamics CRM.

</td></tr><tr><td>

Look up Primary Attributes and Logical Name

</td><td>

Retrieve primary attributes and logical name for the specified entity.

</td></tr><tr><td>

Look up Record by Record ID

</td><td>

Retrieve information of the specified record in an Entity.

</td></tr><tr><td>

Look up Record by Search Query

</td><td>

Retrieve record based on the search query and entity selected from the choice list.

</td></tr><tr><td>

Look Up Records \(Before Paris Version\)

</td><td>

Retrieve records based on the search query and specific entity.

</td></tr><tr><td>

Look up Records Stream

</td><td>

Retrieve records based on the search query and specific entity.

</td></tr><tr><td>

Subflow Helper Action

</td><td>

Parses the JSON input and converts it into an array object. This can action can be used for creating subflows.

</td></tr><tr><td>

Update Record

</td><td>

Update a record in Microsoft Dynamics CRM.

</td></tr></tbody>
</table>## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See [Duplicate an AI agent](https://www.servicenow.com/docs/access?context=clone-ai-agent&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information about creating a clone.
-   See [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for information about AI agents.

Available AI agents include:

|AI agent|Description|
|--------|-----------|
|Microsoft Dynamics CRM record management AI agent|Manages CRM records including deleting, and retrieving the required records.|
|Microsoft Dynamics CRM case management AI agent|Creates case in Microsoft Dynamics CRM and retrieves details of the specified case.|
|Microsoft Dynamics CRM contact management AI agent|Retrieves contact streams and contact details by ID, and creates new contacts.|
|Microsoft Dynamics CRM lead management AI agent|Creates lead in Microsoft Dynamics CRM and retrieves details of the required lead.|
|Microsoft Dynamics CRM account management AI agent|Creates an account in Microsoft Dynamics CRM and retrieves details of the required accounts.|
|Microsoft Dynamics CRM opportunity management AI agent|Creates opportunities, retrieves opportunity details, parses CRM entity data, and manages opportunity streams.|

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## Spoke module

The Microsoft Dynamics CRM spoke adds a Microsoft Dynamics CRM module to your ServiceNow instance. The Opportunities module displays the details of the opportunities.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

This spoke uses the Microsoft\_Dynamics\_CRM alias record to authorize actions.

|Connection alias|Description|Connection URL|
|----------------|-----------|--------------|
|Microsoft\_Dynamics\_CRM|Connection to Microsoft Dynamics CRM|URL configured when you create your application in Azure. This URL ends with `dynamics.com`.|

For information about setting up the spoke, see [Set up Microsoft Dynamics CRM spoke](../task/setup-ms-dynamics-crm.md#).

