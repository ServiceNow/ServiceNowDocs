---
title: Explore Now Assist AI agents
description: Learn how the Now Assist AI agents enhance live agent productivity by mimicking human-like intelligence to manage tasks ranging from automated responses to complex problem solving.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-05-08"
reading_time_minutes: 4
keywords: [AI Agents, Agentic AI]
breadcrumb: [Now Assist AI agents, Enable AI experiences]
---

# Explore Now Assist AI agents

Learn how the Now Assist AI agents enhance live agent productivity by mimicking human-like intelligence to manage tasks ranging from automated responses to complex problem solving.

## Now Assist AI agents overview

The Now Assist AI agents are virtual agents within the ServiceNow AI Platform ecosystem. They can perform specific tasks and functions, often using natural language instead of traditional code.

AI agents can perform the following tasks:

-   Analyze data.
-   Retrieve information from knowledge bases and enterprise systems.
-   Execute automated actions.
-   Collaborate with other agents to resolve issues or accomplish requests.

Example: Imagine you need to reset your password. Multiple AI agents might be involved:

1.  One agent understands the request.
2.  Another verifies your account details.
3.  A third agent conducts a security check.
4.  A fourth agent resets the password and notifies you.

## Agentic AI framework

-   **[AI Agent Studio](ai-agent-studio.md)**

    The AI Agent Studio enables you to create, manage, and test AI agents and agentic workflows in a unified environment.

-   **[agentic system](../../now-assist-platform/concept/now-assist-glossary.md#)**

    The ServiceNow AI Platform's agentic system uses AI agents, orchestrated by an Orchestrator, to execute Agentic workflows.

-   **[AI agents](../../now-assist-platform/concept/now-assist-glossary.md#)**

    On the ServiceNow AI Platform agentic system, an AI agent contains a set of large language model \(LLM\) instructions with the tools to accomplish tasks.

-   **[agentic workflow](../../now-assist-platform/concept/now-assist-glossary.md#)**

    Agentic workflows are smart, context-aware, automated processes designed and executed by AI agents. They represent dynamic, human-like processes where specialized AI agents collaborate to accomplish complex goals. Here are a few key characteristics of Agentic workflows:

    -   **Autonomous**: Operate independently without constant human intervention.
    -   **Adaptive**: Adjust to changing situations and business needs.
    -   **Collaborative**: Work together to complete complex tasks.
    -   **Intelligent**: Use large language models and business data to make informed decisions.
-   **[Orchestrator](../../now-assist-platform/concept/now-assist-glossary.md#)**

    The AI agent Orchestrator is a central management system that coordinates AI agents to ensure they collaborate effectively to complete complex workflows.

    For more information, see [Understand the Now Assist AI agents](understand-na-aia.md).

-   **Guided Setup**

    The guided setup process in the helps you configure your AI Agent triggers, data sources, and display locations based on your specific business needs.

-   **[Now Assist panel](../../now-assist-platform/concept/now-assist-glossary.md#)**

    The Now Assist panel is a user-facing interface, commonly accessed through the context menu or chat interfaces. It provides quick access to agents' capabilities and enhances productivity by summarizing records, creating content, and analyzing alerts.

-   **Tools**

    Tools equip your AI agents with the necessary capabilities to complete their tasks. Adding a tool to an AI agent enables various functionalities and helps the AI agents achieve their objectives.


## How to put Now Assist AI agents to work

AI agents can use a variety of tools, such as web searches, record operations, and flows, to work on agentic workflows that you define.

Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview** &gt; **Get an overview of what to expect** and select **View steps** to see how you can successfully put your AI agents to work.

1.  Create an agentic workflow: agentic workflows define the problem and situation that you want your AI agents to work on. Without an agentic workflow, your agents don’t know when or what to work on.
2.  Create AI agents: AI agents use tools to execute tasks. Consider the tasks needed to solve the agentic workflow you created. Create one or more agents to execute those tasks.
3.  Test the agentic workflow: See how your AI agents perform. Make adjustments to either the agentic workflow or AI agents. Test until everything’s working the way you want.
4.  Deploy: Put your AI agents to work across your organization.

## AI agents configuration and execution

![Workflow describing the configuration of Now Assist AI agents and how they work to execute an agentic workflow.](../image/now-assist-ai-agents-workflow.png)

Now Assist AI agents have two components: AI agents and agentic workflows. By using Guided Setup in AI Agent Studio, you create AI agents and workflows, add tools or define triggers, and define the availability or display location. After they're created, you can duplicate, modify, and test them in AI Agent Studio.

In run time, triggers in the primary and secondary interfaces cause agentic workflow execution, where one or more AI agents execute the plan with the help of the AI agent Orchestrator to accomplish the task. After agentic workflow execution, the output appears in the Now Assist panel. To learn more about an AI agent Orchestrator is, see the [Understand the Now Assist AI agents](understand-na-aia.md).

