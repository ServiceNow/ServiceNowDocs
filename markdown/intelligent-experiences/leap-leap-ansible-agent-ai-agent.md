---
title: LEAP Ansible Agent AI agent
description: The LEAP Ansible agent finds the Ansible job template that best matches the problem behind an automation opportunity. It recommends the template to the user and saves it to the discovered job catalog.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/leap-leap-ansible-agent-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-10-05"
reading_time_minutes: 2
breadcrumb: [AIOps and Leap AI agents, AIOps and AIOps Leap, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# LEAP Ansible Agent AI agent

The LEAP Ansible agent finds the Ansible job template that best matches the problem behind an automation opportunity. It recommends the template to the user and saves it to the discovered job catalog.

## Workflow

The agent helps the user find the most appropriate Ansible job template from Ansible Automation Platform to remediate an automation opportunity.

1.  Accept the automation opportunity number and retrieve the problem context for that opportunity.
2.  Retrieve the full list of available job templates and their descriptions from Ansible Automation Platform.
3.  Compare the problem context with the job templates and identify the template that best matches.
4.  Retrieve the full configuration of the matched job template.
5.  Return the job template name, ID, and relevant configuration details to the user as the recommended remediation job.
6.  Save each matched job template to the discovered job catalog for the automation opportunity.
7.  Inform the user if no relevant job templates are found.

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

-   **Model Context Protocol**

Get Job Template Details

Job Template List

-   **Script**

Get AO Problem Context

Publish Job to Table


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

Not defined.

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

-   sn\_itom\_leap.ansible\_job\_create
-   sn\_itom\_leap.ansible\_job\_read
-   sn\_itom\_leap.group\_ranking\_read
-   sn\_itom\_leap.leap\_ansible\_agent\_worker
-   sn\_itom\_leap.outcome\_snapshot\_read

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

Not applicable.

</td></tr></tbody>
</table>**Parent Topic:**[AIOps and Leap AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aiops-ai-agents-overview.md)

