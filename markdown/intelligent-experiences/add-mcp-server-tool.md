---
title: Add an MCP server tool to an AI agent
description: Add an MCP tool to an AI agent in the AI Agent Studio so that your users can access the MCP server.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Model Context Protocol Client, Model Context Protocol Client, Now Assist AI agents, Enable AI experiences]
---

# Add an MCP server tool to an AI agent

Add an MCP tool to an AI agent in the AI Agent Studio so that your users can access the MCP server.

## Before you begin

Role required: sn\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **AI agents**.

2.  Open the AI agent that you want to add a Model Context Protocol tool to and navigate to the Add tools and information section.

3.  In the Add tool drop-down list, select **MCP server tool**.

4.  On the form, fill in the fields.

<table id="table_hr2_kgm_wfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select Model Context Protocol Server

</td><td>

The Model Context Protocol Server that you want to add to the tool.**Note:** Verify that the MCP Server is authenticated before adding the MCP tool to an AI agent. If the MCP Server isn’t authenticated, then you receive an error message - "Authentication is needed to display tools. Open the MCP server record to authenticate."

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

Description of the Model Context Protocol and what it’s going to do to assist your AI agent.**Note:** This description is sent to the LLM \(LLM\).

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

    A Model Context Protocol tool is added in the Model Context Protocol Tools list on the Add tools and information page.


