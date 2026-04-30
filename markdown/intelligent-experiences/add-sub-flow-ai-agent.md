---
title: Add a subflow to an AI agent
description: Add a subflow to an AI agent in AI Agent Studio. Subflows are reusable sequences of processing steps that can be called from within a flow.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Add tools and information, Create an AI agent, Now Assist AI agents, Enable AI experiences]
---

# Add a subflow to an AI agent

Add a subflow to an AI agent in AI Agent Studio. Subflows are reusable sequences of processing steps that can be called from within a flow.

## Before you begin

When an AI agent uses a subflow tool, the user the AI agent is running as must pass the ACL of the subflow. Ensure that the security configurations for the subflow are met by the AI agent and agentic workflow. For more information, see [Security for AI agents](../concept/aia-security-implementation.md).

Role required: sn\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **AI agents**.

2.  Open the AI agent that you want to add a subflow to and navigate to the Add tools and information section.

3.  In the Add tool drop-down list, select **Subflow**.

4.  On the form, fill in the fields.

<table id="table_rt1_rgv_cdc"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name that you want to specify for your selected subflow.

</td></tr><tr><td>

Description

</td><td>

Description of the subflow and what it’s going to do to assist your AI agent.**Note:** This description is sent to the large language model \(LLM\).

</td></tr><tr><td>

Select subflow

</td><td>

Existing process automation capability you want to add.If there is a tool used by an AI agent for the same subflow, the rest of the form will populate the fields based on the other tool. You can make any changes specific to the current AI agent to suit your needs, and it will not affect the tool of the existing AI agent.

</td></tr><tr><td>

Inputs

</td><td>

Subflow inputs. The values are filled in by the LLM at runtime unless you specify a value override.**Note:** If the agent uses multiple tools, you can choose to use another tool's output as an input value override. Select the data picker icon \(![Data picker icon.](../image/data-picker-icon.png)\) to review the available options.

</td></tr><tr><td>

Execution mode

</td><td>

Mode of execution for your selected subflow:-   **Supervised**: Inputs from your live agent are required during the execution of this tool while the AI agent runs.
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

Style for the LLM to present the results as it passes information between tools and to other agents.-   None
-   Concise
-   Paragraph
-   Verbose
-   Custom


</td></tr></tbody>
</table>5.  Select **Add**.

    A subflow tool is added in the Subflows section on the Add tools and information page.


