---
title: Add a web search tool to an AI agent
description: Add a web search tool to an AI agent to enable it to search the web and retrieve relevant information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/add-web-search-new.html
release: australia
topic_type: task
last_updated: "2026-06-05"
reading_time_minutes: 3
breadcrumb: [Add tools and information, Create an AI agent, AI Agent Studio, Enable AI experiences]
---

# Add a web search tool to an AI agent

Add a web search tool to an AI agent to enable it to search the web and retrieve relevant information.

## Before you begin

**Note:** If you select Google as your web search tool provider, the web search tool leverages [Grounding with Google Search](https://cloud.google.com/vertex-ai/generative-ai/docs/grounding/grounding-with-google-search), offered under a Global Standard deployment. Because grounding is not [data resident](https://cloud.google.com/vertex-ai/generative-ai/docs/security-controls), Google's global infrastructure routes traffic to a global data center for each web search request. This processing may be different than your data processing location chosen for your ServiceNow instance. Please consider your organization's data policies before adding a web search tool with Google as the provider.

Role required: sn\_aia.admin

## About this task

A web search tool allows AI agents to search the web and retrieve relevant information. When adding a web search tool, you can configure its search parameters, execution mode, output display, and processing messages to ensure the tool works effectively within your AI agent's workflow.

## Procedure

1.  In the Tools section, select **Add tools**, then **Create new tool**, then select **Web search**.

2.  Review the resource and provider information.

    The resource is set to Web Search and the provider is configured elsewhere and cannot be changed.

3.  Review the inputs displayed under **Inputs**.

    The inputs are automatically populated based on the web search configuration.

4.  Enter a name for the tool in the **Name** field.

5.  Enter a detailed description of the tool in the **Description for this AI agent** field.

    A thorough description helps the AI agent understand what the tool does and when to use it.

6.  Select an execution mode under **Execution mode**.

    Choose **Supervised** to require human oversight when the tool executes, or **Autonomous** to allow the tool to run without human intervention.

7.  Toggle **Display output to users** to control whether the tool's output is shown to users.

8.  If display output is enabled, select an output widget from the **Widget** dropdown.

    Widgets can only be used by assistants built in Premium Chat experiences. Select the widget type that best formats the tool's output for users.

9.  Choose whether to display a refined widget message under **Display refined widget message**.

10. Expand the **Advanced settings** section to configure output transformation and processing messages.

    1.  Select an output transformation format from the **Output transformation format** dropdown.

        Raw output data usually needs to be transformed into a format that is user-friendly and readable. You can also transform data into smaller formats to reduce the amount of data the AI agent needs to analyze. Transforming data involves tradeoffs between data completeness and latency.

        The available output transformation formats are:

        -   **None**: Output data isn't changed into a different format and users will see raw data.
        -   **Concise**: Output data is changed into the most minimal format for users, with less data for the AI agent to analyze.
        -   **Verbose**: Output data is changed into a summary-like format for users, with slightly less data for the AI agent to analyze.
        -   **Paraphrase**: Output data is changed into a format featuring direct statements for users, with no reduction in data.
        -   **Custom**: Output data is changed into a format you specify \(consider data loss and performance issues\).
    2.  Write processing messages for users under **Write processing messages for users**.

        Describe the action that happens while the tool is running in the **In-progress message** field and the final action when the tool completes in the **Completion message** field. For example, users can see "Searching the web" when the tool is in progress and "Search complete" when the tool is done.


## Result

You have added a web search tool to your AI agent with the appropriate execution mode, output settings, and processing messages configured.

