---
title: Virtual Agent bot-to-bot integration
description: The Virtual Agent API supports environments that use multiple bots. In this situation, a primary bot communicates with third-party secondary bots, such as a ServiceNow bot.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Virtual Agent API, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Virtual Agent bot-to-bot integration

The Virtual Agent API supports environments that use multiple bots. In this situation, a primary bot communicates with third-party secondary bots, such as a ServiceNow bot.

There are two types of bot communication with the primary bot:

-   If the primary bot understands an end user’s request \(intent\), the primary bot routes the request to the appropriate secondary bot, which displays the corresponding topic.
-   If the primary bot cannot determine where to route a user request, the primary bot can broadcast a user’s request to all secondary bots. Each secondary bot returns a prediction confidence score for determining the end user’s intent. The primary bot then routes the request to the secondary bot with the highest prediction confidence score.

In both scenarios, the ServiceNow bot informs the primary bot when the request is completed or when it cannot continue handling the request. The primary bot can then determine whether to inform the end user that the conversation is complete or provide further assistance.

![Diagram of a bot-to-bot ecosystem with the ServiceNow Virtual Agent as a secondary bot.](../images/bot-to-bot-ecosystem.png "Bot-to-Bot ecosystem with ServiceNow Virtual Agent as a secondary bot")

The ServiceNow secondary bot uses a standard request and response through REST endpoints. When the request is received through the Bot Framework or an enterprise app seeking to integrate with the ServiceNow bot, the response for a request is sent asynchronously via the API to the requesting system. Virtual Agent supports Live Agent in the channel as well.

## Properties for bot-to-bot integrations

You can [add system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) to configure the following:

-   Number of times that the Virtual Agent bot tries to get a response
-   Bot normalization score

|Property|Description|Default value|
|--------|-----------|-------------|
|va.bot.to.bot.take.control\_times|Number of times that Virtual Agent tries to get a response, after which control is returned to the primary bot.|2|
|va.bot.to.bot.score.normalization\_factor|A value used to normalize the prediction confidence score returned by Virtual Agent, if the primary bot does not use intents to route requests to the appropriate bot.|1|

**Parent Topic:**[Using Virtual Agent API](use-virtual-agent-api.md)

