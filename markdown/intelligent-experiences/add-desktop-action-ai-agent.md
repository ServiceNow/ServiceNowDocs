---
title: Add a desktop action to an AI agent
description: Add a desktop action as a tool to an AI agent in AI Agent Studio so that AI agents can perform desktop actions for repetitive tasks.
locale: en-US
release: australia
topic_type: task
last_updated: "2025-11-02"
reading_time_minutes: 4
breadcrumb: [Add tools and information, Create an AI agent, Now Assist AI agents, Enable AI experiences]
---

# Add a desktop action to an AI agent

Add a desktop action as a tool to an AI agent in AI Agent Studio so that AI agents can perform desktop actions for repetitive tasks.

## Before you begin

Role required: sn\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **AI agents**.

2.  Open the AI agent that you want to add a desktop action to.

    For creating an AI agent, see [Create an AI agent](configure-next-best-action-agent.md).

3.  Navigate to the Add tools and information step.

4.  In the Add tool drop-down list, select **Desktop action**.

5.  On the form, fill in the fields.

<table id="table_bz1_zcr_ygc"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select a type of desktop action

</td><td>

-   **UI block**: These actions include UI interactions, such as clicking buttons, typing into text boxes, selecting from drop-down menus, and more.

Example: Filling in fields on a payroll application, updating inventory in a point-of-sale system, or submitting a request through a desktop insurance claims app.

-   **Non UI blocks**: These actions are prebuilt components that don’t interact with the UI, but run in the background. Non UI block actions enable your AI agents to interact with various applications and system components and offer prebuilt actions for common tasks, reducing the need for complex scripting.

Example: Reading data from Microsoft Excel, extracting emails from Microsoft Outlook, generating a PDF, compressing files into a ZIP, fetching records from a database, or sending a system notification.

</td></tr><tr><td>

Select a desktop action

</td><td>

Desktop action that you want to add to the AI agent from the list.**Note:** This field appears when **UI block** is selected as the type of desktop action.

</td></tr><tr><td>

Select an application

</td><td>

Select an application from the list to use the associated actions. The following applications are supported for non-UI block actions:-   Microsoft Excel
-   Microsoft Outlook
-   Microsoft Word
-   PDF
-   PowerShell Connector
-   SQL
-   SSH
-   SystemAction
**Note:** This field appears when **Non UI block** is selected as the type of desktop action.

</td></tr><tr><td>

Desktop action description

</td><td>

Read-only. Description of the desktop action or application that you selected.

</td></tr><tr><td>

Applications

</td><td>

Read-only. Applications that this desktop action interacts with.**Note:** This field appears when **UI block** is selected as the type of desktop action and a desktop action is selected from the list.

</td></tr><tr><td>

Created by

</td><td>

Read-only. User who created the desktop action.**Note:** This field appears when **UI block** is selected as the type of desktop action and a desktop action is selected from the list.

</td></tr><tr><td>

Last updated

</td><td>

Read-only. Date when this desktop action was last updated.**Note:** This field appears when **UI block** is selected as the type of desktop action and a desktop action is selected from the list.

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
</table>6.  Select **Add**.

    The desktop action is added in the Desktop actions list on the Add tools and information page.


