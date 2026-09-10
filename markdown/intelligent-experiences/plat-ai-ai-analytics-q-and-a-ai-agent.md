---
title: AI Analytics Q and A AI agent
description: This AI agent answers natural language questions about AI Analytics. It covers KPI definitions, dashboard widgets, source tables, data flows, deflection log states and scenarios, the deflection and metric frameworks, and ServiceNow platform scripts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/plat-ai-ai-analytics-q-and-a-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-06-01"
reading_time_minutes: 2
breadcrumb: [ServiceNow AI Platform AI agents, ServiceNow AI Platform, AI agents library, AI assets, Enable AI experiences]
---

# AI Analytics Q and A AI agent

This AI agent answers natural language questions about AI Analytics. It covers KPI definitions, dashboard widgets, source tables, data flows, deflection log states and scenarios, the deflection and metric frameworks, and ServiceNow platform scripts.

## Workflow

Use this agent for any question about AI Analytics metrics, dashboards, or underlying data architecture.

1.  Receive the user's question and pass it to the Now Assist Analytics Q and A skill exactly as written, without paraphrasing.
2.  Retrieve the skill's grounded answer, which draws from verified platform documentation covering metrics, dashboards, source tables, and scripts.
3.  Present the skill's answer to the user exactly as returned, preserving all identifiers, links, and formatting without summarizing or rewording it.
4.  If the skill returns no usable answer, respond that there is not enough information to answer accurately and direct the user to the documentation or their platform admin.

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

-   **Generative AI skill**

skill


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

snc\_internal

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

sn\_na\_analytics.viewer

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

Not applicable.

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow AI Platform AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-ai-agents-overview.md)

