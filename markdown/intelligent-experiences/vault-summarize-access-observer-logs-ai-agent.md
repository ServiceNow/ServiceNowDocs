---
title: Summarize Access Observer logs AI agent
description: This ServiceNow Vault agent summarizes access observer logs and provides detailed breakdowns by caller type, users, and roles for specific table and column combinations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/vault-summarize-access-observer-logs-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [ServiceNow Vault AI agents, ServiceNow Vault AI agents, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Summarize Access Observer logs AI agent

This ServiceNow Vault agent summarizes access observer logs and provides detailed breakdowns by caller type, users, and roles for specific table and column combinations.

## Workflow

1.  Check the user has the security\_admin role \(required.\)
2.  Retrieve available table/column combinations that have Access Observer logs, display them with log counts, and let the user pick one.
3.  Confirm logs exist for the selected table-column pair.
4.  For each of the seven supported caller types \(UI action, UI page, script include, scripted REST API, scheduled jobs, business rule, and unidentified sources\). Retrieve the access logs and display a summary showing total accesses, users, roles, and caller sources.
5.  Point the user to the **Field Encryption with Vault module** skill for encrypting the field and creating module access policies.

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

Check access log counts by caller type

Check if user has security admin role

Get Access Logs

List available table and column combinations


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

snc\_internal, snc\_internal

</td></tr><tr><td>

Data access roles

</td><td>

security\_admin, sn\_vault\_console.vault\_console\_admin

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

Summarize Access Observer logs

</td></tr></tbody>
</table>Learn more about ServiceNow Vault at [ServiceNow Vault](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-vault-landing.md).

**Parent Topic:**[ServiceNow Vault AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/vault-ai-agents-overview.md)

