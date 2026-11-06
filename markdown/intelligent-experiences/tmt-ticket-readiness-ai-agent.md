---
title: Ticket readiness AI agent
description: The agent predicts the category, subcategory, assignment group, short description, and description for a network incident from similar historical incidents. It also estimates the resolution duration and retrieves the SLA duration, then updates the incident or its work notes with the recommendations the user accepts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/tmt-ticket-readiness-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-10-22"
reading_time_minutes: 2
breadcrumb: [Customer Service Problem Management AI agents, Telecommunications, Media and Technology AI agents, Telecom, Media and Tech AI agents, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Ticket readiness AI agent

The agent predicts the category, subcategory, assignment group, short description, and description for a network incident from similar historical incidents. It also estimates the resolution duration and retrieves the SLA duration, then updates the incident or its work notes with the recommendations the user accepts.

## Workflow

The agent recommends field values for a network incident based on similar incidents, and records the recommendations the user accepts.

1.  Retrieve the available categories and assignment groups.
2.  Search for incidents similar to the current incident, and tell the user when no similar incidents are found.
3.  Recommend the category, subcategory, assignment group, short description, and description from the similar incident data, and derive a resolution duration range.
4.  Retrieve the SLA duration for the incident, and tell the user to prioritize the incident when the SLA is shorter than the minimum resolution duration.
5.  Display the recommendations and ask the user whether to change them.
6.  Update the incident or the work notes of the incident with the recommendations, as the user chooses.

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

Get Incident SLA Duration

Get similar incident data for network incident

-   **Script**

Choices for categories

Choices for subcategories

Get Assignment Groups

Get details of Incident

Update Incident

Update Work Notes


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

