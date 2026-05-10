---
title: Exploring Virtual Agent API
description: Use the ServiceNow Virtual Agent API app to integrate any chat interface or a bot with ServiceNow Virtual Agent or Agent Chat. The app is available from the ServiceNow Store.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [explore]
breadcrumb: [Virtual Agent API, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Exploring Virtual Agent API

Use the ServiceNow® Virtual Agent API app to integrate any chat interface or a bot with ServiceNow® Virtual Agent or Agent Chat. The app is available from the ServiceNow® Store.

## Overview of the Virtual Agent API

The Virtual Agent API is a REST API. This API is built on the conversational custom chat integration framework that is provided with Virtual Agent starting in the Paris release. The API enables ServiceNow developers, advanced users, and admins to use Virtual Agent in either of the following ways:

-   **Standalone bot**

    Use Virtual Agent as a standalone bot that you integrate with enterprise or with any other third-party chat interface that supports conversational interfaces.

    Your end users can interact with the Virtual Agent and Agent Chat through multiple channels by using this integration.

-   **Secondary bot**

    Use Virtual Agent as a secondary bot in an environment that has multiple, specialized bots managed by a primary bot.

    In this scenario, a primary bot manages communication with secondary bots on behalf of the end user. A primary bot could be IBM Watson Assistant or a homegrown primary bot.

    Your secondary bots, such as the ServiceNow bot, might handle specific types of end-user requests, such as service tickets or reservations.


The Virtual Agent API is useful for creating server-to-server integrations. However, for integrations that require the transformation of unsupported controls that must be rendered in your existing chat interface, consider using the [Custom Chat Integration Framework](va-custom-adapter-framework.md).

For information about features such as the URL format and the supported request and response parameters in the Virtual Agent API, see [Virtual Agent Bot Integration API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/bot-api.md).

![Video link to Virtual Agent Academy.](../../conversational-interfaces/image/icon-video-link.png) [Augment your experiences with the Virtual Agent API](https://www.youtube.com/watch?v=cyhmMyG4jKk) \(Virtual Agent Academy video\)

## How the Virtual Agent API works

The following diagram shows how the REST API processes user input from a third-party chat interface or a primary bot, and then generates a bot response.

1.  The user provides input to a primary bot or third-party chat interface.
2.  The bot sends a POST request JSON to the inbound REST endpoint \(via scripted REST API\).
3.  The ServiceNow AI Platform authenticates and processes the request, which is sent to Virtual Agent or a live agent.
4.  The ServiceNow AI Platform sends a POST response JSON from the outbound REST endpoint \(via REST API\) back to the bot.
5.  The primary bot or third-party chat interfaces displays the response to the user.

![Diagram that shows how the REST endpoints in the Virtual Agent API handle user input and authentication and bot response and authentication.](../images/va-api-steps.png "Inbound and outbound REST endpoints in the Virtual Agent API")

To see a demonstration of the Virtual Agent API and an FAQ, see [Getting Started with Virtual Agent APIs](https://community.servicenow.com/community?id=community_article&sys_id=080e3903dbc4e4107d3e02d5ca96198c) on the Community site.

## Limitations

The Virtual Agent API does not support the following features:

-   Chat branding through this Virtual Agent API integration.
-   Now Assist capabilities are supported only in asynchronous mode.

-   **[Supported features in Virtual Agent API](virtual-agent-api-whats-new.md)**  
You can use the Virtual Agent API to integrate many of the same features that are available in Virtual Agent and Agent Chat into your chat environment. Feature support varies depending on your ServiceNow release and the store app version number of the Virtual Agent API.
-   **[Supported versions and licensing requirements in Virtual Agent API](virtual-agent-api-supported-versions-licensing.md)**  
Get a quick overview of the important information that is related to the Virtual Agent API.

**Parent Topic:**[Virtual Agent API](virtual-agent-api-landing-page.md)

