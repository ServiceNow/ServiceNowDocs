---
title: Live interaction recommendations AI agent
description: The agent analyzes the conversation between a customer and a live agent. It recommends actions that help the live agent resolve the customer's issue.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/csm-live-interaction-recommendations-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-30"
reading_time_minutes: 1
breadcrumb: [Customer Service Management AI agents, Customer Service Management, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Live interaction recommendations AI agent

The agent analyzes the conversation between a customer and a live agent. It recommends actions that help the live agent resolve the customer's issue.

## Workflow

The agent helps a live agent during a customer call by surfacing recommendations from the interaction.

1.  Show a **Get Recommendations** button when the session starts.
2.  Analyze the current interaction when the user selects the button.
3.  Display the recommendations, with clarifying options where they apply.
4.  Refine the recommendations when the user selects an option or asks a follow-up question.
5.  Show the button again so the user can refresh the recommendations as the call continues.

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

Get Interaction Context

-   **Tool**

Analyse Interaction and Generate Recommendation


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

sn\_esm\_agent

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

sn\_customerservice\_agent, and sn\_customerservice.consumer\_agent

</td></tr><tr><td>

Triggers

</td><td>

Live interaction recommendations AI agent - Interaction

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>**Parent Topic:**[Customer Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/csm-ai-agents-overview.md)

