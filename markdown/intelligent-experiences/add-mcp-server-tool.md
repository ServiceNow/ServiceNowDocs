---
title: Add an MCP server tool to an AI agent
description: Add a Model Context Protocol \(MCP\) tool to an AI agent in the AI Agent Studio so your users can access the MCP server.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-02"
reading_time_minutes: 3
breadcrumb: [Configure Model Context Protocol Client, Model Context Protocol Client, Now Assist AI agents, Enable AI experiences]
---

# Add an MCP server tool to an AI agent

Add a Model Context Protocol \(MCP\) tool to an AI agent in the AI Agent Studio so your users can access the MCP server.

## Before you begin

Role required: sn\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **AI agents**.

2.  Open the AI agent to which you want to add an MCP tool to and navigate to the Add tools and information section.

3.  In the Add tool drop-down list, select **MCP server tool**.

4.  On the form, fill in the fields.

<table id="table_hr2_kgm_wfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select Model Context Protocol Server

</td><td>

The MCP server that you want to add to the tool.**Note:** Verify that the MCP server is authenticated before adding the MCP tool to an AI agent. If the MCP server isn’t authenticated, then you receive an error message.

</td></tr><tr><td>

Select MCP server tools

</td><td>

The tool that you want to add from the MCP Server.

</td></tr><tr><td>

Select an MCP server tool to view inputs

</td><td>

Various inputs for the selected MCP server to tool.The following inputs are available and are subject to change based on the selected MCP server tool.

-   **Query**: Represents the search query with data type as a string.

**Note:** The search query must not exceed a maximum of 400characters or 50 words.

-   **Count**: Represents the number of results with data type as numeric.

**Note:** Results are displayed from 1 to 20 with the default value as **10**.

-   **Offset**: Represents the pagination with data type as numeric.

**Note:** The pagination offset must not exceed a maximum of 9 pages with the default value as **0**.

</td></tr><tr><td>

Name

</td><td>

Name of the MCP tool.

</td></tr><tr><td>

Tool and Description

</td><td>

Description of the MCP tool and how it can assist your AI agent.**Note:** This description is sent to the large language model \(LLM\).

</td></tr><tr><td>

Execution Mode

</td><td>

Mode of execution for your selected MCP tool. Choose from the following options:-   **Supervised**: Requires input from a human agent are required during the execution of this MCP tool while the AI agent runs.
-   **Autonomous**: Doesn't require any input from a human agent during the execution of the MCP tool while the AI agent runs.


</td></tr><tr><td>

Display output

</td><td>

Option to display the execution output in the Now Assist panel or in Virtual Agent.If you want the AI agent to work in Off Glide architecture with AI-native experience, you must turn-on the **Display output** toggle. When the toggle is turned-on, you can add widgets that can be used in assistants built with AI-native experiences. The widget configuration includes:

-   **Widgets**: Defines the display output to render the content in a better user experience. You can select the widget from the drop-down.
-   **Require widget transformation**: An additional LLM call is required to transform the raw tool. If you choose to skip this transformation step, the tool output will be directly mapped to the widget.
    -   **Yes**
    -   **No**
-   **Display refined widget message**: Refines the widget message when configured.
    -   **Yes**
    -   **No**
**Note:** The display output as a toggle is exclusively available for the AI-native experience when the Off Glide Conversation Server plugin \(com.glide.cs.offglide\) is installed. If the plugin is not installed, you will continue to access the standard display output options.

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

    An MCP server tool is added in the Model Context Protocol Tools list on the Add tools and information page.


