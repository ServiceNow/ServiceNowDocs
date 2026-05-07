---
title: Add an adaptive desktop action tool to an AI agent for web-based tasks
description: Configure and add a desktop action as a tool to an AI agent in AI Agent Studio so that AI agents can perform dynamic steps in the web environment.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-13"
reading_time_minutes: 4
breadcrumb: [Create AI agents, AI Desktop Actions, Enable AI experiences]
---

# Add an adaptive desktop action tool to an AI agent for web-based tasks

Configure and add a desktop action as a tool to an AI agent in AI Agent Studio so that AI agents can perform dynamic steps in the web environment.

## Before you begin

Familiarize yourself with adaptive desktop actions. For more information, see [Adaptive desktop actions for web-based tasks](web-agents-overview.md).

Role required: sn\_aia.admin

## About this task

Desktop actions are tools that AI agents use to interact with web applications through a browser extension. When you configure an AI agent and select desktop action as a tool, you define whether the AI agent follows a defined path \(fixed steps designed in AI Desktop Actions\) or an adaptive path \(high-level goal described in the tool configuration\). Unlike defined path desktop actions that follow preconfigured workflows, adaptive path desktop actions enable AI agents to dynamically plan and execute tasks based on high-level instructions.

An AI agent named **Web Automation Agent** and agentic workflow named **Web Automation** are provided by default when you install AI Desktop Actions. You can create a different AI agent following this procedure.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **AI agents**.

2.  Open the AI agent that you want to add a desktop action to.

    For creating an AI agent, see [Create an AI agent](../../../administer/now-assist-ai-agents/task/configure-next-best-action-agent.md).

3.  Navigate to the Add tools and information step.

4.  In the **Add tool** drop-down list, select **Desktop action**.

    ![Add tool drop-down showing desktop action as an option.](../image/create-web-tool4.png)

5.  On the Add a desktop action modal, select the **Click here to create a desktop action** link.

    ![Add web-based desktop actions](../image/create-web-tool5.png)

6.  Keep the option **Let AI determine the steps dynamically for web-based tasks** selected.

    ![Add web-based desktop actions](../image/create-web-tool6.png)

7.  Select **Continue**

8.  On the form, fill in the fields.

<table id="choicetable_t3f_bgj_y3c"><thead><tr><th align="left" id="d91281e217">

Field

</th><th align="left" id="d91281e220">

Description

</th></tr></thead><tbody><tr><td id="d91281e226">

**Name**

</td><td>

Provide a unique intuitive name.

</td></tr><tr><td id="d91281e235">

**Tool Description**

</td><td>

Description of the tool's purpose, functionality, inputs, and expected outputs, written in complete sentences. The AI agent uses this description to select the appropriate tool. Explain how an AI agent uses the tool and its inputs — including specific fields or data types — to carry out its role. Include exact input requirements such as format rules, character limits, and valid values. Specify what the tool returns and how the AI agent should use the output.

</td></tr><tr><td id="d91281e244">

**Navigation actions**

</td><td>

Add a list of precise steps that the AI agent must execute on the web page or application effectively.

</td></tr><tr><td id="d91281e253">

**Time out**

</td><td>

Enter the maximum number of minutes an AI agent should use the web page or application. Default value: 30 mins.

</td></tr><tr><td id="d91281e265">

**Execution mode**

</td><td>

Mode of execution for your selected desktop action:-   **Supervised**: Inputs from your live agent are required during the execution of this desktop action while the AI agent runs.
-   **Autonomous**: Doesn't require any input from your live agent during the execution of this desktop action while the AI agent runs.


</td></tr><tr><td id="d91281e286">

**Display output**

</td><td>

Permission to display the output of the execution in the Now Assist panel or in Virtual Agent:-   **Yes**
-   **No**
If you want the AI agent to work in Off Glide architecture with AI-native experience, you must turn-on the **Display output** toggle. When the toggle is turned-on, you can add widgets that can be used in assistants built with AI-native experiences. The widget configuration includes:

-   **Widgets**: Defines the display output to render the content in a better user experience. You can select the widget from the drop-down.
-   **Require widget transformation**: An additional LLM call is required to transform the raw tool. If you choose to skip this transformation step, the tool output will be directly mapped to the widget.
    -   **Yes**
    -   **No**
-   **Display refined widget message**: Refines the widget message when configured.
    -   **Yes**
    -   **No**
**Note:** The display output as a toggle is exclusively available for the AI-native experience when the Off Glide Conversation Server plugin \(com.glide.cs.offglide\) is installed. If the plugin is not installed, you will continue to access the standard display output options.

</td></tr><tr><td id="d91281e355">

**Select an output transformation format**

</td><td>

Style for the LLM to present the results as it passes information between tools and to other agents. Out transformation formats:-   None
-   Concise
-   Paragraph
-   Summary
-   Custom


</td></tr><tr><td id="d91281e381">

**Write processing messages for users**

</td><td>

Message to display to users during tool execution.-   In-progress message: Write an in-progress message to be displayed to end-users while the tool is running.
-   Completion message: Write a completion message to be displayed to end-users once the tool finishes running.


</td></tr></tbody>
</table>9.  Select **Add desktop action**.

    The desktop action is added in the Desktop actions list on the Add tools and information page.


## What to do next

For more information about executing desktop actions, see [Examples of executing desktop actions using AI agents](use-agentic-desktop.md).

