---
title: SLA management AI Agent
description: This ServiceNow Otto for Setup agent enables administrators to create and edit SLA definitions through a conversational interface. The agent guides you through SLA configuration, including setting target type \(Resolution/Response\), duration, table, schedule, start/pause/stop conditions, and flow associations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/plat-setup-sla-management-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Setup Hub AI agents, ServiceNow AI Platform, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# SLA management AI Agent

This ServiceNow Otto for Setup agent enables administrators to create and edit SLA definitions through a conversational interface. The agent guides you through SLA configuration, including setting target type \(Resolution/Response\), duration, table, schedule, start/pause/stop conditions, and flow associations.

## Workflow

1.  Determine whether the admin wants to create an SLA or edit an existing one \(asking if unclear\).
2.  Collect the target type \(Resolution/Response\), applicable table, classification \(priority, type, model, or service\), duration, and name, using existing SLAs and smart defaults to recommend values where possible.
3.  Confirm which schedule applies and associate a notification/escalation flow.
4.  Recommend and confirm start, pause, and stop conditions based on the SLA type.
5.  Present a full summary of the configured SLA and get admin confirmation.
6.  Save the SLA definition, handling any duplicate-configuration conflicts along the way.
7.  Display a confirmation summarizing what was created or changed.

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

Agent Context Retriever

Create Update SLA Definition

Get SLA Data

Text to encoded query generation

Validate and Lookup SLA Field Inputs

-   **Generative AI skill**

Flow summariser


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sla\_manager

</td></tr><tr><td>

Data access roles

</td><td>

sla\_manager, sn\_query\_gen.admin, fd\_read\_flows

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
</table>Learn more about ServiceNow Otto for Setup at [ServiceNow Otto for Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ia-landing.md).

**Parent Topic:**[Setup Hub AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-setup-ai-agents-overview.md)

