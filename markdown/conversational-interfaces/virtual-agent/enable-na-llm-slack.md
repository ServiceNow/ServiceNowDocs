---
title: Enable ServiceNow Otto for Virtual Agent in Slack
description: Enable large language model \(LLM\) conversational experiences with ServiceNow Otto in your Slack integration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/virtual-agent/enable-na-llm-slack.html
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 1
breadcrumb: [Use ServiceNow Otto conversations with Slack, Conversational Integration with Slack, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Enable ServiceNow Otto for Virtual Agent in Slack

Enable large language model \(LLM\) conversational experiences with ServiceNow Otto in your Slack integration.

## Before you begin

Ensure that you enable AI Search. For more information about enabling AI Search, see [Enable AI Search for Next Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/enable-ais-next-exp-app.md).

Role required: admin

## Procedure

1.  Log in to your ServiceNow instance and navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer**.

2.  On the Assistants tab, select **Edit** for an assistant that is integrated with Slack.

    For example, select **ServiceNow Otto for Virtual Agent \(default\)**.

    \[Omitted image "assistants-na-va-2.png"\] Alt text: Select an assistant that is integrated with Slack.

    **Note:** Verify that the assistant you choose is integrated with the Slack workspace before selecting it.

3.  On the assistant configuration page, navigate to **Review display experiences** &gt; **Channels**.

4.  Select the Slack channels to integrate with ServiceNow Otto for Virtual Agent.

    \[Omitted image "choose-channels-for-LLM.png"\] Alt text: Select the Slack channels for LLM conversational experience with ServiceNow Otto.

5.  On the assistant configuration page, navigate to **Chat features**.

6.  In the Response streaming section, select the **Allow response streaming** check box.

    \[Omitted image "choose-response-streaming-for-slack-2.png"\] Alt text: Select Allow response streaming check box in the Response streaming section.

7.  Select **Save and Continue**.


**Parent Topic:**[Using ServiceNow Otto for Virtual Agent conversations with Slack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/na-va-llm-slack.md)

