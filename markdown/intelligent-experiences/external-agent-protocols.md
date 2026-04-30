---
title: Integrating external AI agents
description: Integrate and configure external agents with the ServiceNow agentic AI system using Agent2Agent \(A2A\) protocol and manual integration to use in agentic workflows created in AI Agent Studio.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-11-18"
reading_time_minutes: 3
keywords: [a2a]
breadcrumb: [Create an external agent, Create an AI agent, Now Assist AI agents, Enable AI experiences]
---

# Integrating external AI agents

Integrate and configure external agents with the ServiceNow agentic AI system using Agent2Agent \(A2A\) protocol and manual integration to use in agentic workflows created in AI Agent Studio.

## External agent discovery on the ServiceNow AI Platform

You can enable external AI agents on the AI Agent Studio via the Settings page. Navigate to **AI Agent Studio** &gt; **Settings** &gt; **External AI agents** &gt; **Discoverability**.![image.external-agents-discoverability]

-   **Allow ServiceNow to access External AI agents**: Turn on the toggle to enable external AI agents integration with the ServiceNow agentic AI system using the A2A protocol.
-   **Allow third-party to access ServiceNow AI agents**: Turn on the toggle to enables integrating ServiceNow AI agents into external agentic AI systems.

When creating a new external AI agent in AI Agent Studio, you have two options for connecting your agent to the ServiceNow agentic AI system. One option is the Agent2Agent \(A2A\) protocol, and the other is manual integration.

For both options, you must have a Connection &amp; Credential alias record that connects to your agentic AI provider. With manual integration, you must also create structured JSON that fits your agentic AI provider's metadata for the AI agent to work as expected.

After connecting to the external AI agent, you can add details about its role and instructions to provide context for the AI Agent Orchestrator. Additional context helps differentiate your AI agent from other AI agents so that the AI Agent Orchestrator can decide about which agent to use.

## Contextual data access for external agents on the ServiceNow AI Platform

Enable contextual data access for external agents to improve AI agent response during execution.

-   **Short-term memory**: Turn on the toggle to enable external AI agents remember your preferences or facts from the current interaction only.
-   **Long-term memory**: Turn on the toggle to enable external AI agents remember your preferences or facts from previous interaction.
-   **Knowledge graph for external AI agent interactions**: Turn on the toggle to enable external AI agents to use structured and unstructured data from different records across the ServiceNow AI Platform.

![image.a2a-contextual-data-access]

## Manual integration overview

You can manually integrate a third-party agent using a Connection &amp; Credential alias and metadata in a structured JSON format. The alias and metadata connect your third party agent platform to your ServiceNow instance and identifies what information is being returned when the external AI agent sends a message.

See [Create an external AI agent with manual integration](../task/create-manual-external-agent.md) for instructions for manually integrating an external AI agent.

## Agent2Agent protocol overview

Agent2Agent \(A2A\) is an open standard that enables AI agents across different platforms to communicate with each other. The standard relies on every AI agent having an Agent Card associated with it that provides basic information for providers like the ServiceNow AI Platform, Azure, and Google to use them.

Version 0.3 of A2A is supported.

An AI agent's Agent Card uses standardized JSON to help different providers understand its capabilities. The Agent Card is accessed by a specific type of endpoint from a provider's server. Execution plans are communicated through an execution endpoint so that both the provider's server and the ServiceNow AI Platform can track what the external AI agent is doing.

See [Create an external AI agent with the Agent2Agent protocol](../task/create-a2a-agent.md) for instructions for using this protocol to create an AI agent.

## Configuring A2A authentication

A2A connections require authorization from the source platform to execute on the ServiceNow AI Platform. Authentication is established by creating two Connection &amp; Credential Alias and Connection records, one with an Agent Card endpoint and one with an execution endpoint.

## Configuration Properties

The following properties configure different aspects of how your agents can interact with the ServiceNow AI Platform.

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_aia.external\_agents.enabled

</td><td>

Set to `true` to enable external agent features

</td></tr><tr><td>

sn\_aia.external\_agents.parallel\_conversations.enabled

</td><td>

Enables or disables multiple simultaneous conversations per user

</td></tr></tbody>
</table>**Parent Topic:**[Create an external AI agent](create-external-aia.md)

