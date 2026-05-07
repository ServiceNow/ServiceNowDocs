---
title: Add a flow action to an AI agent
description: Add a flow action to an AI agent in AI Agent Studio. Define the flow action to use it as a reusable operation in automating the ServiceNow AI Platform features without having to write code.
locale: en-US
release: australia
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Add tools and information, Create an AI agent, Now Assist AI agents, Enable AI experiences]
---

# Add a flow action to an AI agent

Add a flow action to an AI agent in AI Agent Studio. Define the flow action to use it as a reusable operation in automating the ServiceNow AI Platform features without having to write code.

## Before you begin

When an AI agent uses a flow action tool, the user the AI agent is running as must pass the ACL of the flow action. Ensure that the security configurations for the flow action are met by the AI agent and agentic workflow. For more information, see [Security for AI agents](../concept/aia-security-implementation.md).

Role required: sn\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **AI agents**.

2.  Open the AI agent that you want to add a flow action to and navigate to the Add tools and information section.

3.  In the Add tool drop-down list, select **Flow action**.

4.  On the form, fill in the fields.

<table id="table_wlm_2v5_cdc"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name that you want to specify for your selected flow action.

</td></tr><tr><td>

Description

</td><td>

Description of the flow action and what it’s going to do to assist your AI agent.**Note:** This description is sent to the large language model \(LLM\).

</td></tr><tr><td>

Select flow action

</td><td>

Existing automated process to be selected from the list.If there is a tool used by an AI agent for the same flow action, the rest of the form will populate the fields based on the other tool. You can make any changes specific to the current AI agent to suit your needs, and it will not affect the tool of the existing AI agent.

</td></tr><tr><td>

Inputs

</td><td>

Flow action inputs. The values are filled in by the LLM at runtime unless you specify a value override.**Note:** If the agent uses multiple tools, you can choose to use another tool's output as an input value override. Select the data picker icon \(![Data picker icon.](../image/data-picker-icon.png)\) to review the available options.

</td></tr><tr><td>

Execution mode

</td><td>

Mode of execution for your selected flow action:-   **Supervised**: Inputs from your human agent are required during the execution of this flow action while the AI agent runs.
-   **Autonomous**: Doesn't require any input from your live agent during the execution of this flow action while the AI agent runs.


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
</table>5.  Select **Add**.

    A flow action is added in the Flow actions list on the Add tools and information page.


