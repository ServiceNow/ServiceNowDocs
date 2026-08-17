---
title: Record field value prediction AI agent
description: This AI agent can predict fields for an incoming record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/plat-ai-record-field-value-prediction-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [ServiceNow AI Platform AI agents, ServiceNow AI Platform, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Record field value prediction AI agent

This AI agent can predict fields for an incoming record.

## Workflow

The agent can also provide a summary and justification of the field predictions.

1.  Get the record details.
2.  Using the table and sys\_id, determine if the task is ready to be processed.
3.  With the user's input, use the Predict fields for a record or config tool to predict fields.
4.  Predict fields on related list records only if a potential related list name is found.
5.  Show predictions to the user.
6.  Justify predicted fields if asked.
7.  Update the record with predicted fields.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allow third party to access this AI agent

</td><td>

When enabled, third-party AI agents can use this agent. This value is off \(false\) by default. This setting is defined in the AI Agent configs \[sn\_aia\_agent\_config\] table on the External discoverable field.

</td></tr><tr><td>

Allow AI specialists to access this AI agent

</td><td>

When enabled, AI specialists can use this agent. This value is off \(false\) by default. When set to true, more configuration options for tools become available so that an AI specialist can map inputs and response templates to tool outputs. This setting is defined in the AI Agent configs \[sn\_aia\_agent\_config\] table on the Specialist enabled field.

</td></tr><tr><td>

Manage long-term memory

</td><td>

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Scripts**

Get issue readiness state

Get Related List Records

Get Related Lists

Get Similar Records

Get the record metadata

Predict fields for a record or config

Save activity notes

Summarize and Justify

Update record details


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_uxc\_gen\_ai.platform\_ai\_field\_predictor

</td></tr><tr><td>

Data access roles

</td><td>

sn\_uxc\_gen\_ai.platform\_ai\_field\_predictor, itil, sn\_hr\_core.case\_writer, sn\_lg\_ops.request\_fulfiller

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

-   Triage legal requests
-   Predict service and transfer HR Cases
-   Classify tasks
-   Universal Request Router

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow AI Platform AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-ai-agents-overview.md)

