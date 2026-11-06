---
title: Live interaction recommendations AI agent
description: The AI agent analyzes the conversation between a customer and a human agent. It recommends actions that help a human agent resolve the customer's issue.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/csm-live-interaction-recommendations-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-09-30"
reading_time_minutes: 1
breadcrumb: [Customer Service Management AI agents, Customer Service Management, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Live interaction recommendations AI agent

The AI agent analyzes the conversation between a customer and a human agent. It recommends actions that help a human agent resolve the customer's issue.

## Workflow

The AI agent helps a human agent by providing real-time recommendations during live customer interactions on the voice channel.

1.  Show the welcome message and customer name in the ServiceNow Otto panel when the session starts.
2.  Show the **Get Recommendations** button.
3.  Analyze the current call transcript when the human agent selects the **Get Recommendations** button.
4.  Display the recommendations, with clarifying options where they apply.
5.  Refine the recommendations when the user selects an option or asks a follow-up question.
6.  Show the **Get Recommendations** button again so the user can refresh the recommendations as the call continues.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Manage long-term memory

</td><td>

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Script**

Get Interaction Context

-   **Subflow**

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

Configure an assistant for ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>**Parent Topic:**[Customer Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/csm-ai-agents-overview.md)

