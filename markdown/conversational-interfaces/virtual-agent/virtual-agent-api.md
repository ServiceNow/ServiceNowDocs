---
title: Using Virtual Agent API
description: Use the ServiceNow Virtual Agent API app to integrate any chat interface or a bot with ServiceNow Virtual Agent or Agent Chat. The app is available from the ServiceNow Store.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Using Virtual Agent API

Use the ServiceNow® Virtual Agent API app to integrate any chat interface or a bot with ServiceNow® Virtual Agent or Agent Chat. The app is available from the ServiceNow® Store.

## Overview of the Virtual Agent API

The Virtual Agent API is a REST API. This API is built on the conversational custom chat integration framework that is provided with Virtual Agent starting in the Paris release. The API enables ServiceNow developers, advanced users, and admins to use Virtual Agent in either of the following ways:

-   **Standalone bot**

    Use Virtual Agent as a standalone bot that you integrate with enterprise or with any other third-party chat interface that supports conversational interfaces.

    Your end users can interact with the Virtual Agent and Agent Chat through multiple channels by using this integration.

-   **Secondary bot**

    Use Virtual Agent as a secondary bot in an environment that has multiple, specialized bots managed by a primary bot.

    In this scenario, a primary bot manages communication with secondary bots on behalf of the end user. A primary bot could be IBM Watson Assistant, Microsoft LUIS, or a homegrown primary bot.

    Your secondary bots, such as the ServiceNow bot, might handle specific types of end-user requests, such as service tickets or reservations.

-   **Bot Interconnect**

    Use Virtual Agent Bot Interconnect as the primary bot in a diverse chat environment. Bot Interconnect creates a unified chat experience and gives your end users access to multiple channels and a wide variety of enterprise tasks that are available from ServiceNow.


The Virtual Agent API is useful for creating server-to-server integrations. However, for integrations that require the transformation of unsupported controls that must be rendered in your existing chat interface, consider using the [Custom Chat Integration Framework](va-custom-adapter-framework.md).

For information about features such as the URL format and the supported request and response parameters in the Virtual Agent API, see [Virtual Agent Bot Integration API](https://www.servicenow.com/docs/access?context=bot-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

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

-   Chat branding through this Virtual Agent API integration

## Version and release compatibility

<table id="table_syv_gzb_dqb"><thead><tr><th>

Version

</th><th>

Compatible Releases

</th></tr></thead><tbody><tr><td>

3.10.0

</td><td>

Washington DC

</td></tr><tr><td>

3.9.x

</td><td>

Vancouver

</td></tr><tr><td>

3.8.x

</td><td>

Vancouver

</td></tr><tr><td>

3.7.x

</td><td>

Utah

</td></tr><tr><td>

3.5.x

</td><td>

Tokyo

</td></tr><tr><td>

3.0.x

</td><td>

San Diego

</td></tr><tr><td>

2.0.x

</td><td>

Rome A subset of features is compatible with Quebec.

</td></tr><tr><td>

1.3.0

</td><td>

Quebec

</td></tr><tr><td>

1.0.12

</td><td>

Quebec

</td></tr><tr><td>

1.0.9

</td><td>

Paris

</td></tr></tbody>
</table>**Note:** The Virtual Agent API requires a Pro license similar to that of Virtual Agent.

-   **[Virtual Agent API features](va-api-features.md)**  
You can use the Virtual Agent API to integrate many of the same features that are available in Virtual Agent and Agent Chat into your chat environment. Feature support varies depending on your ServiceNow release and the Store app version number of the API.
-   **[Virtual Agent API features available in Store release 2.0.x](va-api-features-v2.md#)**  
Virtual Agent API version 2.0.x provides access to more of the same features that are available in Virtual Agent and Agent Chat, including rich control support and notifications.
-   **[Virtual Agent API features available in Store release 3.0.x](va-api-features-v3.md#)**  
Virtual Agent API version 3.0.x provides access to more of the same features that are available in Virtual Agent and Agent Chat, including the ability to upload files from a private URL and synchronous handshake enhancements.
-   **[Install the Virtual Agent API](../task/install-virtual-agent-api.md)**  
Install the Virtual Agent API app to integrate any chat interface or a bot with ServiceNow® Virtual Agent or Agent Chat.
-   **[Review the inbound REST endpoint and configure inbound authentication](../task/configure-send-request.md)**  
After you install the Virtual Agent API, navigate to the Scripted REST API resource to review the endpoint and set up authentication.
-   **[Configure Message Authentication for inbound communication](../task/set-up-message-auth-va-api.md)**  
You can configure Message Authentication for the Virtual Agent API instead of Basic or OAuth. Message Authentication involves configuring either Static or Hash tokens, setting up Provider Authentication, and setting the channel identity.
-   **[Configure the output response REST endpoint and outbound authentication for the Virtual Agent API](../task/configure-response-endpoint-va-api.md)**  
Specify the outbound endpoint URL to which the Virtual Agent responses are posted. Configure outbound authentication.
-   **[Virtual Agent bot-to-bot integration](bot2bot.md)**  
The Virtual Agent API supports environments that use multiple bots. In this situation, a primary bot communicates with third-party secondary bots, such as a ServiceNow bot.
-   **[Closing idle bot-to-bot conversations](va-b2b-open-conversation.md)**  
In bot-to-bot integrations \(Virtual Agent API\), abandoned conversations that are "idle" for more than an hour are automatically closed by the scheduled job, **Time Out Abandoned B2B Conversations**. This job runs hourly each day.
-   **[Configure multiple provider applications](configure-multiple-provider-applications.md)**  
You can configure multiple provider applications to support AI agents where there are multiple primary bots using Virtual Agent API and you need to distinguish between them.
-   **[Transform Virtual Agent API request and response](transform-virtual-agent-api-request-and-response.md)**  
You can transform Virtual Agent API request and response into supported formats through the scripted extension points provided in Virtual Agent API.
-   **[Enable Now Assist experience in Virtual Agent API](enable-now-assist-in-virtual-agent-experience-in-virtual-agent-api.md)**  
Enable Now Assist experience in Virtual Agent API to support generative AI skills across multiple provider channels.

**Parent Topic:**[Building and deploying Virtual Agent](using-virtual-agent.md)

