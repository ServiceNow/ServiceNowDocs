---
title: Add a subflow tool to an AI agent
description: Add a subflow tool to an AI agent in AI Agent Studio. Subflows are reusable sequences of processing steps that can be called from within a flow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/add-sub-flow-new.html
release: australia
topic_type: task
last_updated: "2026-06-05"
reading_time_minutes: 2
breadcrumb: [Add tools and information, Create an AI agent, AI Agent Studio, Enable AI experiences]
---

# Add a subflow tool to an AI agent

Add a subflow tool to an AI agent in AI Agent Studio. Subflows are reusable sequences of processing steps that can be called from within a flow.

## Before you begin

When an AI agent uses a subflow tool, the user the AI agent is running as must pass the ACL of the subflow. Ensure that the security configurations for the subflow are met by the AI agent and agentic workflow. For more information, see [Security for AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-security-implementation.md).

Role required: sn\_aia.admin

## About this task

A subflow tool allows AI agents to execute subflows as reusable operations. When adding a subflow tool, you can configure its execution mode, output display, and processing messages to ensure the tool works effectively within your AI agent's workflow.

## Procedure

1.  In the Tools section, select **Add tools**, then **Create new tool**, then select **Subflow**.

2.  Select a subflow from the **Select subflow** dropdown.

    The selected subflow's inputs are displayed automatically.

3.  Enter a name for the tool in the **Name** field.

4.  Enter a detailed description of the tool in the **Description for this AI agent** field.

    A thorough description helps the AI agent understand what the tool does and when to use it.

5.  Select an execution mode under **Execution mode**.

    Choose **Supervised** to require human oversight when the tool executes, or **Autonomous** to allow the tool to run without human intervention.

6.  Toggle **Display output to users** to control whether the tool's output is shown to users.

7.  If display output is enabled, select an output widget from the **Widget** dropdown.

    Widgets can only be used by assistants built in Premium Chat experiences. Select the widget type that best formats the tool's output for users.

8.  Choose whether to display a refined widget message under **Display refined widget message**.

9.  Expand the **Advanced settings** section to configure output transformation and processing messages.

    1.  Select an output transformation format from the **Output transformation format** dropdown.

        Raw output data usually needs to be transformed into a format that is user-friendly and readable. You can also transform data into smaller formats to reduce the amount of data the AI agent needs to analyze. Transforming data involves tradeoffs between data completeness and latency.

        The available output transformation formats are:

        -   **None**: Output data isn't changed into a different format and users will see raw data.
        -   **Concise**: Output data is changed into the most minimal format for users, with less data for the AI agent to analyze.
        -   **Verbose**: Output data is changed into a summary-like format for users, with slightly less data for the AI agent to analyze.
        -   **Paraphrase**: Output data is changed into a format featuring direct statements for users, with no reduction in data.
        -   **Custom**: Output data is changed into a format you specify \(consider data loss and performance issues\).
    2.  Write processing messages for users under **Write processing messages for users**.

        Describe the action that happens while the tool is running in the **In-progress message** field and the final action when the tool completes in the **Completion message** field. For example, users can see "Executing subflow" when the tool is in progress and "Subflow execution complete" when the tool is done.


## Result

You have added a subflow tool to your AI agent with the appropriate execution mode, output settings, and processing messages configured.

