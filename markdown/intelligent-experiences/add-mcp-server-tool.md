---
title: Add a Model Context Protocol to an AI agent
description: Add a Model Context Protocol tool to an AI agent in the AI Agent Studio so that your users can access the MCP Server.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-02"
reading_time_minutes: 1
breadcrumb: [Configuring Model Context Protocol Client, Model Context Protocol Client, Now Assist AI agents, Enable AI experiences]
---

# Add a Model Context Protocol to an AI agent

Add a Model Context Protocol tool to an AI agent in the AI Agent Studio so that your users can access the MCP Server.

## Before you begin

Role required: sn\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **AI agents**.

2.  Open the AI agent that you want to add a Model Context Protocol tool to and navigate to the Add tools and information section.

3.  In the Add tool drop-down list, select **Model Context Protocol**.

4.  On the form, fill in the fields.

<table id="table_hr2_kgm_wfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select Model Context Protocol Server

</td><td>

The Model Context Protocol Server that you want to add to the tool.

</td></tr><tr><td>

Select Tool

</td><td>

The tool that you want to add from the Model Context Protocol Server.

</td></tr><tr><td>

Name

</td><td>

Name of the Model Context Protocol tool.

</td></tr><tr><td>

Tool and Description

</td><td>

Description of the Model Context Protocol and what it’s going to do to assist your AI agent.**Note:** This description is sent to the LLM \(large language model\).

</td></tr><tr><td>

Execution Mode

</td><td>

Mode of execution for your selected Model Context Protocol tool:-   **Supervised**: Inputs from your live agent are required during the execution of this Model Context Protocol tool while the AI agent runs.
-   **Autonomous**: Doesn't require any input from your live agent during the execution of this Model Context Protocol tool while the AI agent runs.


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
-   Custom


</td></tr></tbody>
</table>5.  Select **Add**.

    A Model Context Protocol tool is added in the Model Context Protocol Tools list on the Add tools and information page.


