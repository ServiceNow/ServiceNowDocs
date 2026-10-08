---
title: Anonymization Policy Creation AI agent
description: The agent guides Data Privacy administrators through creating an anonymization policy. It captures the data channel, policy name, and data class, creates a draft policy, recommends anonymization techniques by data type, and then tries to publish the policy, explaining anything that must be fixed first.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/vault-anonymization-policy-creation-agent-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-29"
reading_time_minutes: 2
breadcrumb: [ServiceNow Vault AI agents, ServiceNow Vault AI agents, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Anonymization Policy Creation AI agent

The agent guides Data Privacy administrators through creating an anonymization policy. It captures the data channel, policy name, and data class, creates a draft policy, recommends anonymization techniques by data type, and then tries to publish the policy, explaining anything that must be fixed first.

## Workflow

The agent helps the user create and publish a new anonymization policy.

1.  Ask the user whether the policy anonymizes data tables or columns, or user-specific data.
2.  Ask the user for a policy name and to select a data class from those available on the instance.
3.  For data tables or columns, ask whether the policy should be active during cloning and, if so, the order in which it should run.
4.  Summarize the captured details, let the user update any of them, and create the policy as an inactive draft after the user confirms.
5.  Present the recommended anonymization techniques grouped by data type, walk the user through each data type, and save the assignments.
6.  For user-specific data, ask the user to select a user reference column for each table that requires one.
7.  Publish the policy, or explain what needs to be fixed and leave the policy as a draft.

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

Create Draft Anonymization Policy

Get Bulk Technique Recommendations

Get Child Table Options

Get Data Patterns

Get List of Data classes

Get Primary Reference Columns

Publish Policy

Save Assigned Techniques

Save User References

Update Active Data Patterns

Validate Technique for Data Type


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

data\_privacy\_admin

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

Data Privacy Anonymization Job Scheduler

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow Vault AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/vault-ai-agents-overview.md)

