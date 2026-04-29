---
title: GovNotify Spoke
description: Use the GovNotify spoke to send emails, texts, and letters based on automation in your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# GovNotify Spoke

Use the GovNotify spoke to send emails, texts, and letters based on automation in your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

GovNotify spoke v1.2.0 is the latest version.

## Supported versions

This spoke was built for GovNotify API version v2, but may be compatible with later versions.

## Spoke flows

The GovNotify spoke provides the sample flow, Send a Text Message to User to demonstrate sending a text message to the specified user. To customize the sample flow, copy it to the required application scope.

## Spoke subflows

The GovNotify spoke provides the sample subflow, GovNotify Webhook Callback to demonstrate automating tasks. To customize a sample subflow, copy it to the required application scope.

## Spoke actions

The GovNotify spoke provides actions to automate tasks when events occur in your ServiceNow instance. Available actions include:

|Action|Description|
|------|-----------|
|Look up Notification Status by ID|Retrieves the latest notification by the notification ID.|
|Look up Notifications|Retrieves up to 250 messages and statuses that is one page.|
|Send a Letter|Sends a physical notification letter to a recipient.|
|Send a Text Message|Sends a text message to a recipient.|
|Send an Email|Sends an email notification to the recipient.|

## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See [Duplicate an AI agent](https://www.servicenow.com/docs/access?context=clone-ai-agent&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for more information about creating a clone.
-   See [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for information about AI agents.

Available AI agents include:

|AI Agent|Description|
|--------|-----------|
|GovNotify message manager|Manages notifications and messages \(that is, send a text message, email, or letter, look up notifications, look up notification status by ID\) in GovNotify.|

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## Spoke module

The GovNotify spoke adds the GovNotify Spoke application to your instance and includes these modules:

|Module|Description|
|------|-----------|
|Client Details|Stores the client record that authenticates the requests.|
|Credentials|Contains the default credential record of the GovNotify spoke.|
|Templates|Displays the details of the templates in your GovNotify account.|
|Text Notifications|Displays the details of sent text messages.|
|Transactions|Displays the details of all sent messages. The records include transactions for emails, text messages, and letters.|
|Webhook Decision Answers|Stores the webhook answer record that triggers the required subflow.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the GovNotify spoke](../task/govnotify-setup.md).

