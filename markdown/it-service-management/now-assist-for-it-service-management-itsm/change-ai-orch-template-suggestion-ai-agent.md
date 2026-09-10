---
title: Change template suggestion AI agent \(autonomous\)
description: This AI agent identifies the most relevant change template and model for new change requests by analyzing request details and comparing them against available templates and historical data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/now-assist-for-it-service-management-itsm/change-ai-orch-template-suggestion-ai-agent.html
release: zurich
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: reference
last_updated: "2026-09-01"
reading_time_minutes: 2
breadcrumb: [Agentic AI in the Change Management application, Use agentic AI in IT Service Management, ServiceNow Otto for IT Service Management \(ITSM\), IT Service Management]
---

# Change template suggestion AI agent \(autonomous\)

This AI agent identifies the most relevant change template and model for new change requests by analyzing request details and comparing them against available templates and historical data.

## Workflow

This autonomous AI agent runs as part of the Create change request agent. The agent analyzes change request details and automatically selects the most appropriate change template and model from your organization's inventory.

1.  Autonomously retrieve the complete inventory of available change templates and models.
2.  Analyze the change request details provided by the parent Create change request agent.
3.  Apply large language model judgment to identify candidate templates based on relevance to the change request.
4.  If a template with sufficient confidence is identified, autonomously select it as the best-fit template and return it to the parent agent.
5.  If no template meets the confidence threshold, autonomously perform semantic search over past change requests created by members of the user's assignment group.
6.  Rank semantic search results by combining two factors: frequency of past use and relevance to the current request, weighting each factor roughly equally.
7.  Return the best-fit template identified through semantic search to the parent agent.

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

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Scripts**

Get change models and templates

Get template/model recommendation from Similar Changes from the assignment group


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

itil, sn\_change\_writeThe sn\_change\_write only applies when the dependency plugin com.snc.itsm.roles.change\_management is active.

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

itil, sn\_change\_writeThe sn\_change\_write only applies when the dependency plugin com.snc.itsm.roles.change\_management is active.

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Enable the AI agent for the ServiceNow Otto panel.

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Create a change request AI agent

</td></tr></tbody>
</table>