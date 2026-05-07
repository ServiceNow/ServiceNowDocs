---
title: Add a script to an AI agent
description: Create a script to add it to an AI agent in AI Agent Studio. With scripts, you can use the scriptable APIs and back-end integration to support the AI agent.
locale: en-US
release: australia
topic_type: task
last_updated: "2025-09-17"
reading_time_minutes: 2
breadcrumb: [Add tools and information, Create an AI agent, Now Assist AI agents, Enable AI experiences]
---

# Add a script to an AI agent

Create a script to add it to an AI agent in AI Agent Studio. With scripts, you can use the scriptable APIs and back-end integration to support the AI agent.

## Before you begin

Role required: sn\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **AI agents**.

2.  Open the AI agent that you want to add a script to and navigate to the Add tools and information section.

3.  In the **Add tool** drop-down list, select **Script**.

4.  On the form, fill in the fields.

<table id="table_hg4_cbv_cdc"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select a type of record operation to add

</td><td>

If you select **An existing one**, you can select a record operation tool used by the current AI agent or any other AI agent. You can make changes to the settings of that tool to fit the needs of your specific AI agent.

</td></tr><tr><td>

Name

</td><td>

Name that you want to specify for your script.

</td></tr><tr><td>

Description

</td><td>

Description of the script and what it's going to do to assist your AI agent.**Note:** This description is sent to the large language model \(LLM\).

</td></tr><tr><td>

Script inputs

</td><td>

Input name and description to use in the script. The LLM uses the name and description to determine what value should be used at runtime. Example: Input name is **task\_record\_sys\_id** and description is **sys\_id of the Task Record, this is mandatory**.

</td></tr><tr><td>

Script

</td><td>

JavaScript code that includes an object class or a function for your script. **Note:** For improved security, use GlideRecordSecure instead of GlideRecord and addUserEncodedQuery\(\) instead of addEncodedQuery\(\).

</td></tr><tr><td>

Execution mode

</td><td>

Mode of execution for your script:-   **Supervised**: Inputs from your human agent are required during the execution of this tool while the AI agent runs.
-   **Autonomous**: Doesn't require any input from your live agent during the execution of this tool while the AI agent runs.


</td></tr><tr><td>

Display output

</td><td>

Permission to display the output of the tool execution in the Now Assist panel or in Virtual Agent:-   **Yes**
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

    A script tool is added in the Scripts section on the Add tools and information page.


