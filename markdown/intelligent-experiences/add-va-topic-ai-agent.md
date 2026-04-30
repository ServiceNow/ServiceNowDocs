---
title: Add a conversational topic to an AI agent
description: Add a Virtual Agent topic to an AI agent in AI Agent Studio so that you can use conversations to get additional information from the user. For example, a conversational topic could be used to let a user select a date range for surveys.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-02-10"
reading_time_minutes: 1
breadcrumb: [Add a tool to an AI agent, Create an AI agent, Now Assist AI agents, Enable AI experiences]
---

# Add a conversational topic to an AI agent

Add a Virtual Agent topic to an AI agent in AI Agent Studio so that you can use conversations to get additional information from the user. For example, a conversational topic could be used to let a user select a date range for surveys.

## Before you begin

Role required: sn\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **AI agents**.

2.  Open the AI agent that you want to add a conversational topic to and navigate to the Add tools and information section.

3.  In the Add tool drop-down list, select **Conversational topic**.

4.  On the form, fill in the fields.

<table><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name that you want to specify for your conversational topic.

</td></tr><tr><td>

Description

</td><td>

Description of the conversational topic and what it’s going to do to assist your AI agent.**Note:** This description is sent to the large language model \(LLM\).

</td></tr><tr><td>

Select topic

</td><td>

The Virtual Agent topic that you want to add. After it’s selected, the description of the topic displays underneath the drop-down list.**Note:** Only large language model \(LLM\) topics can be selected.

</td></tr><tr><td>

Execution mode

</td><td>

Mode of execution for your selected conversational topic:-   **Supervised**: Inputs from your live agent are required during the execution of this conversational topic while the AI agent runs.
-   **Autonomous**: Doesn't require any input from your live agent during the execution of this conversational topic while the AI agent runs.


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

    A conversational topic is added in the Conversational topics list on the Add tools and information page.


**Parent Topic:**[Add a tool to an AI agent](../concept/add-tool-aia.md)

