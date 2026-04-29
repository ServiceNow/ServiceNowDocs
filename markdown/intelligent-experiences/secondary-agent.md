---
title: ServiceNow AI agents as secondary agents
description: Integrate ServiceNow AI agents into other agentic AI systems, such as Google Cloud or Azure OpenAI.
locale: en-US
release: australia
topic_type: concept
last_updated: "2025-11-18"
reading_time_minutes: 2
breadcrumb: [Create an external agent, Create an AI agent, Now Assist AI agents, Enable AI experiences]
---

# ServiceNow AI agents as secondary agents

Integrate ServiceNow AI agents into other agentic AI systems, such as Google Cloud or Azure OpenAI.

## Enabling discovery of ServiceNow mobile agents

In AI Agent Studio, on the **Settings** page, under **External AI Agents** &gt; **Discoverability**, you can enable the discovery of ServiceNow AI agents to use on other AI platforms. To do so, toggle **Allow third party to access ServiceNow AI Agents**.

You can also choose between **Synchronous** and **Asynchronous** communication between your external AI agent and the agentic AI provider.

![Discoverability page in AI Agent Studio settings.](../image/A2A-asynchronous.png)

## ServiceNow AI agents as secondary agents overview

You can connect your ServiceNow agent to other agentic AI model providers using the Agent2Agent protocol.

After creating your AI agent in AI Agent Studio, you can point to the Agent Card URL that is displayed for secondary agents for easy access so the admins can view, copy, and consume the URL.

The endpoint to point to for the actual execution of the AI agent is in the format `{{instance}}.service-now.com/api/sn_aia/a2a/v2/agent/id/{{agent-id}}`.

You can use the same OAuth or API key for authenticating the agent discovery and the agent execution.

To verify that your AI agent is running from the ServiceNow side, during a conversation with the AI agent, you can go to the **Execution Plan \[sn\_aia\_execution\_plan\]** table. From the Execution Plan table, you can identify the execution plan based on the **Objective** field that contains the prompt from the conversation on the other platform.

For more information about sample payloads for Google A2A with ServiceNow AI agent as Secondary agent, see [Sample payloads for Google A2A.](https://www.servicenow.com/community/now-assist-articles/sample-payloads-for-google-a2a-servicenow-as-secondary-agent/ta-p/3451904)

## Asynchronous connection

Asynchronous connection involves communication where the sender and receiver don't have to be active simultaneously unlike the synchronous communication mode.

To establish asynchronous connection, you must obtain a callback URL for push notifications to function.

Once you have obtained a callback URL, you must create a record on the External Agent Callback Registries \[sn\_aia\_external\_agent\_callback\_registry\] table. Go to the table, select **New**, and enter the callback URL. Save the record.

Once you save the record, a Connection &amp; Credential Alias \[sys\_alias\] record is created for you. To add authentication, you can open the Connection record associated with the sys\_alias record and add a credential to the **Credential** field.

When the record is created, you can go back to the External Agent Callback Registry record you created and select **Verify URL** to test the connection works as expected.

**Parent Topic:**[Create an external AI agent](create-external-aia.md)

