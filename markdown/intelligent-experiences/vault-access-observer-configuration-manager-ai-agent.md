---
title: Access Observer configuration manager AI agent
description: This ServiceNow Vault agent helps users complete tasks related to Access Observer configuration manager.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/vault-access-observer-configuration-manager-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [ServiceNow Vault AI agents, ServiceNow Vault AI agents, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Access Observer configuration manager AI agent

This ServiceNow Vault agent helps users complete tasks related to Access Observer configuration manager.

## Workflow

1.  Check the user has the security\_admin role.
2.  Identify which operation the user wants to perform, or present the five supported options:
    -   **Create**

        Collect a table and column. Validate that both exist and aren't blocked, collect start/end dates, then run through a series of checks before creating the Access Observer configuration. On success, direct the user to the **Summarize Access Observer logs** skill.

    -   **Delete**

        Collect table and column and show matching configurations. Prompt the user select one, and delete it.

    -   **Deactivate**

        Collect table and column and show matching configurations. Prompt the user select one, and deactivate it.

    -   **Get/Fetch**

        Collect table and column. Retrieve and display all configurations for that specific combination.

    -   **List all**

        Retrieve and display all Access Observer configurations.


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

Check if a table is blocked

Check if user has security\_admin role

Check table and column available

Create Access Observer configuration

Deactivate Access Observer configuration

Delete Access Observer configuration

Get Access Observer configuration

Get all Access Observer configurations

Get child tables recursively

Get parent tables recursively


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

snc\_internal

</td></tr><tr><td>

Data access roles

</td><td>

sn\_vault\_console.vault\_console\_admin, security\_admin

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

Access Observer configuration

</td></tr></tbody>
</table>Learn more about ServiceNow Vault at [ServiceNow Vault](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-vault-landing.md).

**Parent Topic:**[ServiceNow Vault AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/vault-ai-agents-overview.md)

