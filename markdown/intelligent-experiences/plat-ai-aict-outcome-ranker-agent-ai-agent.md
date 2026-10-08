---
title: AICT outcome ranker AI agent
description: This AI agent ranks AI insight outcomes by relevance to each user persona based on their role and responsibilities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/plat-ai-aict-outcome-ranker-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-10-01"
reading_time_minutes: 2
breadcrumb: [ServiceNow AI Platform AI agents, ServiceNow AI Platform, AI agents library, AI assets, Enable AI experiences]
---

# AICT outcome ranker AI agent

This AI agent ranks AI insight outcomes by relevance to each user persona based on their role and responsibilities.

## Workflow

This autonomous agent receives persona descriptions and outcome metadata, determines personalized ranking for each outcome relative to user personas, and writes ranks to enable prioritized insight display.

1.  Receive a JSON objective containing personas, outcomes, and their sys\_ids.
2.  Analyze each persona description to understand their role, priorities, and responsibilities.
3.  For each outcome, understand its business value and impact based on its ID and description.
4.  Rank all outcomes for each persona from most relevant \(1\) to least relevant \(N\).
5.  Call Populate Outcome Ranks to write all persona-outcome ranks, then trigger prioritization recompute.

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

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Scripts**

Populate Outcome Ranks

Recompute Prioritized Insights


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

Not defined.

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

sn\_generative\_ai.data\_steward

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow AI Platform AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/platform-ai-agents-overview.md)

