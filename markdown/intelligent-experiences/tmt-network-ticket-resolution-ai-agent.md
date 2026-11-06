---
title: Network ticket resolution AI agent
description: The agent collects the details of a network incident, analyzes the associated alert to produce a summary, and finds knowledge articles relevant to the incident. The user chooses whether to add the alert summary and the articles to the work notes of the incident.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/tmt-network-ticket-resolution-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-10-22"
reading_time_minutes: 2
breadcrumb: [Customer Service Problem Management AI agents, Telecommunications, Media and Technology AI agents, Telecom, Media and Tech AI agents, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Network ticket resolution AI agent

The agent collects the details of a network incident, analyzes the associated alert to produce a summary, and finds knowledge articles relevant to the incident. The user chooses whether to add the alert summary and the articles to the work notes of the incident.

## Workflow

The agent gathers the information the assigned user needs to troubleshoot a network incident.

1.  Collect the incident number and any specific request details for the incident.
2.  Retrieve the incident details, and ask the user to confirm the incident number when no details are found.
3.  Analyze the alert associated with the incident and display the alert summary.
4.  Ask the user whether to add the alert summary to the work notes of the incident, and update the work notes when the user agrees.
5.  Find the knowledge articles that match the short description of the incident and display them.
6.  Ask the user whether to continue investigating the incident or to add the knowledge articles to the work notes. Also, ask the user whether to update the work notes when the user chooses to add them.

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

-   **Flow Action**

Get details of network incident

Perform telecom alert analysis

-   **Script**

Add to incident work notes

-   **Tool**

Get Relevant Knowledge Articles


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

Not defined.

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

sn\_tmt\_agentic\_ai.sn\_incident\_noc\_user

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

Analyze network incidents

</td></tr></tbody>
</table>Learn more about Customer Service Problem Management at [Customer Service Problem Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/cspm-landing-page.md).

**Parent Topic:**[Customer Service Problem Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/cspm-ai-agents-overview.md)

