---
title: Order fallout AI agent
description: The AI agent analyzes the work notes and comments on an order task, identifies issues or errors, and maps them to existing fallout types. It creates fallout records so that the errors can be followed up.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/tmt-order-fallout-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-11-04"
reading_time_minutes: 2
breadcrumb: [Sales CRM for Telecommunications AI agents, Telecommunications, Media and Technology AI agents, Telecom, Media and Tech AI agents, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Order fallout AI agent

The AI agent analyzes the work notes and comments on an order task, identifies issues or errors, and maps them to existing fallout types. It creates fallout records so that the errors can be followed up.

## Workflow

The agent helps the user identify issues reported on an order task and record them as fallouts.

1.  Retrieve the order task details, including its work notes and comments.
2.  Retrieve the available fallout types.
3.  Analyze the work notes to find issues that match the available fallout types.
4.  Create fallout records for any matching issues.
5.  Show the user a summary of the steps taken, including the fallouts that were created or a note that none were created.

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

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Script**

Create validated and confirmed fallouts

Find all available fallout types

Find all notes for order task


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

Not defined.

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

Not defined.

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>Learn more about Sales CRM for Telecommunications at [Sales Customer Relationship Management for Telecommunications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/sales-crm.md).

**Parent Topic:**[Sales CRM for Telecommunications AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/somt-ai-agents-overview.md)

