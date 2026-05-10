---
title: PagerDuty Spoke
description: The PagerDuty spoke provides actions to view and analyze meaningful usage data for PagerDuty software subscriptions. Analyze on-call users to determine which licenses are stale so that you can reclaim these licenses and realize your potential savings.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# PagerDuty Spoke

The PagerDuty spoke provides actions to view and analyze meaningful usage data for PagerDuty software subscriptions. Analyze on-call users to determine which licenses are stale so that you can reclaim these licenses and realize your potential savings.

## Request apps on the Store

Visit the [ServiceNow](https://store.servicenow.com/sn_appstore_store.do) Store website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Supported versions

This spoke was built for PagerDuty v1.5.1, but may be compatible with later versions.

## Spoke requirements

PagerDuty global admin account.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Integration Hub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke subflows

The PagerDuty spoke provides sample subflows to demonstrate automating PagerDuty tasks. To customize a sample subflow, copy it to a new application scope. Available sample subflows include:

<table id="table_i3x_p4g_h4b"><thead><tr><th>

Subflow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

PagerDuty Download Subscriptions

</td><td>

Downloads user subscriptions from the PagerDuty portal.To use this subflow, perform the steps outlined in [Integrating with PagerDuty](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/saas-license-management/integrate-with-pagerduty.md).

</td></tr><tr><td>

PagerDuty Reclaim Subscription

</td><td>

Deactivates user accounts in PagerDuty.To use this subflow, perform the steps outlined in [Integrating with PagerDuty](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/saas-license-management/integrate-with-pagerduty.md).

</td></tr><tr><td>

PagerDuty Update User Activity

</td><td>

Retrieves the activity of users who are on an on-call schedule.To use this subflow, perform the steps outlined in [Integrating with PagerDuty](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/saas-license-management/integrate-with-pagerduty.md).

</td></tr></tbody>
</table>## Spoke actions

The PagerDuty spoke provides actions to automate PagerDuty tasks when events occur in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Audit Management|Look up Audit Record Stream|Retrieves information about the list of audits.|
|Business Service Management|Create Business Service|Creates business service by passing the Number field.|
|Create Business Service Subscribers|Creates a business service subscriber.|
|Delete Business Service|Deletes a business service.|
|Look up Business Service by ID|Retrieves information about the specified business service.|
|Look up Business Service Dependencies by Business Service ID|Retrieves the Business Service Dependencies by Business Service ID.|
|Look up Business Service Subscribers by Business Service ID|Retrieves Business Service Subscribers by Business Service ID.|
|Look up Business Services Stream|Retrieves a Business Services Stream.|
|Remove Business Service Subscribers|Removes the specified business service subscriber.|
|Update Business Service|Updates a business service.|
|Escalation Policy Management|Delete Escalation Policy|Deletes the specified escalation policy.|
|Look up Escalation Policies Stream|Retrieves information about the list of escalation policies.|
|Look up Escalation Policy by ID|Retrieves Escalation Policy by ID.|
|Update Escalation Policy|Updates an escalation policy.|
|Create Escalation Policy|Creates an escalation policy|
|Extension Management|Create Extension|Creates an extension.|
|Look up Extension by ID|Retrieves information about the specified extension.|
|Look up Extensions Stream|Retrieves information about the list of extensions.|
|Update Extension|Updates an extension.|
|Incident Management|Create Incident|Creates an incident with the specified details.|
|Look up Incident by ID|Retrieves information about an incident by its ID.|
|Look up Incidents Stream|Retrieves information about the list of incidents.|
|Update Incident|Updates an incident with the specified details.|
|Notifications Management|Look Up Notification Stream|Retrieves the list of notifications.|
|Schedule Management|Create Schedule|Creates a schedule.|
|Look up Schedule by ID|Retrieves information about a schedule ID.|
|Look up Schedules Stream|Retrieves information about the list of schedules.|
|Update Schedule|Updates a schedule with the specified information.|
|Service Management|Create Service|Creates a service|
|Look up Service by ID|Retrieves the details of a service by its ID.|
|Look up Services Stream|Retrieves information about the list of services.|
|Update Service|Updates a service with the specified information.|
|Tag Management|Create Tag|Creates a tag.|
|Delete Tag|Deletes the specified tag.|
|Look up Tag by ID|Retrieves information about the specific tag.|
|Look up Tags Stream|Retrieves information about the required tags.|
|Assign Tags|Assigns tags to the required entity.|
|Team Management|Add Escalation Policy to Team|Adds the escalation policy to a team with the specified details.|
|Add User to Team|Adds users to the specified team.|
|Create Team|Creates a team.|
|Create Team Subscriptions|Creates a team subscription.|
|Delete Team|Deletes the specified team.|
|Look up Subscriptions in Team|Retrieves information about the specified subscription in a team.|
|Look up Team by ID|Retrieves the specific team by ID.|
|Look up Teams Stream|Retrieves the information about the list of teams.|
|Look up Users in Team|Retrieves information about the specified users from a team.|
|Remove Escalation Policy from Team|Removes the specified escalation policy from the specified team.|
|Remove Team Subscriptions|Removes the specified team subscription.|
|Remove User from Team|Removes the specified user from the specified team.|
|Update Team|Updates the details of a team.|
|Webhook Management|Create Webhook Subscription|Creates a webhook subscription.|
|Delete Webhook|Deletes a webhook.|
|Look up Webhook Subscription by ID|Retrieves information about the specified webhook subscription ID.|
|Look up Webhook Subscription Stream|Retrieves information about the list of webhook subscriptions.|
|Update Webhook Subscription|Updates the specified webhook subscription.|
|User Management|Look Up Users|Retrieves all PagerDuty user subscriptions.|
|Look Up On Call Users|Retrieves information about the last time that a user was on an on-call schedule.|
|Remove User|Deactivates a user account in PagerDuty.|
|Look up Users Stream|Retrieves information about the list of users.|
|Create User|Creates a user.|
|Update User|Updates the details of the specified user.|

**Note:** This spoke has a Look up User action and Software Asset Management related actions only.

## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See [Create an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-use-case-ai-agents.md) for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/find-ai-agents.md) for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See [Duplicate an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-ai-agent.md) for more information about creating a clone.
-   See [Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/na-ai-agents.md) for information about AI agents.

Available AI agents include:

|AI agent|Description|
|--------|-----------|
|PagerDuty team management AI agent|Creates teams, updates team details, manages users and escalation policies, and retrieves information about teams and their subscriptions.|
|PagerDuty business service management AI agent|Creates, updates, and deletes business services, manages subscribers, and retrieves dependencies.|
|PagerDuty schedule management AI agent|Retrieves schedule streams and details of the required schedule.|
|PagerDuty extension management AI agent|Retrieevs details of the required extensions, creates new extensions, retrieves a stream of extensions, and updates existing extensions.|
|PagerDuty user management AI agent|Retrieves details of the on-call users, updates user details, creates new users, removes the required users and retrieves the user streams.|
|PagerDuty incident management AI agent|Creates new incidents, updates existing ones, and retrieves details of the required incident.|
|PagerDuty notification management AI agent|Retrieves details of notifications.|
|PagerDuty service management AI agent|Creates new services, updates details of existing services, and retrieves details of the required service.|
|PagerDuty audit management AI agent|Retrieves the audit records and integrates the PagerDuty functionalities into broader operational flow.|
|PagerDuty escalation policy management AI agent|Creates, updates, deletes, and retrieves escalation policies, as well as stream policy data for integration into workflows|
|PagerDuty tag management AI agent|Creates tags, retrieves details of the required tag, retrieves tag streams, deletes tags, and assigns tags.|

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/find-ai-agents.md).

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r-credentials.md).

