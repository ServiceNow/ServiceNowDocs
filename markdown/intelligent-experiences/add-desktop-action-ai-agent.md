---
title: Add a defined desktop action tool to an AI agent for desktop and web-based task
description: Add a desktop action as a tool to an AI agent in AI Agent Studio so that AI agents can execute defined path desktop actions for repetitive tasks in desktop and web environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/add-desktop-action-ai-agent.html
release: zurich
topic_type: task
last_updated: "2025-11-02"
reading_time_minutes: 7
breadcrumb: [Add tools and information, Create an AI agent, Now Assist AI agents, Enable AI experiences]
---

# Add a defined desktop action tool to an AI agent for desktop and web-based task

Add a desktop action as a tool to an AI agent in AI Agent Studio so that AI agents can execute defined path desktop actions for repetitive tasks in desktop and web environment.

## Before you begin

Familiarize yourself with defined path desktop actions. For more information, see [Defined desktop actions for desktop and web-based tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/desktop-actions.md) and [Defined path desktop actions in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/desktop-actions-designer-workspace-ad.md).

Role required: sn\_aia.admin

## About this task

Desktop actions are tools that AI agents use to interact with web and desktop applications. When you configure an AI agent and select desktop action as a tool, you define whether the AI agent follows a defined path \(fixed steps designed in AI Desktop Actions\) or an adaptive path \(high-level goal described in the tool configuration\). Unlike adaptive path desktop actions that dynamically plan execution, defined path desktop actions enable AI agents to execute preconfigured workflows through a fixed sequence of steps.

Defined desktop actions are further categorized into on-screen tasks and background tasks.

-   **On-screen tasks**: These actions help you simulate humans interacting with UI elements on your thick client applications, legacy systems, or SaaS applications without APIs. These actions include clicking buttons, typing into text boxes, selecting from drop-down menus, and more. They encapsulate repeatable UI interactions, such as screens, anchors, and steps. You can create, manage, and test your desktop actions in AI Desktop Actions.
-   **Background tasks**: These actions include prebuilt connectors that enable your AI agents to interact with various applications and system components in the background. These connectors streamline automation by offering actions for common tasks, reducing the need for complex scripting. Each connector focuses on a specific application or system area, providing a collection of related methods. You can't create background tasks actions.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **AI agents**.

2.  Open the AI agent that you want to add a desktop action to.

    For creating an AI agent, see [Create an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/configure-next-best-action-agent.md).

3.  Navigate to the Add tools and information step.

4.  In the **Add tool** drop-down list, select **Desktop action**.

    \[Omitted image "create-web-tool4.png"\] Alt text: Add tool drop-down showing desktop action as an option.

5.  Select or create a desktop action.

<table id="table_jqm_b34_bjc"><thead><tr><th>

Existing desktop action

</th><th>

New desktop action

</th></tr></thead><tbody><tr><td>

1.  Select an existing desktop action of type on-screen task or background task from the **Select a desktop action** drop-down list.

The background task desktop actions are supported for the following applications:

    -   Microsoft Excel
    -   Microsoft Outlook
    -   Microsoft Word
    -   PDF
    -   PowerShell Connector
    -   SQL
    -   SSH
    -   SystemAction
2.  Select **Continue**.


</td><td>

1.  On the Add a desktop action modal, select the **Click here to create a desktop action** link.

\[Omitted image "create-web-tool5.png"\] Alt text: Add web-based desktop actions

2.  Select the option **Record a fixed sequence of steps for desktop and web-based tasks**.
3.  Select **Open AI Desktop Actions app**.

Record or manually capture the desktop action in AI Desktop Actions Windows application, activate it, and then come back here to add it as a tool. For more information, see [Defined path desktop actions in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/desktop-actions-designer-workspace-ad.md).

The creation process of defined desktop actions ends here.

</td></tr></tbody>
</table>6.  On the form, fill in the fields.

<table id="table_bz1_zcr_ygc"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Desktop action description

</td><td>

Read-only. Description of the desktop action or application that you selected.

</td></tr><tr><td>

Applications

</td><td>

Read-only. Applications that this desktop action interacts with.**Note:** This field appears only when **On-screen task** desktop action is selected.

</td></tr><tr><td>

Created by

</td><td>

Read-only. User who created the desktop action.**Note:** This field appears only when **On-screen task** desktop action is selected.

</td></tr><tr><td>

Last updated

</td><td>

Read-only. Date when this desktop action was last updated.**Note:** This field appears only when **On-screen task** desktop action is selected.

</td></tr><tr><td>

Inputs

</td><td>

Read-only. Input parameters associated with this desktop action.**Note:** This field appears when a desktop action or application is selected from the list.

</td></tr><tr><td>

Outputs

</td><td>

Read-only. Output parameters associated with this desktop action. **Note:** This field appears when a desktop action or application is selected from the list.

</td></tr><tr><td>

Name

</td><td>

Name that you want to specify for your selected desktop action.

</td></tr><tr><td>

Tool description

</td><td>

Description of the desktop action tool and what it’s going to do to assist your AI agent.**Note:** This description is sent to the large language model \(LLM\).

</td></tr><tr><td colspan="2">

Map parameters**Important:**

If you update a desktop action after mapping its inputs in AI Agent Studio, the agent continues to use the previous mapping until you reopen the tool configuration and save it again.

If you rename an input in the desktop action, the agent treats it as a new input and the existing mapping for that input is removed. You must remap the renamed input before the desktop action can be saved.

</td></tr><tr><td>

Step name

</td><td>

Read-only. The name of the step that is configured to use a parameter.**Note:** This field appears only when an **On-screen task** desktop action with inputs configured for parameters is selected.

</td></tr><tr><td>

Description

</td><td>

Read-only. The description entered for the step that is configured to use a parameter.**Note:** This field appears only when an **On-screen task** desktop action with inputs configured for parameters is selected.

</td></tr><tr><td>

Parameter record

</td><td>

Select the Desktop action parameter record that the AI agent must use to retrieve the value for this step at execution time. Mapping a parameter record is required for all steps before the desktop action can be saved. **Note:** This field appears only when an **On-screen task** desktop action with inputs configured for parameters is selected.

The same parameter record can be mapped to multiple steps. Each step can only be mapped to one parameter record.

</td></tr><tr><td>

Execution mode

</td><td>

Mode of execution for your selected desktop action:-   **Supervised**: Inputs from your live agent are required during the execution of this desktop action while the AI agent runs.
-   **Autonomous**: Doesn't require any input from your live agent during the execution of this desktop action while the AI agent runs.


</td></tr><tr><td>

Display output

</td><td>

Permission to display the output of the execution in the Now Assist panel or in Virtual Agent:-   **Yes**
-   **No**
If you want the AI agent to work in Off Glide architecture with Premium Chat experience, you must turn-on the **Display output** toggle. When the toggle is turned-on, you can add widgets that can be used in assistants built with Premium Chat experiences. The widget configuration includes:

-   **Widget**: Defines the display output to render the content in a better user experience. You can select the widget from the drop-down.
-   **Require widget transformation**: An additional LLM call is required to transform the raw tool. If you choose to skip this transformation step, the tool output will be directly mapped to the widget.
    -   **Yes**
    -   **No**
-   **Display refined widget message**: Refines the widget message when configured.
    -   **Yes**
    -   **No**
**Note:** The display output as a toggle is exclusively available for the Premium Chat experience when the Off Glide Conversation Server plugin \(com.glide.cs.offglide\) is installed. If the plugin is not installed, you will continue to access the standard display output options.

</td></tr><tr><td colspan="2">

Advanced settings

</td></tr><tr><td>

Select an output transformation format

</td><td>

Style for the LLM to present the results as it passes information between tools and to other agents. Out transformation formats:-   None
-   Concise
-   Paragraph
-   Summary
-   Custom


</td></tr><tr><td>

Write processing messages for users

</td><td>

Message to display to users during tool execution.-   In-progress message: Write an in-progress message to be displayed to end-users while the tool is running.
-   Completion message: Write a completion message to be displayed to end-users once the tool finishes running.


</td></tr></tbody>
</table>7.  Select **Add desktop action**.

    The desktop action is added in the Desktop actions list on the Add tools and information page.


## What to do next

For more information about executing desktop actions, see [Examples of executing desktop actions using AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/use-agentic-desktop.md).

