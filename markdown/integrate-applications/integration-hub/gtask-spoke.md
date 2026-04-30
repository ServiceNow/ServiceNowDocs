---
title: Google Tasks Spoke
description: Manage Google tasks and list from your ServiceNow instance.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-09-02"
reading_time_minutes: 4
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Google Tasks Spoke

Manage Google tasks and list from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Supported versions

API version v1.

## Spoke version

Google Tasks spoke v1.4.0 is the latest version.

## Spoke subflows

The Google Tasks spoke provides sample subflows in the draft state to demonstrate automating Google Tasks. To customize a sample subflow, copy it to a new application scope. Available sample subflows include:

|Subflow|Description|
|-------|-----------|
|Move a ServiceNow attachment to Google Tasks|Copies an attachment from ServiceNow to Google Tasks.|

## Spoke actions

The Google Tasks spoke provides actions to automate Google Tasks when events occur in ServiceNow. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Task Management|Complete Task|Mark a task complete in a task list.|
|Create Task|Create a task in a task list.|
|Delete Task|Delete a task from a task list.|
|Get Task|Retrieve details of a specified task from a task list.|
|Look Up Tasks|Retrieve details of specified tasks from a task list.|
|Update Task|Update details of the specified task in a task list.|
|Task List Management|Create Task List|Create a task list in your Google Tasks account.|
|Delete Task List|Delete the specified task list.|
|Get All Task Lists|Retrieve the details of all task lists in your Google Tasks account.|
|Get Task List|Retrieve details of a specified task list.|
|Update Task List|Update details of a specified task list.|

## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See [Duplicate an AI agent](https://www.servicenow.com/docs/access?context=clone-ai-agent&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information about creating a clone.
-   See [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for information about AI agents.

Available AI agents include:

|AI agent|Description|
|--------|-----------|
|Google Tasks Task Management AI Agents|Manages task management tasks \(that is, get a tasklist ID from a tasklist name, delete a task, get a task, update a task, create a task, complete a task\) in Google Tasks.|
|Google Tasks Tasklist Management AI Agents|Manages tasklist management tasks \(that is, update a tasklist, delete a tasklist, get a tasklist, create a tasklist, get all tasklists, get a tasklist ID from a tasklist name\) in Google Tasks.|
|Google Tasks AI Agents|Retrieves tasklist ID from a tasklist name from Google Tasks.|

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## Google Tasks spoke account requirements

The Google Tasks spoke requires a custom app that you create in the Google Developers Console.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Google Tasks spoke](../task/setup-gtask.md#).

## MID Server requirements

These actions use REST calls that can run either on an instance or, optionally, through a MID Server. Use the connection record associated with the Google Tasks alias to configure where actions run and, if needed, specify MID Server selection attributes. For more information, see [MID server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).

