---
title: Enable Now Assist in Virtual Agent for Slack
description: Enable the large language model \(LLM\)-based conversational experience with Now Assist in your Virtual Agent integrated with Slack.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [Use Now Assist in VA conversations with Slack, Conversational Integration with Slack, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Enable Now Assist in Virtual Agent for Slack

Enable the large language model \(LLM\)-based conversational experience with Now Assist in your Virtual Agent integrated with Slack.

## Before you begin

Ensure that you enable AI Search to have Now Assist conversations using the Now LLM Service. For more information about enabling AI Search, see [Enable AI Search for Next Experience](https://www.servicenow.com/docs/access?context=enable-ais-next-exp-app&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

Role required: admin

## Procedure

1.  Log in to your ServiceNow instance and navigate to the Now Assist Features page through one of the following navigation paths:

    -   **All** &gt; **Now Assist Admin** &gt; **Now Assist Features**.
    -   **All** &gt; **Now Assist Admin** &gt; **Features**.
2.  From the Now Assist Features page, select **Platform**.

3.  On the Now Assist skills for Platform page, select **View details**.

4.  On the Conversational experience page, select **Set up Now Assist in Virtual Agent**.

    You're directed to the Assistants page to select the Virtual Agent. For example, the **Now Assist in Virtual Agent \(default\)**.

5.  Select a Virtual Agent of your choice.

    ![Select a Virtual Agent that has Now Assist enabled to proceed with LLM capabilities.](../images/assistants-na-va.png)

    **Note:** Verify that the Virtual Agent you choose is integrated with the Slack workspace before selecting.

6.  On the bot page, navigate to **Display experience** &gt; **Channels** from the pane.

7.  Select the channels to integrate with the Now Assist in Virtual Agent.

    ![Select the Slack channels for LLM conversational experience with Now Assist.](../images/choose-channels-for-LLM.png)

8.  On the bot page, navigate to **Chat experience** &gt; **Chat experience** from the pane.

9.  Scroll down to the Response streaming section and select the **Allow response streaming** check box.

    ![Select Allow response streaming check box in the Response streaming section.](../images/choose-response-streaming-for-slack.png)

    **Important:** In the Now Assist Search Results Output Type \[now\_assist\_va\_search\_results\_output\_type\] table, set the **Streaming Ready** field value to `true` for Slack.![Set the Streaming Ready field value to true for Slack.](../images/choose-response-streaming-for-slack-true.png)

10. Select **Save and Continue**.


**Parent Topic:**[Using Now Assist in Virtual Agent conversations with Slack](../concept/na-va-llm-slack.md)

