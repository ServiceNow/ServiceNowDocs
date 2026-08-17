---
title: DP record selector agent AI agent
description: This ServiceNow Vault agent fetches data using tools or topics to display list of choices related to the action.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/vault-dp-record-selector-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [ServiceNow Vault AI agents, ServiceNow Vault AI agents, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# DP record selector agent AI agent

This ServiceNow Vault agent fetches data using tools or topics to display list of choices related to the action.

## Workflow

1.  Execute one of two operations based on the task received from the workflow:
    -   Fetch policies: Retrieve and display all available data privacy advanced configurations, let the user select one, and return the selected policy ID to the workflow.
    -   Fetch edit options: Retrieve and display the available edit operations for a policy, let the user select one, and return the selection to the workflow.
2.  After either operation, hand the result back to the calling workflow.

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

Fetch advanced DP policy

-   **Conversational topics**

Select a privacy advanced policy

Select DP advanced policy edit options


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

data\_kit\_data\_privacy\_admin, data\_privacy\_admin, virtual\_agent\_data\_privacy\_admin, now\_assist\_data\_privacy\_admin

</td></tr><tr><td>

Data access roles

</td><td>

data\_privacy\_admin, data\_kit\_data\_privacy\_admin, virtual\_agent\_data\_privacy\_admin, now\_assist\_data\_privacy\_admin

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

-   Edit Data Privacy Advanced Configuration
-   Default VA Workflow

</td></tr></tbody>
</table>Learn more about ServiceNow Vault at [ServiceNow Vault](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-vault-landing.md).

**Parent Topic:**[ServiceNow Vault AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/vault-ai-agents-overview.md)

