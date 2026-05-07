---
title: Add a record operation to an AI agent
description: Add a record operation to an AI agent in AI Agent Studio to create, update, look up, or delete records.
locale: en-US
release: australia
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Add tools and information, Create an AI agent, Now Assist AI agents, Enable AI experiences]
---

# Add a record operation to an AI agent

Add a record operation to an AI agent in AI Agent Studio to create, update, look up, or delete records.

## Before you begin

Role required: sn\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **AI agents**.

2.  Open the AI agent that you want to add a record operation to and navigate to the Add tools and information section.

3.  In the Add tool drop-down list, select **Record operation**.

4.  On the form, fill in the fields.

<table><thead><tr><th>

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

Name that you want to specify for your record operation.

</td></tr><tr><td>

Description

</td><td>

Description of the record operation and what it’s going to do to assist your AI agent.**Note:** This description is sent to the large language model \(LLM\).

</td></tr><tr><td>

Inputs

</td><td>

-   **Input name**: Name of the input for the LLM to use.
-   **Description**: Description of the input to give the LLM context.
-   **Value override**: Value for the input. If you leave it blank, generative AI fills in the value for you.

**Note:** If the agent uses multiple tools, you can choose to use another tool's output as an input value override. Select the data picker icon \(![Data picker icon.](../image/data-picker-icon.png)\) to review the available options.

</td></tr><tr><td>

Table

</td><td>

Table that you want to perform the record operation on.

</td></tr><tr><td>

Select operation

</td><td>

Inputs should be referred to as \{\{inputname\}\}. Camelcase is not supported.

 -   **Create record**: Requires values for fields in the new record.
-   **Delete records**: Requires the conditions to determine which records to delete.
-   **Look up records**: Requires the conditions to determine which records to look up, number of results specified, which fields to return, the result order, and the result sort type.
-   **Update records**: Requires the values for fields in the updated record and conditions to determine which records to update.


</td></tr><tr><td>

Execution mode

</td><td>

Mode of execution for your selected record operation:-   **Supervised**: Inputs from your human agent are required during the execution of this tool while the AI agent runs.
-   **Autonomous**: Doesn't require any input from your live agent during the execution of this tool while the AI agent runs.


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

    A record operation is added in the Record operations list on the Add tools and information page.


