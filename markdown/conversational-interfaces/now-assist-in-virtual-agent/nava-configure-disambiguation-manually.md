---
title: Configure disambiguation
description: Configure the disambiguation option that controls when the assistant asks clarifying questions before responding to a Now Assist in Virtual Agent or Now Assist panel user request.
locale: en-US
release: zurich
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2026-03-30"
reading_time_minutes: 1
breadcrumb: [Configuring assistants overview, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Configure disambiguation

Configure the disambiguation option that controls when the assistant asks clarifying questions before responding to a Now Assist in Virtual Agent or Now Assist panel user request.

## Before you begin

Role required: admin

## About this task

Disambiguation or clarification helps the Now Assist assistant handle situations where the user's request is ambiguous. Rather than returning an overwhelming list of results, the assistant evaluates the request using a confidence scoring system and asks clarifying questions if needed.

## Procedure

1.  In the filter navigator field, enter `sys_properties.list`.

2.  In the selection fields, select **Name** from the drop-down list and enter `type_2_disamb` in the Search field.

3.  Configure the property:

<table id="table_pkn_sn1_53c"><thead><tr><th>

Property

</th><th>

Possible values

</th><th>

Default value

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

sn\_aia.type\_2\_disamb

</td><td>

off/low/high

</td><td>

off

</td><td>

-   off - clarification is disabled. The assistant responds directly to all queries without asking follow-up questions.
-   low - clarification is triggered only for highly ambiguous queries.
-   high - clarification is triggered more frequently, covering a broader range of ambiguous queries.


</td></tr></tbody>
</table>4.  To view the disambiguation data, in the filter navigator field, enter `sys_generative_ai_log`.

5.  To filter conversations, use these criteria:

    -   **Definition** contains `planner 2`.
    -   **Response** contains `clarification_question`.

