---
title: Add a deep research tool to an AI agent
description: Add a deep research tool to an AI agent so it can search multiple sources and provide answers with sources listed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/add-deep-research-new.html
release: australia
topic_type: task
last_updated: "2026-06-05"
reading_time_minutes: 3
breadcrumb: [Add tools and information, Create an AI agent, AI Agent Studio, Enable AI experiences]
---

# Add a deep research tool to an AI agent

Add a deep research tool to an AI agent so it can search multiple sources and provide answers with sources listed.

## Before you begin

Role required: sn\_aia.admin

## About this task

Deep research tools allow AI agents to perform step-by-step investigation across multiple sources to synthesize clear, cited answers. When adding a deep research tool, you can configure its query, depth, knowledge sources, instructions, execution mode, output display, and processing messages to ensure the tool works effectively within your AI agent's workflow.

## Procedure

1.  In the Tools section, select **Add tools**, then **Create new tool**, then select **Deep research**.

2.  Enter a name for the tool in the **Name** field.

3.  Enter a detailed description of the tool in the **Description for this AI agent** field.

    A thorough description helps the AI agent understand what the tool does and when to use it.

4.  Enter the deep research query in the **Query** field.

5.  Select a depth level from the **Depth** dropdown.

    The depth determines how thoroughly the research investigation is conducted. The available depth levels are:

    -   **Basic research**
    -   **Standard research**
    -   **Advanced research**
6.  Add knowledge sources by selecting **+ Add** next to Knowledge sources.

    1.  Select a search profile from the **Search profile** dropdown.

    2.  Configure search sources under **Search sources**.

    3.  Specify fields to be returned under **Fields to be returned**.

    4.  Configure semantic indexed fields under **Semantic indexed fields**.

        Semantic indexed fields are fields that have been indexed to understand meaning and context. This allows the search to find results based on semantic similarity, so searches can match related concepts even if exact words don't appear.

    5.  Select **Add** to add the knowledge source configuration.

7.  Enter instructions in the **Instructions** field.

    Provide instructions for guiding the research process. These instructions help break down the research into smaller questions and guide how the final answer is created.

8.  Select an execution mode under **Execution mode**.

    Choose **Supervised** to require human oversight when the tool executes, or **Autonomous** to allow the tool to run without human intervention.

9.  Toggle **Display output to users** to control whether the tool's output is shown to users.

10. If display output is enabled, select an output widget from the **Widget** dropdown.

    Widgets can only be used by assistants built in Premium Chat experiences. Select the widget type that best formats the tool's output for users.

11. Choose whether to display a refined widget message under **Display refined widget message**.

12. Expand the **Advanced settings** section to configure output transformation and processing messages.

    1.  Select an output transformation format from the **Output transformation format** dropdown.

        Raw output data usually needs to be transformed into a format that is user-friendly and readable. You can also transform data into smaller formats to reduce the amount of data the AI agent needs to analyze. Transforming data involves tradeoffs between data completeness and latency.

        The available output transformation formats are:

        -   **None**: Output data isn't changed into a different format and users will see raw data.
        -   **Concise**: Output data is changed into the most minimal format for users, with less data for the AI agent to analyze.
        -   **Verbose**: Output data is changed into a summary-like format for users, with slightly less data for the AI agent to analyze.
        -   **Paraphrase**: Output data is changed into a format featuring direct statements for users, with no reduction in data.
        -   **Custom**: Output data is changed into a format you specify \(consider data loss and performance issues\).
    2.  Write processing messages for users under **Write processing messages for users**.

        Describe the action that happens while the tool is running in the **In-progress message** field and the final action when the tool completes in the **Completion message** field. For example, users can see "Searching the knowledge base" when the tool is in progress and "Found results" when the tool is done.


## Result

You have added a deep research tool to your AI agent with the appropriate query, depth, knowledge sources, execution mode, output settings, and processing messages configured.

