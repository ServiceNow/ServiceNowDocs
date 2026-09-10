---
title: Add a script tool to an AI agent
description: Add a script tool to an AI agent to enable it to execute custom scripts to perform specialized tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/add-script-new.html
release: australia
topic_type: task
last_updated: "2026-06-05"
reading_time_minutes: 3
breadcrumb: [Add tools and information, Create an AI agent, AI Agent Studio, Enable AI experiences]
---

# Add a script tool to an AI agent

Add a script tool to an AI agent to enable it to execute custom scripts to perform specialized tasks.

## Before you begin

Role required: sn\_aia.admin

## About this task

A script tool allows AI agents to execute custom scripts to perform specialized tasks. When adding a script tool, you can configure its script inputs, execution mode, output display, and processing messages. You can reference the scripts that come with AI agents associated with AI applications as examples to help you write custom scripts.

## Procedure

1.  In the Tools section, select **Add tools**, then **Create new tool**, then select **Script**.

2.  Choose whether to create a new script or use an existing one.

    Select **A new script** to create a new script, or select **An existing one** to use a previously created script.

3.  If you want to use an existing script, select the name of the script from the **Select a script** dropdown.

    The script's inputs and script content are populated automatically.

4.  Add script inputs under **Script inputs**.

    Select **Add an input** to add each required input. For each input, enter the input name, description, and mark whether it is mandatory.

5.  Write or edit the script in the **Script** field.

    Only string inputs are allowed. The script should return outputs as an object where the keys are understandable by the language model.

    Field names must match exactly. A typo in a variable or column name produces a run-time error that reads as a tool failure.

    **Note:** For improved security, use GlideRecordSecure instead of GlideRecord and addUserEncodedQuery\(\) instead of addEncodedQuery\(\).

6.  Enter a name for the tool in the **Name** field.

7.  Enter a detailed description of the tool in the **Description for this AI agent** field.

    A thorough description helps the AI agent understand what the tool does and when to use it.

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

        Describe the action that happens while the tool is running in the **In-progress message** field and the final action when the tool completes in the **Completion message** field. For example, users can see "Executing script" when the tool is in progress and "Script execution complete" when the tool is done.


## Result

You have added a script tool to your AI agent with the appropriate script inputs, execution mode, output settings, and processing messages configured.

