---
title: Create a Virtual Agent Bot Interconnect shell topic to call Virtual Agent secondary topics
description: To use ServiceNow Virtual Agent as a secondary bot with Virtual Agent Bot Interconnect, you must create at least one shell topic in Bot Interconnect.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Using ServiceNow Virtual Agent as a secondary bot with Virtual Agent Bot Interconnect, Using Virtual Agent Bot Interconnect in your configuration, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Create a Virtual Agent Bot Interconnect shell topic to call Virtual Agent secondary topics

To use ServiceNow® Virtual Agent as a secondary bot with Virtual Agent Bot Interconnect, you must create at least one shell topic in Bot Interconnect.

## Before you begin

Create and publish topics in the secondary instance of ServiceNow Virtual Agent.

Enable synchronous or asynchronous mode on the secondary ServiceNow Virtual Agent instance.

Role required: virtual\_agent\_admin or admin

## About this task

There are two ways to integrate secondary Virtual Agent topics with Bot Interconnect:

-   Create one Virtual Agent Bot Interconnect topic per secondary Virtual Agent topic.

    In case of NLU topics, each Bot Interconnect topic has the same name as the corresponding secondary Virtual Agent topic. For example, if you have two secondary Virtual Agent topics named **order a drink** and **book a ticket**, then you would create two Virtual Agent Bot Interconnect topics also named **order a drink** and **book a ticket**.

    In case of LLM topics, each Bot Interconnect topic has the same name and description as the corresponding secondary Virtual Agent topic.

-   Map multiple secondary Virtual Agent topics to a single Virtual Agent Bot Interconnect topic. This scenario is applicable only for NLU topics.

    Create one Virtual Agent Bot Interconnect topic and name it accordingly. For example, **SVA ordering issues**. In this scenario, the secondary Virtual Agent topics are mapped to the Bot Interconnect shell topic as either keywords or utterances, depending on your method of topic discovery. So if you have two secondary Virtual Agent topics named **order a drink** and **book a ticket**, you would add both phrases to the Bot Interconnect topic as keywords or you would add them as utterances to the Bot Interconnect topic's corresponding intent.


## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  [Create a topic](create-virtual-agent-topic.md) in your primary instance of Virtual Agent.

    In case of NLU topics, include the secondary Virtual Agent topic names as either keywords or utterances in the corresponding Bot Interconnect intent. In case of LLM topics, the topic name and description of the Bot Interconnect topic should match the topic name and description of the secondary Virtual Agent topic.

3.  On the **Flow** tab, drag a Topic Block utility node onto the canvas.

4.  Select the node, and then fill in the form as follows:

<table id="table_oq1_5px_ksbxxx"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Topic Block

</td><td>

Select **Bot Interconnect** topic block for NLU topics and **Bot Interconnect - LLM** topic block for LLM topics.

</td></tr><tr><td>

Action Name

</td><td>

-   If the secondary bot is configured in synchronous mode, enter `sn_va_bot_ic.va_api_bot_interconnect_integration_handler`
-   If the secondary bot is configured in asynchronous mode, enter `sn_va_bot_ic.va_api_bot_interconnect_async_integration_handler`


</td></tr><tr><td>

Action Type

</td><td>

Enter `subflow`.

</td></tr><tr><td>

Async Response Transformer

</td><td>

If the secondary bot is configured in asynchronous mode, enter `sn_va_bot_ic.va_api_bot_interconnect_async_response_handler`

</td></tr></tbody>
</table>5.  Click **Save**.

6.  Click **Publish**.


**Parent Topic:**[Using ServiceNow Virtual Agent as a secondary bot with Virtual Agent Bot Interconnect](../concept/using-sn-secondary-bot-with-sn-primary.md)

**Previous topic:**[Create an auth token in the ServiceNow secondary instance](create-auth-token-sn-secondary-instance.md)

**Next topic:**[Enable live agent connection on the primary instance](../concept/enable-live-agent-connection-on-the-secondary-instance.md)

