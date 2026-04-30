---
title: Create a Virtual Agent Bot Interconnect shell topic to call Google Dialogflow topics
description: To access topics in the Google Dialogflow secondary bot, you must create at least one Virtual Agent Bot Interconnect topic.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Using Google Dialogflow as a secondary bot with Virtual Agent Bot Interconnect, Using Virtual Agent Bot Interconnect in your configuration, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Create a Virtual Agent Bot Interconnect shell topic to call Google Dialogflow topics

To access topics in the Google Dialogflow secondary bot, you must create at least one Virtual Agent Bot Interconnect topic.

## Before you begin

Create one or more intents in Google Dialogflow. For details, refer to the [Dialogflow documentation](https://cloud.google.com/dialogflow/es/docs/quick/build-agent).

[Configure connections to Google Dialogflow in your Virtual Agent Bot Interconnect instance](configure-sn-instance-google-dialogflow.md).

Role required: virtual\_agent\_admin or admin

## About this task

There are two ways to integrate Google Dialogflow intents with Bot Interconnect

-   Create one Virtual Agent Bot Interconnect topic per Dialogflow intent.

    In case of NLU topics, each Virtual Agent topic has the same name as a single Dialogflow intent. For example, if you have two Dialogflow intents named **order a drink** and **book a ticket**, then you would create two Virtual Agent topics also named **order a drink** and **book a ticket**.

    In case of LLM topics, each Bot Interconnect topic has the same name and description as the corresponding Google Dialogflow topic.

-   Map multiple Dialogflow intents to a single Virtual Agent Bot Interconnect topic. This scenario is applicable only for NLU topics.

    Create a Virtual Agent topic for your Dialogflow intents and name it accordingly. For example, **DG ordering issues**. In this scenario, the Dialogflow intents are mapped to the topic as either keywords or utterances, depending on your method of topic discovery. So if you have two Dialogflow intents named **order a drink** and **book a ticket**, you would add both phrases to the topic as keywords or you would add them as utterances to the topic's corresponding intent.


## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  [Create a topic](create-virtual-agent-topic.md) for your Dialogflow intents.

    In case of NLU topics, include the Dialogflow intent names as either keywords or utterances in the corresponding ServiceNow Virtual Agent intent. In case of LLM topics, the topic name and description of the Bot Interconnect topic should match the topic name and description of the Google Dialogflow topic.

3.  On the **Flow** tab, drag a Topic Block utility node onto the canvas.

4.  Select the node, and then fill in the form as follows:

    |Property|Description|
    |--------|-----------|
    |Topic Block|Select **Bot Interconnect** topic block for NLU topics and **Bot Interconnect - LLM** topic block for LLM topics.|
    |Action Name|Enter: `sn_va_bot_ic.dialogflow_bot_interconnect_integration`|
    |Action Type|Enter `subflow`.|

5.  Click **Save**.

6.  Click **Publish**.


## What to do next

Test your configuration. You can execute the topics that are available in the secondary bot from channels where Bot Interconnect is deployed.

**Parent Topic:**[Using Google Dialogflow as a secondary bot with Virtual Agent Bot Interconnect](../concept/using-va-api-ggl-dialogflow.md)

**Previous topic:**[Configure connections to Google Dialogflow in your Virtual Agent Bot Interconnect instance](configure-sn-instance-google-dialogflow.md)

**Next topic:**[Using Microsoft Power Virtual Agents as a secondary bot with Virtual Agent Bot Interconnect](../concept/using-va-api-ms-powerva.md)

