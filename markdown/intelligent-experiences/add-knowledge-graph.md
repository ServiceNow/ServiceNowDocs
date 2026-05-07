---
title: Add a Knowledge Graph to an AI agent
description: Add a Knowledge Graph to an AI agent in AI Agent Studio that uses the structured and unstructured data from different ServiceNow records to enhance the performance of AI agents.
locale: en-US
release: australia
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Add tools and information, Create an AI agent, Now Assist AI agents, Enable AI experiences]
---

# Add a Knowledge Graph to an AI agent

Add a Knowledge Graph to an AI agent in AI Agent Studio that uses the structured and unstructured data from different ServiceNow records to enhance the performance of AI agents.

## Before you begin

Role required: sn\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **AI agents**.

2.  Select **New** or open the AI agent that you want to add a Knowledge Graph to and navigate to the Add tools and information section.

3.  In the Add tool drop-down list, select **Knowledge graph**.

    You may need to scroll down.

4.  On the form, fill in the fields.

<table id="table_wlm_2v5_cdc"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name that you want to specify for your selected Knowledge Graph.

</td></tr><tr><td>

Description

</td><td>

Description of the Knowledge Graph and what it’s going to do to assist your AI agent.**Note:** This description is sent to the large language model \(LLM\).

</td></tr><tr><td>

Select Knowledge Graph

</td><td>

Existing Knowledge Graph to be added to the AI agent. If there is a tool used by an AI agent for the same Knowledge Graph, the rest of the form will populate the fields based on the other tool. You can make any changes specific to the current AI agent to suit your needs, and it will not affect the tool of the existing AI agent.

You can utilize Enterprise Graph and Enterprise Graph \(Small\) as Knowledge Graph resources while creating the Knowledge Graph tool.

</td></tr><tr><td>

Query instruction

</td><td>

The search query. Translate your request into a search query, including a verb.The query instruction is passed on to the LLM to generate a structured query for the Graph from the inputs selected in the tool form.

</td></tr><tr><td>

Execution mode

</td><td>

Mode of execution for your selected Knowledge Graph:-   **Supervised**: Inputs from your human agent are required during the execution of this Knowledge Graph while the AI agent runs.
-   **Autonomous**: Doesn't require any input from your live agent during the execution of this Knowledge Graph while the AI agent runs.


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

    The Knowledge Graph tool is added to the AI agent.


