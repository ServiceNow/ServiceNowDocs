---
title: Vault crypto module manager AI agent
description: This ServiceNow Vault agent manages the Vault crypto module configuration and access policies. The agent handles encrypted field configurations for fields, and manages module access policies for roles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/vault-vault-crypto-module-manager-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [ServiceNow Vault AI agents, ServiceNow Vault AI agents, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Vault crypto module manager AI agent

This ServiceNow Vault agent manages the Vault crypto module configuration and access policies. The agent handles encrypted field configurations for fields, and manages module access policies for roles.

## Workflow

1.  Check that the required roles \(KMF admin/cryptographic manager and security\_admin\) are available \(required\) and whether Field Encryption Enterprise is installed \(recommended\).
2.  Present the four supported operations and let the user choose one:
    -   **Encrypt a field**

        Collect the table and field name, validate both exist, check whether the field is already encrypted, and if not, encrypt it with the vault crypto module.

    -   **Grant role access**

        Collect a role name, check if it already has access, and if not, create a module access policy for that role.

    -   **Check encryption status**

        Collect a table and field name, validate both exist, and report whether the field is currently encrypted.

    -   **List roles with access**
3.  Display the outcome \(success, failure, or current status\) and end execution.

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

Check if field is encrypted

Check prerequisites

Check table and field available

Create module access policy for role

Encrypt field with vault crypto module

Get all roles with vault crypto module access


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

snc\_internal

</td></tr><tr><td>

Data access roles

</td><td>

sn\_vault\_console.vault\_console\_admin, security\_admin, sn\_kmf.admin, sn\_kmf.cryptographic\_manager

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

Field Encryption with Vault module

</td></tr></tbody>
</table>Learn more about ServiceNow Vault at [ServiceNow Vault](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-vault-landing.md).

**Parent Topic:**[ServiceNow Vault AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/vault-ai-agents-overview.md)

