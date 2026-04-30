---
title: Add a Knowledge Graph to an AI agent
description: Add a Knowledge Graph to an AI agent in AI Agent Studio that uses the structured and unstructured data from different ServiceNow records to enhance the performance of AI agents.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Add a tool to an AI agent, Create an AI agent, Now Assist AI agents, Enable AI experiences]
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

Existing Knowledge Graph to be added to the AI agent.

</td></tr><tr><td>

Query instruction

</td><td>

The search query. Translate your request into a search query, including a verb.The query instruction is passed on to the LLM to generate a structured query for the Graph from the inputs selected in the tool form.

</td></tr><tr><td>

Execution mode

</td><td>

Mode of execution for your selected Knowledge Graph:-   **Supervised**: Inputs from your live agent are required during the execution of this Knowledge Graph while the AI agent runs.
-   **Autonomous**: Doesn't require any input from your live agent during the execution of this Knowledge Graph while the AI agent runs.


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

    The Knowledge Graph tool is added to the AI agent.


**Parent Topic:**[Add a tool to an AI agent](../concept/add-tool-aia.md)

