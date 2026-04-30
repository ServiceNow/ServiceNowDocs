---
title: Add a catalog item to an AI agent
description: Add a Service Catalog to an AI agent in AI Agent Studio so that your users can access conversational catalog items.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Add tools and information, Create an AI agent, Now Assist AI agents, Enable AI experiences]
---

# Add a catalog item to an AI agent

Add a Service Catalog to an AI agent in AI Agent Studio so that your users can access conversational catalog items.

## Before you begin

Role required: sn\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **AI agents**.

2.  Open the AI agent that you want to add a catalog item to and navigate to the Add tools and information section.

3.  In the Add tool drop-down list, select **Catalog item**.

4.  On the form, fill in the fields.

<table><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name that you want to specify for your catalog item.

</td></tr><tr><td>

Description

</td><td>

Description of the catalog item and what it’s going to do to assist your AI agent.**Note:** This description is sent to the large language model \(LLM\).

</td></tr><tr><td>

Select catalog item

</td><td>

Catalog item that you want to add. If there is a tool used by an AI agent for the same catalog item, the rest of the form will populate the fields based on the other tool. You can make any changes specific to the current AI agent to suit your needs, and it will not affect the tool of the existing AI agent.

</td></tr><tr id="supervised-execution"><td>

Execution mode

</td><td>

Mode of execution for your selected catalog item:-   **Supervised**: Inputs from your human agent are required during the execution of this catalog item while the AI agent runs.
-   **Autonomous**: Doesn't require any input from your live agent during the execution of this catalog item while the AI agent runs.


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

Style for the LLM to present the results as it passes information between tools and to other agents.-   None
-   Concise
-   Paragraph
-   Verbose
-   Custom


</td></tr></tbody>
</table>5.  Select **Add**.

    A catalog item is added in the Catalog items list on the Add tools and information page.


