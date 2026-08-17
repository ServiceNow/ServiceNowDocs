---
title: Create Data Privacy advanced configuration AI agent
description: This ServiceNow Vault agent helps users complete tasks related to creating data privacy advanced configuration agents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/vault-create-data-privacy-advanced-configuration-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [ServiceNow Vault AI agents, ServiceNow Vault AI agents, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Create Data Privacy advanced configuration AI agent

This ServiceNow Vault agent helps users complete tasks related to creating data privacy advanced configuration agents.

## Workflow

1.  Execute one of six operations based on the task received from the workflow:
    -   **Fetch active configuration**

        Look up the active data privacy policy configuration for a given data channel.

    -   **Fetch data channels**

        Retrieve the list of all available data channels with their IDs.

    -   **Create default Data Extraction configuration**

        Create a policy configuration for the data extraction channel using defaults.

    -   **Create policy configuration**

        Create an advanced policy configuration with a user-provided name and data channel.

    -   **Activate policy configuration**

        Activate an existing policy configuration \(fully non-interactive, no user prompts\).

    -   **Generate configuration URL**

        Produce a link to view a specific policy configuration.

2.  After any operation completes, hand the result back to the calling workflow.

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

Create data extraction configuration

Create new advanced configuration in dp\_configuration\_domain\_separated

Generate data privacy policy configuration link

Get all data channels

Update privacy advanced configuration tool

-   **Record Operation**

Fetch active data privacy policy configuration for data channel


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

data\_privacy\_admin, virtual\_agent\_data\_privacy\_admin, data\_kit\_data\_privacy\_admin, now\_assist\_data\_privacy\_admin

</td></tr><tr><td>

Data access roles

</td><td>

now\_assist\_data\_privacy\_admin, data\_kit\_data\_privacy\_admin, data\_privacy\_admin, virtual\_agent\_data\_privacy\_admin

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

Create Data Privacy advanced configuration

</td></tr></tbody>
</table>Learn more about ServiceNow Vault at [ServiceNow Vault](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-vault-landing.md).

**Parent Topic:**[ServiceNow Vault AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/vault-ai-agents-overview.md)

