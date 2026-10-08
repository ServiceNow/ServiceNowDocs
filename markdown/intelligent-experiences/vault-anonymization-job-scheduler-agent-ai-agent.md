---
title: Anonymization Job Scheduler AI agent
description: The agent helps Data Privacy administrators schedule anonymization jobs against existing records by using a published anonymization policy. It checks for conflicting jobs, configures the job frequency, targets, and conditions, offers an optional dry run, and asks for explicit confirmation because starting a job is irreversible.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/vault-anonymization-job-scheduler-agent-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-29"
reading_time_minutes: 2
breadcrumb: [ServiceNow Vault AI agents, ServiceNow Vault AI agents, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Anonymization Job Scheduler AI agent

The agent helps Data Privacy administrators schedule anonymization jobs against existing records by using a published anonymization policy. It checks for conflicting jobs, configures the job frequency, targets, and conditions, offers an optional dry run, and asks for explicit confirmation because starting a job is irreversible.

## Workflow

The agent helps the user schedule an anonymization job that uses an existing anonymization policy.

1.  Find the anonymization policies that are eligible to be scheduled, and ask the user to select one.
2.  Load the fields that the selected policy can anonymize, and surface any warnings or child table requirements.
3.  Check the policy for conflicts with other running jobs and inform the user of any conflicts.
4.  Ask whether the user wants to run a dry run first, and if so, whether they want a sample or a detailed preview.
5.  For a regular job, ask how often it should run and, optionally, the time window.
6.  If the policy doesn't cover the whole data class, ask the user which users or groups the job should target.
7.  Build the job record, confirm the saved details with the user, and share a direct link so that the user can open the job and start it.

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

Anonymization Job Builder Tool

Anonymization Job Conflict Check Tool

Anonymization Job Details Tool

Anonymization Job Link Tool

Anonymization Policy Lookup Tool

Anonymization Policy Table Loader Tool

Anonymization Target Lookup Tool


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

data\_privacy\_clone\_processor,data\_privacy\_processor

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

