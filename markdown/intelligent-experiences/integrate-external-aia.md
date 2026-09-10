---
title: Integrate external AI agents
description: Integrate external AI agents in AI Agent Studio to connect the ServiceNow AI Platform with third-party agentic AI providers as primary agents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/integrate-external-aia.html
release: australia
topic_type: concept
last_updated: "2026-08-25"
reading_time_minutes: 3
breadcrumb: [AI Agent Studio, Enable AI experiences]
---

# Integrate external AI agents

Integrate external AI agents in AI Agent Studio to connect the ServiceNow AI Platform with third-party agentic AI providers as primary agents.

## What are External Agents

External agents are autonomous AI systems deployed on platforms other than ServiceNow. They are designed to perform specialized tasks within their native environments and can be connected to ServiceNow AI agents through integration protocols. External agents bring domain-specific intelligence, proprietary algorithms, or third-party automation capabilities into your ServiceNow ecosystem.

External agents operate independently and aren't managed directly by the ServiceNow platform. Instead, they are invoked by ServiceNow agents through defined API contracts or messaging protocols, allowing two-way communication and task orchestration across system boundaries.

## Discover External AI agents

You can enable external AI agents on the AI Agent Studio via the Settings page. Navigate to **AI Agent Studio** &gt; **Settings** &gt; **External Agents** &gt; **Discoverability**.\[Omitted image "aia-a2a-discoverability-new.png"\] Alt text: Discover External AI agents to accessed by ServiceNow and third-parties.

-   **Allow ServiceNow to access external AI agents**: The external AI agents can integrate with the ServiceNow agentic AI system using the A2A protocol, with the **Allow** radio button selected by default.

    To prevent external AI agents from being integrated with the ServiceNow agentic AI system using the A2A protocol, select **Do not allow**.

-   **Allow third party access to ServiceNow AI agents**: The ServiceNow AI agents are configured by default for integration into external AI systems, with the **Allow** option selected by default.

    To prevent ServiceNow AI agents from being integrated into the external agentic AI system, select **Do not allow**.

    **Important:** You can integrate ServiceNow AI agents into other agentic AI systems, such as Google Cloud or Azure OpenAI.

    For information about setting up ServiceNow AI agents as secondary agents \(acting as A2A server\) for integrating into other agentic AI systems, see [ServiceNow AI agents as secondary agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/a2a-secondary-agent.md).

-   **Communication mode**: Controls how external AI agents interact with the ServiceNow agentic AI system.

    You have two types of communication modes:

    -   **Synchronous**: The external AI agent waits for a response before proceeding. The communication is real-time and blocking — the agent pauses until ServiceNow returns a result.
    -   **Asynchronous**: The external AI agent does not wait for an immediate response. Communication is non-blocking — the agent can continue processing and handle ServiceNow responses when they are available, typically through callbacks or event-driven mechanisms. Asynchronous mode is the default communication mode.

When creating a new external AI agent in AI Agent Studio, you can connect your agent to the ServiceNow agentic AI system using the Agent2Agent \(A2A\) protocol integration. To do this, you must have a Connection &amp; Credential alias record that connects to your agentic AI provider.

After connecting to the external AI agent, you can add details about its role and instructions to provide context for the AI Agent Orchestrator. Additional context helps differentiate your AI agent from other AI agents so that the AI Agent Orchestrator can decide about which agent to use.

## Contextual data access for External AI agents

You can enable contextual data access for external AI agents to improve AI agent response during execution on the AI Agent Studio via the Settings page. Navigate to **AI Agent Studio** &gt; **Settings** &gt; **External Agents** &gt; **Discoverability**.\[Omitted image "aia-a2a-contextual-data.png"\] Alt text: Enable contextual data access for External AI agents.

-   **Short-term memory**: Turn on the toggle to enable external AI agents remember your preferences or facts from the current interaction only. The toggle is turned on by default.
-   **Long-term memory**: Turn on the toggle to enable external AI agents remember your preferences or facts from previous interaction. The toggle is turned on by default.
-   **Knowledge graph for external AI agent interactions**: Turn on the toggle to enable external AI agents to use structured and unstructured data from different records across the ServiceNow AI Platform. The toggle is turned off by default.

