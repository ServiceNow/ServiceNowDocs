---
title: Network correlation monitor AI agent
description: The agent identifies the network services, customer accounts, and products that a network incident affects. It checks for service problem cases created recently and, with the user's approval, creates a major service problem case, links the incident and related cases to it, and creates child cases for the affected accounts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/tmt-network-correlation-monitor-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-10-22"
reading_time_minutes: 2
breadcrumb: [Customer Service Problem Management AI agents, Telecommunications, Media and Technology AI agents, Telecom, Media and Tech AI agents, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Network correlation monitor AI agent

The agent identifies the network services, customer accounts, and products that a network incident affects. It checks for service problem cases created recently and, with the user's approval, creates a major service problem case, links the incident and related cases to it, and creates child cases for the affected accounts.

## Workflow

The agent correlates a network incident with the accounts and service problem cases it affects, and creates a major service problem case for them.

1.  Identify the affected network services, customer accounts, and products for the incident, and update the incident with the impacted services.
2.  Display the affected accounts and the affected products to the user.
3.  Find the service problem cases created for the affected products in the last few minutes, and display each case found with its affected product names.
4.  Ask the user whether to create a major service problem case when no cases are found.
5.  Create the major service problem case, which requires human approval.
6.  Link the incident and the recent service problem cases to the major case, and display the major case number as a hyperlink.
7.  Ask the user whether to create child cases, and create a problem case for each affected account when the user agrees.
8.  Display the number of child cases created and a summary of the steps taken.

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

Create New Problem Case

Get Service Problem Cases Created in the Last x min

-   **Script**

Create Major Service Problem Case

Get Incident Affected Accounts and Products

Update Major Case with Link Incident and Cases


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

