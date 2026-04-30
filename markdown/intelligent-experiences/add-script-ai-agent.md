---
title: Add a script to an AI agent
description: Create a script to add it to an AI agent in AI Agent Studio. With scripts, you can use the scriptable APIs and back-end integration to support the AI agent.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Add a tool to an AI agent, Create an AI agent, Now Assist AI agents, Enable AI experiences]
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

Mode of execution for your script:-   **Supervised**: Inputs from your live agent are required during the execution of this tool while the AI agent runs.
-   **Autonomous**: Doesn't require any input from your live agent during the execution of this tool while the AI agent runs.


</td></tr><tr><td>

Display output

</td><td>

Permission to display the output of the tool execution in the Now Assist panel or in Virtual Agent:-   **Yes**
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

    A script tool is added in the Scripts section on the Add tools and information page.


**Parent Topic:**[Add a tool to an AI agent](../concept/add-tool-aia.md)

