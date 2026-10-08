---
title: Real Time Anonymization\(RTA\) Test AI agent
description: The agent tests Real-Time Anonymization \(RTA\) by taking a text string from the user and returning the anonymized version.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/vault-real-time-anonymization-rta-test-agent-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-29"
reading_time_minutes: 1
breadcrumb: [ServiceNow Vault AI agents, ServiceNow Vault AI agents, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Real Time Anonymization\(RTA\) Test AI agent

The agent tests Real-Time Anonymization \(RTA\) by taking a text string from the user and returning the anonymized version.

## Workflow

The agent helps the user see how Real-Time Anonymization treats sample text.

1.  Ask the user for the text string to test.
2.  Anonymize the string.
3.  Display the original string, the anonymized string, and the intermediate results.
4.  Let the user repeat the test as many times as needed.

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

Real time anonymization\(RTA\) Test Script Tool


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

data\_discovery\_admin,data\_privacy\_admin, sn\_data\_discovery.data\_discovery\_admin

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

