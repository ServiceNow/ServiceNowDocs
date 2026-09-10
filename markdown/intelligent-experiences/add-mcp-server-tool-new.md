---
title: Add an MCP server tool to an AI agent
description: Add an MCP tool to an AI agent in the AI Agent Studio so that your users can access the MCP server.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/add-mcp-server-tool-new.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring Model Context Protocol Client, MCP Client, AI Agent Studio, Enable AI experiences]
---

# Add an MCP server tool to an AI agent

Add an MCP tool to an AI agent in the AI Agent Studio so that your users can access the MCP server.

## Before you begin

Role required: sn\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Agentic Solutions**.

2.  On the Agentic solutions page, open the **AI agents** tab and select an AI agent.

3.  In the Tools section, select **+Add tool**, select **Create new tool**, and then select **MCP Server tool**.

4.  In the Add a Model Context Protocol tool page, select an MCP server from the **Select Model Context Provider server** drop down.

5.  Select a tool for the MCP server from the **Select tool** drop down.

6.  Define the tool settings which are used only by the selected AI agent.

    -   **Name**: The name is auto-populated from the Select tool field. You can also change the name if you would like to.
    -   **Description for this AI agent**: Provide a description that covers the tool's purpose, exact input rules, what the tool returns, and how this AI agent should use outputs.

        **Note:** This description is critical because the AI agent uses it to invoke the tool. Testing shows details of actual tool usage.

7.  Select an execution mode under **Execution mode**.

    Choose **Supervised** to require human oversight when the tool executes, or **Autonomous** to allow the tool to run without human intervention.

8.  Toggle **Display output** to control whether the tool's output is shown to users.

9.  Select an output widget from the **Widget** drop down.

    Widgets can only be used by assistants built in Premium Chat experiences. Select the widget type that best formats the tool's output for users.

10. Display the refined widget message.

    Select **Yes** if you would like a refined widget message.

11. Expand the **Advanced settings** section to configure output transformation and processing messages.

    1.  Select an output transformation format from the **Output transformation format** drop down.

        Raw output data usually needs to be transformed into a format that is user-friendly and readable. You can also transform data into smaller formats to reduce the amount of data the AI agent needs to analyze. Transforming data involves tradeoffs between data completeness and latency.

        The available output transformation formats are:

        -   **None**: Output data isn't changed into a different format and users will see raw data.
        -   **Concise**: Output data is changed into the most minimal format for users, with less data for the AI agent to analyze.
        -   **Verbose**: Output data is changed into a summary-like format for users, with slightly less data for the AI agent to analyze.
        -   **Paraphrase**: Output data is changed into a format featuring direct statements for users, with no reduction in data.
        -   **Custom**: Output data is changed into a format you specify \(consider data loss and performance issues\).
12. Generate or write processing message for users under **Tool processing messages for users**.

    Describe the action that happens while the tool is running in the **In-progress message** field and the final action when the tool completes in the **Completion message** field. For example, users can see "Requesting a service" when the tool is in progress and "Requested a service" when the tool is done.

13. Select **Save**.


## What to do next

You can [test your AI agent on a record manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-ai-asset-new.md) to see an example execution. You can also [create an automated agentic evaluation to test the AI agent over repeated interactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/launch-aia-eval.md). Automated evaluations can recommend specific optimizations if the LLM judges find underlying patterns for low success rates.

Activate your AI agent and make it ready for use by selecting **Activate**.

**Note:** The status of the external AI agent is shown as **Inactive** until it is activated.

