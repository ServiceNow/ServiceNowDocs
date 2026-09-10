---
title: ServiceNow AI agents as secondary agents
description: Secondary agents are specialized AI agents that handle specific workflow tasks delegated by a primary agent or user. You can connect your ServiceNow agent to other agentic AI model providers using the Agent2Agent protocol.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/a2a-secondary-agent.html
release: australia
topic_type: concept
last_updated: "2026-08-31"
reading_time_minutes: 1
breadcrumb: [Integrate external AI agents, AI Agent Studio, Enable AI experiences]
---

# ServiceNow AI agents as secondary agents

Secondary agents are specialized AI agents that handle specific workflow tasks delegated by a primary agent or user. You can connect your ServiceNow agent to other agentic AI model providers using the Agent2Agent protocol.

## Enable ServiceNow AI agents as secondary agents

You can enable ServiceNow AI agents as secondary agents to use on other AI platforms. To do so, navigate to **AI Agent Studio** &gt; **Settings** &gt; **External AI agents** and toggle **Allow third party access to ServiceNow AI agents**.\[Omitted image "third-party-snow-agents.png"\] Alt text: Option to enable integration of ServiceNow AI agents int external agentic AI systems.

## Secondary agents overview

After creating your AI agent in AI Agent Studio, you can point it to the Agent Card URL that is displayed for secondary agents. Admins can view, copy, and consume the URL for easy access. The endpoint to point the AI agent to Agent Card for the actual execution of the AI agent is in the `{{instance}}.service-now.com/api/sn_aia/a2a/v2/agent/id/{{agent-id}}` format.

You can use the same OAuth or API key for authenticating the agent discovery and the agent execution. For more information, see [A2A API Key credential behavior](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/a2a-api-key-credential-behavior-new.md).

To verify that your AI agent is running from the ServiceNow side, during a conversation with the AI agent, you can go to the **Execution Plan \[sn\_aia\_execution\_plan\]** table. From the Execution Plan table, you can identify the execution plan based on the **Objective** field that contains the prompt from the conversation on the other platform.

For more information about setting up instructions for your ServiceNow AI agents as secondary agents \(acting as A2A server\), refer to [Authentication for Google A2A - ServiceNow as Secondary Agent](https://www.servicenow.com/community/now-assist-articles/authentication-for-google-a2a-servicenow-as-secondary-agent/ta-p/3446091).

For more information about sample payloads for Google A2A with ServiceNow AI agent as Secondary agent, see [Sample payloads for Google A2A](https://www.servicenow.com/community/now-assist-articles/sample-payloads-for-google-a2a-servicenow-as-secondary-agent/ta-p/3451904).

