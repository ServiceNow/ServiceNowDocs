---
title: Data Discovery recommendation AI agent
description: This ServiceNow Vault agent provides job info, findings, attributes, and related details for a list of tables provided. The agent also returns scan recommendations you can use to create policy and schedule the discovery job by another agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/vault-data-discovery-recommendation-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [ServiceNow Vault AI agents, ServiceNow Vault AI agents, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Data Discovery recommendation AI agent

This ServiceNow Vault agent provides job info, findings, attributes, and related details for a list of tables provided. The agent also returns scan recommendations you can use to create policy and schedule the discovery job by another agent.

## Workflow

The agent helps users complete tasks related to data discovery recommendation agent.

1.  Take a list of instance table names from the user.
2.  Check whether previous discovery jobs have run against those tables \(standard or attachment scans\).
3.  Determine which data patterns have already been scanned and which remain unscanned across the provided tables.
4.  Suggest an appropriate scan \(Sample, Full, Incremental, or Attachment\) based on whether previous jobs exist, data volume, and how frequently data changes.
5.  Suggest daily, weekly, or monthly based on the previous job's run type.
6.  Rate each table's risk based on the presence of PII patterns.
7.  Display a single structured recommendation covering all provided tables: status, scanned/unscanned patterns, suggested scan type and frequency, sensitivity risk, and recommended next action.

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

Get Attachment Data Discovery insights for tables

Get Discovery Insights for tables


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_data\_discovery.data\_discovery\_admin

</td></tr><tr><td>

Data access roles

</td><td>

sn\_data\_discovery.data\_discovery\_admin

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

Data discovery job scheduler workflow

</td></tr></tbody>
</table>Learn more about ServiceNow Vault at [ServiceNow Vault](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-vault-landing.md).

**Parent Topic:**[ServiceNow Vault AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/vault-ai-agents-overview.md)

