---
title: Alert automation AI agent
description: This agent interprets free-text user requests related to alert automation and guides users to the appropriate automation experience. It detects whether the user intends to enrich alerts, group alerts, respond to alerts, or any combination of these actions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aiops-alert-automation-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [AIOps and AIOps Leap AI agents, AIOps and AIOps Leap, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Alert automation AI agent

This agent interprets free-text user requests related to alert automation and guides users to the appropriate automation experience. It detects whether the user intends to enrich alerts, group alerts, respond to alerts, or any combination of these actions.

## Workflow

The agent helps users complete tasks related to alert automation.

1.  Identify requested alert automations, including alert enrichment, alert response, and alert grouping.
2.  Provide links to alert automations that fit the query.
3.  Create an alert grouping automation record when requested.

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

Activate Alert Group Automation

Alert Group Automation Canonicalizer

Create Alerts Grouping Automation

Delete Alerts Grouping Automation

Get Alert Automation Link


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

evt\_mgmt\_admin, evt\_team\_operator

</td></tr><tr><td>

Data access roles

</td><td>

evt\_mgmt\_admin, evt\_team\_operator

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

Create alert automation

</td></tr></tbody>
</table>Learn more about Learning Enhanced Automation Platform \(LEAP\) at [Learning Enhanced Automation Platform \(LEAP\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap.md).

**Parent Topic:**[AIOps and AIOps Leap AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aiops-ai-agents-overview.md)

