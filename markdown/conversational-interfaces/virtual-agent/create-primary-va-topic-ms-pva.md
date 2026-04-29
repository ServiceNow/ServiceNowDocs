---
title: Create a Virtual Agent Bot Interconnect shell topic to call Microsoft Power Virtual Agents topics
description: To access topics in the Power Virtual Agents secondary bot, you must create at least one Virtual Agent Bot Interconnect topic.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Virtual Agent, Bot Interconnect, Microsoft, Power, shell, topic]
breadcrumb: [Using Microsoft Power Virtual Agents as a secondary bot with Virtual Agent Bot Interconnect, Using Virtual Agent Bot Interconnect in your configuration, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Create a Virtual Agent Bot Interconnect shell topic to call Microsoft Power Virtual Agents topics

To access topics in the Power Virtual Agents secondary bot, you must create at least one Virtual Agent Bot Interconnect topic.

## Before you begin

Create one or more topics in Microsoft Power Virtual Agents.

[Add the Direct Line secret key to your Virtual Agent Bot Interconnect instance](add-dl-secret-key-sn-instance.md).

Role required: virtual\_agent\_admin or admin

## About this task

There are two ways to integrate Microsoft Power Virtual Agents topics with Bot Interconnect:

-   Create one Virtual Agent Bot Interconnect topic per Power Virtual Agents topic.

    In case of NLU topics, each Virtual Agent topic has the same name as a single Power Virtual Agents topic. For example, if you have two Power Virtual Agents topics named **order a drink** and **book a ticket**, then you would create two Virtual Agent topics also named **order a drink** and **book a ticket**.

    In case of LLM topics, each Bot Interconnect topic has the same name and description as the corresponding Power Virtual Agents topic.

-   Map multiple Power Virtual Agents topics to a single Virtual Agent Bot Interconnect topic. This scenario is applicable only for NLU topics.

    Create one Virtual Agent topic for your Power Virtual Agents topics and name it accordingly. For example, **PVA ordering issues**. In this scenario, the Power Virtual Agents topics are mapped to the topic as either keywords or utterances, depending on your method of topic discovery. So if you have two Power Virtual Agents topics named **order a drink** and **book a ticket**, you would add both phrases to the topic as keywords or you would add them as utterances to the topic's corresponding intent.


## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  [Create a topic](create-virtual-agent-topic.md) for your Power Virtual Agents topics.

    In case of NLU topics, include the Power Virtual Agents topic names as either keywords or utterances in the corresponding ServiceNow Virtual Agent intent. In case of LLM topics, the topic name and description of the Bot Interconnect topic should match the topic name and description of the Power Virtual Agents topic.

3.  On the **Flow** tab, drag a Topic Block utility node onto the canvas.

4.  Select the node, and then fill in the form as follows:

<table id="table_oq1_5px_ksb"><thead><tr><th>

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

Enter: `sn_va_bot_ic.direct_line_bot_interconnect_integration_handler`

</td></tr><tr><td>

Action Type

</td><td>

Enter `subflow`.

</td></tr><tr><td>

Additional Params \(String\)

</td><td>

Follow these steps:1.  Select the script icon ![Script icon.](../images/icon-script.png).
2.  In the Additional Params \(String\) window, add this code:

    ```
(function execute() {
    return JSON.stringify({'quick': false});
})()
    ```

3.  Select **Save**.


</td></tr></tbody>
</table>5.  Select **Save**.

6.  Select **Publish**.


## What to do next

Test your configuration. You can execute the topics that are available in the secondary bot from channels where Bot Interconnect is deployed.

**Note:** Conversations always remain open in Power Virtual Agents.

**Parent Topic:**[Using Microsoft Power Virtual Agents as a secondary bot with Virtual Agent Bot Interconnect](../concept/using-va-api-ms-powerva.md)

**Previous topic:**[Add the Direct Line secret key to your Virtual Agent Bot Interconnect instance](add-dl-secret-key-sn-instance.md)

**Next topic:**[Using ServiceNow Virtual Agent as a secondary bot with Virtual Agent Bot Interconnect](../concept/using-sn-secondary-bot-with-sn-primary.md)

