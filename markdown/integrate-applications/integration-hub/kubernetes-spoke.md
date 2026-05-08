---
title: Kubernetes Spoke
description: Automate changes in Kubernetes when an event occurs in ServiceNow.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Kubernetes Spoke

Automate changes in Kubernetes when an event occurs in ServiceNow.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Kubernetes spoke v1.3.0 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Supported versions

API version v1.

## Spoke actions

The Kubernetes spoke provides actions to automate Kubernetes tasks when events occur in ServiceNow. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Endpoint Management|Create Endpoints|Creates an endpoint in the Kubernetes instance.|
|Delete Endpoints|Deletes an endpoint from the Kubernetes instance.|
|Namespace Management|Create Namespace|Creates a namespace in the Kubernetes instance.|
|Delete Namespace|Deletes a namespace from the Kubernetes instance.|
|Node Management|Create Node|Creates a node in the Kubernetes instance.|
|Delete Node|Deletes a node in the Kubernetes instance.|
|Inspect Node|Inspects a specified node in the Kubernetes instance and returns node information and status.|
|Pod Management|Create Pod|Creates a Pod in the Kubernetes instance.|
|Delete Pod|Deletes a pod from the Kubernetes instance.|
|Inspect Pod|Inspects the specified pod in the Kubernetes instance and returns pod information and status.|
|Secret Management|Create Docker Hub Secret|Creates a secret in the Kubernetes instance.|
|Delete Docker Hub Secret|Deletes a Secret from the Kubernetes instance.|
|Service Management|Create Service|Creates a service on a Kubernetes server.|
|Delete Service|Deletes a service from the Kubernetes server.|
|Volume Management|Create Persistent Volume|Creates a persistent volume in the Kubernetes instance.|
|Create Persistent Volume Claim|Creates a Persistent Volume Claim in a Kubernetes instance.|
|Delete Persistent Volume|Deletes a persistent volume from the Kubernetes instance.|
|Delete Persistent Volume Claim|Deletes a persistent volume claim from the Kubernetes instance.|
|Inspect Persistent Volume Claim|Inspects a persistent volume claim in a Kubernetes instance and returns claim information and status.|

## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See Create an agentic workflow for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See Find AI agents for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See Duplicate an AI agent for more information about creating a clone.
-   See Now Assist AI agents for information about AI agents.

Available AI agents include:

<table id="table_ugm_jds_k2c"><thead><tr><th>

AI Agent

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Kubernetes endpoint management AI agent

</td><td>

Manages \(that is, creates or deletes\) an endpoint in the Kubernetes instance.

</td></tr><tr><td>

Kubernetes namespace management AI agent

</td><td>

Manages \(that is, creates or deletes\) a namespace in the Kubernetes instance.

</td></tr><tr><td>

Kubernetes node management AI agent

</td><td>

Manages \(that is, creates or deletes\) and inspects the specified node in the Kubernetes instance.

</td></tr><tr><td>

Kubernetes pod management AI agent

</td><td>

Manages \(that is, creates or deletes\) and inspects the specified pod in the Kubernetes instance.

</td></tr><tr><td>

Kubernetes secret management AI agent

</td><td>

Manages \(that is, creates or deletes\) a secret in the Kubernetes instance.

</td></tr><tr><td>

Kubernetes service management AI agent

</td><td>

Manages \(that is, creates or deletes\) a service in the Kubernetes instance.

</td></tr><tr><td>

Kubernetes volume management AI agent

</td><td>

-   Manages \(that is, creates or deletes\) a persistent volume.
-   Manages \(that is, creates or deletes\) and inspects the specified persistent volume claim.

</td></tr></tbody>
</table>There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see Find AI agents.

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## Kubernetes account requirements

The Kubernetes spoke requires generating and configuring your Kubernetes account to use a web API key.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

This spoke uses the Kubernetes alias record to authorize actions. To use the spoke connection alias, create an associated Connection record and an associated Credential record. For information about setting up the spoke, see [Set up the Kubernetes spoke](../task/set-up-kubernetes.md#).

## MID Server requirements

These actions use REST calls that can run either on an instance or, optionally, through a MID Server. Use the connection record associated with the Kubernetes alias to configure where actions run and, if needed, specify MID Server selection attributes. For more information, see MID server.

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).

