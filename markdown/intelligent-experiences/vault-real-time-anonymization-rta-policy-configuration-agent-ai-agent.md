---
title: Real Time Anonymization\(RTA\) Policy Configuration AI agent
description: The agent creates Real-Time Anonymization \(RTA\) policies that mask or anonymize sensitive column values as they're accessed. It guides the user through naming the policy, selecting the target columns to anonymize, and choosing any child tables that should inherit the same protection.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/vault-real-time-anonymization-rta-policy-configuration-agent-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-29"
reading_time_minutes: 2
breadcrumb: [ServiceNow Vault AI agents, ServiceNow Vault AI agents, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Real Time Anonymization\(RTA\) Policy Configuration AI agent

The agent creates Real-Time Anonymization \(RTA\) policies that mask or anonymize sensitive column values as they're accessed. It guides the user through naming the policy, selecting the target columns to anonymize, and choosing any child tables that should inherit the same protection.

## Workflow

The agent helps the user create a Real-Time Anonymization policy.

1.  Ask the user for a policy name.
2.  Fetch the available target columns and display them for the user to select, or inform the user if none are available.
3.  Confirm the selected columns with the user.
4.  Fetch the child tables for the selected columns and ask the user which child tables should inherit the protection.
5.  Create the RTA policy and display the result.

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

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Script**

Create RTA policy

Fetch available target columns

Fetch child tables


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

data\_discovery\_admin, data\_privacy\_admin, data\_privacy\_admin

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

Not defined.

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Realtime Anonymization\(RTA\) Policy Creation Agentic Workflow

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow Vault AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/vault-ai-agents-overview.md)

