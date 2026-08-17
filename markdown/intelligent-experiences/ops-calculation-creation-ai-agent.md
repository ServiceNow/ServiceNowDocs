---
title: Calculation creation AI agent
description: This AI agent creates a calculated metric definition record using the formula passed in the input.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ops-calculation-creation-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Operational Sustainability Management AI agents, Operational Sustainability Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Calculation creation AI agent

This AI agent creates a calculated metric definition record using the formula passed in the input.

## Workflow

The agent helps users complete tasks related to calculation creation.

1.  If the final formula is empty, tell the user it can't be calculated.
2.  With the formula and name given in the input context, create a calculated metric definition and show the response to the user.

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

-   **Script**

Create Calculated metric definition


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_esg\_gen\_ai.cmd\_agent\_user

</td></tr><tr><td>

Data access roles

</td><td>

sn\_grc\_metric.manager

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

Generate carbon calculations for metrics

</td></tr></tbody>
</table>Learn more about Operational Sustainability Management at [Operational Sustainability Management \(formerly Environmental, Social, and Governance\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/esg-landing-page.md).

**Parent Topic:**[Operational Sustainability Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ops-ai-agents-overview.md)

