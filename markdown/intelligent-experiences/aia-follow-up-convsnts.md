---
title: Follow-up conversations
description: AI agents continue with follow-up conversations after the AI agent execution is complete.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [AI Agents, Agentic AI]
breadcrumb: [Configure, Now Assist AI agents, Enable AI experiences]
---

# Follow-up conversations

AI agents continue with follow-up conversations after the AI agent execution is complete.

## Before you begin

Role required: sn\_aia\_admin

## About this task

When the \[sn\_aia.enable\_follow\_up\] system property is set to **true** and if there is no record for the agentic workflow created in the Agent properties \[sn\_aia\_property\] table, then the AI agents continue with the `How else can I help you?` follow-up message after the agentic workflow execution.

The AI agent conversation doesn't get closed after the execution is complete by default. If you would like to override the follow-up behavior for your AI agents for a specific agentic workflow, you must create a record in the Agent Properties \[sn\_aia\_property\] table.

## Procedure

1.  Navigate to **All** &gt; **System Definitions** &gt; **Tables** and open the Agent Properties \[sn\_aia\_property\] table.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_p1w_dxp_x2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the agent property record for the agentic workflow.For example,`follow_up_behaviour`

</td></tr><tr><td>

Value

</td><td>

Provide the following values as per the requirement:-   **no\_followup\_close\_conversation**: Closes the conversation after the use case is complete.
-   **no\_followup\_open\_conversation**: Keeps the conversation open after the use case is complete.


</td></tr><tr><td>

Target table

</td><td>

The table where the target agentic workflow resides: Agentic workflows \[sn\_aia\_use case\] table.

</td></tr><tr><td>

Target record

</td><td>

The record of the target agentic workflow or AI agent.

</td></tr><tr><td>

Application

</td><td>

The application scope for the agent property record: Now Assist AI agents.

</td></tr></tbody>
</table>4.  Select **Submit**.


