---
title: X Spoke \(formerly Twitter Spoke\)
description: Use the X spoke \(formerly Twitter spoke\) to have private chats and group chats, and to automatically tweet messages or media in your X account from your ServiceNow instance.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-09-02"
reading_time_minutes: 2
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# X Spoke \(formerly Twitter Spoke\)

Use the X spoke \(formerly Twitter spoke\) to have private chats and group chats, and to automatically tweet messages or media in your X account from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

X spoke v2.3.0 is the latest version.

## Supported versions

API version v1.1.

## Spoke requirements

-   X developer account
-   X developer app to access the X APIs
-   Access token and secret of your X developer app
-   Consumer key and secret from your X developer app

See the [X Developers](https://developer.twitter.com) documentation for instructions on creating the developer application and gathering the required details.

## Spoke actions

The X spoke provides actions to automate tweeting when events occur in ServiceNow. Available actions include:

<table id="table_sjg_qjx_cjb"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tweet

</td><td>

Tweets a message or media. Messages and media are tweeted as per X limits.**Note:** If you wish to tweet media, use the Look Up Attachment Records action before this action in your custom flow to retrieve the required media.

</td></tr></tbody>
</table>## Available AI agents

Install Now Assist for Spokes and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

The X Spoke provides AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance. For more information about AI agents, see [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

Available AI agents include:

<table id="table_ugm_jds_k2c"><thead><tr><th>

AI Agent

</th><th>

Description

</th></tr></thead><tbody><tr><td>

X Tweet management AI agent

</td><td>

This AI Agent posts tweets to the X handle that you had configured that contain text.**Note:** You must configure a valid X handle before using this AI Agent.

</td></tr></tbody>
</table>Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

**Note:** Two connection and credential alias records are needed for the X spoke. One for tweeting messages and other for tweeting media. Each alias should be associated with the respective X API.

For information about setting up the spoke, see [Set up the X spoke](../task/setup-x-spk.md#).

