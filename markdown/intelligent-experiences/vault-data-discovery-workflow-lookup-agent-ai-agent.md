---
title: Data Discovery workflow lookup AI agent
description: This ServiceNow Vault agent receives provide recommendation for different tables associated with workflows, and identifies what kind of sensitive data can present in those tables such as PII,PFI,PCI,PHI,FCI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/vault-data-discovery-workflow-lookup-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [ServiceNow Vault AI agents, ServiceNow Vault AI agents, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Data Discovery workflow lookup AI agent

This ServiceNow Vault agent receives provide recommendation for different tables associated with workflows, and identifies what kind of sensitive data can present in those tables such as PII,PFI,PCI,PHI,FCI.

## Workflow

1.  Determine whether the user provided specific workflow names, specific table names, or wants to process all workflows.
2.  If workflow names were given, retrieve all active workflows from the instance and confirm the user's entries are valid. Ask one clarification question and values are invalid.
3.  Either fetch tables associated with the validated workflows, or use the directly provided table names, pulling in associated tables as well.
4.  Determine which sensitive data group classifications \(PII, PHI, PFI, PCI, FCI\) apply to each table.
5.  Present the findings in a structured card format showing each table with its sensitive data classifications, grouped by workflow if workflows were the input.

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

Find available workflows in the instance

-   **Web searches**

Workflow table fetcher


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

