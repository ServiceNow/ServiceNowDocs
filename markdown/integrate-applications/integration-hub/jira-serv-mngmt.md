---
title: Jira Service Management Spoke
description: Automate service management tasks in Jira Service Management from your ServiceNow instance.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-10-09"
reading_time_minutes: 6
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Jira Service Management Spoke

Automate service management tasks in Jira Service Management from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Jira Service Management spoke v1.2.0 is the latest version.

## Spoke requirements

JIRA Service Management account.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   Integrations - External Authentication Framework \(com.glide.external.app\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Jira Service Management spoke provides actions to automate tasks when events occur in your ServiceNow instance. Available actions include:

<table id="table_zvq_ykf_4qb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Metadata

</td><td>

Look up Service Desk IDs \(Metadata\)

</td><td>

Retrieves the list of all service desk IDs from the specified JIRA instance.

</td></tr><tr><td rowspan="8">

Organization Management

</td><td>

Add Organization to Service Desk

</td><td>

Adds the specified organization ID to the specified service desk instance.

</td></tr><tr><td>

Add Users to Organization

</td><td>

Adds users to the specified organization.

</td></tr><tr><td>

Create Organization

</td><td>

Creates an organization account for the specified service management instance.

</td></tr><tr><td>

Delete Organization

</td><td>

Deletes an organization account from the specified service management instance.

</td></tr><tr><td>

Look up Organizations

</td><td>

Retrieves the list of organizations in service management instance.

</td></tr><tr><td>

Look up Users in Organization

</td><td>

Retrieves the list of users in an organization.

</td></tr><tr><td>

Remove Organization from Service Desk

</td><td>

Removes the specified organization from the specified service desk instance.

</td></tr><tr><td>

Remove Users from Organization

</td><td>

Removes users from the specified organization.

</td></tr><tr><td rowspan="16">

Request Management

</td><td>

Add Customer Request Participants

</td><td>

Adds customers to request for the specified service desk instance.

</td></tr><tr><td>

Create Customer Request

</td><td>

Creates customer request for the specified service desk instance.

</td></tr><tr><td>

Create Customer Request Comment

</td><td>

Creates a customer request comment for the specified service desk instance.

</td></tr><tr><td>

Create Temporary Attachment

</td><td>

Creates a temporary attachment for the specified request. **Note:** This action works only for Jira Service Management Cloud.

</td></tr><tr><td>

Create Temporary File

</td><td>

Creates a temporary file for the specified request.

</td></tr><tr><td>

Look up Comment Attachment

</td><td>

Retrieves comment attachment for the specified issue ID or issue key. **Note:** This action works only for Jira Service Management Cloud.

</td></tr><tr><td>

Look up Customer Request Comments

</td><td>

Retrieves the list of customer request comments for the service desk.

</td></tr><tr><td>

Look up Customer Request Participants

</td><td>

Retrieves the list of request participants related to customer request for the specified service desk instance.

</td></tr><tr><td>

Look up Customer Request Status History

</td><td>

Retrieves the customer request status history for the specified service desk instance.

</td></tr><tr><td>

Look up Customer Request Transitions

</td><td>

Retrieves a list of customer request transitions for the specified service desk instance.

</td></tr><tr><td>

Look up Customer Requests

</td><td>

Retrieves a list of customer request for the specified service desk instance.

</td></tr><tr><td>

Look up SLA Information

</td><td>

Retrieves the SLA information for the specified service desk instance.

</td></tr><tr><td>

Look up Subscription Status

</td><td>

Retrieves subscription status for the specified service desk instance.**Note:** This action works only for Jira Service Management Cloud.

</td></tr><tr><td>

Perform Customer Request Transition

</td><td>

Changes the state of a customer request for the specified service desk instance.**Note:** This action works only for Jira Service Management Cloud.

</td></tr><tr><td>

Remove Customer Request Participants

</td><td>

Removes a customer request from the specified service desk instance.

</td></tr><tr><td>

Subscribe Customer Request

</td><td>

Subscribes to a customer request for the specified service desk instance.

</td></tr><tr><td rowspan="7">

ServiceDesk Management

</td><td>

Add Customers

</td><td>

Adds the specified users to the service desk.

</td></tr><tr><td>

Look up Issues in Queue

</td><td>

Retrieves the list of issues in a queue for the specified service desk instance.

</td></tr><tr><td>

Look up Queue

</td><td>

Retrieves the list of queues specified in service desk instance.

</td></tr><tr><td>

Look up Request Type Fields

</td><td>

Retrieves the list of request type fields for the specified service desk instance.

</td></tr><tr><td>

Look up Request Types

</td><td>

Retrieves the list of request types for the specified service desk instance.

</td></tr><tr><td>

Look up Service Desks

</td><td>

Retrieves the list of all service desk for the specified service management instance from JIRA instance.

</td></tr><tr><td>

Look up User Account ID

</td><td>

Retrieves the user account ID of user.**Note:** This action works only for Jira Service Management Cloud.

</td></tr></tbody>
</table>## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See [Duplicate an AI agent](https://www.servicenow.com/docs/access?context=clone-ai-agent&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) for more information about creating a clone.
-   See [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) for information about AI agents.

Available AI agents include:

|AI agent|Description|
|--------|-----------|
|Jira Service Management request management AI agent|Automates and manages workflows in Jira Service Management. Retrieves customer request details, manages participants, handles SLA information, and automates transitions.|
|Jira Service Management organization management AI agent|Manages organizations, service desk associations, and user lookups.|
|Jira Service Management service desk management AI agent|Automates and manages tasks within Jira Service Management. Retrieves service desks, request type fields, queues, request types, and issues in queues.|

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).



For information about setting up the spoke, see [Set up the Jira Service Management spoke](../task/setup-jira-serv-mgmt.md#).

