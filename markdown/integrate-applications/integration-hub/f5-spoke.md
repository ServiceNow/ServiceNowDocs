---
title: F5 BIG-IP Spoke
description: Manage servers and pools in the F5 BIG-IP system.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-09-02"
reading_time_minutes: 5
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# F5 BIG-IP Spoke

Manage servers and pools in the F5 BIG-IP system.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Supported version

BIG-IP 13.1.0.

## Spoke version

F5 BIG-IP spoke v1.3.0 is the latest version.

## Spoke flows

The F5 BIG-IP spoke provides sample flows in the draft state to demonstrate automating F5 tasks. To customize a sample flow, copy it to a new application scope. Available sample flows include:

|Flow|Description|
|----|-----------|
|Local Traffic Management Using F5 Big-IP|Creates a virtual server, associates it to a pool, and adds pool member in the BIG-IP system from a ServiceNow Service Catalog request.|

## Spoke subflows

The F5 BIG-IP spoke provides sample subflows to demonstrate automating F5 tasks. Available sample subflows include:

|Flow|Description|
|----|-----------|
|F5 Server - Pool Management|Creates a pool in the BIG-IP system and manages it.|

## Spoke actions

The F5 BIG-IP spoke provides actions to automate F5 tasks when events occur in ServiceNow. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Pool Management|Create Pool|Creates a pool in the BIG-IP system.|
|Add Pool Member|Creates a pool member in the BIG-IP system.|
|Check Pool|Checks pool health in BIG-IP system. Returns whether the pool is available, unavailable, offline, or if the status is unknown.|
|Delete Pool|Deletes a pool from the BIG-IP system.|
|Disable Pool Member|Disables a pool member in the BIG-IP system.|
|Enable Pool Member|Enables a pool member of a specified pool in the BIG-IP system.|
|Get Pool Members|Retrieves the list of members of a specified pool from the BIG-IP system.|
|Remove Pool Member|Deletes a pool member in the BIG-IP system.|
|Server Management|Add Profile to Virtual Server|Adds a profile to a virtual server in the BIG-IP system. Profiles enable you to control network traffic. For example, you can enable HTTP connections to the virtual server.|
|Create Virtual Server|Creates a virtual server in the BIG-IP system.|
|Delete Virtual Server|Deletes a virtual server from the BIG-IP system.|
|Update Virtual Server|Updates virtual server attributes in the BIG-IP system.|

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
|F5 BIG-IP pool management AI agent|Manages \(that is, adds a pool member, fetches pool members, disable a pool member, removes a pool member, creates a pool, deletes a pool, verifies a pool\) pools in BIG-IP system.|
|F5 BIG-IP server management AI agent|Manages \(that is, adds a profile to virtual server, deletes a virtual server, updates a virtual server, creates a virtual server\) servers in BIG-IP system.|

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

This spoke uses this alias record to authorize actions.

<table id="table_nnk_g2h_gfb"><thead><tr><th>

Connection &amp; Credential alias

</th><th>

Description

</th><th>

Connection alias requirements

</th></tr></thead><tbody><tr><td>

F5\_BIG\_IP

</td><td>

Connection to the F5 BIG-IP system.

</td><td>

-   Connection type: HTTP
-   Connection URL: URL of the host machine where the F5 server is installed.

</td></tr></tbody>
</table>To use the spoke connection alias, create an associated Connection record and an associated Credential record. For information about setting up the spoke, see [Configure a connection for the F5 BIG-IP spoke](../task/set-up-f5.md).

## MID Server requirements

These actions use REST calls that can run either on an instance or, optionally, through a MID Server. Use the connection record associated with the F5 BIG-IP alias to configure where actions run and, if needed, specify MID Server selection attributes. For more information, see [MID server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).

