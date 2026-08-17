---
title: Edit Data Privacy advanced configuration mapping AI agent
description: This ServiceNow Vault agent helps users complete tasks related to edit data privacy advanced configuration mapping agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/vault-edit-data-privacy-advanced-configuration-mapping-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [ServiceNow Vault AI agents, ServiceNow Vault AI agents, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Edit Data Privacy advanced configuration mapping AI agent

This ServiceNow Vault agent helps users complete tasks related to edit data privacy advanced configuration mapping agent.

## Workflow

1.  Execute one of three operations based on the task received from the calling workflow or agent:
    -   Change mapping: Update the existing pattern-technique mapping for the given policy.
    -   Add mapping: Look up available patterns for the policy, let the user select one or more, and add them.
    -   Remove mapping: Deactivate the pattern-technique mappings for the given policy.
2.  After any operation completes \(or if no policy ID was provided\), hand control back to the caller.

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

Add pattern in DP advanced policy

-   **Conversational topics**

Deactivate data patterns

Lookup patterns for DP advance policy edit

Update DP advanced configuration mapping tool


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

virtual\_agent\_data\_privacy\_admin, data\_kit\_data\_privacy\_admin, data\_privacy\_admin, now\_assist\_data\_privacy\_admin

</td></tr><tr><td>

Data access roles

</td><td>

now\_assist\_data\_privacy\_admin, data\_privacy\_admin, data\_kit\_data\_privacy\_admin, virtual\_agent\_data\_privacy\_admin

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

-   Default VA Workflow
-   Edit Data Privacy Advanced Configuration
-   Create Data Privacy Advanced Configuration

</td></tr></tbody>
</table>Learn more about ServiceNow Vault at [ServiceNow Vault](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-vault-landing.md).

**Parent Topic:**[ServiceNow Vault AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/vault-ai-agents-overview.md)

