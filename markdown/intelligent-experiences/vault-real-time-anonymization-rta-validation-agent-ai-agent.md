---
title: Real Time Anonymization\(RTA\) Validation AI agent
description: The agent confirms that Real-Time Anonymization \(RTA\) policy creation is supported for the user, and helps the user configure the tables and active data patterns that an RTA policy requires. The agent can add tables and add or remove active data patterns.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/vault-real-time-anonymization-rta-validation-agent-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-29"
reading_time_minutes: 2
breadcrumb: [ServiceNow Vault AI agents, ServiceNow Vault AI agents, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Real Time Anonymization\(RTA\) Validation AI agent

The agent confirms that Real-Time Anonymization \(RTA\) policy creation is supported for the user, and helps the user configure the tables and active data patterns that an RTA policy requires. The agent can add tables and add or remove active data patterns.

## Workflow

The agent helps the user prepare the tables and data patterns needed to create a Real-Time Anonymization policy.

1.  Confirm that the RTA feature is supported for the user.
2.  Display the configured tables, or explain that at least one table is required.
3.  Ask whether the user wants to add tables, validate that the requested tables are supported, and add them.
4.  Display the active data patterns, or explain that at least one active data pattern is required.
5.  Check the shared services usage entitlement, which is required for AI model-based data patterns.
6.  Display the available data patterns grouped by type, and let the user add or remove multiple patterns at once.
7.  Confirm that the tables and data patterns were added successfully.

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

Add active data pattern records

Add target table records

Check if shared service usage entitlement is available

Delete active data pattern records

Fetch active data patterns

Realtime anonymization\(RTA\) feature support validation script

Fetch taget table records

Validate selected table is supported

-   **Record operations**

Fetch data paterns


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

data\_privacy\_admin, data\_discovery\_admin, sn\_data\_discovery.data\_discovery\_admin

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

