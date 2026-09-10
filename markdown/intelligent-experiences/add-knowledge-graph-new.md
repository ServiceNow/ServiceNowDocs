---
title: Add a knowledge graph tool to an AI agent
description: Add a Knowledge Graph to an AI agent in AI Agent Studio that uses the structured and unstructured data from different ServiceNow records to enhance the performance of AI agents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/add-knowledge-graph-new.html
release: australia
topic_type: task
last_updated: "2026-06-05"
reading_time_minutes: 2
breadcrumb: [Add tools and information, Create an AI agent, AI Agent Studio, Enable AI experiences]
---

# Add a knowledge graph tool to an AI agent

Add a Knowledge Graph to an AI agent in AI Agent Studio that uses the structured and unstructured data from different ServiceNow records to enhance the performance of AI agents.

## Before you begin

Role required: sn\_aia.admin

## About this task

A Knowledge Graph is a semantic layer that connects data, relationships, and context across your enterprise. It structures information as a graph of entities and their connections, transforming raw data into actionable knowledge. A Knowledge Graph allows AI agents to understand the relationships between real-world entities and retrieve insights, facts, and relationships directly to automate actions and improve accuracy. When adding a Knowledge Graph tool, you can configure its query instruction, conversation history, execution mode, output display, and processing messages to ensure the tool works effectively within your AI agent's workflow.

## Procedure

1.  In the Tools section, select **Add tools**, then **Create new tool**, then select **Knowledge graph**.

2.  Select a Knowledge Graph from the **Select knowledge graph** dropdown.

3.  Enter a name for the tool in the **Name** field.

4.  Enter a detailed description of the tool in the **Description for this AI agent** field.

    A thorough description helps the AI agent understand what the tool does and when to use it.

5.  Enter a query instruction in the **Query instruction** field.

    The query instruction should be a direct translation of the request into a search query without any added interpretations.

6.  Toggle **Conversation history** to control whether the tool uses conversation history.

7.  Select an execution mode under **Execution mode**.

    Choose **Supervised** to require human oversight when the tool executes, or **Autonomous** to allow the tool to run without human intervention.

8.  Toggle **Display output to users** to control whether the tool's output is shown to users.

9.  If display output is enabled, select an output widget from the **Widget** dropdown.

    Widgets can only be used by assistants built in Premium Chat experiences. Select the widget type that best formats the tool's output for users.

10. Choose whether to display a refined widget message under **Display refined widget message**.

11. Expand the **Advanced settings** section to configure output transformation and processing messages.

    1.  Select an output transformation format from the **Output transformation format** dropdown.

        Raw output data usually needs to be transformed into a format that is user-friendly and readable. You can also transform data into smaller formats to reduce the amount of data the AI agent needs to analyze. Transforming data involves tradeoffs between data completeness and latency.

        The available output transformation formats are:

        -   **None**: Output data isn't changed into a different format and users will see raw data.
        -   **Concise**: Output data is changed into the most minimal format for users, with less data for the AI agent to analyze.
        -   **Verbose**: Output data is changed into a summary-like format for users, with slightly less data for the AI agent to analyze.
        -   **Paraphrase**: Output data is changed into a format featuring direct statements for users, with no reduction in data.
        -   **Custom**: Output data is changed into a format you specify \(consider data loss and performance issues\).
    2.  Write processing messages for users under **Write processing messages for users**.

        Describe the action that happens while the tool is running in the **In-progress message** field and the final action when the tool completes in the **Completion message** field. For example, users can see "Querying knowledge graph" when the tool is in progress and "Query complete" when the tool is done.


## Result

You have added a Knowledge Graph tool to your AI agent with the appropriate query instruction, execution mode, output settings, and processing messages configured.

