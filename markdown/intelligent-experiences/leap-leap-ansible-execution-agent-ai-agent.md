---
title: LEAP Ansible Execution Agent AI agent
description: The LEAP Ansible Execution agent runs the Ansible playbooks mapped to each resolution step of an incident. It launches jobs through Ansible Automation Platform, prompts the user to complete unmapped steps manually, and reports job status on request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/leap-leap-ansible-execution-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-10-05"
reading_time_minutes: 2
breadcrumb: [AIOps and Leap AI agents, AIOps and AIOps Leap, AI agents library, AI assets, Enable AI experiences]
---

# LEAP Ansible Execution Agent AI agent

The LEAP Ansible Execution agent runs the Ansible playbooks mapped to each resolution step of an incident. It launches jobs through Ansible Automation Platform, prompts the user to complete unmapped steps manually, and reports job status on request.

## Workflow

The agent helps the user remediate an incident by running the Ansible playbooks mapped to its resolution steps.

1.  Identify the incident record and log on the record that execution has started.
2.  Retrieve the mapping between the resolution steps and their Ansible jobs, and inform the user if no mapping exists.
3.  Work through the resolution steps in order, asking the user to complete any step that has no playbook mapped and to confirm when it's done.
4.  For each mapped job, show the user the job template details and collect any required launch inputs in a single form.
5.  Launch the job, report the Ansible job ID and its status, and wait for the user to confirm before moving to the next step.
6.  Summarize the steps processed, the jobs launched and their status, the manual steps completed, and any failures.
7.  Record the overall success or failure status on the incident record.
8.  Check job status, show job output, cancel a job, or relaunch a job whenever the user asks.

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

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Model Context Protocol**

Get Job Details

Job Template Launch Retrieve

Job Templates Retrieve

Launch Job Templates

-   **Record Operation**

Get LEAP Ansible Mapping

-   **Script**

Fetch Record SysId and publish Journal entry


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

Not defined.

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

sn\_itom\_leap.leap\_ansible\_agent\_worker

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>**Parent Topic:**[AIOps and Leap AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aiops-ai-agents-overview.md)

