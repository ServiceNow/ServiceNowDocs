---
title: Configure AI Agent Studio
description: Configure AI agents, agentic workflows, and tools so that AI agents can plan and execute tasks using your record data and knowledge base content.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/configuring-aia-new.html
release: australia
topic_type: concept
last_updated: "2026-06-06"
reading_time_minutes: 5
keywords: [Configure AI Agents]
breadcrumb: [AI Agent Studio, Enable AI experiences]
---

# Configure AI Agent Studio

Configure AI agents, agentic workflows, and tools so that AI agents can plan and execute tasks using your record data and knowledge base content.

AI agents follow your instructions and act toward a specific goal by using the tools you configure for them. Using the context of your records and searchable content, AI agents plan and analyze tasks by combining business logic with instructions sent to large language models \(LLMs\), which suggest the next best action to take.

**Note:** Keep your record data and knowledge base up to date for best results.

## Prerequisites

Before configuring AI agents, establish a clear plan to improve agent performance and result quality. A solid foundation minimizes redundant agents and maximizes the efficiency of existing ones.

-   Identify the different kinds of tasks your agentic workflow must handle.
-   Understand the general flow for your agentic workflow and agents.
-   Prepare agentic tools with well-written descriptions.

## Configurable elements

Use the following elements to instruct agentic workflows and AI agents within the framework.

-   **__Base plan__**

    Instructions to the AI Agent Orchestrator for the initial planning procedure. Configured at the agentic workflow level.

-   **__Role__**

    A clear identity for the AI agent, comprising two elements:

    -   **__Agent reasoning__**

        When a role is added to each reasoning prompt, it gives the LLM a sense of identity for the content it generates.

    -   **__Agent proficiency__**

        An auto-generated, LLM-produced description of what an agent is capable of, derived from the role, instructions, and the descriptions of its assigned tools.

-   **__Instructions__**

    Clear directives for the AI agent. Write instructions as a step-by-step algorithm that describes the operational flow the agent should follow.


## Tool elements for agentic workflows

Each tool in an agentic workflow is defined by three elements: its functionality, its description, and its error messages.

-   **Functionality**

    Functionality defines what an AI agent contributes to the agentic workflow. Configure each tool with a single, clearly scoped purpose. Multipurpose tools degrade agent performance for two reasons:

    -   They are harder for the AI Agent Orchestrator to reason through. When a tool can serve more than one purpose, the orchestrator must determine which purpose applies, which increases runtime.
    -   The tool description must account for every usage scenario, making it harder to write accurately and completely.
    **Note:** Configure each tool as the solution to a single problem. Avoid tools that can operate in different modes.

-   **Tool description**

    Tool descriptions are natural language statements that explain the utility a tool provides. Clear scope and limits help verify tools are selected for appropriate scenarios. A strong tool description includes all of the following:

    -   What the tool does.
    -   The specific agentic workflows and tasks where the tool applies.
    -   Scenarios where the tool is explicitly not useful, especially cases where an AI agent might incorrectly select it.
    -   Definitions of any terms used. For example, if a tool assigns a role to a user, explain what "role" means in the context of that instance.
-   **Error messages**

    AI agents learn through trial and error. Error messages give an agent feedback on incorrect tool executions, helping it reach more valid conclusions in subsequent steps. Understanding where a tool can fail helps keep execution on track.


## Invoke Conversations with the AI Agent Background Channel

The AI Agent Background Channel lets you invoke AI agent or agentic workflow execution from the Workspace. Use it with the AI Agent Background Provider, which is based on the Custom Adapter Framework from Virtual Agent. For more information, see [Configure a provider for your custom chat integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/create-provider-va-cccif.md).

To add conversational capabilities to your own provider application and obtain a new inbound ID, create a channel identifier in the Provider Channel Identities table \[sys\_cs\_provider\_application\]. For more information, see [Create a channel identifier for your custom chat integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/create-channel-id-va-cccif.md).

To start a conversation, trigger the flow using the sn\_aia.AiAgentRunttimeUtil\(\).startAiAgentConversation\(request\) API in the Script Include \(sys\_script\_include\) of the AIAgentBackgroundProvider, then select **Run Script**. When the script execution status shows **Success**, the conversation begins in the order of utterances defined in the script.

Conversations invoked for AI agent execution are logged in the Execution Plans \[sn\_aia\_execution\_plan\] table. Open the conversation record to confirm the device type as **AI Agent Background**. Open the execution record to review the **Execution Tasks**, **Messages**, and **Tool Executions**.

You can also review the complete execution steps on the AI Agent Studio Testing page. Copy the execution plan record's sys\_id and test it there. On the **Chat responses** tab, the AI agent decision logs show agent details and the tools used to resolve the issue.

## Interactive and non-interactive execution modes

AI agents operate in one of the two execution modes, which determine how the agent handles fallback scenarios during execution.

-   **Interactive**

    The AI agent reaches out to the user for information when a fallback occurs, then re-triggers the flow after receiving a response.

-   **Non-interactive**

    The AI agent does not contact the user at any fallback stage. Instead, it uses a dynamic prompt approach through the ReAct layer, where the prompt adapts based on the execution mode. Fallback options don't collect user input. The output of the AI agent or agentic workflow is still presented to the user, and any execution failure displays a message in the Now Assist panel or Virtual Agent.


The execution mode is set in the **Execution Mode** field in the Execution Plans \[sn\_aia\_execution\_plan\] table and is determined at runtime.

AI agents and agentic workflows can run concurrently in the AI Agent Background Channel and in non-interactive mode. Background execution allows AI agents to operate alongside any chat panel, such as the Now Assist panel or Virtual Agent.

## Multilingual support

AI agents support multiple languages to improve translation quality. You can:

-   Tune system prompts for native-language translations.
-   Implement dynamic translation strategies when native support is unavailable.
-   Validate translation quality through automated and manual evaluations.

## AI Agent Studio skills migration

You can automatically migrate all AI Agent Studio skills from the on-glide execution path to the off-glide execution path by enabling the **Off-Glide Enabled** setting. This migrates skills to Mosaic.

1.  Navigate to the OneExtend Capabilities \[sys\_one\_extend\_capability.list\] table.
2.  Find the Now Assist AI Agents application.
3.  Set **Off-Glide Enabled** to **true**.
4.  Select **Save**.

