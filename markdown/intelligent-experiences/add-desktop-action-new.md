---
title: Add a desktop action tool to an AI agent
description: Add a desktop action as a tool to an AI agent so that AI agents can automate tasks in desktop and web-based applications.The Map parameters section appears when you configure an On-screen task desktop action with parameter inputs in AI Agent Studio. Map a parameter record to each step before saving the desktop action.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/add-desktop-action-new.html
release: australia
topic_type: task
last_updated: "2026-06-05"
reading_time_minutes: 7
keywords: [desktop action, AI agent tool, agentic desktop, Desktop action parameter record]
breadcrumb: [Add tools and information, Create an AI agent, AI Agent Studio, Enable AI experiences]
---

# Add a desktop action tool to an AI agent

Add a desktop action as a tool to an AI agent so that AI agents can automate tasks in desktop and web-based applications.

## Before you begin

Familiarize yourself with desktop actions. For more information, see [AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/agentic-desktop-landing-page.md) documentation.

Role required: sn\_aia.admin

## About this task

Desktop actions are tools that AI agents use to interact with web and desktop applications. An AI agent uses a desktop action to automate tasks in desktop-based or web-based applications on the end user's system. You can create a desktop action or add an existing one as a tool to your AI agent.

-   Create a defined desktop action in the AI Desktop Actions client application on the Windows machine, then add it as a tool to an AI agent.
-   Configure an adaptive desktop action in AI Agent Studio during AI agent tool configuration.

For more information about executing desktop actions, see [Examples of executing desktop actions using AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/use-agentic-desktop.md).

## Procedure

1.  In the Tools section, select **Add tools**, then **Create new tool**, then select **Desktop action**.

2.  Choose one of the following options.

<table id="choicetable_hlg_gzl_lkc"><thead><tr><th align="left" id="d166591e137">

Option

</th><th align="left" id="d166591e140">

Description

</th></tr></thead><tbody><tr><td id="d166591e146">

**An existing one**

</td><td>

Option to add a previously created defined desktop action.Defined desktop actions are categorized into on-screen tasks and background tasks.

-   **On-screen tasks**: These actions help you simulate humans interacting with UI elements on your thick client applications, legacy systems, or SaaS applications without APIs. These actions include clicking buttons, typing into text boxes, selecting from drop-down menus, and more. They encapsulate repeatable UI interactions, such as screens, anchors, and steps. You can create, manage, and test your desktop actions in AI Desktop Actions.

When you add an on-screen task desktop action, additional fields require configuration. For more information, see [Parameter mapping for defined desktop actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-desktop-action-new.md).

-   **Background tasks**: These actions include prebuilt connectors that enable your AI agents to interact with applications and system components in the background. These connectors streamline automation by offering actions for common tasks, reducing the need for complex scripting. Each connector focuses on a specific application or system area and provides a collection of related methods. You can't create background tasks actions.


</td></tr><tr><td id="d166591e187">

**A new desktop action**

</td><td>

Option to create a defined or adaptive desktop actions. For more information, see the next step.

</td></tr></tbody>
</table>3.  If creating a new desktop action, select how you want to create it.

<table id="choicetable_em4_fbm_lkc"><thead><tr><th align="left" id="d166591e207">

Option

</th><th align="left" id="d166591e210">

Description

</th></tr></thead><tbody><tr><td id="d166591e216">

**Let AI determine the steps dynamically**

</td><td>

Option to configure adaptive desktop actions that enable the AI agent to plan execution dynamically.Select the environment where these desktop actions run:

-   **Desktop applications**: AI agents run these desktop actions in the AI Desktop Actions client application on the macOS machine.

For more information, see [Adaptive desktop actions for desktop and web-based tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai_desktop_actions_adaptive.md).

**Warning:** This is a beta feature in this release. Functionality, behavior, and execution logic may change in subsequent releases. Test these desktop actions thoroughly in a test environment before deploying to production. Report issues or feedback through your support channels.

-   **Web based applications**: AI agents run these desktop actions in the Google Chrome browser through a browser extension.

For more information, see [Adaptive desktop actions for web-based tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/web-agents-overview.md).

</td></tr><tr><td id="d166591e271">

**Record a fixed sequence of steps**

</td><td>

Option to configure defined desktop actions that are a fixed sequence of steps that are recorded in the AI Desktop Actions client application on the Windows machine and then added as a tool to an AI agent.

</td></tr></tbody>
</table>4.  Enter a name for the desktop action in the **Name** field.

5.  Enter a detailed description of the desktop action in the **Tool description** field.

    A thorough description helps the AI agent interpret the tool purpose and when to use it. This description is sent to the language model.

6.  In the **Navigation actions** field, add a list of precise steps that the AI agent must execute on the web or desktop applications.

7.  In the **Time out** field, enter the maximum number of minutes an AI agent must try to execute desktop actions on web or desktop.

    The default value is 30 minutes.

8.  Select an execution mode under **Execution mode**.

    Choose **Supervised** to require human input during execution, or **Autonomous** to allow the tool to run without human intervention.

9.  Toggle **Display output** to control whether the tool's output is shown to users.

10. If display output is enabled, select an output widget from the **Widget** dropdown.

    Widgets can only be used by assistants built in Premium Chat experiences. Select the widget type that best formats the tool's output for users.

11. Choose whether widget transformation is required under **Requires widget transformation**.

    Select **Yes** if the tool's output needs to be transformed before it can be displayed by the widget.

12. Choose whether to display a refined widget message under **Display refined widget message**.

13. Expand the **Advanced settings** section to configure output transformation and processing messages.

    1.  Select an output transformation format from the **Output transformation format** dropdown.

        Raw output data usually needs to be transformed into a format that is user-friendly and readable. You can also transform data into smaller formats to reduce the amount of data the AI agent needs to analyze. Transforming data involves tradeoffs between data completeness and latency.

        The available output transformation formats are:

        -   **None**: Output data isn't changed into a different format and users will see raw data.
        -   **Concise**: Output data is changed into the most minimal format for users, with less data for the AI agent to analyze.
        -   **Verbose**: Output data is changed into a summary-like format for users, with slightly less data for the AI agent to analyze.
        -   **Paraphrase**: Output data is changed into a format featuring direct statements for users, with no reduction in data.
        -   **Custom**: Output data is changed into a format you specify \(consider data loss and performance issues\).
    2.  Write processing messages for users under **Write processing messages for users**.

        Describe the action that happens while the tool is running in the **In-progress message** field and the final action when the tool completes in the **Completion message** field. For example, users can see "Requesting a service" when the tool is in progress and "Requested a service" when the tool is done.


## Result

You have added a desktop action tool to your AI agent with the appropriate configuration, execution mode, output settings, and processing messages.

## Parameter mapping for defined desktop actions

The Map parameters section appears when you configure an **On-screen task** desktop action with parameter inputs in AI Agent Studio. Map a parameter record to each step before saving the desktop action.

### Map parameters

**Note:** These fields appear only when you select an **On-screen task** desktop action configured with parameter inputs.

<table id="table_bz1_zcr_ygc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Step name

</td><td>

Name of the step configured to use a parameter.

</td></tr><tr><td>

Description

</td><td>

Description of the step configured to use a parameter.

</td></tr><tr><td>

Parameter record

</td><td>

The Desktop action parameter record the agent uses to retrieve the value for this step at execution time. Map a parameter record for every step before saving the desktop action. The same parameter record can map to multiple steps. Each step maps to one parameter record only.

</td></tr></tbody>
</table>**Warning:** If you update a desktop action after mapping its inputs in AI Agent Studio, the agent continues to use the previous mapping until you reopen the tool configuration and save it again. If you rename an input, the agent registers it as a new input and removes the existing mapping. Remap the renamed input before saving the desktop action.

