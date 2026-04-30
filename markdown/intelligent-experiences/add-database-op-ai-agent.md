---
title: Add a record operation to an AI agent
description: Add a record operation to an AI agent in AI Agent Studio to create, update, look up, or delete records.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-02-10"
reading_time_minutes: 2
breadcrumb: [Add a tool to an AI agent, Create an AI agent, Now Assist AI agents, Enable AI experiences]
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

-   **Create record**: Requires values for fields in the new record.
-   **Delete records**: Requires the conditions to determine which records to delete.
-   **Look up records**: Requires the conditions to determine which records to look up, number of results specified, which fields to return, the result order, and the result sort type.
-   **Update records**: Requires the values for fields in the updated record and conditions to determine which records to update.


</td></tr><tr><td>

Execution mode

</td><td>

Mode of execution for your selected record operation:-   **Supervised**: Inputs from your live agent are required during the execution of this tool while the AI agent runs.
-   **Autonomous**: Doesn't require any input from your live agent during the execution of this tool while the AI agent runs.


</td></tr><tr><td>

Display output

</td><td>

Permission to display the output of the execution in the Now Assist panel or in Virtual Agent:-   **Yes**
-   **No**


</td></tr><tr><td>

Processing message

</td><td>

Message to display to users when the tool is running.

</td></tr><tr><td>

Output transformation strategy

</td><td>

Style for the LLM to present the results. -   None
-   Concise
-   Paragraph
-   Verbose


</td></tr></tbody>
</table>5.  Select **Add**.

    A record operation is added in the Record operations list on the Add tools and information page.


**Parent Topic:**[Add a tool to an AI agent](../concept/add-tool-aia.md)

