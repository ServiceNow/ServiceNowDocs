---
title: Data Discovery policy and job manager AI agent
description: This ServiceNow Vault agent checks whether a given list of tables supports data discovery scanning. The agent then creates data discovery job policies using these tables, and creates discovery job policies and schedules and data discovery jobs using the created policy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/vault-data-discovery-policy-and-job-manager-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [ServiceNow Vault AI agents, ServiceNow Vault AI agents, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Data Discovery policy and job manager AI agent

This ServiceNow Vault agent checks whether a given list of tables supports data discovery scanning. The agent then creates data discovery job policies using these tables, and creates discovery job policies and schedules and data discovery jobs using the created policy.

## Workflow

1.  Take a list of table names, validate each one for discovery scan support using the validation tool, and separate them into supported and unsupported groups.
2.  Show the results and let the user add, remove, or replace tables. Re-validate after each edit until the user confirms the final list.
3.  Generate a policy name and create the policy using the supported tables and selected data patterns.
4.  Gather the required inputs for a discovery job: scan type, trigger frequency, and the corresponding date/time parameters for the chosen frequency.
5.  Confirm the collected details with the user, submit to the job scheduler tool, and display the created job's name and ID.

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

Check AI shared services usage entitlement

Create Data Discovery policy

Discovery Job scheduler tool

Get available Discovery Data patterns

Validate input table Discovery scan support


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

